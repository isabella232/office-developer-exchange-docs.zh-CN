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
description: ContactsView 元素定义基于按字母顺序排列的显示名称的联系人项搜索。
ms.openlocfilehash: e578eb4dd0042b8c478e883c7fa54d7f2e984229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753520"
---
# <a name="contactsview"></a><span data-ttu-id="81b71-103">ContactsView</span><span class="sxs-lookup"><span data-stu-id="81b71-103">ContactsView</span></span>

<span data-ttu-id="81b71-104">**ContactsView**元素定义基于按字母顺序排列的显示名称的联系人项搜索。</span><span class="sxs-lookup"><span data-stu-id="81b71-104">The **ContactsView** element defines a search for contact items based on alphabetical display names.</span></span> 
  
[<span data-ttu-id="81b71-105">FindItem</span><span class="sxs-lookup"><span data-stu-id="81b71-105">FindItem</span></span>](finditem.md)
  
[<span data-ttu-id="81b71-106">ContactsView</span><span class="sxs-lookup"><span data-stu-id="81b71-106">ContactsView</span></span>](contactsview.md)
  
```xml
<ContactsView MaxEntriesReturned="" InitialName="" FinalName="" />
```

<span data-ttu-id="81b71-107">**ContactsViewType**</span><span class="sxs-lookup"><span data-stu-id="81b71-107">**ContactsViewType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="81b71-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="81b71-108">Attributes and elements</span></span>

<span data-ttu-id="81b71-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="81b71-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="81b71-110">属性</span><span class="sxs-lookup"><span data-stu-id="81b71-110">Attributes</span></span>

|<span data-ttu-id="81b71-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="81b71-111">**Attribute**</span></span>|<span data-ttu-id="81b71-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="81b71-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="81b71-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="81b71-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="81b71-114">最大个数要[FindItem](finditem.md)响应中返回的结果。</span><span class="sxs-lookup"><span data-stu-id="81b71-114">Describes the maximum number of results to return in the [FindItem](finditem.md) response.</span></span>  <br/> |
|<span data-ttu-id="81b71-115">**InitialName**</span><span class="sxs-lookup"><span data-stu-id="81b71-115">**InitialName**</span></span> <br/> |<span data-ttu-id="81b71-116">在联系人列表中要返回的响应中定义第一个名称。</span><span class="sxs-lookup"><span data-stu-id="81b71-116">Defines the first name in the contacts list to return in the response.</span></span> <span data-ttu-id="81b71-117">如果指定的初始名称定义的文化上下文不在联系人列表中，按字母顺序排列的下一个名称将返回，除**FinalName**如果出现的下一个名称。</span><span class="sxs-lookup"><span data-stu-id="81b71-117">If the specified initial name is not in the contacts list, the next alphabetical name as defined by the cultural context will be returned, except if the next name comes after **FinalName**.</span></span> <span data-ttu-id="81b71-118">如果省略**InitialName**属性，则响应将包含联系人列表中的第一个名称开头的联系人的列表。</span><span class="sxs-lookup"><span data-stu-id="81b71-118">If the **InitialName** attribute is omitted, the response will contain a list of contacts that starts with the first name in the contact list.</span></span> <span data-ttu-id="81b71-119">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="81b71-119">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="81b71-120">**FinalName**</span><span class="sxs-lookup"><span data-stu-id="81b71-120">**FinalName**</span></span> <br/> |<span data-ttu-id="81b71-121">在联系人列表中要返回的响应中定义的最后一个名称。</span><span class="sxs-lookup"><span data-stu-id="81b71-121">Defines the last name in the contacts list to return in the response.</span></span> <span data-ttu-id="81b71-122">如果省略**FinalName**属性，则响应中将包含指定的排序顺序中的所有后续联系人。</span><span class="sxs-lookup"><span data-stu-id="81b71-122">If the **FinalName** attribute is omitted, the response will contain all subsequent contacts in the specified sort order.</span></span> <span data-ttu-id="81b71-123">如果指定的最终名称不在联系人列表中，按字母顺序排列的下一个名称由文化上下文定义将排除。</span><span class="sxs-lookup"><span data-stu-id="81b71-123">If the specified final name is not in the contacts list, the next alphabetical name as defined by the cultural context will be excluded.</span></span>  <br/><br/><span data-ttu-id="81b71-124">例如，如果 FinalName ="Name"，但名称不在联系人列表、 具有的联系人显示 Name1 的名称或名称将不包括在内。</span><span class="sxs-lookup"><span data-stu-id="81b71-124">For example, if FinalName="Name", but Name is not in the contacts list, contacts that have display names of Name1 or NAME will not be included.</span></span>  <br/><br/><span data-ttu-id="81b71-125">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="81b71-125">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="81b71-126">子元素</span><span class="sxs-lookup"><span data-stu-id="81b71-126">Child elements</span></span>

<span data-ttu-id="81b71-127">无。</span><span class="sxs-lookup"><span data-stu-id="81b71-127">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="81b71-128">父元素</span><span class="sxs-lookup"><span data-stu-id="81b71-128">Parent elements</span></span>

|<span data-ttu-id="81b71-129">**元素**</span><span class="sxs-lookup"><span data-stu-id="81b71-129">**Element**</span></span>|<span data-ttu-id="81b71-130">**说明**</span><span class="sxs-lookup"><span data-stu-id="81b71-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="81b71-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="81b71-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="81b71-132">定义查找邮箱中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="81b71-132">Defines a request to find items in a mailbox.</span></span><br/><br/> <span data-ttu-id="81b71-133">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="81b71-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81b71-134">备注</span><span class="sxs-lookup"><span data-stu-id="81b71-134">Remarks</span></span>

<span data-ttu-id="81b71-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="81b71-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="81b71-136">示例</span><span class="sxs-lookup"><span data-stu-id="81b71-136">Example</span></span>

<span data-ttu-id="81b71-137">请求的下面的示例演示如何查找与前三个联系人启动与联系人已凯利的显示名称。</span><span class="sxs-lookup"><span data-stu-id="81b71-137">The following example of a request demonstrates how to find the first three contacts starting with the contact that has the display name of Kelly Rollin.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="81b71-138">元素信息</span><span class="sxs-lookup"><span data-stu-id="81b71-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81b71-139">命名空间</span><span class="sxs-lookup"><span data-stu-id="81b71-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="81b71-140">架构名称</span><span class="sxs-lookup"><span data-stu-id="81b71-140">Schema Name</span></span>  <br/> |<span data-ttu-id="81b71-141">消息架构</span><span class="sxs-lookup"><span data-stu-id="81b71-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="81b71-142">验证文件</span><span class="sxs-lookup"><span data-stu-id="81b71-142">Validation File</span></span>  <br/> |<span data-ttu-id="81b71-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="81b71-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="81b71-144">可以为空</span><span class="sxs-lookup"><span data-stu-id="81b71-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="81b71-145">False</span><span class="sxs-lookup"><span data-stu-id="81b71-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="81b71-146">另请参阅</span><span class="sxs-lookup"><span data-stu-id="81b71-146">See also</span></span>

- [<span data-ttu-id="81b71-147">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="81b71-147">FindItem operation</span></span>](finditem-operation.md)
- [<span data-ttu-id="81b71-148">查找项目</span><span class="sxs-lookup"><span data-stu-id="81b71-148">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

