---
title: IncludeMimeContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludeMimeContent
api_type:
- schema
ms.assetid: 3f3c2300-55cd-41c0-900e-b470b290d52f
description: IncludeMimeContent 元素指定是否在响应中返回的项目或附件多用途 Internet 邮件扩展 (MIME) 内容。
ms.openlocfilehash: ddd6988be93231ac7c574a2e19c9ba4b562c7d0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825903"
---
# <a name="includemimecontent"></a><span data-ttu-id="35739-103">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="35739-103">IncludeMimeContent</span></span>

<span data-ttu-id="35739-104">**IncludeMimeContent**元素指定是否在响应中返回的项目或附件多用途 Internet 邮件扩展 (MIME) 内容。</span><span class="sxs-lookup"><span data-stu-id="35739-104">The **IncludeMimeContent** element specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 <span data-ttu-id="35739-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="35739-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="35739-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="35739-106">Attributes and elements</span></span>

<span data-ttu-id="35739-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="35739-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35739-108">属性</span><span class="sxs-lookup"><span data-stu-id="35739-108">Attributes</span></span>

<span data-ttu-id="35739-109">无。</span><span class="sxs-lookup"><span data-stu-id="35739-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="35739-110">子元素</span><span class="sxs-lookup"><span data-stu-id="35739-110">Child elements</span></span>

<span data-ttu-id="35739-111">无。</span><span class="sxs-lookup"><span data-stu-id="35739-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="35739-112">父元素</span><span class="sxs-lookup"><span data-stu-id="35739-112">Parent elements</span></span>

|<span data-ttu-id="35739-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="35739-113">**Element**</span></span>|<span data-ttu-id="35739-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="35739-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="35739-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="35739-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="35739-116">标识要[GetAttachment](getattachment.md)请求的响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="35739-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/> <br/> <span data-ttu-id="35739-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="35739-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="35739-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="35739-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="35739-119">标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="35739-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="35739-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="35739-120">The following are the XPath expressions to this element:</span></span><br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="35739-121">文本值</span><span class="sxs-lookup"><span data-stu-id="35739-121">Text value</span></span>

<span data-ttu-id="35739-122">此元素可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="35739-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="35739-123">默认值为 **false** 。</span><span class="sxs-lookup"><span data-stu-id="35739-123">The default value is **false**.</span></span> <span data-ttu-id="35739-124">这是 Boolean 数据类型。</span><span class="sxs-lookup"><span data-stu-id="35739-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35739-125">备注</span><span class="sxs-lookup"><span data-stu-id="35739-125">Remarks</span></span>

<span data-ttu-id="35739-126">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="35739-126">This element is optional.</span></span>
  
<span data-ttu-id="35739-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="35739-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="35739-128">示例</span><span class="sxs-lookup"><span data-stu-id="35739-128">Example</span></span>

<span data-ttu-id="35739-129">请求的下面的示例演示如何设置**IncludeMimeContent**元素。</span><span class="sxs-lookup"><span data-stu-id="35739-129">The following example of a request demonstrates a how to set the **IncludeMimeContent** element.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="35739-130">附件 Id 属性将被截断，若要保留可读性。</span><span class="sxs-lookup"><span data-stu-id="35739-130">The attachment Id attribute is truncated to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="35739-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="35739-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35739-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="35739-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="35739-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="35739-133">Schema Name</span></span>  <br/> |<span data-ttu-id="35739-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="35739-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="35739-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="35739-135">Validation File</span></span>  <br/> |<span data-ttu-id="35739-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="35739-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="35739-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="35739-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="35739-138">False</span><span class="sxs-lookup"><span data-stu-id="35739-138">False</span></span>  <br/> |
   

