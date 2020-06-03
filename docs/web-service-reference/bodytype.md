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
description: Office.mailboxenums.bodytype 元素标识如何在响应中设置正文文本的格式。
ms.openlocfilehash: 448d20ac54b09a2f4f6a273a1099519371ac7f5b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465945"
---
# <a name="bodytype"></a><span data-ttu-id="910c0-103">BodyType</span><span class="sxs-lookup"><span data-stu-id="910c0-103">BodyType</span></span>

<span data-ttu-id="910c0-104">**Office.mailboxenums.bodytype**元素标识如何在响应中设置正文文本的格式。</span><span class="sxs-lookup"><span data-stu-id="910c0-104">The **BodyType** element identifies how the body text is formatted in the response.</span></span> 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

<span data-ttu-id="910c0-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="910c0-105">**BodyTypeResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="910c0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="910c0-106">Attributes and elements</span></span>

<span data-ttu-id="910c0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="910c0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="910c0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="910c0-108">Attributes</span></span>

<span data-ttu-id="910c0-109">无。</span><span class="sxs-lookup"><span data-stu-id="910c0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="910c0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="910c0-110">Child elements</span></span>

<span data-ttu-id="910c0-111">无。</span><span class="sxs-lookup"><span data-stu-id="910c0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="910c0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="910c0-112">Parent elements</span></span>

|<span data-ttu-id="910c0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="910c0-113">**Element**</span></span>|<span data-ttu-id="910c0-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="910c0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="910c0-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="910c0-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="910c0-116">标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="910c0-116">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/><br/><span data-ttu-id="910c0-117">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="910c0-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="910c0-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="910c0-118">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="910c0-119">标识要在对[GetAttachment](getattachment.md)请求的响应中返回的其他扩展项属性。</span><span class="sxs-lookup"><span data-stu-id="910c0-119">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/><span data-ttu-id="910c0-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="910c0-120">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="910c0-121">文本值</span><span class="sxs-lookup"><span data-stu-id="910c0-121">Text value</span></span>

<span data-ttu-id="910c0-122">下表列出了**office.mailboxenums.bodytype**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="910c0-122">The following table lists the possible values for the **BodyType** element.</span></span> 
  
|<span data-ttu-id="910c0-123">**值**</span><span class="sxs-lookup"><span data-stu-id="910c0-123">**Value**</span></span>|<span data-ttu-id="910c0-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="910c0-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="910c0-125">最好</span><span class="sxs-lookup"><span data-stu-id="910c0-125">Best</span></span>  <br/> |<span data-ttu-id="910c0-126">响应将返回正文文本的最丰富的可用内容。</span><span class="sxs-lookup"><span data-stu-id="910c0-126">The response will return the richest available content of body text.</span></span> <span data-ttu-id="910c0-127">如果不知道内容是文本还是 HTML，这将非常有用。</span><span class="sxs-lookup"><span data-stu-id="910c0-127">This is useful if it is unknown whether the content is text or HTML.</span></span><br/><br/> <span data-ttu-id="910c0-128">如果存储的正文为纯文本，则返回的正文将为文本。</span><span class="sxs-lookup"><span data-stu-id="910c0-128">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="910c0-129">否则，如果存储的正文是 HTML 格式或 RTF 格式，则响应将返回 HTML。</span><span class="sxs-lookup"><span data-stu-id="910c0-129">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span><br/><br/> <span data-ttu-id="910c0-130">此值为默认值。</span><span class="sxs-lookup"><span data-stu-id="910c0-130">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="910c0-131">HTML</span><span class="sxs-lookup"><span data-stu-id="910c0-131">HTML</span></span>  <br/> |<span data-ttu-id="910c0-132">响应将以 HTML 形式返回项目正文。</span><span class="sxs-lookup"><span data-stu-id="910c0-132">The response will return an item body as HTML.</span></span>  <br/> |
|<span data-ttu-id="910c0-133">文本</span><span class="sxs-lookup"><span data-stu-id="910c0-133">Text</span></span>  <br/> |<span data-ttu-id="910c0-134">响应将以纯文本形式返回项目正文。</span><span class="sxs-lookup"><span data-stu-id="910c0-134">The response will return an item body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="910c0-135">备注</span><span class="sxs-lookup"><span data-stu-id="910c0-135">Remarks</span></span>

<span data-ttu-id="910c0-136">您可以通过检查[body](body.md)元素的**office.mailboxenums.bodytype**属性来标识响应中返回的正文的类型。</span><span class="sxs-lookup"><span data-stu-id="910c0-136">You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element.</span></span> <span data-ttu-id="910c0-137">**Office.mailboxenums.bodytype**属性将正文标识为 HTML 或文本。</span><span class="sxs-lookup"><span data-stu-id="910c0-137">The **BodyType** attribute will identify the body as either HTML or text.</span></span> 
  
<span data-ttu-id="910c0-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="910c0-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="910c0-139">示例</span><span class="sxs-lookup"><span data-stu-id="910c0-139">Example</span></span>

<span data-ttu-id="910c0-140">下面的请求示例显示了**office.mailboxenums.bodytype**元素的使用位置。</span><span class="sxs-lookup"><span data-stu-id="910c0-140">The following example of a request shows where a **BodyType** element is used.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="910c0-141">已缩短 Id 属性以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="910c0-141">The Id attribute has been shortened to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="910c0-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="910c0-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="910c0-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="910c0-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="910c0-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="910c0-144">Schema Name</span></span>  <br/> |<span data-ttu-id="910c0-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="910c0-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="910c0-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="910c0-146">Validation File</span></span>  <br/> |<span data-ttu-id="910c0-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="910c0-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="910c0-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="910c0-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="910c0-149">False</span><span class="sxs-lookup"><span data-stu-id="910c0-149">False</span></span>  <br/> |
   

