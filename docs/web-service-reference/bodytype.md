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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465945"
---
# <a name="bodytype"></a><span data-ttu-id="ae01f-103">BodyType</span><span class="sxs-lookup"><span data-stu-id="ae01f-103">BodyType</span></span>

<span data-ttu-id="ae01f-104">**Office.mailboxenums.bodytype**元素标识如何在响应中设置正文文本的格式。</span><span class="sxs-lookup"><span data-stu-id="ae01f-104">The **BodyType** element identifies how the body text is formatted in the response.</span></span> 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

<span data-ttu-id="ae01f-105">**BodyTypeResponseType**</span><span class="sxs-lookup"><span data-stu-id="ae01f-105">**BodyTypeResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ae01f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ae01f-106">Attributes and elements</span></span>

<span data-ttu-id="ae01f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ae01f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae01f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ae01f-108">Attributes</span></span>

<span data-ttu-id="ae01f-109">无。</span><span class="sxs-lookup"><span data-stu-id="ae01f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae01f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ae01f-110">Child elements</span></span>

<span data-ttu-id="ae01f-111">无。</span><span class="sxs-lookup"><span data-stu-id="ae01f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ae01f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ae01f-112">Parent elements</span></span>

|<span data-ttu-id="ae01f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ae01f-113">**Element**</span></span>|<span data-ttu-id="ae01f-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="ae01f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae01f-115">ItemShape</span><span class="sxs-lookup"><span data-stu-id="ae01f-115">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="ae01f-116">标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="ae01f-116">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/><br/><span data-ttu-id="ae01f-117">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="ae01f-117">The following are the XPath expressions to this element:</span></span><br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[<span data-ttu-id="ae01f-118">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="ae01f-118">AttachmentShape</span></span>](attachmentshape.md) <br/> |<span data-ttu-id="ae01f-119">标识要在对[GetAttachment](getattachment.md)请求的响应中返回的其他扩展项属性。</span><span class="sxs-lookup"><span data-stu-id="ae01f-119">Identifies additional extended item properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/><br/><span data-ttu-id="ae01f-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="ae01f-120">The following is the XPath expression to this element:</span></span><br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ae01f-121">文本值</span><span class="sxs-lookup"><span data-stu-id="ae01f-121">Text value</span></span>

<span data-ttu-id="ae01f-122">下表列出了**office.mailboxenums.bodytype**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="ae01f-122">The following table lists the possible values for the **BodyType** element.</span></span> 
  
|<span data-ttu-id="ae01f-123">**值**</span><span class="sxs-lookup"><span data-stu-id="ae01f-123">**Value**</span></span>|<span data-ttu-id="ae01f-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="ae01f-124">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae01f-125">最好</span><span class="sxs-lookup"><span data-stu-id="ae01f-125">Best</span></span>  <br/> |<span data-ttu-id="ae01f-126">响应将返回正文文本的最丰富的可用内容。</span><span class="sxs-lookup"><span data-stu-id="ae01f-126">The response will return the richest available content of body text.</span></span> <span data-ttu-id="ae01f-127">如果不知道内容是文本还是 HTML，这将非常有用。</span><span class="sxs-lookup"><span data-stu-id="ae01f-127">This is useful if it is unknown whether the content is text or HTML.</span></span><br/><br/> <span data-ttu-id="ae01f-128">如果存储的正文为纯文本，则返回的正文将为文本。</span><span class="sxs-lookup"><span data-stu-id="ae01f-128">The returned body will be text if the stored body is plain text.</span></span> <span data-ttu-id="ae01f-129">否则，如果存储的正文是 HTML 格式或 RTF 格式，则响应将返回 HTML。</span><span class="sxs-lookup"><span data-stu-id="ae01f-129">Otherwise, the response will return HTML if the stored body is in either HTML or RTF format.</span></span><br/><br/> <span data-ttu-id="ae01f-130">此值为默认值。</span><span class="sxs-lookup"><span data-stu-id="ae01f-130">This is the default value.</span></span>  <br/> |
|<span data-ttu-id="ae01f-131">HTML</span><span class="sxs-lookup"><span data-stu-id="ae01f-131">HTML</span></span>  <br/> |<span data-ttu-id="ae01f-132">响应将以 HTML 形式返回项目正文。</span><span class="sxs-lookup"><span data-stu-id="ae01f-132">The response will return an item body as HTML.</span></span>  <br/> |
|<span data-ttu-id="ae01f-133">文本</span><span class="sxs-lookup"><span data-stu-id="ae01f-133">Text</span></span>  <br/> |<span data-ttu-id="ae01f-134">响应将以纯文本形式返回项目正文。</span><span class="sxs-lookup"><span data-stu-id="ae01f-134">The response will return an item body as plain text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae01f-135">备注</span><span class="sxs-lookup"><span data-stu-id="ae01f-135">Remarks</span></span>

<span data-ttu-id="ae01f-136">您可以通过检查[body](body.md)元素的**office.mailboxenums.bodytype**属性来标识响应中返回的正文的类型。</span><span class="sxs-lookup"><span data-stu-id="ae01f-136">You can identify the type of body returned in the response by checking the **BodyType** attribute of the [Body](body.md) element.</span></span> <span data-ttu-id="ae01f-137">**Office.mailboxenums.bodytype**属性将正文标识为 HTML 或文本。</span><span class="sxs-lookup"><span data-stu-id="ae01f-137">The **BodyType** attribute will identify the body as either HTML or text.</span></span> 
  
<span data-ttu-id="ae01f-138">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ae01f-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="ae01f-139">示例</span><span class="sxs-lookup"><span data-stu-id="ae01f-139">Example</span></span>

<span data-ttu-id="ae01f-140">下面的请求示例显示了**office.mailboxenums.bodytype**元素的使用位置。</span><span class="sxs-lookup"><span data-stu-id="ae01f-140">The following example of a request shows where a **BodyType** element is used.</span></span> 
  
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

<span data-ttu-id="ae01f-141">已缩短 Id 属性以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="ae01f-141">The Id attribute has been shortened to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae01f-142">元素信息</span><span class="sxs-lookup"><span data-stu-id="ae01f-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae01f-143">命名空间</span><span class="sxs-lookup"><span data-stu-id="ae01f-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ae01f-144">架构名称</span><span class="sxs-lookup"><span data-stu-id="ae01f-144">Schema Name</span></span>  <br/> |<span data-ttu-id="ae01f-145">类型架构</span><span class="sxs-lookup"><span data-stu-id="ae01f-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="ae01f-146">验证文件</span><span class="sxs-lookup"><span data-stu-id="ae01f-146">Validation File</span></span>  <br/> |<span data-ttu-id="ae01f-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ae01f-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ae01f-148">可以为空</span><span class="sxs-lookup"><span data-stu-id="ae01f-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae01f-149">False</span><span class="sxs-lookup"><span data-stu-id="ae01f-149">False</span></span>  <br/> |
   

