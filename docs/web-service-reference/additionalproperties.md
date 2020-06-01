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
description: AdditionalProperties 元素标识在 GetItem、UpdateItem、CreateItem、FindItem 或 FindFolder 请求中使用的其他属性。
ms.openlocfilehash: 90a307ba4d5ece10e15d2cec56cf5042c3d38685
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455812"
---
# <a name="additionalproperties"></a><span data-ttu-id="45751-103">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="45751-103">AdditionalProperties</span></span>

<span data-ttu-id="45751-104">**AdditionalProperties**元素标识在[GetItem](getitem.md)、 [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)或[FindFolder](findfolder.md)请求中使用的其他属性。</span><span class="sxs-lookup"><span data-stu-id="45751-104">The **AdditionalProperties** element identifies additional properties for use in [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> 
  
```xml
<AdditionalProperties>
   <ExtendedFieldURI/>
   <FieldURI/>
   <IndexedFieldURI/>
</AdditionalProperties>
```

 <span data-ttu-id="45751-105">**NonEmptyArrayOfPathsToElementType**</span><span class="sxs-lookup"><span data-stu-id="45751-105">**NonEmptyArrayOfPathsToElementType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45751-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="45751-106">Attributes and elements</span></span>

<span data-ttu-id="45751-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="45751-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45751-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="45751-108">Attributes</span></span>

<span data-ttu-id="45751-109">无。</span><span class="sxs-lookup"><span data-stu-id="45751-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45751-110">子元素</span><span class="sxs-lookup"><span data-stu-id="45751-110">Child elements</span></span>

|<span data-ttu-id="45751-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="45751-111">**Element**</span></span>|<span data-ttu-id="45751-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="45751-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45751-113">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="45751-113">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="45751-114">标识要获取、设置或创建的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="45751-114">Identifies extended MAPI properties to get, set, or create.</span></span>  <br/> |
|[<span data-ttu-id="45751-115">FieldURI</span><span class="sxs-lookup"><span data-stu-id="45751-115">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="45751-116">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="45751-116">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="45751-117">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="45751-117">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="45751-118">按 URI 标识经常引用的字典属性。</span><span class="sxs-lookup"><span data-stu-id="45751-118">Identifies frequently referenced dictionary properties by URI.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45751-119">父元素</span><span class="sxs-lookup"><span data-stu-id="45751-119">Parent elements</span></span>

|<span data-ttu-id="45751-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="45751-120">**Element**</span></span>|<span data-ttu-id="45751-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="45751-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45751-122">FolderShape</span><span class="sxs-lookup"><span data-stu-id="45751-122">FolderShape</span></span>](foldershape.md) <br/> | <span data-ttu-id="45751-123">标识要包括在[GetFolder](getfolder.md)、 [FindFolder](findfolder.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)响应中的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="45751-123">Identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span><br/><br/>  <span data-ttu-id="45751-124">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="45751-124">The following are the XPath expressions to this element:</span></span><br/><br/>  `/FindFolder/FolderShape` <br/>  `/GetFolder/FolderShape` <br/>  `/SyncFolderHierarchy/FolderShape` <br/> |
|[<span data-ttu-id="45751-125">ItemShape</span><span class="sxs-lookup"><span data-stu-id="45751-125">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="45751-126">标识要包括在[GetItem](getitem.md)、 [FindItem](finditem.md)或[SyncFolderItems](syncfolderitems.md)响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="45751-126">Identifies the item properties and content to include in a [GetItem](getitem.md), [FindItem](finditem.md), or [SyncFolderItems](syncfolderitems.md) response.</span></span><br/><br/>  <span data-ttu-id="45751-127">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="45751-127">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape` <br/>  `/FindItem/ItemShape` <br/>  `/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="45751-128">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="45751-128">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="45751-129">标识要在对[GetItem](getitem.md)请求的响应中返回的其他扩展项属性。</span><span class="sxs-lookup"><span data-stu-id="45751-129">Identifies additional extended item properties to return in a response to a [GetItem](getitem.md) request.</span></span><br/><br/> <span data-ttu-id="45751-130">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="45751-130">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45751-131">备注</span><span class="sxs-lookup"><span data-stu-id="45751-131">Remarks</span></span>

<span data-ttu-id="45751-132">并非所有子元素都可与[GetItem](getitem.md)、 [UpdateItem](updateitem.md)、 [CreateItem](createitem.md)、 [FindItem](finditem.md)或[FindFolder](findfolder.md)请求一起使用。</span><span class="sxs-lookup"><span data-stu-id="45751-132">Not all the child elements can be used with [GetItem](getitem.md), [UpdateItem](updateitem.md), [CreateItem](createitem.md), [FindItem](finditem.md), or [FindFolder](findfolder.md) requests.</span></span> <span data-ttu-id="45751-133">该属性必须适用于访问的文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="45751-133">The property must be applicable to the folder or item that is accessed.</span></span> <span data-ttu-id="45751-134">使用扩展属性访问其他属性。</span><span class="sxs-lookup"><span data-stu-id="45751-134">Use extended properties to access other properties.</span></span> <span data-ttu-id="45751-135">如果给定项的属性不存在，则将不会在生成的 XML 中发出相应的元素。</span><span class="sxs-lookup"><span data-stu-id="45751-135">If the property does not exist for a given item, no corresponding element will be emitted into the resulting XML.</span></span> 
  
<span data-ttu-id="45751-136">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="45751-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
<span data-ttu-id="45751-137">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="45751-137">This element is optional.</span></span>
  
## <a name="example"></a><span data-ttu-id="45751-138">示例</span><span class="sxs-lookup"><span data-stu-id="45751-138">Example</span></span>

<span data-ttu-id="45751-139">以下请求示例演示如何使用**AdditionalProperties**元素获取项目主题。</span><span class="sxs-lookup"><span data-stu-id="45751-139">The following request example shows how to get an item subject by using the **AdditionalProperties** element.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="45751-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="45751-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45751-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="45751-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45751-142">架构名称</span><span class="sxs-lookup"><span data-stu-id="45751-142">Schema Name</span></span>  <br/> |<span data-ttu-id="45751-143">类型架构</span><span class="sxs-lookup"><span data-stu-id="45751-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="45751-144">验证文件</span><span class="sxs-lookup"><span data-stu-id="45751-144">Validation File</span></span>  <br/> |<span data-ttu-id="45751-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="45751-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="45751-146">可以为空</span><span class="sxs-lookup"><span data-stu-id="45751-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="45751-147">False</span><span class="sxs-lookup"><span data-stu-id="45751-147">False</span></span>  <br/> |
   

