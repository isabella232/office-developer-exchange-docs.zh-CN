---
title: AdditionalProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AdditionalProperties
api_type:
- schema
ms.assetid: 7a269aed-dcfd-4c3e-9e14-094e53828101
description: AdditionalProperties 元素标识用于 GetItem UpdateItem、 CreateItem、 FindItem，其他属性或 FindFolder 请求。
ms.openlocfilehash: 64e4f1ee6b24cf8015b7893dc4a904ca8b32d58e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753114"
---
# <a name="additionalproperties"></a><span data-ttu-id="a0e40-103">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="a0e40-103">AdditionalProperties</span></span>

<span data-ttu-id="a0e40-104">**AdditionalProperties**元素标识用于[GetItem](getitem.md) [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)，其他属性或[FindFolder](findfolder.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a0e40-104">The **AdditionalProperties** element identifies additional properties for use in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 <span data-ttu-id="a0e40-105">**NonEmptyArrayOfPathsToElementType**</span><span class="sxs-lookup"><span data-stu-id="a0e40-105">**NonEmptyArrayOfPathsToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0e40-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a0e40-106">Attributes and elements</span></span>

<span data-ttu-id="a0e40-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a0e40-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0e40-108">属性</span><span class="sxs-lookup"><span data-stu-id="a0e40-108">Attributes</span></span>

<span data-ttu-id="a0e40-109">无。</span><span class="sxs-lookup"><span data-stu-id="a0e40-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a0e40-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a0e40-110">Child elements</span></span>

|<span data-ttu-id="a0e40-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a0e40-111">**Element**</span></span>|<span data-ttu-id="a0e40-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a0e40-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0e40-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a0e40-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="a0e40-114">标识扩展的 MAPI 属性以获取、 设置或创建。</span><span class="sxs-lookup"><span data-stu-id="a0e40-114">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="a0e40-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="a0e40-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="a0e40-116">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="a0e40-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="a0e40-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a0e40-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="a0e40-118">标识经常引用的词典属性的 URI。</span><span class="sxs-lookup"><span data-stu-id="a0e40-118">Identifies frequently referenced dictionary properties by URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a0e40-119">父元素</span><span class="sxs-lookup"><span data-stu-id="a0e40-119">Parent elements</span></span>

|<span data-ttu-id="a0e40-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="a0e40-120">**Element**</span></span>|<span data-ttu-id="a0e40-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="a0e40-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0e40-122">FolderShape</span><span class="sxs-lookup"><span data-stu-id="a0e40-122">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="a0e40-123">标识要在[GetFolder](getfolder.md)、 [FindFolder](findfolder.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)响应中包含的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="a0e40-123">Identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span><br/><br/>  <span data-ttu-id="a0e40-124">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a0e40-124">The following are the XPath expressions to this element:</span></span><br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="a0e40-125">ItemShape</span><span class="sxs-lookup"><span data-stu-id="a0e40-125">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="a0e40-126">标识项目属性和[GetItem](getitem.md)、 [FindItem](finditem.md)或[SyncFolderItems](syncfolderitems.md)响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="a0e40-126">Identifies the item properties and content to include in a [GetItem](getitem.md), [FindItem](finditem.md), or [SyncFolderItems](syncfolderitems.md) response.</span></span><br/><br/>  <span data-ttu-id="a0e40-127">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a0e40-127">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="a0e40-128">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="a0e40-128">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="a0e40-129">标识要[GetItem](getitem.md)请求的响应中返回的其他扩展的项属性。</span><span class="sxs-lookup"><span data-stu-id="a0e40-129">Identifies additional extended item properties to return in a response to a [GetItem](getitem.md) request.</span></span><br/><br/> <span data-ttu-id="a0e40-130">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a0e40-130">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0e40-131">注解</span><span class="sxs-lookup"><span data-stu-id="a0e40-131">Remarks</span></span>

<span data-ttu-id="a0e40-132">并非所有的子元素可用于[GetItem](getitem.md)、 [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)或[FindFolder](findfolder.md)请求。</span><span class="sxs-lookup"><span data-stu-id="a0e40-132">Not all the child elements can be used with [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> <span data-ttu-id="a0e40-133">该属性必须是适用于文件夹或项目的访问。</span><span class="sxs-lookup"><span data-stu-id="a0e40-133">The property must be applicable to the folder or item that is accessed.</span></span> <span data-ttu-id="a0e40-134">使用扩展的属性访问其他属性。</span><span class="sxs-lookup"><span data-stu-id="a0e40-134">Use extended properties to access other properties.</span></span> <span data-ttu-id="a0e40-135">如果属性不存在的给定项目，将到所产生的 XML 激发没有相应的元素。</span><span class="sxs-lookup"><span data-stu-id="a0e40-135">If the property does not exist for a given item, no corresponding element will be emitted into the resulting XML.</span></span> 
  
<span data-ttu-id="a0e40-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a0e40-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="a0e40-137">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="a0e40-137">This element is optional.</span></span>
  
## <a name="example"></a><span data-ttu-id="a0e40-138">示例</span><span class="sxs-lookup"><span data-stu-id="a0e40-138">Example</span></span>

<span data-ttu-id="a0e40-139">下面的请求示例演示如何通过使用**AdditionalProperties**元素中获取项目主题。</span><span class="sxs-lookup"><span data-stu-id="a0e40-139">The following request example shows how to get an item subject by using the **AdditionalProperties** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject"/>
        </t:AdditionalProperties>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="ASkAS="/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="a0e40-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="a0e40-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0e40-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="a0e40-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a0e40-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="a0e40-142">Schema Name</span></span>  <br/> |<span data-ttu-id="a0e40-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="a0e40-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="a0e40-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="a0e40-144">Validation File</span></span>  <br/> |<span data-ttu-id="a0e40-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a0e40-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a0e40-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="a0e40-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="a0e40-147">False</span><span class="sxs-lookup"><span data-stu-id="a0e40-147">False</span></span>  <br/> |
   

