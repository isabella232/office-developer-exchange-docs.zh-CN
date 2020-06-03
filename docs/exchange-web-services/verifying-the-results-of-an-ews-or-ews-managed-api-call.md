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
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a><span data-ttu-id="2c4a0-103">验证 EWS 或 EWS 托管 API 调用的结果</span><span class="sxs-lookup"><span data-stu-id="2c4a0-103">Verifying the results of an EWS or EWS Managed API call</span></span>

<span data-ttu-id="2c4a0-104">了解如何验证 EWS 或 EWS 托管 API 调用的结果。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-104">Learn how to verify the results of your EWS or EWS Managed API calls.</span></span>
  
<span data-ttu-id="2c4a0-105">在无法正常工作的情况下，通过检查您的应用程序通过网络发送的 SOAP 请求以及服务器发送回的响应，有助于查看正在进行的操作。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-105">When things aren't working correctly, it helps to see what's going on by examining the SOAP requests that your application is sending over the network and the responses that the server is sending back.</span></span> <span data-ttu-id="2c4a0-106">[用于排查 EWS 应用程序文章的工具和资源](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)包括可帮助捕获和查看这些 SOAP 请求的工具的链接。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-106">The [tools and resources for troubleshooting EWS applications](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) article includes links to tools to help capture and view those SOAP requests.</span></span> <span data-ttu-id="2c4a0-107">获取请求和响应后，如何验证发送到服务器的请求是否已正确处理？</span><span class="sxs-lookup"><span data-stu-id="2c4a0-107">After you've got the requests and the responses, how do you verify that the request you sent to the server was processed correctly?</span></span> <span data-ttu-id="2c4a0-108">请继续阅读以了解。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-108">Read on to find out.</span></span> 
  
<span data-ttu-id="2c4a0-109">如果要发送 EWS 请求，您将通过检查响应中每个响应消息的**ResponseClass**属性来开始验证。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-109">If you're sending EWS requests, you're going to start your verification by checking the **ResponseClass** attribute for each response message in the response.</span></span> <span data-ttu-id="2c4a0-110">这将告知您是否已在每个项目上成功完成该操作。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-110">That will tell you whether the operation completed successfully on each item.</span></span> 
  
<span data-ttu-id="2c4a0-111">如果要使用 EWS 托管 API 发送请求，则可以使用 response 对象进行一些验证，具体取决于您的方法正在调用的对象。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-111">Depending on the object that your method is calling, if you're using the EWS Managed API to send requests, you can do some verification using the response objects.</span></span> <span data-ttu-id="2c4a0-112">但是，由于 SOAP 响应包含 EWS 托管 API 响应对象中包含的内容的超集，因此您可能还需要查看 SOAP 响应。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-112">But because the SOAP response contains a superset of what's included in the EWS Managed API response objects, you might want to look at the SOAP response as well.</span></span> <span data-ttu-id="2c4a0-113">由于 SOAP 响应通常包含比 EWS 托管 API 响应对象更多的信息，因此请使用 SOAP 响应启动验证。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-113">Because the SOAP response can often contain more information than the EWS Managed API response objects, start your verification with the SOAP response.</span></span>
  
## <a name="verifying-the-results-of-a-soap-response"></a><span data-ttu-id="2c4a0-114">验证 SOAP 响应的结果</span><span class="sxs-lookup"><span data-stu-id="2c4a0-114">Verifying the results of a SOAP response</span></span>
<span data-ttu-id="2c4a0-115"><a name="bk_verifysoap"> </a></span><span class="sxs-lookup"><span data-stu-id="2c4a0-115"><a name="bk_verifysoap"> </a></span></span>

<span data-ttu-id="2c4a0-116">在收到 SOAP 响应时，首先要注意的一点是**ResponseClass**属性。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-116">When you receive a SOAP response, the first thing to look at is the **ResponseClass** attribute.</span></span> <span data-ttu-id="2c4a0-117">此属性包含在[ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx)元素中的每个**ResponseMessageType**实例中，如以下示例中所示。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-117">This attribute is included in each **ResponseMessageType** instance in the [ResponseMessages](https://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) element, as shown in the following example.</span></span> 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

<span data-ttu-id="2c4a0-118">由于 SOAP 响应可能在单个 SOAP 响应中包含多个响应邮件，因此请务必单独检查每条响应消息。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-118">Because a SOAP response might contain multiple response messages in a single SOAP response, it's important to check each response message individually.</span></span>
  
<span data-ttu-id="2c4a0-119">如果您正在使用包含**ResponseClass**的操作作为操作响应的一部分（如下所示），则可能会引诱您仅检查操作的**ResponseClass** 。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-119">If you're working with an operation that includes a **ResponseClass** as part of the operation response, like the following, you might be tempted to only check the **ResponseClass** of the operation.</span></span> 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

<span data-ttu-id="2c4a0-120">但是，操作状态仅反映顶级响应的形状，而不反映所有单个邮件响应的状态。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-120">However, the operation status only reflects the shape of the top-level response and does not reflect the status of all the individual message responses.</span></span> <span data-ttu-id="2c4a0-121">在下面的示例中， [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx)操作的**ResponseClass**为 "**成功**"，但基础[DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx)元素的 " **ResponseClass** " 值为 " **Error**"。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-121">In the following example, the [AddDelegateResponse](https://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) operation has a **ResponseClass** of **Success**, but the underlying [DelegateUserResponseMessageType](https://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) element has a **ResponseClass** value of **Error**.</span></span>
  
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

<span data-ttu-id="2c4a0-122">因此，对于 SOAP EWS 响应，不能依赖操作的**ResponseClass** -您必须查看每个响应消息的**ResponseClass** ，以确定操作是否遇到处理项目时遇到的任何错误。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-122">So for SOAP EWS responses, you can't rely on the **ResponseClass** of the operation - you have to look at the **ResponseClass** of each response message to determine whether the operation encountered any errors processing the items.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="2c4a0-123">验证是否成功</span><span class="sxs-lookup"><span data-stu-id="2c4a0-123">Verifying success</span></span>

<span data-ttu-id="2c4a0-124">如果每个**ResponseMessage**属性的每个**ResponseClass**属性设置为 "**成功**"，则该操作在所有项目上成功完成，并且您可以继续执行下一个任务。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-124">If each **ResponseClass** attribute for each **ResponseMessage** attribute is set to **Success**, the operation completed successfully on all the items, and you can move on to your next task.</span></span>
  
<span data-ttu-id="2c4a0-125">下面的示例演示对[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作请求的检索单个项目的成功响应。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-125">The following example shows a successful response to a [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation request to retrieve a single item.</span></span> <span data-ttu-id="2c4a0-126">请注意，如果将**ResponseClass**设置为 "**成功**"，则关联的[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)始终设置为**NoError**。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-126">Note that when the **ResponseClass** is set to **Success**, the associated [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) is always set to **NoError**.</span></span>
  
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

<span data-ttu-id="2c4a0-127">以下是对检索多个项目的**GetItem**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-127">The following is a successful response to a **GetItem** operation request to retrieve multiple items.</span></span> <span data-ttu-id="2c4a0-128">每个[GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx)元素都有一个**成功**的**ResponseClass** 。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-128">Each of the [GetItemResponseMessage](https://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) elements has a **ResponseClass** of **Success**.</span></span>
  
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

### <a name="handling-errors-and-warnings"></a><span data-ttu-id="2c4a0-129">处理错误和警告</span><span class="sxs-lookup"><span data-stu-id="2c4a0-129">Handling errors and warnings</span></span>

<span data-ttu-id="2c4a0-130">当您收到响应且**ResponseClass**属性设置为 "**错误**" 时，不会在一个或多个项目上成功完成该操作。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-130">When you receive a response and the **ResponseClass** attribute is set to **Error**, the operation did not complete successfully on one or more items.</span></span> <span data-ttu-id="2c4a0-131">更正问题，然后重试您的请求或请求失败的部分。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-131">Correct the issue and retry your request, or the part of your request that failed.</span></span> <span data-ttu-id="2c4a0-132">**警告**值的**ResponseClass**属性值仅由[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作返回，并指示无法将实体解析为唯一标识。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-132">A **ResponseClass** attribute value of **Warning** value is only returned by the [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation, and indicates that the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="2c4a0-133">您可以对所有其他操作忽略它。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-133">You can ignore it for all other operations.</span></span> 
  
<span data-ttu-id="2c4a0-134">在以下响应中， **ResponseClass**属性的值为**Error**。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-134">In the following response, the **ResponseClass** attribute has a value of **Error**.</span></span>
  
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

<span data-ttu-id="2c4a0-135">在此示例中，EWS 提供了用于调试问题的线索。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-135">In this example, EWS provides clues to debug the issue.</span></span> <span data-ttu-id="2c4a0-136">当**ResponseClass**属性的值为**Error**时，响应中包含以下附加元素：</span><span class="sxs-lookup"><span data-stu-id="2c4a0-136">When the **ResponseClass** attribute has a value of **Error**, the following additional elements are included in the response when applicable:</span></span>
  
- <span data-ttu-id="2c4a0-137">[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) —描述错误。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-137">[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="2c4a0-138">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) —包含可用于查找其他故障排除资源的错误代码。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-138">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="2c4a0-139">[MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) —标识导致错误的元素。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-139">[MessageXml](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — Identifies the elements that caused the error.</span></span> 
    
- <span data-ttu-id="2c4a0-140">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) —未使用。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-140">[DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — Unused.</span></span> 
    
<span data-ttu-id="2c4a0-141">您可以使用这些元素中提供的信息来调查您的问题。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-141">You can use the information provided in these elements to investigate your issue.</span></span> <span data-ttu-id="2c4a0-142">在上面的示例中， **MessageText**指示属性对对象类型无效。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-142">In the previous example, the **MessageText** indicates that the property isn't valid for the object type.</span></span> <span data-ttu-id="2c4a0-143">请求是获取电子邮件，但属性集包含**AssociatedCalendarItemId**，这仅对约会项目有效。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-143">The request was to get an email message, but the property set included the **AssociatedCalendarItemId**, which is only valid for appointment items.</span></span>
  
<span data-ttu-id="2c4a0-144">下面的示例显示作为批处理操作的一部分收到的错误，以获取多个电子邮件项目。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-144">The following example shows an error that was received as part of a batched operation to get multiple email items.</span></span> <span data-ttu-id="2c4a0-145">成功检索了第一项，并将**ResponseClass**设置为**Success**。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-145">The first item was retrieved successfully and the **ResponseClass** is set to **Success**.</span></span> <span data-ttu-id="2c4a0-146">找不到第二个项目，并将**ResponseClass**设置为**Error**。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-146">The second item could not be found, and the **ResponseClass** is set to **Error**.</span></span>
  
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

<span data-ttu-id="2c4a0-147">当批处理请求中的一个或多个项目无法按要求处理时，将为每个失败的项目返回一个错误，并按预期处理批处理中的其余项目。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-147">When one or more items in a batched request can't be processed as requested, an error is returned for each item that failed, and the rest of the items in the batch are processed as expected.</span></span> <span data-ttu-id="2c4a0-148">如果项目已被删除、无法发送、检索或更新，或者项目移到其他文件夹中，因此具有新的项目 ID，批处理过程中可能会发生故障。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-148">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID.</span></span> <span data-ttu-id="2c4a0-149">由于在无法处理一个或多个项目时，对某些项目的操作将完成，并且在无法处理一个或多个项目时不会返回错误，因此在继续执行下一个操作之前检查每个**ResponseClass**属性是非常重要的。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-149">Because the operation will complete for some items and not return an error when one or more items can't be processed, it's important to check each **ResponseClass** attribute before you move on to your next operation.</span></span> 
  
<span data-ttu-id="2c4a0-150">如果响应元素提供的信息不能帮助您更正请求或以其他方式取消阻止，请参阅[后续步骤](#bk_nextsteps)。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-150">If the information provided by the response elements doesn't help you correct your request or otherwise unblock you, see [Next steps](#bk_nextsteps).</span></span>
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a><span data-ttu-id="2c4a0-151">验证 EWS 托管 API 方法调用的结果</span><span class="sxs-lookup"><span data-stu-id="2c4a0-151">Verifying the results of an EWS Managed API method call</span></span>
<span data-ttu-id="2c4a0-152"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="2c4a0-152"><a name="bk_successful"> </a></span></span>

<span data-ttu-id="2c4a0-153">如果您使用 EWS 托管 API 并对[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象调用方法，则方法可能返回[ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx)对象，该对象包含[ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的集合，或者是从**ServiceResponse**对象派生的对象的集合。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-153">If you're using the EWS Managed API and calling a method on an [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, your method will likely return a [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) object, which contains a collection of [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) objects, or a collection of objects derived from the **ServiceResponse** objects.</span></span> <span data-ttu-id="2c4a0-154">**ServiceResponseCollection**和包含的**ServiceResponse**对象包含有关方法调用结果的信息，可使用此信息来验证结果。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-154">The **ServiceResponseCollection** and included **ServiceResponse** objects contain information about the result of the method call, which you can use to verify your results.</span></span> 
  
<span data-ttu-id="2c4a0-155">如果使用 EWS 托管 API 并对[项目](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)对象或某个派生对象调用方法，该方法可能不会返回响应对象以检查是否成功，但如果方法未成功完成，则会引发[异常](https://msdn.microsoft.com/library/c18k6c59)。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-155">If you're using the EWS Managed API and calling a method on an [Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object, or one of the derived objects, the method likely does not return a response object to check for success, but does throw an [Exception](https://msdn.microsoft.com/library/c18k6c59) if the method does not complete successfully.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="2c4a0-156">验证是否成功</span><span class="sxs-lookup"><span data-stu-id="2c4a0-156">Verifying success</span></span>

<span data-ttu-id="2c4a0-157">使用 EWS 托管 API 的一个好处是，它在处理一个响应中的多个项目时提供了总体状态。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-157">One benefit of using the EWS Managed API is that it provides an overall status when dealing with multiple items in one response.</span></span> <span data-ttu-id="2c4a0-158">因此，如果您调用的方法返回一个**ServiceResponseCollection**，则可以检查**ServiceResponseCollection**的[OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx)属性是否等于[ServiceResult。 "成功](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)"。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-158">So if the method you called returns a **ServiceResponseCollection**, you can check that the [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) property of the **ServiceResponseCollection** is equal to [ServiceResult.Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="2c4a0-159">如果是这样，批处理过程中的所有项目都已成功完成;您无需单独检查每个**ServiceResponse**对象。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-159">If so, all the items in the batched process were completed successfully; you don't have to check each **ServiceResponse** object individually.</span></span> <span data-ttu-id="2c4a0-160">如果**OverallResult**属性未设置为**ServiceResult**，则必须[处理错误或警告](#bk_ewsmaerrors)。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-160">If the **OverallResult** property is not set to **ServiceResult.Success**, you have to [handle the error or warning](#bk_ewsmaerrors).</span></span>
  
<span data-ttu-id="2c4a0-161">如果要调用的方法不返回**ServiceResponseCollection**，但却返回**ServiceResponse**对象，则必须检查**Result**属性的值。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-161">If the method you're calling does not return a **ServiceResponseCollection**, but does return a **ServiceResponse** object, you have to check the value of the **Result** property.</span></span> <span data-ttu-id="2c4a0-162">如果将**结果**值设置为 "**成功**"，则表示方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-162">If the **Result** value is set to **Success**, you know the method completed successfully.</span></span>
  
<span data-ttu-id="2c4a0-163">如果要调用的方法没有返回值，则实际上无法通过 EWS 托管 API 检查是否成功。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-163">If the method you're calling has no return value, there's really no way to check for success via the EWS Managed API.</span></span> <span data-ttu-id="2c4a0-164">只要不引发异常，就可以假定方法已成功完成。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-164">As long as an exception is not thrown, you can assume the method completed successfully.</span></span> <span data-ttu-id="2c4a0-165">若要进行其他验证，您还可以[检查 SOAP 响应以验证结果](#bk_verifysoap)。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-165">For additional validation, you can also [check the SOAP response to verify the results](#bk_verifysoap).</span></span>
  
### <a name="handling-errors-warnings-and-exceptions"></a><span data-ttu-id="2c4a0-166">处理错误、警告和异常</span><span class="sxs-lookup"><span data-stu-id="2c4a0-166">Handling errors, warnings, and exceptions</span></span>
<span data-ttu-id="2c4a0-167"><a name="bk_ewsmaerrors"> </a></span><span class="sxs-lookup"><span data-stu-id="2c4a0-167"><a name="bk_ewsmaerrors"> </a></span></span>

<span data-ttu-id="2c4a0-168">如果您的 EWS 托管 API 代码引发**异常**，则可以使用[异常。消息](https://msdn.microsoft.com/library/9btwf6wk)值来确定错误的来源。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-168">If your EWS Managed API code throws an **Exception**, you can use the [Exception.Message](https://msdn.microsoft.com/library/9btwf6wk) value to determine the source of the error.</span></span> <span data-ttu-id="2c4a0-169">**Message**属性包含基础 SOAP 响应中的[MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)元素的内容。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-169">The **Message** property contains the contents of the [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) element in the underlying SOAP response.</span></span> <span data-ttu-id="2c4a0-170">此外，如果异常的类型为[ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)对象，最常见的异常之一，您还可以检索基础 SOAP [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素中包含的[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx)以及用于标识关联的[ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的[响应](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-170">In addition, if the exception is of type [ServiceResponseException](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) object, one of the most common exceptions, you can also retrieve the [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) contained in the underlying SOAP [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element, and the [Response](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) property that identifies the associated [ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="2c4a0-171">下面的代码演示如何捕获和显示**ServiceResponseException**的内容。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-171">The following code shows how to catch and display the contents of a **ServiceResponseException**.</span></span> 
  
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

<span data-ttu-id="2c4a0-172">如果您调用的方法返回一个**ServiceResponseCollection**，并且**OverallResult**属性的值等于**警告**或**错误**，则必须循环访问**ServiceResponseCollection**中的每个对象以查找错误。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-172">If the method you called returns a **ServiceResponseCollection**, and the value of the **OverallResult** property is equal to **Warning** or **Error**, you'll have to loop through each object in the **ServiceResponseCollection** to find the error.</span></span> <span data-ttu-id="2c4a0-173">如果至少有一个响应将其**结果**值设置为 "**警告**"，并且所有其他响应的**结果**值设置为 "**成功**"，则**OverallResult**属性设置为 "**警告**"。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-173">The **OverallResult** property is set to **Warning** if at least one response has its **Result** value set to **Warning** and all other responses have their **Result** values set to **Success**.</span></span> <span data-ttu-id="2c4a0-174">如果至少有一个响应将其**结果**值设置为**error**，则将**OverallResult**属性设置为**error** 。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-174">The **OverallResult** property is set to **Error** if at least one response has its **Result** value set to **Error**.</span></span> <span data-ttu-id="2c4a0-175">当**OverallResult**设置为**警告**或**错误**时，将根据需要在**ServiceResponse**对象上设置以下属性：</span><span class="sxs-lookup"><span data-stu-id="2c4a0-175">When the **OverallResult** is set to **Warning** or **Error**, the following properties are set on the **ServiceResponse** objects as appropriate:</span></span> 
  
- <span data-ttu-id="2c4a0-176">[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) —包含可用于查找其他故障排除资源的错误代码。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-176">[ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="2c4a0-177">[ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) —包含有关某些**ErrorCodes**的错误的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-177">[ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — Contains details about the error for some **ErrorCodes**.</span></span> <span data-ttu-id="2c4a0-178">例如，如果错误代码为**ErrorRecurrenceHasNoOccurrence**，则**ErrorDetails**将包含**EffectiveStartDate**和**EffectiveEndDate**的键。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-178">For example, when the error code is **ErrorRecurrenceHasNoOccurrence**, the **ErrorDetails** will contain keys for **EffectiveStartDate** and **EffectiveEndDate**.</span></span> 
    
- <span data-ttu-id="2c4a0-179">[ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) —描述错误。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-179">[ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="2c4a0-180">[ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) —如果可用，则标识导致错误的属性。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-180">[ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — If available, identifies the properties that caused the error.</span></span> <span data-ttu-id="2c4a0-181">例如，如果错误代码为**ErrorInvalidPropertyForOperation**，则**ErrorProperties**包含对请求无效的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-181">For example, when the error code is **ErrorInvalidPropertyForOperation**, **ErrorProperties** contains the definition of the property that was invalid for the request.</span></span> 
    
- <span data-ttu-id="2c4a0-182">[Result](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) —在遇到问题时包含**错误**或**警告**。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-182">[Result](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) — Contains **Error** or **Warning** when an issue is encountered.</span></span> 
    
<span data-ttu-id="2c4a0-183">如果**ServiceResponse**属性提供的信息没有提供足够的信息来更正您的方法调用或取消阻止您的，请参阅[后续步骤](#bk_nextsteps)，以深入了解有关**ErrorCode**值的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2c4a0-183">If the information provided by the **ServiceResponse** properties doesn't provide enough information to correct your method call or unblock you, see [Next steps](#bk_nextsteps) to dig up more information on **ErrorCode** values.</span></span> 
  
## 
<span data-ttu-id="2c4a0-184"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="2c4a0-184"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="2c4a0-185">您可以在以下主题中查找其他疑难解答信息：</span><span class="sxs-lookup"><span data-stu-id="2c4a0-185">You can look up additional troubleshooting information in the following topics:</span></span>
  
- <span data-ttu-id="2c4a0-186">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="2c4a0-186">[ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element</span></span> 
    
- <span data-ttu-id="2c4a0-187">[ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)枚举</span><span class="sxs-lookup"><span data-stu-id="2c4a0-187">[ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) enumeration</span></span> 
    
- [<span data-ttu-id="2c4a0-188">EWS 属性相关的错误</span><span class="sxs-lookup"><span data-stu-id="2c4a0-188">EWS property-related errors</span></span>](ews-property-related-errors.md)
    
<span data-ttu-id="2c4a0-189">此外，根据你在请求中尝试完成的操作，你可能会在以下主题中找到有关错误代码的其他有用信息：</span><span class="sxs-lookup"><span data-stu-id="2c4a0-189">In addition, depending on what you're trying to accomplish in your request, you might find additional helpful information about the error code in the following topics:</span></span>
  
- [<span data-ttu-id="2c4a0-190">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="2c4a0-190">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="2c4a0-191">在 Exchange 中处理 EWS 中与通知相关的错误</span><span class="sxs-lookup"><span data-stu-id="2c4a0-191">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="2c4a0-192">在 Exchange 中处理 EWS 中与同步相关的错误</span><span class="sxs-lookup"><span data-stu-id="2c4a0-192">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="2c4a0-193">在 Exchange 中处理 EWS 中的与删除相关的错误</span><span class="sxs-lookup"><span data-stu-id="2c4a0-193">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="2c4a0-194">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c4a0-194">See also</span></span>


- [<span data-ttu-id="2c4a0-195">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="2c4a0-195">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="2c4a0-196">工具和资源来解决 exchange 的 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="2c4a0-196">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

