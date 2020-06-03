---
title: 验证 EWS 或 EWS 托管 API 调用的结果
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 78a1741c-1bbe-4cb4-9331-9d6d3171fc11
description: 了解如何验证 EWS 或 EWS 托管 API 调用的结果。
localization_priority: Priority
ms.openlocfilehash: be8e76898dd111a6dec33d4a57d9d50a2a935390
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457394"
---
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a>验证 EWS 或 EWS 托管 API 调用的结果

了解如何验证 EWS 或 EWS 托管 API 调用的结果。
  
在无法正常工作的情况下，通过检查您的应用程序通过网络发送的 SOAP 请求以及服务器发送回的响应，有助于查看正在进行的操作。 [用于排查 EWS 应用程序文章的工具和资源](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)包括可帮助捕获和查看这些 SOAP 请求的工具的链接。 获取请求和响应后，如何验证发送到服务器的请求是否已正确处理？ 请继续阅读以了解。 
  
如果要发送 EWS 请求，您将通过检查响应中每个响应消息的**ResponseClass**属性来开始验证。 这将告知您是否已在每个项目上成功完成该操作。 
  
如果要使用 EWS 托管 API 发送请求，则可以使用 response 对象进行一些验证，具体取决于您的方法正在调用的对象。 但是，由于 SOAP 响应包含 EWS 托管 API 响应对象中包含的内容的超集，因此您可能还需要查看 SOAP 响应。 由于 SOAP 响应通常包含比 EWS 托管 API 响应对象更多的信息，因此请使用 SOAP 响应启动验证。
  
## <a name="verifying-the-results-of-a-soap-response"></a>验证 SOAP 响应的结果
<a name="bk_verifysoap"> </a>

在收到 SOAP 响应时，首先要注意的一点是**ResponseClass**属性。 此属性包含在[ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx)元素中的每个**ResponseMessageType**实例中，如以下示例中所示。 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

由于 SOAP 响应可能在单个 SOAP 响应中包含多个响应邮件，因此请务必单独检查每条响应消息。
  
如果您正在使用包含**ResponseClass**的操作作为操作响应的一部分（如下所示），则可能会引诱您仅检查操作的**ResponseClass** 。 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

但是，操作状态仅反映顶级响应的形状，而不反映所有单个邮件响应的状态。 在下面的示例中， [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx)操作的**ResponseClass**为 "**成功**"，但基础[DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx)元素的 " **ResponseClass** " 值为 " **Error**"。
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
    <m:ResponseCode>NoError</m:ResponseCode>
    <m:ResponseMessages>
      <m:DelegateUserResponseMessageType ResponseClass="Error">
        <m:MessageText>The user is already a delegate for the mailbox.</m:MessageText>
        <m:ResponseCode>ErrorDelegateAlreadyExists</m:ResponseCode>
        <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      </m:DelegateUserResponseMessageType>
    </m:ResponseMessages>
  </m:AddDelegateResponse>
</soap:Body>
```

因此，对于 SOAP EWS 响应，不能依赖操作的**ResponseClass** -您必须查看每个响应消息的**ResponseClass** ，以确定操作是否遇到处理项目时遇到的任何错误。 
  
### <a name="verifying-success"></a>验证是否成功

如果每个**ResponseMessage**属性的每个**ResponseClass**属性设置为 "**成功**"，则该操作在所有项目上成功完成，并且您可以继续执行下一个任务。
  
下面的示例演示对[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作请求的检索单个项目的成功响应。 请注意，如果将**ResponseClass**设置为 "**成功**"，则关联的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)始终设置为**NoError**。
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
            <m:ResponseCode>NoError</m:ResponseCode>
            <m:Items>
              <t:Message>
                <t:ItemId Id="Er5bAAA=" 
                          ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/M" />
                <t:Subject>Dinner Party</t:Subject>
              </t:Message>
            </m:Items>
          </m:GetItemResponseMessage>
        </m:ResponseMessages>
      </m:GetItemResponse>
    </s:Body>
```

以下是对检索多个项目的**GetItem**操作请求的成功响应。 每个[GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx)元素都有一个**成功**的**ResponseClass** 。
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                     xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <m:ResponseMessages>
      <m:GetItemResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Items>
          <t:Message>
            <t:ItemId Id="Er5bAAA=" 
                      ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/M" /
            <t:Subject>Dinner Party</t:Subject>
          </t:Message>
        </m:Items>
      </m:GetItemResponseMessage>
      <m:GetItemResponseMessage ResponseClass="Success">
        <m:ResponseCode>NoError</m:ResponseCode>
        <m:Items>
          <t:Message>
            <t:ItemId Id="3c66AAA="
                      ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAc3kqm" />
            <t:Subject>Company Soccer Team</t:Subject>
          </t:Message>
        </m:Items>
      </m:GetItemResponseMessage>
    </m:ResponseMessages>
  </m:GetItemResponse>
</s:Body>
```

### <a name="handling-errors-and-warnings"></a>处理错误和警告

当您收到响应且**ResponseClass**属性设置为 "**错误**" 时，不会在一个或多个项目上成功完成该操作。 更正问题，然后重试您的请求或请求失败的部分。 **警告**值的**ResponseClass**属性值仅由[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作返回，并指示无法将实体解析为唯一标识。 您可以对所有其他操作忽略它。 
  
在以下响应中， **ResponseClass**属性的值为**Error**。
  
```XML
<m:GetItemResponseMessage ResponseClass="Error">
  <m:MessageText>Property is not valid for this object type.</m:MessageText>
  <m:ResponseCode>ErrorInvalidPropertyRequest</m:ResponseCode>
  <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
  <m:MessageXml>
    <t:FieldURI FieldURI="meeting:AssociatedCalendarItemId" />
  </m:MessageXml>
  <m:Items />
</m:GetItemResponseMessage>
```

在此示例中，EWS 提供了用于调试问题的线索。 当**ResponseClass**属性的值为**Error**时，响应中包含以下附加元素：
  
- [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) —描述错误。 
    
- [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) —包含可用于查找其他故障排除资源的错误代码。 
    
- [MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) —标识导致错误的元素。 
    
- [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) —未使用。 
    
您可以使用这些元素中提供的信息来调查您的问题。 在上面的示例中， **MessageText**指示属性对对象类型无效。 请求是获取电子邮件，但属性集包含**AssociatedCalendarItemId**，这仅对约会项目有效。
  
下面的示例显示作为批处理操作的一部分收到的错误，以获取多个电子邮件项目。 成功检索了第一项，并将**ResponseClass**设置为**Success**。 找不到第二个项目，并将**ResponseClass**设置为**Error**。
  
```XML
<m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <m:ResponseMessages>
    <m:GetItemResponseMessage ResponseClass="Success">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:Items>
        <t:Message>
          <t:ItemId Id="Er5cAAA="
                    ChangeKey="CQAAABYAAAD32nSTjepyT63rYH17n9THAAAhE0/O" />
          <t:Subject>Business plans</t:Subject>
        </t:Message>
      </m:Items>
    </m:GetItemResponseMessage>
    <m:GetItemResponseMessage ResponseClass="Error">
      <m:MessageText>The specified object was not found in the store.</m:MessageText>
      <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
      <m:Items />
    </m:GetItemResponseMessage>
  </m:ResponseMessages>
</m:GetItemResponse>
```

当批处理请求中的一个或多个项目无法按要求处理时，将为每个失败的项目返回一个错误，并按预期处理批处理中的其余项目。 如果项目已被删除、无法发送、检索或更新，或者项目移到其他文件夹中，因此具有新的项目 ID，批处理过程中可能会发生故障。 由于在无法处理一个或多个项目时，对某些项目的操作将完成，并且在无法处理一个或多个项目时不会返回错误，因此在继续执行下一个操作之前检查每个**ResponseClass**属性是非常重要的。 
  
如果响应元素提供的信息不能帮助您更正请求或以其他方式取消阻止，请参阅[后续步骤](#bk_nextsteps)。
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a>验证 EWS 托管 API 方法调用的结果
<a name="bk_successful"> </a>

如果您使用 EWS 托管 API 并对[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象调用方法，则方法可能返回[ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx)对象，该对象包含[ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的集合，或者是从**ServiceResponse**对象派生的对象的集合。 **ServiceResponseCollection**和包含的**ServiceResponse**对象包含有关方法调用结果的信息，可使用此信息来验证结果。 
  
如果使用 EWS 托管 API 并对[项目](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)对象或某个派生对象调用方法，该方法可能不会返回响应对象以检查是否成功，但如果方法未成功完成，则会引发[异常](https://msdn.microsoft.com/library/c18k6c59)。 
  
### <a name="verifying-success"></a>验证是否成功

使用 EWS 托管 API 的一个好处是，它在处理一个响应中的多个项目时提供了总体状态。 因此，如果您调用的方法返回一个**ServiceResponseCollection**，则可以检查**ServiceResponseCollection**的[OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx)属性是否等于[ServiceResult。 "成功](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)"。 如果是这样，批处理过程中的所有项目都已成功完成;您无需单独检查每个**ServiceResponse**对象。 如果**OverallResult**属性未设置为**ServiceResult**，则必须[处理错误或警告](#bk_ewsmaerrors)。
  
如果要调用的方法不返回**ServiceResponseCollection**，但却返回**ServiceResponse**对象，则必须检查**Result**属性的值。 如果将**结果**值设置为 "**成功**"，则表示方法已成功完成。
  
如果要调用的方法没有返回值，则实际上无法通过 EWS 托管 API 检查是否成功。 只要不引发异常，就可以假定方法已成功完成。 若要进行其他验证，您还可以[检查 SOAP 响应以验证结果](#bk_verifysoap)。
  
### <a name="handling-errors-warnings-and-exceptions"></a>处理错误、警告和异常
<a name="bk_ewsmaerrors"> </a>

如果您的 EWS 托管 API 代码引发**异常**，则可以使用[异常。消息](https://msdn.microsoft.com/library/9btwf6wk)值来确定错误的来源。 **Message**属性包含基础 SOAP 响应中的[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)元素的内容。 此外，如果异常的类型为[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)对象，最常见的异常之一，您还可以检索基础 SOAP [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素中包含的[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx)以及用于标识关联的[ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的[响应](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx)属性。 下面的代码演示如何捕获和显示**ServiceResponseException**的内容。 
  
```cs
try
    {
         …
    }
    catch (ServiceResponseException ex)
    {
        Console.WriteLine("Error code: " + ex.ErrorCode);
        Console.WriteLine("Error message: " + ex.Message);
        Console.WriteLine("Response: " + ex.Response);
    }
```

如果您调用的方法返回一个**ServiceResponseCollection**，并且**OverallResult**属性的值等于**警告**或**错误**，则必须循环访问**ServiceResponseCollection**中的每个对象以查找错误。 如果至少有一个响应将其**结果**值设置为 "**警告**"，并且所有其他响应的**结果**值设置为 "**成功**"，则**OverallResult**属性设置为 "**警告**"。 如果至少有一个响应将其**结果**值设置为**error**，则将**OverallResult**属性设置为**error** 。 当**OverallResult**设置为**警告**或**错误**时，将根据需要在**ServiceResponse**对象上设置以下属性： 
  
- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) —包含可用于查找其他故障排除资源的错误代码。 
    
- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) —包含有关某些**ErrorCodes**的错误的详细信息。 例如，如果错误代码为**ErrorRecurrenceHasNoOccurrence**，则**ErrorDetails**将包含**EffectiveStartDate**和**EffectiveEndDate**的键。 
    
- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) —描述错误。 
    
- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) —如果可用，则标识导致错误的属性。 例如，如果错误代码为**ErrorInvalidPropertyForOperation**，则**ErrorProperties**包含对请求无效的属性的定义。 
    
- [Result](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) —在遇到问题时包含**错误**或**警告**。 
    
如果**ServiceResponse**属性提供的信息没有提供足够的信息来更正您的方法调用或取消阻止您的，请参阅[后续步骤](#bk_nextsteps)，以深入了解有关**ErrorCode**值的详细信息。 
  
## 
<a name="bk_nextsteps"> </a>

您可以在以下主题中查找其他疑难解答信息：
  
- [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素 
    
- [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)枚举 
    
- [EWS 属性相关的错误](ews-property-related-errors.md)
    
此外，根据你在请求中尝试完成的操作，你可能会在以下主题中找到有关错误代码的其他有用信息：
  
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 中处理 EWS 中与通知相关的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中与同步相关的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 中处理 EWS 中的与删除相关的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

