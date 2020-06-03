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
description: ItemShape 元素标识要在 GetItem 操作、FindItem 操作或 SyncFolderItems 操作响应中返回的一组属性。
ms.openlocfilehash: ffb666ee331b55a4f04cad076c705e4bec980e03
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458122"
---
# <a name="itemshape"></a><span data-ttu-id="e4e2a-103">ItemShape</span><span class="sxs-lookup"><span data-stu-id="e4e2a-103">ItemShape</span></span>

<span data-ttu-id="e4e2a-104">**ItemShape**元素标识要在[GetItem 操作](getitem-operation.md)、 [FindItem 操作](finditem-operation.md)或[SyncFolderItems 操作](syncfolderitems-operation.md)响应中返回的一组属性。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-104">The **ItemShape** element identifies a set of properties to return in a [GetItem operation](getitem-operation.md), [FindItem operation](finditem-operation.md), or [SyncFolderItems operation](syncfolderitems-operation.md) response.</span></span> 
  
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

 <span data-ttu-id="e4e2a-105">**ItemResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-105">**ItemResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e4e2a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e4e2a-106">Attributes and elements</span></span>

<span data-ttu-id="e4e2a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e4e2a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e4e2a-108">Attributes</span></span>

<span data-ttu-id="e4e2a-109">无。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e4e2a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e4e2a-110">Child elements</span></span>

|<span data-ttu-id="e4e2a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-111">**Element**</span></span>|<span data-ttu-id="e4e2a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4e2a-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="e4e2a-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="e4e2a-114">标识要在项目或文件夹响应中返回的属性的基本配置。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-114">Identifies the basic configuration of properties to return in an item or folder response.</span></span>  <br/> |
|[<span data-ttu-id="e4e2a-115">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="e4e2a-115">IncludeMimeContent</span></span>](includemimecontent.md) <br/> |<span data-ttu-id="e4e2a-116">指定是否在响应中返回项目的多用途 Internet 邮件扩展（MIME）内容。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-116">Specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item is returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="e4e2a-117">BodyType</span><span class="sxs-lookup"><span data-stu-id="e4e2a-117">BodyType</span></span>](bodytype.md) <br/> |<span data-ttu-id="e4e2a-118">标识正文文本在响应中的格式。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-118">Identifies how the body text is formatted in the response.</span></span>  <br/> |
|[<span data-ttu-id="e4e2a-119">ConvertHtmlCodePageToUTF8</span><span class="sxs-lookup"><span data-stu-id="e4e2a-119">ConvertHtmlCodePageToUTF8</span></span>](converthtmlcodepagetoutf8.md) <br/> |<span data-ttu-id="e4e2a-120">指示是否将项目 HTML 正文转换为 UTF8。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-120">Indicates whether the item HTML body is converted to UTF8.</span></span>  <br/> |
|[<span data-ttu-id="e4e2a-121">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="e4e2a-121">FilterHtmlContent</span></span>](filterhtmlcontent.md) <br/> |<span data-ttu-id="e4e2a-122">指定是否启用 HTML 内容筛选。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-122">Specifies whether HTML content filtering is enabled.</span></span>  <br/> |
|[<span data-ttu-id="e4e2a-123">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="e4e2a-123">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="e4e2a-124">标识要在响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-124">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e4e2a-125">父元素</span><span class="sxs-lookup"><span data-stu-id="e4e2a-125">Parent elements</span></span>

|<span data-ttu-id="e4e2a-126">**元素**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-126">**Element**</span></span>|<span data-ttu-id="e4e2a-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="e4e2a-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e4e2a-128">GetItem</span><span class="sxs-lookup"><span data-stu-id="e4e2a-128">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="e4e2a-129">定义从 Exchange 存储中的邮箱检索项目的请求。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-129">Defines a request to retrieve items from a mailbox in the Exchange store.</span></span>  <br/> <span data-ttu-id="e4e2a-130">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="e4e2a-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="e4e2a-131">FindItem</span><span class="sxs-lookup"><span data-stu-id="e4e2a-131">FindItem</span></span>](finditem.md) <br/> |<span data-ttu-id="e4e2a-132">定义一个请求，以查找文件夹中包含的所有项目。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-132">Defines a request to find all items that are contained in a folder.</span></span>  <br/> <span data-ttu-id="e4e2a-133">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="e4e2a-133">The following is the XPath expression to this element:</span></span>  <br/>  `/FindItem` <br/> |
|[<span data-ttu-id="e4e2a-134">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e4e2a-134">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="e4e2a-135">定义对 Exchange 存储文件夹中的项目进行同步的请求。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-135">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="e4e2a-136">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="e4e2a-136">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderItems` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e4e2a-137">文本值</span><span class="sxs-lookup"><span data-stu-id="e4e2a-137">Text value</span></span>

<span data-ttu-id="e4e2a-138">无。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e4e2a-139">说明</span><span class="sxs-lookup"><span data-stu-id="e4e2a-139">Remarks</span></span>

<span data-ttu-id="e4e2a-140">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e4e2a-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e4e2a-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="e4e2a-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4e2a-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="e4e2a-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e4e2a-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="e4e2a-143">Schema Name</span></span>  <br/> |<span data-ttu-id="e4e2a-144">消息架构</span><span class="sxs-lookup"><span data-stu-id="e4e2a-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e4e2a-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="e4e2a-145">Validation File</span></span>  <br/> |<span data-ttu-id="e4e2a-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e4e2a-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e4e2a-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="e4e2a-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="e4e2a-148">False</span><span class="sxs-lookup"><span data-stu-id="e4e2a-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4e2a-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e4e2a-149">See also</span></span>



[<span data-ttu-id="e4e2a-150">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="e4e2a-150">GetItem operation</span></span>](getitem-operation.md)
  
[<span data-ttu-id="e4e2a-151">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="e4e2a-151">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="e4e2a-152">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="e4e2a-152">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="e4e2a-153">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e4e2a-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

