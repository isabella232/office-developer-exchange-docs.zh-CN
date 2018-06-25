---
title: ItemShape
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemShape
api_type:
- schema
ms.assetid: c5604161-bbc0-40bc-ad75-ff7e837d745f
description: ItemShape 元素标识一要 GetItem 操作、 FindItem 操作或 SyncFolderItems 操作响应中返回的属性。
ms.openlocfilehash: 95174a85a8fa05cb2612e1289d46c8db32b6e052
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826191"
---
# <a name="itemshape"></a><span data-ttu-id="96a2f-103">ItemShape</span><span class="sxs-lookup"><span data-stu-id="96a2f-103">ItemShape</span></span>

<span data-ttu-id="96a2f-104">**ItemShape**元素标识一要[GetItem 操作](getitem-operation.md)、 [FindItem 操作](finditem-operation.md)或[SyncFolderItems 操作](syncfolderitems-operation.md)的响应中返回的属性。</span><span class="sxs-lookup"><span data-stu-id="96a2f-104">The **ItemShape** element identifies a set of properties to return in a [GetItem operation](getitem-operation.md), [FindItem operation](finditem-operation.md), or [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> 
  
```XML
<ItemShape>
   <BaseShape/>
   <IncludeMimeContent/>
   <BodyType/>
   <FilterHtmlContent/>
   <ConvertHtmlCodePageToUTF8/>
   <AdditionalProperties/>
</ItemShape>
```

 <span data-ttu-id="96a2f-105">**ItemResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="96a2f-105">**ItemResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="96a2f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="96a2f-106">Attributes and elements</span></span>

<span data-ttu-id="96a2f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="96a2f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96a2f-108">属性</span><span class="sxs-lookup"><span data-stu-id="96a2f-108">Attributes</span></span>

<span data-ttu-id="96a2f-109">无。</span><span class="sxs-lookup"><span data-stu-id="96a2f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="96a2f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="96a2f-110">Child elements</span></span>

|<span data-ttu-id="96a2f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="96a2f-111">**Element**</span></span>|<span data-ttu-id="96a2f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="96a2f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96a2f-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="96a2f-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="96a2f-114">标识要项目或文件夹响应中返回的属性的基本配置。</span><span class="sxs-lookup"><span data-stu-id="96a2f-114">Identifies the basic configuration of properties to return in an item or folder response.</span></span>  <br/> |
|[<span data-ttu-id="96a2f-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="96a2f-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="96a2f-116">指定是否在响应中返回的项的多用途 Internet 邮件扩展 (MIME) 内容。</span><span class="sxs-lookup"><span data-stu-id="96a2f-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item is returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="96a2f-117">BodyType</span><span class="sxs-lookup"><span data-stu-id="96a2f-117">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="96a2f-118">介绍如何在响应中设置的正文文本的格式。</span><span class="sxs-lookup"><span data-stu-id="96a2f-118">Identifies how the body text is formatted in the response.</span></span>  <br/> |
|[<span data-ttu-id="96a2f-119">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="96a2f-119">ConvertHtmlCodePageToUTF8</span></span>](converthtmlcodepagetoutf8.md) <br/> |<span data-ttu-id="96a2f-120">指示是否将项目 HTML 正文转换为 UTF8。</span><span class="sxs-lookup"><span data-stu-id="96a2f-120">Indicates whether the item HTML body is converted to UTF8.</span></span>  <br/> |
|[<span data-ttu-id="96a2f-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="96a2f-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="96a2f-122">指定是否启用 HTML 内容筛选。</span><span class="sxs-lookup"><span data-stu-id="96a2f-122">Specifies whether HTML content filtering is enabled.</span></span>  <br/> |
|[<span data-ttu-id="96a2f-123">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="96a2f-123">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="96a2f-124">标识要返回的响应中的其他属性。</span><span class="sxs-lookup"><span data-stu-id="96a2f-124">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="96a2f-125">父元素</span><span class="sxs-lookup"><span data-stu-id="96a2f-125">Parent elements</span></span>

|<span data-ttu-id="96a2f-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="96a2f-126">**Element**</span></span>|<span data-ttu-id="96a2f-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="96a2f-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="96a2f-128">GetItem</span><span class="sxs-lookup"><span data-stu-id="96a2f-128">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="96a2f-129">定义请求从 Exchange 存储中的邮箱检索项目。</span><span class="sxs-lookup"><span data-stu-id="96a2f-129">Defines a request to retrieve items from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="96a2f-130">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="96a2f-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="96a2f-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="96a2f-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="96a2f-132">定义查找文件夹中包含的所有项的请求。</span><span class="sxs-lookup"><span data-stu-id="96a2f-132">Defines a request to find all items that are contained in a folder.</span></span>  <br/> <span data-ttu-id="96a2f-133">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="96a2f-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="96a2f-134">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="96a2f-134">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="96a2f-135">定义同步 Exchange 存储区文件夹中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="96a2f-135">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="96a2f-136">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="96a2f-136">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="96a2f-137">文本值</span><span class="sxs-lookup"><span data-stu-id="96a2f-137">Text value</span></span>

<span data-ttu-id="96a2f-138">无。</span><span class="sxs-lookup"><span data-stu-id="96a2f-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96a2f-139">备注</span><span class="sxs-lookup"><span data-stu-id="96a2f-139">Remarks</span></span>

<span data-ttu-id="96a2f-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="96a2f-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96a2f-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="96a2f-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96a2f-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="96a2f-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="96a2f-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="96a2f-143">Schema Name</span></span>  <br/> |<span data-ttu-id="96a2f-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="96a2f-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="96a2f-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="96a2f-145">Validation File</span></span>  <br/> |<span data-ttu-id="96a2f-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="96a2f-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="96a2f-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="96a2f-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="96a2f-148">False</span><span class="sxs-lookup"><span data-stu-id="96a2f-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="96a2f-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="96a2f-149">See also</span></span>



[<span data-ttu-id="96a2f-150">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="96a2f-150">GetItem operation</span></span>](getitem-operation.md)
  
[<span data-ttu-id="96a2f-151">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="96a2f-151">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="96a2f-152">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="96a2f-152">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="96a2f-153">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="96a2f-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

