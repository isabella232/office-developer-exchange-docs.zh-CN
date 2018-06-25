---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: BodyType 元素标识如何响应中设置的正文文本的格式。
ms.openlocfilehash: f8be2e96390b40faa367cf0d34c533accc3b8afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753363"
---
# <a name="bodytype"></a><span data-ttu-id="30b6d-103">BodyType</span><span class="sxs-lookup"><span data-stu-id="30b6d-103">BodyType</span></span>

<span data-ttu-id="30b6d-104">**BodyType**元素标识如何响应中设置的正文文本的格式。</span><span class="sxs-lookup"><span data-stu-id="30b6d-104">The **BodyType** element identifies how the body text is formatted in the response.</span></span> 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

<span data-ttu-id="30b6d-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="30b6d-105">**BodyTypeResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="30b6d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="30b6d-106">Attributes and elements</span></span>

<span data-ttu-id="30b6d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="30b6d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30b6d-108">属性</span><span class="sxs-lookup"><span data-stu-id="30b6d-108">Attributes</span></span>

<span data-ttu-id="30b6d-109">无。</span><span class="sxs-lookup"><span data-stu-id="30b6d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30b6d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="30b6d-110">Child elements</span></span>

<span data-ttu-id="30b6d-111">无。</span><span class="sxs-lookup"><span data-stu-id="30b6d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="30b6d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="30b6d-112">Parent elements</span></span>

|<span data-ttu-id="30b6d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="30b6d-113">**Element**</span></span>|<span data-ttu-id="30b6d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="30b6d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30b6d-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="30b6d-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="30b6d-116">标识项目属性和 GetItem、 FindItem 或 SyncFolderItems 响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="30b6d-116">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/><br/><span data-ttu-id="30b6d-117">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="30b6d-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="30b6d-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="30b6d-118">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="30b6d-119">标识要[GetAttachment](getattachment.md)请求的响应中返回的其他扩展的项属性。</span><span class="sxs-lookup"><span data-stu-id="30b6d-119">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/><span data-ttu-id="30b6d-120">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="30b6d-120">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="30b6d-121">文本值</span><span class="sxs-lookup"><span data-stu-id="30b6d-121">Text value</span></span>

<span data-ttu-id="30b6d-122">下表列出了**BodyType**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="30b6d-122">The following table lists the possible values for the **BodyType** element.</span></span> 
  
|<span data-ttu-id="30b6d-123">**值**</span><span class="sxs-lookup"><span data-stu-id="30b6d-123">**Value**</span></span>|<span data-ttu-id="30b6d-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="30b6d-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="30b6d-125">最佳</span><span class="sxs-lookup"><span data-stu-id="30b6d-125">Best</span></span>  <br/> |<span data-ttu-id="30b6d-126">响应将返回正文文本的丰富的可用内容。</span><span class="sxs-lookup"><span data-stu-id="30b6d-126">The response will return the richest available content of body text.</span></span> <span data-ttu-id="30b6d-127">这很有用，如果不知道的内容是否是文本或 HTML。</span><span class="sxs-lookup"><span data-stu-id="30b6d-127">This is useful if it is unknown whether the content is text or HTML.</span></span><br/><br/> <span data-ttu-id="30b6d-128">返回的正文将文本，如果存储的正文采用纯文本。</span><span class="sxs-lookup"><span data-stu-id="30b6d-128">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="30b6d-129">否则，如果存储的正文采用 HTML 或 RTF 格式响应将返回 HTML。</span><span class="sxs-lookup"><span data-stu-id="30b6d-129">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span><br/><br/> <span data-ttu-id="30b6d-130">这是默认值。</span><span class="sxs-lookup"><span data-stu-id="30b6d-130">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="30b6d-131">HTML</span><span class="sxs-lookup"><span data-stu-id="30b6d-131">HTML</span></span>  <br/> |<span data-ttu-id="30b6d-132">响应将以 HTML 形式返回项目正文。</span><span class="sxs-lookup"><span data-stu-id="30b6d-132">The response will return an item body as HTML.</span></span>  <br/> |
|<span data-ttu-id="30b6d-133">Text</span><span class="sxs-lookup"><span data-stu-id="30b6d-133">Text</span></span>  <br/> |<span data-ttu-id="30b6d-134">响应将以纯文本形式返回项目正文。</span><span class="sxs-lookup"><span data-stu-id="30b6d-134">The response will return an item body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30b6d-135">注解</span><span class="sxs-lookup"><span data-stu-id="30b6d-135">Remarks</span></span>

<span data-ttu-id="30b6d-136">您可以标识正文响应中返回通过检查[Body](body.md)元素的**BodyType**属性的类型。</span><span class="sxs-lookup"><span data-stu-id="30b6d-136">You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element.</span></span> <span data-ttu-id="30b6d-137">**BodyType**属性将标识以 HTML 或文本正文。</span><span class="sxs-lookup"><span data-stu-id="30b6d-137">The **BodyType** attribute will identify the body as either HTML or text.</span></span> 
  
<span data-ttu-id="30b6d-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="30b6d-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="30b6d-139">示例</span><span class="sxs-lookup"><span data-stu-id="30b6d-139">Example</span></span>

<span data-ttu-id="30b6d-140">请求的下面的示例演示使用**BodyType**元素的位置。</span><span class="sxs-lookup"><span data-stu-id="30b6d-140">The following example of a request shows where a **BodyType** element is used.</span></span> 
  
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
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="30b6d-141">已缩短的 Id 属性保留可读性。</span><span class="sxs-lookup"><span data-stu-id="30b6d-141">The Id attribute has been shortened to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30b6d-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="30b6d-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b6d-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="30b6d-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="30b6d-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="30b6d-144">Schema Name</span></span>  <br/> |<span data-ttu-id="30b6d-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="30b6d-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="30b6d-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="30b6d-146">Validation File</span></span>  <br/> |<span data-ttu-id="30b6d-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="30b6d-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="30b6d-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="30b6d-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="30b6d-149">False</span><span class="sxs-lookup"><span data-stu-id="30b6d-149">False</span></span>  <br/> |
   

