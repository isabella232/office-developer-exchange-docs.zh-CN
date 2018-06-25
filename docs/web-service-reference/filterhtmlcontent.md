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
description: FilterHtmlContent 元素指定是否从项目或附件筛选存在安全隐患的 HTML 内容。
ms.openlocfilehash: db181eff9586061d728a5e4ef55a78f4955b5713
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754311"
---
# <a name="filterhtmlcontent"></a><span data-ttu-id="09e93-103">FilterHtmlContent</span><span class="sxs-lookup"><span data-stu-id="09e93-103">FilterHtmlContent</span></span>

<span data-ttu-id="09e93-104">**FilterHtmlContent**元素指定是否从项目或附件筛选存在安全隐患的 HTML 内容。</span><span class="sxs-lookup"><span data-stu-id="09e93-104">The **FilterHtmlContent** element specifies whether potentially unsafe HTML content is filtered from an item or attachment.</span></span> 
  
```xml
<FilterHtmlContent>true or false</FilterHtmlContent>
```

 <span data-ttu-id="09e93-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="09e93-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09e93-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="09e93-106">Attributes and elements</span></span>

<span data-ttu-id="09e93-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="09e93-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09e93-108">属性</span><span class="sxs-lookup"><span data-stu-id="09e93-108">Attributes</span></span>

<span data-ttu-id="09e93-109">无。</span><span class="sxs-lookup"><span data-stu-id="09e93-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09e93-110">子元素</span><span class="sxs-lookup"><span data-stu-id="09e93-110">Child elements</span></span>

<span data-ttu-id="09e93-111">无。</span><span class="sxs-lookup"><span data-stu-id="09e93-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09e93-112">父元素</span><span class="sxs-lookup"><span data-stu-id="09e93-112">Parent elements</span></span>

|<span data-ttu-id="09e93-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="09e93-113">**Element**</span></span>|<span data-ttu-id="09e93-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="09e93-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09e93-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="09e93-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="09e93-116">标识要[GetAttachment](getattachment.md)请求的响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="09e93-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/>  <span data-ttu-id="09e93-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="09e93-117">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="09e93-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="09e93-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="09e93-119">标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="09e93-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="09e93-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="09e93-120">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetItem/ItemShape`<br/> <br/>  `/FindItem/ItemShape`<br/> <br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09e93-121">文本值</span><span class="sxs-lookup"><span data-stu-id="09e93-121">Text value</span></span>

<span data-ttu-id="09e93-122">此元素可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="09e93-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="09e93-123">默认值为 **false** 。</span><span class="sxs-lookup"><span data-stu-id="09e93-123">The default value is **false**.</span></span> <span data-ttu-id="09e93-124">这是 Boolean 数据类型。</span><span class="sxs-lookup"><span data-stu-id="09e93-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09e93-125">备注</span><span class="sxs-lookup"><span data-stu-id="09e93-125">Remarks</span></span>

<span data-ttu-id="09e93-126">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="09e93-126">This element is optional.</span></span>
  
<span data-ttu-id="09e93-127">描述此元素的架构位于安装了客户端访问服务器角色与运行 Exchange Server 的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="09e93-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09e93-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="09e93-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09e93-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="09e93-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="09e93-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="09e93-130">Schema Name</span></span>  <br/> |<span data-ttu-id="09e93-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="09e93-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="09e93-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="09e93-132">Validation File</span></span>  <br/> |<span data-ttu-id="09e93-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="09e93-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09e93-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="09e93-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="09e93-135">False</span><span class="sxs-lookup"><span data-stu-id="09e93-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09e93-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09e93-136">See also</span></span>

- [<span data-ttu-id="09e93-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="09e93-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

