---
title: 验证 EWS 或 EWS 托管 API 调用的结果
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78a1741c-1bbe-4cb4-9331-9d6d3171fc11
description: 了解如何验证 EWS 或 EWS 托管 API 调用的结果。
ms.openlocfilehash: 077dd923710a1a7f5cad4c822cbbd58ab3603661
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753019"
---
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a>验证 EWS 或 EWS 托管 API 调用的结果

了解如何验证 EWS 或 EWS 托管 API 调用的结果。
  
当操作不能正常工作时，有助于查看了什么事通过检查您的应用程序发送网络和服务器发送回响应通过 SOAP 请求。 [工具和资源的 EWS 应用程序疑难解答](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)文章包括指向工具，以帮助捕获和查看这些 SOAP 请求。 您就得到请求和响应后，如何验证是否正确处理该请求发送到服务器？ 继续阅读以查明。 
  
如果要发送 EWS 请求，您将首先您验证检查响应中每个响应消息的**ResponseClass**属性。 会告诉您是否操作已成功完成对每一项。 
  
根据对象，正在呼叫您的方法，如果您使用 EWS 托管 API 发送请求，您可以使用响应对象一些验证。 但是，因为 SOAP 响应中包含的 EWS 托管 API 响应对象中包括的内容超集，您可能想要查看的 SOAP 响应。 由于的 SOAP 响应通常可以包含比 EWS 托管 API 的响应对象的详细信息，从您验证开始操作的 SOAP 响应。
  
## <a name="verifying-the-results-of-a-soap-response"></a>验证 SOAP 响应的结果
<a name="bk_verifysoap"> </a>

当您收到的 SOAP 响应时，首先要查看是**ResponseClass**属性。 在[ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx)元素中，每个**ResponseMessageType**实例包含此属性中下面的示例中所示。 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

因为 SOAP 响应可能包含单个 SOAP 响应中的多个响应消息，务必单独检查每个响应消息。
  
如果您正在使用的操作响应，如图所示的一部分包括**ResponseClass**操作可能会临时只检查操作**ResponseClass** 。 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

但是，操作状态仅反映顶级响应的形状，并且不会反映的所有单个邮件答复状态。 在以下示例中， [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx)操作已**成功**， **ResponseClass**但基础[DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx)元素具有**错误** **ResponseClass**值。
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
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

因此 SOAP EWS 响应，不能依赖操作**ResponseClass** -您必须在每个响应邮件以确定是否操作遇到任何错误处理项目**ResponseClass**查看。 
  
### <a name="verifying-success"></a>检查成功

如果每个**ResponseMessage**属性的每个**ResponseClass**属性设置为**成功**，操作成功完成所有项目，并且您可以转到下一个任务。
  
下面的示例演示检索单个项目的[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作请求成功响应。 请注意，当**ResponseClass**设置为**成功**，关联的[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)始终设置为**NoError**。
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

下面是对**GetItem**操作请求以便检索多个项目的成功响应。 每个[GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx)元素具有**成功** **ResponseClass** 。
  
```XML
<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                     xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

当您收到的响应并**ResponseClass**属性设置为**错误**时，该操作未成功完成对一个或多个项目。 纠正此问题，然后重试您的请求或您失败的请求的一部分。 **警告**值**ResponseClass**属性值仅返回[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作，并指示不能解析为唯一标识实体。 可以将其忽略所有其他操作。 
  
以下响应， **ResponseClass**属性的值为**错误**。
  
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

本示例中，EWS 提供线索调试问题。 当**ResponseClass**属性具有**错误**的值时，以下其他元素包含在响应时适用：
  
- [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — 描述错误。 
    
- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — 包含可以用于查找其他疑难解答的资源的错误代码。 
    
- [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — 标识导致出错的元素。 
    
- [DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — 未使用。 
    
您可以使用这些元素中提供的信息来进行调查您的问题。 在上面的示例， **MessageText**指示属性不是有效的对象类型。 请求是要获取电子邮件，但属性集包括**AssociatedCalendarItemId**，这只是有效的约会项目。
  
下面的示例演示批处理操作，以获取多个电子邮件项目的一部分收到一个错误。 成功检索到的第一项，并且**ResponseClass**设置为**成功**。 找不到第二项，并且**ResponseClass**设置**错误**。
  
```XML
<m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

无法处理批处理请求中的一个或多个项目，如请求时失败，每个项返回错误和预期所处理的批次中的项目的剩余部分。 在批处理中可能会出现故障如果项目已删除，因此无法发送、 检索，或更新，或者如果项目移动到另一个文件夹，并因此新的项 id。 因为该操作将对一些项目完成并不返回错误，不能处理一个或多个项时，务必您移到下一步操作之前，请检查每个**ResponseClass**属性。 
  
如果响应元素提供的信息不会帮助您更正您的请求或否则取消阻止您，请参阅[下一步步骤](#bk_nextsteps)。
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a>验证 EWS 托管 API 方法调用的结果
<a name="bk_successful"> </a>

如果您正在使用 EWS 托管 API 和[ExchangeService](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象上调用方法，您方法可能将返回一个[ServiceResponseCollection](http://msdn.microsoft.com/EN-US/library/dd633715%28v=exchg.80%29.aspx)对象，其中包含[服务](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的集合或集合的对象对象派生的**服务**对象。 **ServiceResponseCollection**和包括的**服务**对象包含有关方法调用，可用来验证结果的结果的信息。 
  
如果您正在使用 EWS 托管 API 和[项目](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)对象，或一个派生的对象上调用方法，可能的方法不会返回一个响应对象，以检查成功，但未完成该方法会引发[异常](http://msdn.microsoft.com/EN-US/library/c18k6c59)成功。 
  
### <a name="verifying-success"></a>检查成功

使用 EWS 托管 API 的一个好处是，它提供了总体状态时处理一个响应中的多个项目。 因此，如果您调用的方法返回**ServiceResponseCollection**，您可以检查**ServiceResponseCollection**的[OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx)属性等于[ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)。 如果是这样，批处理过程中的所有项是否已成功; 都完成您无需单独检查每个**服务**对象。 如果未设置为**ServiceResult.Success** **OverallResult**属性，必须[处理错误或警告](#bk_ewsmaerrors)。
  
如果您正在呼叫的方法不会返回**ServiceResponseCollection**，但无法返回**服务**对象，必须检查**结果**属性的值。 如果**结果**值设置为**成功**，就会知道该方法成功完成。
  
如果您正在呼叫的方法没有返回值，是真正无法检查成功通过 EWS 托管 API。 只要不引发异常，您可以假定该方法成功完成。 对于其他验证，您还可以[检查来验证结果的 SOAP 响应](#bk_verifysoap)。
  
### <a name="handling-errors-warnings-and-exceptions"></a>处理错误、 警告和异常
<a name="bk_ewsmaerrors"> </a>

如果 EWS 托管 API 代码引发**异常**，您可以使用[Exception.Message](http://msdn.microsoft.com/EN-US/library/9btwf6wk)值以确定错误的源。 **Message**属性包含基础的 SOAP 响应中的[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)元素的内容。 此外，如果例外的类型[ServiceResponseException](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)对象，一个最常见的异常，您还可以检索的基础的 SOAP [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素和[响应](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx)中包含[错误代码](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx)标识相关联的[服务](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的属性。 下面的代码演示如何捕获并显示**ServiceResponseException**的内容。 
  
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

如果您调用的方法返回**ServiceResponseCollection**，并且**OverallResult**属性的值等于**警告**或**错误**，您将需要遍历到**ServiceResponseCollection**中每个对象查找错误。 **OverallResult**属性设置为**警告**如果至少一个响应具有其**结果**值设置为**Warning** ，并且所有其他响应其**结果**将值设置为**成功**。 **OverallResult**属性设置为**错误**如果至少一个响应具有其**结果**值设置为**错误**。 当**OverallResult**设置为**警告**或**错误**时，将以下属性设置为适当的**服务**对象： 
  
- [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — 包含可以用于查找其他疑难解答的资源的错误代码。 
    
- [ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — 包含一些**ErrorCodes**有关错误的详细信息。 例如，错误代码时**ErrorRecurrenceHasNoOccurrence**， **ErrorDetails**将**EffectiveStartDate**和**EffectiveEndDate**包含键。 
    
- [ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — 描述错误。 
    
- [ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — 如果可用，标识导致出错的属性。 例如时的错误代码， **ErrorInvalidPropertyForOperation**, **ErrorProperties**包含无效请求的属性的定义。 
    
- [结果](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)— 包含**错误**或**警告**时遇到问题。 
    
如果**服务**属性并由它们提供的信息不提供足够的信息来纠正方法调用或取消阻止您，请参阅[下一步步骤](#bk_nextsteps)搜集**ErrorCode**值的详细信息。 
  
## 
<a name="bk_nextsteps"> </a>

您可以查找以下主题中的其他问题排查信息：
  
- [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素 
    
- [服务错误](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)枚举 
    
- [EWS 属性相关错误](ews-property-related-errors.md)
    
此外，具体取决于什么您正在尝试完成您的请求中，可能会发现的错误代码的其他有用信息在以下主题：
  
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    
- [在 Exchange 处理与通知相关 EWS 中的错误](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 处理同步相关 EWS 中的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [在 Exchange 处理删除相关 EWS 中的错误](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>另请参阅


- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    
- [工具和资源来解决 exchange 的 EWS 应用程序](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

