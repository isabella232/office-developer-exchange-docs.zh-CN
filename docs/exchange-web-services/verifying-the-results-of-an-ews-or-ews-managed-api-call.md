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
# <a name="verifying-the-results-of-an-ews-or-ews-managed-api-call"></a><span data-ttu-id="a9de9-103">验证 EWS 或 EWS 托管 API 调用的结果</span><span class="sxs-lookup"><span data-stu-id="a9de9-103">Verifying the results of an EWS or EWS Managed API call</span></span>

<span data-ttu-id="a9de9-104">了解如何验证 EWS 或 EWS 托管 API 调用的结果。</span><span class="sxs-lookup"><span data-stu-id="a9de9-104">Learn how to verify the results of your EWS or EWS Managed API calls.</span></span>
  
<span data-ttu-id="a9de9-105">当操作不能正常工作时，有助于查看了什么事通过检查您的应用程序发送网络和服务器发送回响应通过 SOAP 请求。</span><span class="sxs-lookup"><span data-stu-id="a9de9-105">When things aren't working correctly, it helps to see what's going on by examining the SOAP requests that your application is sending over the network and the responses that the server is sending back.</span></span> <span data-ttu-id="a9de9-106">[工具和资源的 EWS 应用程序疑难解答](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)文章包括指向工具，以帮助捕获和查看这些 SOAP 请求。</span><span class="sxs-lookup"><span data-stu-id="a9de9-106">The [tools and resources for troubleshooting EWS applications](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md) article includes links to tools to help capture and view those SOAP requests.</span></span> <span data-ttu-id="a9de9-107">您就得到请求和响应后，如何验证是否正确处理该请求发送到服务器？</span><span class="sxs-lookup"><span data-stu-id="a9de9-107">After you've got the requests and the responses, how do you verify that the request you sent to the server was processed correctly?</span></span> <span data-ttu-id="a9de9-108">继续阅读以查明。</span><span class="sxs-lookup"><span data-stu-id="a9de9-108">Read on to find out.</span></span> 
  
<span data-ttu-id="a9de9-109">如果要发送 EWS 请求，您将首先您验证检查响应中每个响应消息的**ResponseClass**属性。</span><span class="sxs-lookup"><span data-stu-id="a9de9-109">If you're sending EWS requests, you're going to start your verification by checking the **ResponseClass** attribute for each response message in the response.</span></span> <span data-ttu-id="a9de9-110">会告诉您是否操作已成功完成对每一项。</span><span class="sxs-lookup"><span data-stu-id="a9de9-110">That will tell you whether the operation completed successfully on each item.</span></span> 
  
<span data-ttu-id="a9de9-111">根据对象，正在呼叫您的方法，如果您使用 EWS 托管 API 发送请求，您可以使用响应对象一些验证。</span><span class="sxs-lookup"><span data-stu-id="a9de9-111">Depending on the object that your method is calling, if you're using the EWS Managed API to send requests, you can do some verification using the response objects.</span></span> <span data-ttu-id="a9de9-112">但是，因为 SOAP 响应中包含的 EWS 托管 API 响应对象中包括的内容超集，您可能想要查看的 SOAP 响应。</span><span class="sxs-lookup"><span data-stu-id="a9de9-112">But because the SOAP response contains a superset of what's included in the EWS Managed API response objects, you might want to look at the SOAP response as well.</span></span> <span data-ttu-id="a9de9-113">由于的 SOAP 响应通常可以包含比 EWS 托管 API 的响应对象的详细信息，从您验证开始操作的 SOAP 响应。</span><span class="sxs-lookup"><span data-stu-id="a9de9-113">Because the SOAP response can often contain more information than the EWS Managed API response objects, start your verification with the SOAP response.</span></span>
  
## <a name="verifying-the-results-of-a-soap-response"></a><span data-ttu-id="a9de9-114">验证 SOAP 响应的结果</span><span class="sxs-lookup"><span data-stu-id="a9de9-114">Verifying the results of a SOAP response</span></span>
<span data-ttu-id="a9de9-115"><a name="bk_verifysoap"> </a></span><span class="sxs-lookup"><span data-stu-id="a9de9-115"></span></span>

<span data-ttu-id="a9de9-116">当您收到的 SOAP 响应时，首先要查看是**ResponseClass**属性。</span><span class="sxs-lookup"><span data-stu-id="a9de9-116">When you receive a SOAP response, the first thing to look at is the **ResponseClass** attribute.</span></span> <span data-ttu-id="a9de9-117">在[ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx)元素中，每个**ResponseMessageType**实例包含此属性中下面的示例中所示。</span><span class="sxs-lookup"><span data-stu-id="a9de9-117">This attribute is included in each **ResponseMessageType** instance in the [ResponseMessages](http://msdn.microsoft.com/library/2071bed8-ea66-4627-aa4f-a1d9a025cf3d%28Office.15%29.aspx) element, as shown in the following example.</span></span> 
  
```XML
<s:Body>
      <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
        <m:ResponseMessages>
          <m:GetItemResponseMessage ResponseClass="Success">
          …
```

<span data-ttu-id="a9de9-118">因为 SOAP 响应可能包含单个 SOAP 响应中的多个响应消息，务必单独检查每个响应消息。</span><span class="sxs-lookup"><span data-stu-id="a9de9-118">Because a SOAP response might contain multiple response messages in a single SOAP response, it's important to check each response message individually.</span></span>
  
<span data-ttu-id="a9de9-119">如果您正在使用的操作响应，如图所示的一部分包括**ResponseClass**操作可能会临时只检查操作**ResponseClass** 。</span><span class="sxs-lookup"><span data-stu-id="a9de9-119">If you're working with an operation that includes a **ResponseClass** as part of the operation response, like the following, you might be tempted to only check the **ResponseClass** of the operation.</span></span> 
  
```XML
<soap:Body>
  <m:AddDelegateResponse xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                         ResponseClass="Success"
                         xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
  …

```

<span data-ttu-id="a9de9-120">但是，操作状态仅反映顶级响应的形状，并且不会反映的所有单个邮件答复状态。</span><span class="sxs-lookup"><span data-stu-id="a9de9-120">However, the operation status only reflects the shape of the top-level response and does not reflect the status of all the individual message responses.</span></span> <span data-ttu-id="a9de9-121">在以下示例中， [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx)操作已**成功**， **ResponseClass**但基础[DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx)元素具有**错误** **ResponseClass**值。</span><span class="sxs-lookup"><span data-stu-id="a9de9-121">In the following example, the [AddDelegateResponse](http://msdn.microsoft.com/library/d7e6bebb-5dbf-43c1-aacf-4b3ca6a7c429%28Office.15%29.aspx) operation has a **ResponseClass** of **Success**, but the underlying [DelegateUserResponseMessageType](http://msdn.microsoft.com/library/3dc9552c-1e2d-40ac-a137-827883c2bb88%28Office.15%29.aspx) element has a **ResponseClass** value of **Error**.</span></span>
  
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

<span data-ttu-id="a9de9-122">因此 SOAP EWS 响应，不能依赖操作**ResponseClass** -您必须在每个响应邮件以确定是否操作遇到任何错误处理项目**ResponseClass**查看。</span><span class="sxs-lookup"><span data-stu-id="a9de9-122">So for SOAP EWS responses, you can't rely on the **ResponseClass** of the operation - you have to look at the **ResponseClass** of each response message to determine whether the operation encountered any errors processing the items.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="a9de9-123">检查成功</span><span class="sxs-lookup"><span data-stu-id="a9de9-123">Verifying success</span></span>

<span data-ttu-id="a9de9-124">如果每个**ResponseMessage**属性的每个**ResponseClass**属性设置为**成功**，操作成功完成所有项目，并且您可以转到下一个任务。</span><span class="sxs-lookup"><span data-stu-id="a9de9-124">If each **ResponseClass** attribute for each **ResponseMessage** attribute is set to **Success**, the operation completed successfully on all the items, and you can move on to your next task.</span></span>
  
<span data-ttu-id="a9de9-125">下面的示例演示检索单个项目的[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="a9de9-125">The following example shows a successful response to a [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation request to retrieve a single item.</span></span> <span data-ttu-id="a9de9-126">请注意，当**ResponseClass**设置为**成功**，关联的[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)始终设置为**NoError**。</span><span class="sxs-lookup"><span data-stu-id="a9de9-126">Note that when the **ResponseClass** is set to **Success**, the associated [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) is always set to **NoError**.</span></span>
  
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

<span data-ttu-id="a9de9-127">下面是对**GetItem**操作请求以便检索多个项目的成功响应。</span><span class="sxs-lookup"><span data-stu-id="a9de9-127">The following is a successful response to a **GetItem** operation request to retrieve multiple items.</span></span> <span data-ttu-id="a9de9-128">每个[GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx)元素具有**成功** **ResponseClass** 。</span><span class="sxs-lookup"><span data-stu-id="a9de9-128">Each of the [GetItemResponseMessage](http://msdn.microsoft.com/library/cc583723-54d1-4a17-8c1f-6586f70fdefd%28Office.15%29.aspx) elements has a **ResponseClass** of **Success**.</span></span>
  
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

### <a name="handling-errors-and-warnings"></a><span data-ttu-id="a9de9-129">处理错误和警告</span><span class="sxs-lookup"><span data-stu-id="a9de9-129">Handling errors and warnings</span></span>

<span data-ttu-id="a9de9-130">当您收到的响应并**ResponseClass**属性设置为**错误**时，该操作未成功完成对一个或多个项目。</span><span class="sxs-lookup"><span data-stu-id="a9de9-130">When you receive a response and the **ResponseClass** attribute is set to **Error**, the operation did not complete successfully on one or more items.</span></span> <span data-ttu-id="a9de9-131">纠正此问题，然后重试您的请求或您失败的请求的一部分。</span><span class="sxs-lookup"><span data-stu-id="a9de9-131">Correct the issue and retry your request, or the part of your request that failed.</span></span> <span data-ttu-id="a9de9-132">**警告**值**ResponseClass**属性值仅返回[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作，并指示不能解析为唯一标识实体。</span><span class="sxs-lookup"><span data-stu-id="a9de9-132">A **ResponseClass** attribute value of **Warning** value is only returned by the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation, and indicates that the entity could not be resolved to a unique identity.</span></span> <span data-ttu-id="a9de9-133">可以将其忽略所有其他操作。</span><span class="sxs-lookup"><span data-stu-id="a9de9-133">You can ignore it for all other operations.</span></span> 
  
<span data-ttu-id="a9de9-134">以下响应， **ResponseClass**属性的值为**错误**。</span><span class="sxs-lookup"><span data-stu-id="a9de9-134">In the following response, the **ResponseClass** attribute has a value of **Error**.</span></span>
  
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

<span data-ttu-id="a9de9-135">本示例中，EWS 提供线索调试问题。</span><span class="sxs-lookup"><span data-stu-id="a9de9-135">In this example, EWS provides clues to debug the issue.</span></span> <span data-ttu-id="a9de9-136">当**ResponseClass**属性具有**错误**的值时，以下其他元素包含在响应时适用：</span><span class="sxs-lookup"><span data-stu-id="a9de9-136">When the **ResponseClass** attribute has a value of **Error**, the following additional elements are included in the response when applicable:</span></span>
  
- <span data-ttu-id="a9de9-137">[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — 描述错误。</span><span class="sxs-lookup"><span data-stu-id="a9de9-137">[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="a9de9-138">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — 包含可以用于查找其他疑难解答的资源的错误代码。</span><span class="sxs-lookup"><span data-stu-id="a9de9-138">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="a9de9-139">[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — 标识导致出错的元素。</span><span class="sxs-lookup"><span data-stu-id="a9de9-139">[MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) — Identifies the elements that caused the error.</span></span> 
    
- <span data-ttu-id="a9de9-140">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — 未使用。</span><span class="sxs-lookup"><span data-stu-id="a9de9-140">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) — Unused.</span></span> 
    
<span data-ttu-id="a9de9-141">您可以使用这些元素中提供的信息来进行调查您的问题。</span><span class="sxs-lookup"><span data-stu-id="a9de9-141">You can use the information provided in these elements to investigate your issue.</span></span> <span data-ttu-id="a9de9-142">在上面的示例， **MessageText**指示属性不是有效的对象类型。</span><span class="sxs-lookup"><span data-stu-id="a9de9-142">In the previous example, the **MessageText** indicates that the property isn't valid for the object type.</span></span> <span data-ttu-id="a9de9-143">请求是要获取电子邮件，但属性集包括**AssociatedCalendarItemId**，这只是有效的约会项目。</span><span class="sxs-lookup"><span data-stu-id="a9de9-143">The request was to get an email message, but the property set included the **AssociatedCalendarItemId**, which is only valid for appointment items.</span></span>
  
<span data-ttu-id="a9de9-144">下面的示例演示批处理操作，以获取多个电子邮件项目的一部分收到一个错误。</span><span class="sxs-lookup"><span data-stu-id="a9de9-144">The following example shows an error that was received as part of a batched operation to get multiple email items.</span></span> <span data-ttu-id="a9de9-145">成功检索到的第一项，并且**ResponseClass**设置为**成功**。</span><span class="sxs-lookup"><span data-stu-id="a9de9-145">The first item was retrieved successfully and the **ResponseClass** is set to **Success**.</span></span> <span data-ttu-id="a9de9-146">找不到第二项，并且**ResponseClass**设置**错误**。</span><span class="sxs-lookup"><span data-stu-id="a9de9-146">The second item could not be found, and the **ResponseClass** is set to **Error**.</span></span>
  
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

<span data-ttu-id="a9de9-147">无法处理批处理请求中的一个或多个项目，如请求时失败，每个项返回错误和预期所处理的批次中的项目的剩余部分。</span><span class="sxs-lookup"><span data-stu-id="a9de9-147">When one or more items in a batched request can't be processed as requested, an error is returned for each item that failed, and the rest of the items in the batch are processed as expected.</span></span> <span data-ttu-id="a9de9-148">在批处理中可能会出现故障如果项目已删除，因此无法发送、 检索，或更新，或者如果项目移动到另一个文件夹，并因此新的项 id。</span><span class="sxs-lookup"><span data-stu-id="a9de9-148">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID.</span></span> <span data-ttu-id="a9de9-149">因为该操作将对一些项目完成并不返回错误，不能处理一个或多个项时，务必您移到下一步操作之前，请检查每个**ResponseClass**属性。</span><span class="sxs-lookup"><span data-stu-id="a9de9-149">Because the operation will complete for some items and not return an error when one or more items can't be processed, it's important to check each **ResponseClass** attribute before you move on to your next operation.</span></span> 
  
<span data-ttu-id="a9de9-150">如果响应元素提供的信息不会帮助您更正您的请求或否则取消阻止您，请参阅[下一步步骤](#bk_nextsteps)。</span><span class="sxs-lookup"><span data-stu-id="a9de9-150">If the information provided by the response elements doesn't help you correct your request or otherwise unblock you, see [Next steps](#bk_nextsteps).</span></span>
  
## <a name="verifying-the-results-of-an-ews-managed-api-method-call"></a><span data-ttu-id="a9de9-151">验证 EWS 托管 API 方法调用的结果</span><span class="sxs-lookup"><span data-stu-id="a9de9-151">Verifying the results of an EWS Managed API method call</span></span>
<span data-ttu-id="a9de9-152"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="a9de9-152"></span></span>

<span data-ttu-id="a9de9-153">如果您正在使用 EWS 托管 API 和[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象上调用方法，您方法可能将返回一个[ServiceResponseCollection](http://msdn.microsoft.com/zh-cn/library/dd633715%28v=exchg.80%29.aspx)对象，其中包含[服务](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的集合或集合的对象对象派生的**服务**对象。</span><span class="sxs-lookup"><span data-stu-id="a9de9-153">If you're using the EWS Managed API and calling a method on an [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object, your method will likely return a [ServiceResponseCollection](http://msdn.microsoft.com/zh-cn/library/dd633715%28v=exchg.80%29.aspx) object, which contains a collection of [ServiceResponse](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) objects, or a collection of objects derived from the **ServiceResponse** objects.</span></span> <span data-ttu-id="a9de9-154">**ServiceResponseCollection**和包括的**服务**对象包含有关方法调用，可用来验证结果的结果的信息。</span><span class="sxs-lookup"><span data-stu-id="a9de9-154">The **ServiceResponseCollection** and included **ServiceResponse** objects contain information about the result of the method call, which you can use to verify your results.</span></span> 
  
<span data-ttu-id="a9de9-155">如果您正在使用 EWS 托管 API 和[项目](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx)对象，或一个派生的对象上调用方法，可能的方法不会返回一个响应对象，以检查成功，但未完成该方法会引发[异常](http://msdn.microsoft.com/zh-cn/library/c18k6c59)成功。</span><span class="sxs-lookup"><span data-stu-id="a9de9-155">If you're using the EWS Managed API and calling a method on an [Item](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object, or one of the derived objects, the method likely does not return a response object to check for success, but does throw an [Exception](http://msdn.microsoft.com/zh-cn/library/c18k6c59) if the method does not complete successfully.</span></span> 
  
### <a name="verifying-success"></a><span data-ttu-id="a9de9-156">检查成功</span><span class="sxs-lookup"><span data-stu-id="a9de9-156">Verifying success</span></span>

<span data-ttu-id="a9de9-157">使用 EWS 托管 API 的一个好处是，它提供了总体状态时处理一个响应中的多个项目。</span><span class="sxs-lookup"><span data-stu-id="a9de9-157">One benefit of using the EWS Managed API is that it provides an overall status when dealing with multiple items in one response.</span></span> <span data-ttu-id="a9de9-158">因此，如果您调用的方法返回**ServiceResponseCollection**，您可以检查**ServiceResponseCollection**的[OverallResult](http://msdn.microsoft.com/zh-cn/library/dd634515%28v=exchg.80%29.aspx)属性等于[ServiceResult.Success](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="a9de9-158">So if the method you called returns a **ServiceResponseCollection**, you can check that the [OverallResult](http://msdn.microsoft.com/zh-cn/library/dd634515%28v=exchg.80%29.aspx) property of the **ServiceResponseCollection** is equal to [ServiceResult.Success](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="a9de9-159">如果是这样，批处理过程中的所有项是否已成功; 都完成您无需单独检查每个**服务**对象。</span><span class="sxs-lookup"><span data-stu-id="a9de9-159">If so, all the items in the batched process were completed successfully; you don't have to check each **ServiceResponse** object individually.</span></span> <span data-ttu-id="a9de9-160">如果未设置为**ServiceResult.Success** **OverallResult**属性，必须[处理错误或警告](#bk_ewsmaerrors)。</span><span class="sxs-lookup"><span data-stu-id="a9de9-160">If the **OverallResult** property is not set to **ServiceResult.Success**, you have to [handle the error or warning](#bk_ewsmaerrors).</span></span>
  
<span data-ttu-id="a9de9-161">如果您正在呼叫的方法不会返回**ServiceResponseCollection**，但无法返回**服务**对象，必须检查**结果**属性的值。</span><span class="sxs-lookup"><span data-stu-id="a9de9-161">If the method you're calling does not return a **ServiceResponseCollection**, but does return a **ServiceResponse** object, you have to check the value of the **Result** property.</span></span> <span data-ttu-id="a9de9-162">如果**结果**值设置为**成功**，就会知道该方法成功完成。</span><span class="sxs-lookup"><span data-stu-id="a9de9-162">If the **Result** value is set to **Success**, you know the method completed successfully.</span></span>
  
<span data-ttu-id="a9de9-163">如果您正在呼叫的方法没有返回值，是真正无法检查成功通过 EWS 托管 API。</span><span class="sxs-lookup"><span data-stu-id="a9de9-163">If the method you're calling has no return value, there's really no way to check for success via the EWS Managed API.</span></span> <span data-ttu-id="a9de9-164">只要不引发异常，您可以假定该方法成功完成。</span><span class="sxs-lookup"><span data-stu-id="a9de9-164">As long as an exception is not thrown, you can assume the method completed successfully.</span></span> <span data-ttu-id="a9de9-165">对于其他验证，您还可以[检查来验证结果的 SOAP 响应](#bk_verifysoap)。</span><span class="sxs-lookup"><span data-stu-id="a9de9-165">For additional validation, you can also [check the SOAP response to verify the results](#bk_verifysoap).</span></span>
  
### <a name="handling-errors-warnings-and-exceptions"></a><span data-ttu-id="a9de9-166">处理错误、 警告和异常</span><span class="sxs-lookup"><span data-stu-id="a9de9-166">Handling errors, warnings, and exceptions</span></span>
<span data-ttu-id="a9de9-167"><a name="bk_ewsmaerrors"> </a></span><span class="sxs-lookup"><span data-stu-id="a9de9-167"></span></span>

<span data-ttu-id="a9de9-168">如果 EWS 托管 API 代码引发**异常**，您可以使用[Exception.Message](http://msdn.microsoft.com/zh-cn/library/9btwf6wk)值以确定错误的源。</span><span class="sxs-lookup"><span data-stu-id="a9de9-168">If your EWS Managed API code throws an **Exception**, you can use the [Exception.Message](http://msdn.microsoft.com/zh-cn/library/9btwf6wk) value to determine the source of the error.</span></span> <span data-ttu-id="a9de9-169">**Message**属性包含基础的 SOAP 响应中的[MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)元素的内容。</span><span class="sxs-lookup"><span data-stu-id="a9de9-169">The **Message** property contains the contents of the [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx) element in the underlying SOAP response.</span></span> <span data-ttu-id="a9de9-170">此外，如果例外的类型[ServiceResponseException](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx)对象，一个最常见的异常，您还可以检索的基础的 SOAP [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素和[响应](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx)中包含[错误代码](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx)标识相关联的[服务](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx)对象的属性。</span><span class="sxs-lookup"><span data-stu-id="a9de9-170">In addition, if the exception is of type [ServiceResponseException](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception%28v=exchg.80%29.aspx) object, one of the most common exceptions, you can also retrieve the [ErrorCode](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception.errorcode%28v=exchg.80%29.aspx) contained in the underlying SOAP [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element, and the [Response](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponseexception.response%28v=exchg.80%29.aspx) property that identifies the associated [ServiceResponse](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) object.</span></span> <span data-ttu-id="a9de9-171">下面的代码演示如何捕获并显示**ServiceResponseException**的内容。</span><span class="sxs-lookup"><span data-stu-id="a9de9-171">The following code shows how to catch and display the contents of a **ServiceResponseException**.</span></span> 
  
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

<span data-ttu-id="a9de9-172">如果您调用的方法返回**ServiceResponseCollection**，并且**OverallResult**属性的值等于**警告**或**错误**，您将需要遍历到**ServiceResponseCollection**中每个对象查找错误。</span><span class="sxs-lookup"><span data-stu-id="a9de9-172">If the method you called returns a **ServiceResponseCollection**, and the value of the **OverallResult** property is equal to **Warning** or **Error**, you'll have to loop through each object in the **ServiceResponseCollection** to find the error.</span></span> <span data-ttu-id="a9de9-173">**OverallResult**属性设置为**警告**如果至少一个响应具有其**结果**值设置为**Warning** ，并且所有其他响应其**结果**将值设置为**成功**。</span><span class="sxs-lookup"><span data-stu-id="a9de9-173">The **OverallResult** property is set to **Warning** if at least one response has its **Result** value set to **Warning** and all other responses have their **Result** values set to **Success**.</span></span> <span data-ttu-id="a9de9-174">**OverallResult**属性设置为**错误**如果至少一个响应具有其**结果**值设置为**错误**。</span><span class="sxs-lookup"><span data-stu-id="a9de9-174">The **OverallResult** property is set to **Error** if at least one response has its **Result** value set to **Error**.</span></span> <span data-ttu-id="a9de9-175">当**OverallResult**设置为**警告**或**错误**时，将以下属性设置为适当的**服务**对象：</span><span class="sxs-lookup"><span data-stu-id="a9de9-175">When the **OverallResult** is set to **Warning** or **Error**, the following properties are set on the **ServiceResponse** objects as appropriate:</span></span> 
  
- <span data-ttu-id="a9de9-176">[ErrorCode](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — 包含可以用于查找其他疑难解答的资源的错误代码。</span><span class="sxs-lookup"><span data-stu-id="a9de9-176">[ErrorCode](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx) — Contains the error code, which can be used to find additional troubleshooting resources.</span></span> 
    
- <span data-ttu-id="a9de9-177">[ErrorDetails](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — 包含一些**ErrorCodes**有关错误的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a9de9-177">[ErrorDetails](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx) — Contains details about the error for some **ErrorCodes**.</span></span> <span data-ttu-id="a9de9-178">例如，错误代码时**ErrorRecurrenceHasNoOccurrence**， **ErrorDetails**将**EffectiveStartDate**和**EffectiveEndDate**包含键。</span><span class="sxs-lookup"><span data-stu-id="a9de9-178">For example, when the error code is **ErrorRecurrenceHasNoOccurrence**, the **ErrorDetails** will contain keys for **EffectiveStartDate** and **EffectiveEndDate**.</span></span> 
    
- <span data-ttu-id="a9de9-179">[ErrorMessage](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — 描述错误。</span><span class="sxs-lookup"><span data-stu-id="a9de9-179">[ErrorMessage](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx) — Describes the error.</span></span> 
    
- <span data-ttu-id="a9de9-180">[ErrorProperties](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — 如果可用，标识导致出错的属性。</span><span class="sxs-lookup"><span data-stu-id="a9de9-180">[ErrorProperties](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx) — If available, identifies the properties that caused the error.</span></span> <span data-ttu-id="a9de9-181">例如时的错误代码， **ErrorInvalidPropertyForOperation**, **ErrorProperties**包含无效请求的属性的定义。</span><span class="sxs-lookup"><span data-stu-id="a9de9-181">For example, when the error code is **ErrorInvalidPropertyForOperation**, **ErrorProperties** contains the definition of the property that was invalid for the request.</span></span> 
    
- <span data-ttu-id="a9de9-182">[结果](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)— 包含**错误**或**警告**时遇到问题。</span><span class="sxs-lookup"><span data-stu-id="a9de9-182">[Result](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx) — Contains **Error** or **Warning** when an issue is encountered.</span></span> 
    
<span data-ttu-id="a9de9-183">如果**服务**属性并由它们提供的信息不提供足够的信息来纠正方法调用或取消阻止您，请参阅[下一步步骤](#bk_nextsteps)搜集**ErrorCode**值的详细信息。</span><span class="sxs-lookup"><span data-stu-id="a9de9-183">If the information provided by the **ServiceResponse** properties doesn't provide enough information to correct your method call or unblock you, see [Next steps](#bk_nextsteps) to dig up more information on **ErrorCode** values.</span></span> 
  
## 
<span data-ttu-id="a9de9-184"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="a9de9-184"></span></span>

<span data-ttu-id="a9de9-185">您可以查找以下主题中的其他问题排查信息：</span><span class="sxs-lookup"><span data-stu-id="a9de9-185">You can look up additional troubleshooting information in the following topics:</span></span>
  
- <span data-ttu-id="a9de9-186">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)元素</span><span class="sxs-lookup"><span data-stu-id="a9de9-186">[ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element</span></span> 
    
- <span data-ttu-id="a9de9-187">[服务错误](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)枚举</span><span class="sxs-lookup"><span data-stu-id="a9de9-187">[ServiceError](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) enumeration</span></span> 
    
- [<span data-ttu-id="a9de9-188">EWS 属性相关错误</span><span class="sxs-lookup"><span data-stu-id="a9de9-188">EWS property-related errors</span></span>](ews-property-related-errors.md)
    
<span data-ttu-id="a9de9-189">此外，具体取决于什么您正在尝试完成您的请求中，可能会发现的错误代码的其他有用信息在以下主题：</span><span class="sxs-lookup"><span data-stu-id="a9de9-189">In addition, depending on what you're trying to accomplish in your request, you might find additional helpful information about the error code in the following topics:</span></span>
  
- [<span data-ttu-id="a9de9-190">处理自动发现错误消息</span><span class="sxs-lookup"><span data-stu-id="a9de9-190">Handling Autodiscover error messages</span></span>](handling-autodiscover-error-messages.md)
    
- [<span data-ttu-id="a9de9-191">在 Exchange 处理与通知相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="a9de9-191">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="a9de9-192">在 Exchange 处理同步相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="a9de9-192">Handling synchronization-related errors in EWS in Exchange</span></span>](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="a9de9-193">在 Exchange 处理删除相关 EWS 中的错误</span><span class="sxs-lookup"><span data-stu-id="a9de9-193">Handling deletion-related errors in EWS in Exchange</span></span>](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a><span data-ttu-id="a9de9-194">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a9de9-194">See also</span></span>


- [<span data-ttu-id="a9de9-195">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="a9de9-195">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="a9de9-196">工具和资源来解决 exchange 的 EWS 应用程序</span><span class="sxs-lookup"><span data-stu-id="a9de9-196">Tools and resources for troubleshooting EWS applications for Exchange</span></span>](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

