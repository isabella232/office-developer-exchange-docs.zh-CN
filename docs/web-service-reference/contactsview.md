---
title: ContactsView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsView
api_type:
- schema
ms.assetid: 8534f44b-a5af-4a9f-9621-23a3eff5f9d8
description: ContactsView 元素根据字母显示名称定义对联系人项目的搜索。
ms.openlocfilehash: 23c3fe13c44cdd0e5a054ecb3378bc3d633e55aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463816"
---
# <a name="contactsview"></a><span data-ttu-id="a0b94-103">ContactsView</span><span class="sxs-lookup"><span data-stu-id="a0b94-103">ContactsView</span></span>

<span data-ttu-id="a0b94-104">**ContactsView**元素根据字母显示名称定义对联系人项目的搜索。</span><span class="sxs-lookup"><span data-stu-id="a0b94-104">The **ContactsView** element defines a search for contact items based on alphabetical display names.</span></span> 
  
[<span data-ttu-id="a0b94-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="a0b94-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="a0b94-106">ContactsView</span><span class="sxs-lookup"><span data-stu-id="a0b94-106">ContactsView</span></span>](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

<span data-ttu-id="a0b94-107">**ContactsViewType**</span><span class="sxs-lookup"><span data-stu-id="a0b94-107">**ContactsViewType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a0b94-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a0b94-108">Attributes and elements</span></span>

<span data-ttu-id="a0b94-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a0b94-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0b94-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="a0b94-110">Attributes</span></span>

|<span data-ttu-id="a0b94-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="a0b94-111">**Attribute**</span></span>|<span data-ttu-id="a0b94-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a0b94-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0b94-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="a0b94-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="a0b94-114">描述在[FindItem](finditem.md)响应中返回的最大结果数。</span><span class="sxs-lookup"><span data-stu-id="a0b94-114">Describes the maximum number of results to return in the [FindItem](finditem.md) response.</span></span>  <br/> |
|<span data-ttu-id="a0b94-115">**InitialName**</span><span class="sxs-lookup"><span data-stu-id="a0b94-115">**InitialName**</span></span> <br/> |<span data-ttu-id="a0b94-116">定义要在响应中返回的 "联系人" 列表中的第一个名称。</span><span class="sxs-lookup"><span data-stu-id="a0b94-116">Defines the first name in the contacts list to return in the response.</span></span> <span data-ttu-id="a0b94-117">如果指定的初始名称不在 "联系人" 列表中，则将返回由区域性上下文定义的下一个字母名称，但在**FinalName**后面的下一个名称除外。</span><span class="sxs-lookup"><span data-stu-id="a0b94-117">If the specified initial name is not in the contacts list, the next alphabetical name as defined by the cultural context will be returned, except if the next name comes after **FinalName**.</span></span> <span data-ttu-id="a0b94-118">如果省略了**InitialName**属性，则响应将包含以联系人列表中的第一个名称开头的联系人列表。</span><span class="sxs-lookup"><span data-stu-id="a0b94-118">If the **InitialName** attribute is omitted, the response will contain a list of contacts that starts with the first name in the contact list.</span></span> <span data-ttu-id="a0b94-119">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="a0b94-119">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="a0b94-120">**FinalName**</span><span class="sxs-lookup"><span data-stu-id="a0b94-120">**FinalName**</span></span> <br/> |<span data-ttu-id="a0b94-121">定义要在响应中返回的 "联系人" 列表中的最后一个名称。</span><span class="sxs-lookup"><span data-stu-id="a0b94-121">Defines the last name in the contacts list to return in the response.</span></span> <span data-ttu-id="a0b94-122">如果省略了**FinalName**属性，则响应将包含指定的排序顺序中的所有后续联系人。</span><span class="sxs-lookup"><span data-stu-id="a0b94-122">If the **FinalName** attribute is omitted, the response will contain all subsequent contacts in the specified sort order.</span></span> <span data-ttu-id="a0b94-123">如果指定的最终名称不在联系人列表中，则将排除由区域性上下文定义的下一个按字母顺序排列的名称。</span><span class="sxs-lookup"><span data-stu-id="a0b94-123">If the specified final name is not in the contacts list, the next alphabetical name as defined by the cultural context will be excluded.</span></span>  <br/><br/><span data-ttu-id="a0b94-124">例如，如果 FinalName = "Name"，但名称不在 "联系人" 列表中，则将不包含显示名称为 "Name1" 或 "名称" 的联系人。</span><span class="sxs-lookup"><span data-stu-id="a0b94-124">For example, if FinalName="Name", but Name is not in the contacts list, contacts that have display names of Name1 or NAME will not be included.</span></span>  <br/><br/><span data-ttu-id="a0b94-125">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="a0b94-125">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a0b94-126">子元素</span><span class="sxs-lookup"><span data-stu-id="a0b94-126">Child elements</span></span>

<span data-ttu-id="a0b94-127">无。</span><span class="sxs-lookup"><span data-stu-id="a0b94-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0b94-128">父元素</span><span class="sxs-lookup"><span data-stu-id="a0b94-128">Parent elements</span></span>

|<span data-ttu-id="a0b94-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="a0b94-129">**Element**</span></span>|<span data-ttu-id="a0b94-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="a0b94-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0b94-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="a0b94-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="a0b94-132">定义在邮箱中查找项目的请求。</span><span class="sxs-lookup"><span data-stu-id="a0b94-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="a0b94-133">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="a0b94-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0b94-134">说明</span><span class="sxs-lookup"><span data-stu-id="a0b94-134">Remarks</span></span>

<span data-ttu-id="a0b94-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a0b94-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="a0b94-136">示例</span><span class="sxs-lookup"><span data-stu-id="a0b94-136">Example</span></span>

<span data-ttu-id="a0b94-137">下面的请求示例演示如何查找从具有 "王凯利" 显示名称的联系人开始的前三个联系人。</span><span class="sxs-lookup"><span data-stu-id="a0b94-137">The following example of a request demonstrates how to find the first three contacts starting with the contact that has the display name of Kelly Rollin.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ContactsView MaxEntriesReturned="3" InitialName="Kelly Rollin" />
      <SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="contacts:DisplayName"/>
        </t:FieldOrder>
        </SortOrder>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="contacts"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="a0b94-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="a0b94-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0b94-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="a0b94-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a0b94-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="a0b94-140">Schema Name</span></span>  <br/> |<span data-ttu-id="a0b94-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="a0b94-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a0b94-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="a0b94-142">Validation File</span></span>  <br/> |<span data-ttu-id="a0b94-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a0b94-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a0b94-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="a0b94-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="a0b94-145">False</span><span class="sxs-lookup"><span data-stu-id="a0b94-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0b94-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a0b94-146">See also</span></span>

- [<span data-ttu-id="a0b94-147">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="a0b94-147">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="a0b94-148">查找项目</span><span class="sxs-lookup"><span data-stu-id="a0b94-148">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

