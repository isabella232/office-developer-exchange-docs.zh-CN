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
description: IncludeMimeContent 元素指定响应中是否返回项目或附件的多用途 Internet 邮件扩展（MIME）内容。
ms.openlocfilehash: 6198e4bef2dc59e6e56a8d3cbe463dad13e544e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457191"
---
# <a name="includemimecontent"></a><span data-ttu-id="26f37-103">IncludeMimeContent</span><span class="sxs-lookup"><span data-stu-id="26f37-103">IncludeMimeContent</span></span>

<span data-ttu-id="26f37-104">**IncludeMimeContent**元素指定响应中是否返回项目或附件的多用途 Internet 邮件扩展（MIME）内容。</span><span class="sxs-lookup"><span data-stu-id="26f37-104">The **IncludeMimeContent** element specifies whether the Multipurpose Internet Mail Extensions (MIME) content of an item or attachment is returned in the response.</span></span> 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 <span data-ttu-id="26f37-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="26f37-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="26f37-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="26f37-106">Attributes and elements</span></span>

<span data-ttu-id="26f37-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="26f37-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26f37-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="26f37-108">Attributes</span></span>

<span data-ttu-id="26f37-109">无。</span><span class="sxs-lookup"><span data-stu-id="26f37-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26f37-110">子元素</span><span class="sxs-lookup"><span data-stu-id="26f37-110">Child elements</span></span>

<span data-ttu-id="26f37-111">无。</span><span class="sxs-lookup"><span data-stu-id="26f37-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26f37-112">父元素</span><span class="sxs-lookup"><span data-stu-id="26f37-112">Parent elements</span></span>

|<span data-ttu-id="26f37-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="26f37-113">**Element**</span></span>|<span data-ttu-id="26f37-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="26f37-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26f37-115">AttachmentShape</span><span class="sxs-lookup"><span data-stu-id="26f37-115">AttachmentShape</span></span>](attachmentshape.md) <br/> | <span data-ttu-id="26f37-116">标识在对[GetAttachment](getattachment.md)请求的响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="26f37-116">Identifies additional properties to return in a response to a [GetAttachment](getattachment.md) request.</span></span>  <br/> <br/> <span data-ttu-id="26f37-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="26f37-117">The following is the XPath expression to this element:</span></span>  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[<span data-ttu-id="26f37-118">ItemShape</span><span class="sxs-lookup"><span data-stu-id="26f37-118">ItemShape</span></span>](itemshape.md) <br/> | <span data-ttu-id="26f37-119">标识要包括在 GetItem、FindItem 或 SyncFolderItems 响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="26f37-119">Identifies the item properties and content to include in a GetItem, FindItem, or SyncFolderItems response.</span></span>  <br/> <br/> <span data-ttu-id="26f37-120">下面是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="26f37-120">The following are the XPath expressions to this element:</span></span><br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26f37-121">文本值</span><span class="sxs-lookup"><span data-stu-id="26f37-121">Text value</span></span>

<span data-ttu-id="26f37-122">此元素可以是**true** ，也可以是**false**。</span><span class="sxs-lookup"><span data-stu-id="26f37-122">This element can be either **true** or **false**.</span></span> <span data-ttu-id="26f37-123">默认值为 **false**。</span><span class="sxs-lookup"><span data-stu-id="26f37-123">The default value is **false**.</span></span> <span data-ttu-id="26f37-124">这是一个 Boolean 数据类型。</span><span class="sxs-lookup"><span data-stu-id="26f37-124">This is a Boolean data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26f37-125">说明</span><span class="sxs-lookup"><span data-stu-id="26f37-125">Remarks</span></span>

<span data-ttu-id="26f37-126">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="26f37-126">This element is optional.</span></span>
  
<span data-ttu-id="26f37-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="26f37-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="26f37-128">示例</span><span class="sxs-lookup"><span data-stu-id="26f37-128">Example</span></span>

<span data-ttu-id="26f37-129">下面的请求示例演示如何设置**IncludeMimeContent**元素。</span><span class="sxs-lookup"><span data-stu-id="26f37-129">The following example of a request demonstrates a how to set the **IncludeMimeContent** element.</span></span> 
  
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

<span data-ttu-id="26f37-130">将截断附件 Id 属性以保留可读性。</span><span class="sxs-lookup"><span data-stu-id="26f37-130">The attachment Id attribute is truncated to preserve readability.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26f37-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="26f37-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26f37-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="26f37-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26f37-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="26f37-133">Schema Name</span></span>  <br/> |<span data-ttu-id="26f37-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="26f37-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="26f37-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="26f37-135">Validation File</span></span>  <br/> |<span data-ttu-id="26f37-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26f37-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26f37-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="26f37-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="26f37-138">False</span><span class="sxs-lookup"><span data-stu-id="26f37-138">False</span></span>  <br/> |
   

