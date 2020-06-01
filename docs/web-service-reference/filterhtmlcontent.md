---
title: FilterHtmlContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FilterHtmlContent
api_type:
- schema
ms.assetid: 2f9358a0-de1d-4544-9aa0-d9f6519f3b5f
description: FilterHtmlContent 元素指定是否从项目或附件筛选出可能不安全的 HTML 内容。
ms.openlocfilehash: 28e3be86b550c3f330fbb6846b64732b5674304d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462673"
---
# <a name="filterhtmlcontent"></a><span data-ttu-id="541df-103">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="541df-103">FilterHtmlContent</span></span>

<span data-ttu-id="541df-104">**FilterHtmlContent**元素指定是否从项目或附件筛选出可能不安全的 HTML 内容。</span><span class="sxs-lookup"><span data-stu-id="541df-104">The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment.</span></span> 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 <span data-ttu-id="541df-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="541df-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="541df-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="541df-106">Attributes and elements</span></span>

<span data-ttu-id="541df-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="541df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="541df-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="541df-108">Attributes</span></span>

<span data-ttu-id="541df-109">无。</span><span class="sxs-lookup"><span data-stu-id="541df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="541df-110">子元素</span><span class="sxs-lookup"><span data-stu-id="541df-110">Child elements</span></span>

<span data-ttu-id="541df-111">无。</span><span class="sxs-lookup"><span data-stu-id="541df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="541df-112">父元素</span><span class="sxs-lookup"><span data-stu-id="541df-112">Parent elements</span></span>

|<span data-ttu-id="541df-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="541df-113">**Element**</span></span>|<span data-ttu-id="541df-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="541df-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="541df-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="541df-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="541df-116">标识在对[GetAttachment](getattachment.md)请求的响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="541df-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/>  <span data-ttu-id="541df-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="541df-117">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="541df-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="541df-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="541df-119">标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="541df-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="541df-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="541df-120">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="541df-121">文本值</span><span class="sxs-lookup"><span data-stu-id="541df-121">Text value</span></span>

<span data-ttu-id="541df-122">此元素可以是**true** ，也可以是**false**。</span><span class="sxs-lookup"><span data-stu-id="541df-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="541df-123">默认值为 **false**。</span><span class="sxs-lookup"><span data-stu-id="541df-123">The default value is **false**.</span></span> <span data-ttu-id="541df-124">这是一个 Boolean 数据类型。</span><span class="sxs-lookup"><span data-stu-id="541df-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="541df-125">说明</span><span class="sxs-lookup"><span data-stu-id="541df-125">Remarks</span></span>

<span data-ttu-id="541df-126">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="541df-126">This element is optional.</span></span>
  
<span data-ttu-id="541df-127">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="541df-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="541df-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="541df-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="541df-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="541df-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="541df-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="541df-130">Schema Name</span></span>  <br/> |<span data-ttu-id="541df-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="541df-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="541df-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="541df-132">Validation File</span></span>  <br/> |<span data-ttu-id="541df-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="541df-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="541df-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="541df-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="541df-135">False</span><span class="sxs-lookup"><span data-stu-id="541df-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="541df-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="541df-136">See also</span></span>

- [<span data-ttu-id="541df-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="541df-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

