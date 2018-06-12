---
title: UpdateItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateItem
api_type:
- schema
ms.assetid: 5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4
description: UpdateItem 操作用于修改 Exchange 存储中现有项目的属性。
ms.openlocfilehash: 009ba16315017c4418fbd71d49744015c4d6d1b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838401"
---
# <a name="updateitem-operation"></a><span data-ttu-id="c7254-103">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="c7254-103">UpdateItem operation</span></span>

<span data-ttu-id="c7254-104">**UpdateItem**操作用于修改 Exchange 存储中现有项目的属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-104">The **UpdateItem** operation is used to modify the properties of an existing item in the Exchange store.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c7254-105">备注</span><span class="sxs-lookup"><span data-stu-id="c7254-105">Remarks</span></span>

<span data-ttu-id="c7254-106">您可以在项目上执行三个基本 update 操作。</span><span class="sxs-lookup"><span data-stu-id="c7254-106">You can perform three basic update actions on an item.</span></span> <span data-ttu-id="c7254-107">下表列出了您可以执行的操作。</span><span class="sxs-lookup"><span data-stu-id="c7254-107">The following table lists the actions that you can perform.</span></span>
  
|<span data-ttu-id="c7254-108">**操作**</span><span class="sxs-lookup"><span data-stu-id="c7254-108">**Action**</span></span>|<span data-ttu-id="c7254-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7254-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7254-110">追加</span><span class="sxs-lookup"><span data-stu-id="c7254-110">Append</span></span>  <br/> |<span data-ttu-id="c7254-111">将数据添加到现有属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-111">Adds data to an existing property.</span></span> <span data-ttu-id="c7254-112">此操作可保留当前的数据。</span><span class="sxs-lookup"><span data-stu-id="c7254-112">This action preserves the current data.</span></span> <span data-ttu-id="c7254-113">追加不适用于所有属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-113">Append does not apply to all properties.</span></span>  <br/> |
|<span data-ttu-id="c7254-114">设置</span><span class="sxs-lookup"><span data-stu-id="c7254-114">Set</span></span>  <br/> |<span data-ttu-id="c7254-115">如果属性包含数据，或创建属性并设置其值，如果属性不存在，将替换为属性的数据。</span><span class="sxs-lookup"><span data-stu-id="c7254-115">Replaces data for a property if the property contains data, or creates the property and sets its value if the property does not exist.</span></span> <span data-ttu-id="c7254-116">设置操作仅适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-116">The set action is only applicable to writable properties.</span></span>  <br/> |
|<span data-ttu-id="c7254-117">Delete</span><span class="sxs-lookup"><span data-stu-id="c7254-117">Delete</span></span>  <br/> |<span data-ttu-id="c7254-118">从项目中删除属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-118">Removes a property from an item.</span></span> <span data-ttu-id="c7254-119">这与属性设置为空值。</span><span class="sxs-lookup"><span data-stu-id="c7254-119">This differs from setting a property to an empty value.</span></span> <span data-ttu-id="c7254-120">完成此操作后，该属性不存在的项目。</span><span class="sxs-lookup"><span data-stu-id="c7254-120">When this action is finished, the property does not exist for the item.</span></span> <span data-ttu-id="c7254-121">删除才适用于可写属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-121">Delete is only applicable to writable properties.</span></span>  <br/> |
   
<span data-ttu-id="c7254-122">**UpdateItem**呼叫可修改一个或多个项目和对每个项目的一个或多个属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-122">An **UpdateItem** call can be used to modify one or more items, and one or more properties on each item.</span></span> <span data-ttu-id="c7254-123">[ItemChanges](itemchanges.md)元素包含要执行此呼叫的一部分的所有的修改。</span><span class="sxs-lookup"><span data-stu-id="c7254-123">The [ItemChanges](itemchanges.md) element contains all the modifications that are to be performed as part of this call.</span></span> <span data-ttu-id="c7254-124">[ItemChange](itemchange.md)元素， [ItemChanges](itemchanges.md)元素的子元素均表示单个项目上执行的修改。</span><span class="sxs-lookup"><span data-stu-id="c7254-124">The [ItemChange](itemchange.md) element, a child of the [ItemChanges](itemchanges.md) element, represents the modifications to be performed on a single item.</span></span> <span data-ttu-id="c7254-125">[ItemChange](itemchange.md)元素包含一组可对单个项目执行的 update 操作。</span><span class="sxs-lookup"><span data-stu-id="c7254-125">The [ItemChange](itemchange.md) element contains a set of update actions that can be performed on a single item.</span></span> <span data-ttu-id="c7254-126">[更新 （项）](updates-item.md)元素中包含这些更改。</span><span class="sxs-lookup"><span data-stu-id="c7254-126">These changes are contained in the [Updates (Item)](updates-item.md) element.</span></span> <span data-ttu-id="c7254-127">[ItemId](itemid.md)元素标识要更新的项。</span><span class="sxs-lookup"><span data-stu-id="c7254-127">The [ItemId](itemid.md) element identifies the item to update.</span></span> <span data-ttu-id="c7254-128">若要更新的项的多个属性， [SetItemField](setitemfield.md)、 [AppendToItemField](appendtoitemfield.md)或[DeleteItemField](deleteitemfield.md)必须提供需要更新的每个属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-128">To update more than one property on an item, a [SetItemField](setitemfield.md), [AppendToItemField](appendtoitemfield.md), or [DeleteItemField](deleteitemfield.md) must be provided for each property that requires the update.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c7254-129">指定它们的顺序应用更新操作。</span><span class="sxs-lookup"><span data-stu-id="c7254-129">Update actions are applied in the order in which they are specified.</span></span> 
  
<span data-ttu-id="c7254-130">对于每个更改，您必须使用其新的值指定要更改的属性的路径和该项目的表示形式。</span><span class="sxs-lookup"><span data-stu-id="c7254-130">For each change, you have to specify the path of the property to change and a representation of that item with its new value.</span></span> <span data-ttu-id="c7254-131">删除操作是略有不同的这是的只有属性应删除的路径，则需要。</span><span class="sxs-lookup"><span data-stu-id="c7254-131">The delete action is slightly different in that only the path of the property that should be deleted is required.</span></span> <span data-ttu-id="c7254-132">组和追加操作，指定的路径必须指向同一属性中的项目表示要设置的。</span><span class="sxs-lookup"><span data-stu-id="c7254-132">For set and append actions, the path that is specified must refer to the same property that is being set in the item representation.</span></span> <span data-ttu-id="c7254-133">如果这些不同，则将返回错误。</span><span class="sxs-lookup"><span data-stu-id="c7254-133">If these differ, an error will be returned.</span></span>
  
<span data-ttu-id="c7254-134">**UpdateItem**操作可以设置 Exchange 存储项目的[开始](start.md)和[结束](end-ex15websvcsotherref.md)时间。</span><span class="sxs-lookup"><span data-stu-id="c7254-134">The **UpdateItem** operation can set the [Start](start.md) and [End ](end-ex15websvcsotherref.md) time of an Exchange store item.</span></span> <span data-ttu-id="c7254-135">在**UpdateItem**请求中，可以没有还设置的[结束](end-ex15websvcsotherref.md)时间设置[开始](start.md)时间。</span><span class="sxs-lookup"><span data-stu-id="c7254-135">In an **UpdateItem** request, the [Start](start.md) time can be set without also setting the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="c7254-136">如果[开始](start.md)时间晚于的[结束](end-ex15websvcsotherref.md)时间，这会导致错误。</span><span class="sxs-lookup"><span data-stu-id="c7254-136">This can cause an error if the [Start](start.md) time is later than the [End ](end-ex15websvcsotherref.md) time.</span></span> <span data-ttu-id="c7254-137">注意客户端应用程序必须调整[开始](start.md)时间才能保留持续时间的更改时的[结束](end-ex15websvcsotherref.md)时间。</span><span class="sxs-lookup"><span data-stu-id="c7254-137">Be aware that client applications must adjust the [End ](end-ex15websvcsotherref.md) time when the [Start](start.md) time is changed in order to preserve the duration.</span></span> 
  
<span data-ttu-id="c7254-138">更新单个日历项目时成为定期主日历项，您必须[MeetingTimeZone](meetingtimezone.md)属性的设置**UpdateItem**操作才能保留的日历项目的原始时区。</span><span class="sxs-lookup"><span data-stu-id="c7254-138">When a single calendar item is updated to become a recurring master calendar item, the [MeetingTimeZone](meetingtimezone.md) property must be set by the **UpdateItem** operation in order to preserve the calendar item's original time zone.</span></span> 
  
## <a name="setitemfield-request-example"></a><span data-ttu-id="c7254-139">SetItemField 请求示例</span><span class="sxs-lookup"><span data-stu-id="c7254-139">SetItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="c7254-140">说明</span><span class="sxs-lookup"><span data-stu-id="c7254-140">Description</span></span>

<span data-ttu-id="c7254-141">**UpdateItem**请求的下面的示例演示如何设置对项目的 sensitivity 属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-141">The following example of an **UpdateItem** request shows how to set the sensitivity property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7254-142">代码</span><span class="sxs-lookup"><span data-stu-id="c7254-142">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkb..." ChangeKey="CQAAABYAAAB..."/>
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Sensitivity"/>
              <t:Message>
                <t:Sensitivity>Normal</t:Sensitivity>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c7254-143">注释</span><span class="sxs-lookup"><span data-stu-id="c7254-143">Comments</span></span>

<span data-ttu-id="c7254-144">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="c7254-144">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="setitemfield-request-elements"></a><span data-ttu-id="c7254-145">SetItemField 请求元素</span><span class="sxs-lookup"><span data-stu-id="c7254-145">SetItemField Request Elements</span></span>

<span data-ttu-id="c7254-146">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7254-146">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="c7254-147">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c7254-147">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="c7254-148">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="c7254-148">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="c7254-149">ItemChange</span><span class="sxs-lookup"><span data-stu-id="c7254-149">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="c7254-150">ItemId</span><span class="sxs-lookup"><span data-stu-id="c7254-150">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="c7254-151">更新 （项）</span><span class="sxs-lookup"><span data-stu-id="c7254-151">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="c7254-152">SetItemField</span><span class="sxs-lookup"><span data-stu-id="c7254-152">SetItemField</span></span>](setitemfield.md)
    
- [<span data-ttu-id="c7254-153">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c7254-153">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="c7254-154">Message</span><span class="sxs-lookup"><span data-stu-id="c7254-154">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c7254-155">Sensitivity</span><span class="sxs-lookup"><span data-stu-id="c7254-155">Sensitivity</span></span>](sensitivity.md)
    
## <a name="appendtoitemfield-request-example"></a><span data-ttu-id="c7254-156">AppendToItemField 请求示例</span><span class="sxs-lookup"><span data-stu-id="c7254-156">AppendToItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="c7254-157">说明</span><span class="sxs-lookup"><span data-stu-id="c7254-157">Description</span></span>

<span data-ttu-id="c7254-158">**UpdateItem**请求的下面的示例演示如何将文本追加到的项的 body 属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-158">The following example of an **UpdateItem** request shows how to append text to the body property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7254-159">代码</span><span class="sxs-lookup"><span data-stu-id="c7254-159">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYA..."/>
          <t:Updates>
            <t:AppendToItemField>
              <t:FieldURI FieldURI="item:Body"/>
              <t:Message>
                <t:Body BodyType="Text">Some additional text to append</t:Body>
              </t:Message>
            </t:AppendToItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c7254-160">注释</span><span class="sxs-lookup"><span data-stu-id="c7254-160">Comments</span></span>

<span data-ttu-id="c7254-161">以下属性支持 append 操作：</span><span class="sxs-lookup"><span data-stu-id="c7254-161">The following properties support the append action:</span></span>
  
- <span data-ttu-id="c7254-162">**消息： 回复**</span><span class="sxs-lookup"><span data-stu-id="c7254-162">**message:ReplyTo**</span></span>
    
- <span data-ttu-id="c7254-163">**项目： 正文**</span><span class="sxs-lookup"><span data-stu-id="c7254-163">**item:Body**</span></span>
    
- <span data-ttu-id="c7254-164">所有收件人和与会者集合属性</span><span class="sxs-lookup"><span data-stu-id="c7254-164">All the recipient and attendee collection properties</span></span>
    
<span data-ttu-id="c7254-165">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="c7254-165">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="appendtoitemfield-request-elements"></a><span data-ttu-id="c7254-166">AppendToItemField 请求元素</span><span class="sxs-lookup"><span data-stu-id="c7254-166">AppendToItemField Request Elements</span></span>

<span data-ttu-id="c7254-167">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7254-167">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="c7254-168">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c7254-168">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="c7254-169">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="c7254-169">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="c7254-170">ItemChange</span><span class="sxs-lookup"><span data-stu-id="c7254-170">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="c7254-171">ItemId</span><span class="sxs-lookup"><span data-stu-id="c7254-171">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="c7254-172">更新 （项）</span><span class="sxs-lookup"><span data-stu-id="c7254-172">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="c7254-173">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="c7254-173">AppendToItemField</span></span>](appendtoitemfield.md)
    
- [<span data-ttu-id="c7254-174">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c7254-174">FieldURI</span></span>](fielduri.md)
    
- [<span data-ttu-id="c7254-175">Message</span><span class="sxs-lookup"><span data-stu-id="c7254-175">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c7254-176">Body</span><span class="sxs-lookup"><span data-stu-id="c7254-176">Body</span></span>](body.md)
    
## <a name="deleteitemfield-request-example"></a><span data-ttu-id="c7254-177">DeleteItemField 请求示例</span><span class="sxs-lookup"><span data-stu-id="c7254-177">DeleteItemField request example</span></span>

### <a name="description"></a><span data-ttu-id="c7254-178">说明</span><span class="sxs-lookup"><span data-stu-id="c7254-178">Description</span></span>

<span data-ttu-id="c7254-179">**UpdateItem**请求的下面的示例演示如何删除上一个项目的属性。</span><span class="sxs-lookup"><span data-stu-id="c7254-179">The following example of an **UpdateItem** request shows how to delete a property on an item.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7254-180">代码</span><span class="sxs-lookup"><span data-stu-id="c7254-180">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
  xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AutoResolve" 
                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="AAAtAEFkbWluaXN0cm..." ChangeKey="CQAAABYAA..."/>
          <t:Updates>
            <t:DeleteItemField>
              <t:FieldURI FieldURI="item:Body"/>
            </t:DeleteItemField>
          </t:Updates>
        </t:ItemChange>
      </ItemChanges>
    </UpdateItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c7254-181">注释</span><span class="sxs-lookup"><span data-stu-id="c7254-181">Comments</span></span>

<span data-ttu-id="c7254-182">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="c7254-182">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="deleteitemfield-request-elements"></a><span data-ttu-id="c7254-183">DeleteItemField 请求元素</span><span class="sxs-lookup"><span data-stu-id="c7254-183">DeleteItemField Request Elements</span></span>

<span data-ttu-id="c7254-184">请求中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7254-184">The following elements are used in the request:</span></span>
  
- [<span data-ttu-id="c7254-185">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="c7254-185">UpdateItem</span></span>](updateitem.md)
    
- [<span data-ttu-id="c7254-186">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="c7254-186">ItemChanges</span></span>](itemchanges.md)
    
- [<span data-ttu-id="c7254-187">ItemChange</span><span class="sxs-lookup"><span data-stu-id="c7254-187">ItemChange</span></span>](itemchange.md)
    
- [<span data-ttu-id="c7254-188">ItemId</span><span class="sxs-lookup"><span data-stu-id="c7254-188">ItemId</span></span>](itemid.md)
    
- [<span data-ttu-id="c7254-189">更新 （项）</span><span class="sxs-lookup"><span data-stu-id="c7254-189">Updates (Item)</span></span>](updates-item.md)
    
- [<span data-ttu-id="c7254-190">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="c7254-190">DeleteItemField</span></span>](deleteitemfield.md)
    
- [<span data-ttu-id="c7254-191">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c7254-191">FieldURI</span></span>](fielduri.md)
    
## <a name="successful-response-example"></a><span data-ttu-id="c7254-192">成功的响应示例</span><span class="sxs-lookup"><span data-stu-id="c7254-192">Successful response example</span></span>

### <a name="description"></a><span data-ttu-id="c7254-193">说明</span><span class="sxs-lookup"><span data-stu-id="c7254-193">Description</span></span>

<span data-ttu-id="c7254-194">下面的示例演示对**UpdateItem**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="c7254-194">The following example shows a successful response to an **UpdateItem** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="c7254-195">代码</span><span class="sxs-lookup"><span data-stu-id="c7254-195">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
  xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="664" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <UpdateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAAtAEFkbW..." ChangeKey="CQAAABYAAA..."/>
            </t:Message>
          </m:Items>
        </m:UpdateItemResponseMessage>
      </m:ResponseMessages>
    </UpdateItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="c7254-196">注释</span><span class="sxs-lookup"><span data-stu-id="c7254-196">Comments</span></span>

<span data-ttu-id="c7254-197">已缩短的项标识符和更改密钥，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="c7254-197">The item identifier and change key have been shortened to preserve readability.</span></span>
  
### <a name="successful-response-elements"></a><span data-ttu-id="c7254-198">成功响应元素</span><span class="sxs-lookup"><span data-stu-id="c7254-198">Successful response elements</span></span>

<span data-ttu-id="c7254-199">在响应中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="c7254-199">The following elements are used in the response:</span></span>
  
- [<span data-ttu-id="c7254-200">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="c7254-200">ServerVersionInfo</span></span>](serverversioninfo.md)
    
- [<span data-ttu-id="c7254-201">UpdateItemResponse</span><span class="sxs-lookup"><span data-stu-id="c7254-201">UpdateItemResponse</span></span>](updateitemresponse.md)
    
- [<span data-ttu-id="c7254-202">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7254-202">ResponseMessages</span></span>](responsemessages.md)
    
- [<span data-ttu-id="c7254-203">UpdateItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c7254-203">UpdateItemResponseMessage</span></span>](updateitemresponsemessage.md)
    
- [<span data-ttu-id="c7254-204">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="c7254-204">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="c7254-205">Items</span><span class="sxs-lookup"><span data-stu-id="c7254-205">Items</span></span>](items.md)
    
- [<span data-ttu-id="c7254-206">Message</span><span class="sxs-lookup"><span data-stu-id="c7254-206">Message</span></span>](message-ex15websvcsotherref.md)
    
- [<span data-ttu-id="c7254-207">ItemId</span><span class="sxs-lookup"><span data-stu-id="c7254-207">ItemId</span></span>](itemid.md)
    
## <a name="see-also"></a><span data-ttu-id="c7254-208">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c7254-208">See also</span></span>



[<span data-ttu-id="c7254-209">UpdateItem 操作 （任务）</span><span class="sxs-lookup"><span data-stu-id="c7254-209">UpdateItem operation (task)</span></span>](updateitem-operation-task.md)
  
[<span data-ttu-id="c7254-210">UpdateItem 操作 （联系人）</span><span class="sxs-lookup"><span data-stu-id="c7254-210">UpdateItem operation (contact)</span></span>](updateitem-operation-contact.md)


- [<span data-ttu-id="c7254-211">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c7254-211">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c7254-212">更新联系人</span><span class="sxs-lookup"><span data-stu-id="c7254-212">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="c7254-213">更新任务</span><span class="sxs-lookup"><span data-stu-id="c7254-213">Updating Tasks</span></span>](http://msdn.microsoft.com/library/0a1bf360-d40c-4a99-929b-4c73a14394d5%28Office.15%29.aspx)

