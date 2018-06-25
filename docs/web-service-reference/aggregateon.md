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
description: AggregateOn 元素均表示用于确定组合 FindItem 结果集的顺序分组的项目的属性。
ms.openlocfilehash: fe14de23e6a4c90d826200cae927427acfccc3c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753131"
---
# <a name="aggregateon"></a><span data-ttu-id="c828f-103">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="c828f-103">AggregateOn</span></span>

<span data-ttu-id="c828f-104">**AggregateOn**元素均表示用于确定组合 FindItem 结果集的顺序分组的项目的属性。</span><span class="sxs-lookup"><span data-stu-id="c828f-104">The **AggregateOn** element represents the property that is used to determine the order of grouped items for a grouped FindItem result set.</span></span> 
  
- [<span data-ttu-id="c828f-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="c828f-105">FindItem</span></span>](finditem.md)  
- [<span data-ttu-id="c828f-106">GroupBy</span><span class="sxs-lookup"><span data-stu-id="c828f-106">GroupBy</span></span>](groupby.md)
- [<span data-ttu-id="c828f-107">AggregateOn</span><span class="sxs-lookup"><span data-stu-id="c828f-107">AggregateOn</span></span>](aggregateon.md)
  
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
 
<span data-ttu-id="c828f-108">**AggregateOnType**</span><span class="sxs-lookup"><span data-stu-id="c828f-108">**AggregateOnType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c828f-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c828f-109">Attributes and elements</span></span>

<span data-ttu-id="c828f-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c828f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c828f-111">属性</span><span class="sxs-lookup"><span data-stu-id="c828f-111">Attributes</span></span>

|<span data-ttu-id="c828f-112">**属性**</span><span class="sxs-lookup"><span data-stu-id="c828f-112">**Attribute**</span></span>|<span data-ttu-id="c828f-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="c828f-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c828f-114">**Aggregate**</span><span class="sxs-lookup"><span data-stu-id="c828f-114">**Aggregate**</span></span> <br/> | <span data-ttu-id="c828f-115">指示由[FieldURI](fielduri.md)元素用于排序的项目的组的标识的属性的最大值或最小值。</span><span class="sxs-lookup"><span data-stu-id="c828f-115">Indicates the maximum or minimum value of the property identified by the [FieldURI](fielduri.md) element that is used for ordering the groups of items.</span></span><br/><br/><span data-ttu-id="c828f-116">以下是可能的值：</span><span class="sxs-lookup"><span data-stu-id="c828f-116">The following are the possible values:</span></span>  <br/><br/><span data-ttu-id="c828f-117">-最小值</span><span class="sxs-lookup"><span data-stu-id="c828f-117">- Minimum</span></span>  <br/><span data-ttu-id="c828f-118">到最大</span><span class="sxs-lookup"><span data-stu-id="c828f-118">- Maximum</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c828f-119">子元素</span><span class="sxs-lookup"><span data-stu-id="c828f-119">Child elements</span></span>

|<span data-ttu-id="c828f-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="c828f-120">**Element**</span></span>|<span data-ttu-id="c828f-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="c828f-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c828f-122">FieldURI</span><span class="sxs-lookup"><span data-stu-id="c828f-122">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="c828f-123">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="c828f-123">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="c828f-124">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c828f-124">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="c828f-125">标识词典中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="c828f-125">Identifies individual members of a dictionary.</span></span>  <br/> |
|[<span data-ttu-id="c828f-126">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="c828f-126">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="c828f-127">标识扩展的 MAPI 属性以获取、 设置或创建。</span><span class="sxs-lookup"><span data-stu-id="c828f-127">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c828f-128">父元素</span><span class="sxs-lookup"><span data-stu-id="c828f-128">Parent elements</span></span>

|<span data-ttu-id="c828f-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="c828f-129">**Element**</span></span>|<span data-ttu-id="c828f-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="c828f-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c828f-131">GroupBy</span><span class="sxs-lookup"><span data-stu-id="c828f-131">GroupBy</span></span>](groupby.md) <br/> |<span data-ttu-id="c828f-132">指定 FindItem 查询的任意分组。</span><span class="sxs-lookup"><span data-stu-id="c828f-132">Specifies arbitrary groupings for FindItem queries.</span></span>  <br/> <span data-ttu-id="c828f-133">下面是此元素的 XPath 表达式:  `/FindItem/GroupBy`</span><span class="sxs-lookup"><span data-stu-id="c828f-133">The following is the XPath expression to this element:  `/FindItem/GroupBy`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c828f-134">备注</span><span class="sxs-lookup"><span data-stu-id="c828f-134">Remarks</span></span>

<span data-ttu-id="c828f-135">[FindItem 操作](finditem-operation.md)可以返回分组的结果。</span><span class="sxs-lookup"><span data-stu-id="c828f-135">The [FindItem operation](finditem-operation.md) can return grouped results.</span></span> <span data-ttu-id="c828f-136">在分组结果，具有相同的值为给定的分组属性的所有项目是收集在一起，并为主该组的子级。</span><span class="sxs-lookup"><span data-stu-id="c828f-136">Within grouped results, all items that have the same value for a given grouping property are gathered together and presented as children of that group.</span></span> <span data-ttu-id="c828f-137">例如，如果按发件人进行分组，所有电子邮件组织成单独组基于是否从发件人 A、 发件人 B，等等。</span><span class="sxs-lookup"><span data-stu-id="c828f-137">For example, if you group by sender, all e-mails are organized into separate groups based on whether they are from sender A, sender B, and so on.</span></span> <span data-ttu-id="c828f-138">这些组是发件人组中的子级。</span><span class="sxs-lookup"><span data-stu-id="c828f-138">These groups are children of the sender group.</span></span> 
  
<span data-ttu-id="c828f-139">每个组的发件人组中包含的项目，如实际的电子邮件从每个发件人的集合。</span><span class="sxs-lookup"><span data-stu-id="c828f-139">Each of the groups within the sender group contains a collection of items, such as the actual e-mails that came from each sender.</span></span> <span data-ttu-id="c828f-140">您可以使用[SortOrder](sortorder.md)元素组中的项进行排序。</span><span class="sxs-lookup"><span data-stu-id="c828f-140">You can use the [SortOrder](sortorder.md) element to sort the items within a group.</span></span> <span data-ttu-id="c828f-141">若要排序基于项目的属性值的组，但是，必须使用聚合。</span><span class="sxs-lookup"><span data-stu-id="c828f-141">To sort the groups based on an item's property values, however, you must use aggregation.</span></span> 
  
<span data-ttu-id="c828f-142">聚合，与组的顺序基于组内的项目的特定属性。</span><span class="sxs-lookup"><span data-stu-id="c828f-142">With aggregation, the order of groups is based on a specific property of the items within the group.</span></span> <span data-ttu-id="c828f-143">当您使用聚合组中的项进行排序时，您必须标识用于排序组代表属性。</span><span class="sxs-lookup"><span data-stu-id="c828f-143">When you use aggregation to sort items within a group, you must identify a representative property by which to sort the groups.</span></span> <span data-ttu-id="c828f-144">**AggregateOn**元素用于指定代表属性。</span><span class="sxs-lookup"><span data-stu-id="c828f-144">You can use the **AggregateOn** element to specify the representative property.</span></span> 
  
<span data-ttu-id="c828f-145">确定代表属性后，**聚合**属性用于指示是否根据最大值或标识属性的最小值排序组。</span><span class="sxs-lookup"><span data-stu-id="c828f-145">When a representative property is identified, the **Aggregate** attribute is used to indicate whether the groups are sorted according to the maximum or the minimum value of the identified property.</span></span> <span data-ttu-id="c828f-146">**聚合**属性设置为最大值，如果组的排序开头**AggregateOn**属性的最大值。</span><span class="sxs-lookup"><span data-stu-id="c828f-146">If the **Aggregate** attribute is set to Maximum, the groups are sorted beginning with the largest value for the **AggregateOn** property.</span></span> <span data-ttu-id="c828f-147">**聚合**属性设置为最小值，如果组的排序开头**AggregateOn**属性的最小值。</span><span class="sxs-lookup"><span data-stu-id="c828f-147">If the **Aggregate** attribute is set to Minimum, the groups are sorted beginning with the smallest value for the **AggregateOn** property.</span></span> 
  
<span data-ttu-id="c828f-148">例如，如果要颁发 FindItem 分组的查询，分组发件人，但不是想对组进行排序，以便具有最新的电子邮件的组位于顶部，您可以组合的发件人和 aggregate 上接收的带有**聚合**的日期/时间最大值的属性。</span><span class="sxs-lookup"><span data-stu-id="c828f-148">For example, if you want to issue a FindItem grouped query, grouping by sender, but you want to order the groups so that the group with the most recent e-mail message is on top, you can group by sender and aggregate on date/time received with an **Aggregate** attribute of Maximum.</span></span> 
  
<span data-ttu-id="c828f-149">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c828f-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="c828f-150">示例</span><span class="sxs-lookup"><span data-stu-id="c828f-150">Example</span></span>

<span data-ttu-id="c828f-151">下面的示例演示组合 FindItem 请求和响应。</span><span class="sxs-lookup"><span data-stu-id="c828f-151">The following example shows a grouped FindItem request and response.</span></span> <span data-ttu-id="c828f-152">该示例演示请求返回项目分组依据**ConversationTopic**属性。</span><span class="sxs-lookup"><span data-stu-id="c828f-152">The example shows a request to return items grouped by the **ConversationTopic** property.</span></span> <span data-ttu-id="c828f-153">两个组，A 和 B，按降序顺序基于[DateTimeReceived](datetimereceived.md)属性的最大值返回。</span><span class="sxs-lookup"><span data-stu-id="c828f-153">Two groups, A and B, are returned in descending order based on the maximum value of the [DateTimeReceived](datetimereceived.md) property.</span></span> 
  
```XML
<!-- EXAMPLE REQUEST -->
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="c828f-154">若要对组中的项目进行排序，使用[SortOrder](sortorder.md)元素。</span><span class="sxs-lookup"><span data-stu-id="c828f-154">To sort the items in a group, use the [SortOrder](sortorder.md) element.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c828f-155">已缩短的项标识符和更改键，以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="c828f-155">The item identifiers and change keys have been shortened to preserve readability.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c828f-156">元素信息</span><span class="sxs-lookup"><span data-stu-id="c828f-156">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c828f-157">命名空间</span><span class="sxs-lookup"><span data-stu-id="c828f-157">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c828f-158">架构名称</span><span class="sxs-lookup"><span data-stu-id="c828f-158">Schema Name</span></span>  <br/> |<span data-ttu-id="c828f-159">类型架构</span><span class="sxs-lookup"><span data-stu-id="c828f-159">Types schema</span></span>  <br/> |
|<span data-ttu-id="c828f-160">验证文件</span><span class="sxs-lookup"><span data-stu-id="c828f-160">Validation File</span></span>  <br/> |<span data-ttu-id="c828f-161">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c828f-161">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c828f-162">可以为空</span><span class="sxs-lookup"><span data-stu-id="c828f-162">Can be Empty</span></span>  <br/> |<span data-ttu-id="c828f-163">False</span><span class="sxs-lookup"><span data-stu-id="c828f-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c828f-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c828f-164">See also</span></span>

- [<span data-ttu-id="c828f-165">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="c828f-165">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="c828f-166">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c828f-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="c828f-167">查找项目</span><span class="sxs-lookup"><span data-stu-id="c828f-167">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

