---
title: AggregateOn
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AggregateOn
api_type:
- schema
ms.assetid: 9b0a03f2-3282-46e1-b1a0-cbb9a0fbe9bb
description: AggregateOn 元素表示用于确定分组的 FindItem 结果集的分组项顺序的属性。
ms.openlocfilehash: 04359c187ef11538d64f8f0d3ea2fe84bc3d048b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463564"
---
# <a name="aggregateon"></a><span data-ttu-id="49150-103">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="49150-103">AggregateOn</span></span>

<span data-ttu-id="49150-104">**AggregateOn**元素表示用于确定分组的 FindItem 结果集的分组项顺序的属性。</span><span class="sxs-lookup"><span data-stu-id="49150-104">The **AggregateOn** element represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span> 
  
- [<span data-ttu-id="49150-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="49150-105">FindItem</span></span>](finditem.md)  
- [<span data-ttu-id="49150-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="49150-106">GroupBy</span></span>](groupby.md)
- [<span data-ttu-id="49150-107">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="49150-107">AggregateOn</span></span>](aggregateon.md)
  
```xml
<AggregateOn>
   <FieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <IndexedFieldURI/>
</AggregateOn>
```

```xml
<AggregateOn>
   <ExtendedFieldURI/>
</AggregateOn>
```
 
<span data-ttu-id="49150-108">**AggregateOnType**</span><span class="sxs-lookup"><span data-stu-id="49150-108">**AggregateOnType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="49150-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="49150-109">Attributes and elements</span></span>

<span data-ttu-id="49150-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="49150-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="49150-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="49150-111">Attributes</span></span>

|<span data-ttu-id="49150-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="49150-112">**Attribute**</span></span>|<span data-ttu-id="49150-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="49150-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="49150-114">**Aggregate**</span><span class="sxs-lookup"><span data-stu-id="49150-114">**Aggregate**</span></span> <br/> | <span data-ttu-id="49150-115">指示用于对项目组进行排序的[FieldURI](fielduri.md)元素所标识的属性的最大值或最小值。</span><span class="sxs-lookup"><span data-stu-id="49150-115">Indicates the maximum or minimum value of the property identified by the [FieldURI](fielduri.md) element that is used for ordering the groups of items.</span></span><br/><br/><span data-ttu-id="49150-116">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="49150-116">The following are the possible values:</span></span>  <br/><br/><span data-ttu-id="49150-117">-最低</span><span class="sxs-lookup"><span data-stu-id="49150-117">- Minimum</span></span>  <br/><span data-ttu-id="49150-118">-最大</span><span class="sxs-lookup"><span data-stu-id="49150-118">- Maximum</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="49150-119">子元素</span><span class="sxs-lookup"><span data-stu-id="49150-119">Child elements</span></span>

|<span data-ttu-id="49150-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="49150-120">**Element**</span></span>|<span data-ttu-id="49150-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="49150-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49150-122">FieldURI</span><span class="sxs-lookup"><span data-stu-id="49150-122">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="49150-123">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="49150-123">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="49150-124">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="49150-124">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="49150-125">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="49150-125">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="49150-126">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="49150-126">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="49150-127">标识要获取、设置或创建的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="49150-127">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="49150-128">父元素</span><span class="sxs-lookup"><span data-stu-id="49150-128">Parent elements</span></span>

|<span data-ttu-id="49150-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="49150-129">**Element**</span></span>|<span data-ttu-id="49150-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="49150-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="49150-131">GroupBy</span><span class="sxs-lookup"><span data-stu-id="49150-131">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="49150-132">指定 FindItem 查询的任意分组。</span><span class="sxs-lookup"><span data-stu-id="49150-132">Specifies arbitrary groupings for FindItem queries.</span></span>  <br/> <span data-ttu-id="49150-133">下面是此元素的 XPath 表达式:  `/FindItem/GroupBy`</span><span class="sxs-lookup"><span data-stu-id="49150-133">The following is the XPath expression to this element:  `/FindItem/GroupBy`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49150-134">备注</span><span class="sxs-lookup"><span data-stu-id="49150-134">Remarks</span></span>

<span data-ttu-id="49150-135">[FindItem 操作](finditem-operation.md)可以返回已分组的结果。</span><span class="sxs-lookup"><span data-stu-id="49150-135">The [FindItem operation](finditem-operation.md) can return grouped results.</span></span> <span data-ttu-id="49150-136">在分组结果中，具有给定分组属性的相同值的所有项都将一起收集，并显示为该组的子级。</span><span class="sxs-lookup"><span data-stu-id="49150-136">Within grouped results, all items that have the same value for a given grouping property are gathered together and presented as children of that group.</span></span> <span data-ttu-id="49150-137">例如，如果按发件人进行分组，则所有电子邮件都将根据用户是否来自发件人 A、发件人 B 等组织到不同的组中。</span><span class="sxs-lookup"><span data-stu-id="49150-137">For example, if you group by sender, all e-mails are organized into separate groups based on whether they are from sender A, sender B, and so on.</span></span> <span data-ttu-id="49150-138">这些组是发件人组的子项。</span><span class="sxs-lookup"><span data-stu-id="49150-138">These groups are children of the sender group.</span></span> 
  
<span data-ttu-id="49150-139">发件人组中的每个组都包含项目的集合，例如来自每个发件人的实际电子邮件。</span><span class="sxs-lookup"><span data-stu-id="49150-139">Each of the groups within the sender group contains a collection of items, such as the actual e-mails that came from each sender.</span></span> <span data-ttu-id="49150-140">您可以使用[SortOrder](sortorder.md)元素对组中的项目进行排序。</span><span class="sxs-lookup"><span data-stu-id="49150-140">You can use the [SortOrder](sortorder.md) element to sort the items within a group.</span></span> <span data-ttu-id="49150-141">但是，若要根据项目的属性值对组进行排序，则必须使用聚合。</span><span class="sxs-lookup"><span data-stu-id="49150-141">To sort the groups based on an item's property values, however, you must use aggregation.</span></span> 
  
<span data-ttu-id="49150-142">使用聚合，组的顺序基于组中项目的特定属性。</span><span class="sxs-lookup"><span data-stu-id="49150-142">With aggregation, the order of groups is based on a specific property of the items within the group.</span></span> <span data-ttu-id="49150-143">使用聚合对组中的项目进行排序时，必须确定对组进行排序所依据的代表性属性。</span><span class="sxs-lookup"><span data-stu-id="49150-143">When you use aggregation to sort items within a group, you must identify a representative property by which to sort the groups.</span></span> <span data-ttu-id="49150-144">您可以使用**AggregateOn**元素来指定代表属性。</span><span class="sxs-lookup"><span data-stu-id="49150-144">You can use the **AggregateOn** element to specify the representative property.</span></span> 
  
<span data-ttu-id="49150-145">如果确定了代表性属性，则**聚合**属性用于指示是否根据已确定的属性的最大值或最小值对组进行排序。</span><span class="sxs-lookup"><span data-stu-id="49150-145">When a representative property is identified, the **Aggregate** attribute is used to indicate whether the groups are sorted according to the maximum or the minimum value of the identified property.</span></span> <span data-ttu-id="49150-146">如果将**Aggregate**属性设置为 "最大值"，则将从**AggregateOn**属性的最大值开始对组进行排序。</span><span class="sxs-lookup"><span data-stu-id="49150-146">If the **Aggregate** attribute is set to Maximum, the groups are sorted beginning with the largest value for the **AggregateOn** property.</span></span> <span data-ttu-id="49150-147">如果将**Aggregate**属性设置为 "最小值"，则将从**AggregateOn**属性的最小值开始对组进行排序。</span><span class="sxs-lookup"><span data-stu-id="49150-147">If the **Aggregate** attribute is set to Minimum, the groups are sorted beginning with the smallest value for the **AggregateOn** property.</span></span> 
  
<span data-ttu-id="49150-148">例如，如果您想要发出 FindItem 分组查询，按发件人进行分组，但您希望对组进行排序，以便将最近的电子邮件的组放在最上面，则可以按发件人进行分组，并按接收到最大的**聚合**属性的日期/时间进行聚合。</span><span class="sxs-lookup"><span data-stu-id="49150-148">For example, if you want to issue a FindItem grouped query, grouping by sender, but you want to order the groups so that the group with the most recent e-mail message is on top, you can group by sender and aggregate on date/time received with an **Aggregate** attribute of Maximum.</span></span> 
  
<span data-ttu-id="49150-149">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="49150-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="49150-150">示例</span><span class="sxs-lookup"><span data-stu-id="49150-150">Example</span></span>

<span data-ttu-id="49150-151">下面的示例展示了一个分组的 FindItem 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="49150-151">The following example shows a grouped FindItem request and response.</span></span> <span data-ttu-id="49150-152">该示例演示返回按**ConversationTopic**属性分组的项的请求。</span><span class="sxs-lookup"><span data-stu-id="49150-152">The example shows a request to return items grouped by the **ConversationTopic** property.</span></span> <span data-ttu-id="49150-153">根据[DateTimeReceived](datetimereceived.md)属性的最大值，以降序返回两个组： A 和 B。</span><span class="sxs-lookup"><span data-stu-id="49150-153">Two groups, A and B, are returned in descending order based on the maximum value of the [DateTimeReceived](datetimereceived.md) property.</span></span> 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
                Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="message:ConversationTopic"/>
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AdditionalProperties>    
      </ItemShape>
      <IndexedPageItemView BasePoint="Beginning" MaxEntriesReturned="20" Offset="0"/>
      <GroupBy Order="Ascending">
        <t:FieldURI FieldURI="message:ConversationTopic"/>
        <t:AggregateOn Aggregate="Maximum">
          <t:FieldURI FieldURI="item:DateTimeReceived"/>
        </t:AggregateOn>
      </GroupBy>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
<!-- EXAMPLE RESPONSE -->
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="8" TotalItemsInView="8" IncludesLastItemInRange="true">
            <t:Groups>
              <t:GroupedItems>
                <t:GroupIndex>B</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAH=" ChangeKey="CQAAABY" />
                    <t:DateTimeReceived>2006-09-14T23:59:18Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnAHR=" ChangeKey="CQAAAw" />
                    <t:DateTimeReceived>2006-09-15T00:00:24Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQAnA==" ChangeKey="CQAAJXT" />
                    <t:DateTimeReceived>2006-09-15T00:22:45Z</t:DateTimeReceived>
                    <t:ConversationTopic>B</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
              <t:GroupedItems>
                <t:GroupIndex>A</t:GroupIndex>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AQAnAAA==" ChangeKey="CQCJNe" />
                    <t:DateTimeReceived>2006-09-14T23:56:12Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AQWgAA==" ChangeKey="CQAACJV6" />
                    <t:DateTimeReceived>2006-09-14T23:57:33Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                  <t:Message>
                    <t:ItemId Id="AAAA==" ChangeKey="CQA6CJXw" />
                    <t:DateTimeReceived>2006-09-15T00:23:31Z</t:DateTimeReceived>
                    <t:ConversationTopic>A</t:ConversationTopic>
                  </t:Message>
                </t:Items>
              </t:GroupedItems>
            </t:Groups>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="49150-154">若要对组中的项目进行排序，请使用[SortOrder](sortorder.md)元素。</span><span class="sxs-lookup"><span data-stu-id="49150-154">To sort the items in a group, use the [SortOrder](sortorder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="49150-155">项目标识符和更改密钥已缩短，以保持可读性。</span><span class="sxs-lookup"><span data-stu-id="49150-155">The item identifiers and change keys have been shortened to preserve readability.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="49150-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="49150-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49150-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="49150-157">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="49150-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="49150-158">Schema Name</span></span>  <br/> |<span data-ttu-id="49150-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="49150-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="49150-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="49150-160">Validation File</span></span>  <br/> |<span data-ttu-id="49150-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="49150-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="49150-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="49150-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="49150-163">False</span><span class="sxs-lookup"><span data-stu-id="49150-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="49150-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="49150-164">See also</span></span>

- [<span data-ttu-id="49150-165">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="49150-165">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="49150-166">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="49150-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="49150-167">查找项目</span><span class="sxs-lookup"><span data-stu-id="49150-167">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

