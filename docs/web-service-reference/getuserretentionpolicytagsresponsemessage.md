---
title: GetUserRetentionPolicyTagsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9991d6e0-8c31-4e73-8af3-da4298474b66
description: GetUserRetentionPolicyTagsResponseMessage 元素指定 GetUserRetentionPolicyTags 请求的响应消息。
ms.openlocfilehash: e65266e72010f42a2052bbb8cfab21ea4059f92b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461805"
---
# <a name="getuserretentionpolicytagsresponsemessage"></a><span data-ttu-id="c2c8e-103">GetUserRetentionPolicyTagsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c2c8e-103">GetUserRetentionPolicyTagsResponseMessage</span></span>

<span data-ttu-id="c2c8e-104">**GetUserRetentionPolicyTagsResponseMessage**元素指定**GetUserRetentionPolicyTags**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c2c8e-104">The **GetUserRetentionPolicyTagsResponseMessage** element specifies the response message for a **GetUserRetentionPolicyTags** request.</span></span> 
  
```XML
<GetUserRetentionPolicyTagsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RetentionPolicyTags/>
</GetUserRetentionPolicyTagsResponseMessage>
```

 <span data-ttu-id="c2c8e-105">**GetUserRetentionPolicyTagsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="c2c8e-105">**GetUserRetentionPolicyTagsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2c8e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c2c8e-106">Attributes and elements</span></span>

<span data-ttu-id="c2c8e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c2c8e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2c8e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c2c8e-108">Attributes</span></span>

<span data-ttu-id="c2c8e-109">无。</span><span class="sxs-lookup"><span data-stu-id="c2c8e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2c8e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c2c8e-110">Child elements</span></span>

<span data-ttu-id="c2c8e-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [RetentionPolicyTags](retentionpolicytags.md)</span><span class="sxs-lookup"><span data-stu-id="c2c8e-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c2c8e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c2c8e-112">Parent elements</span></span>

[<span data-ttu-id="c2c8e-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c2c8e-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="c2c8e-114">备注</span><span class="sxs-lookup"><span data-stu-id="c2c8e-114">Remarks</span></span>

<span data-ttu-id="c2c8e-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c2c8e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c2c8e-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c2c8e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2c8e-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="c2c8e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2c8e-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="c2c8e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c2c8e-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="c2c8e-119">Schema name</span></span>  <br/> |<span data-ttu-id="c2c8e-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="c2c8e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c2c8e-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="c2c8e-121">Validation file</span></span>  <br/> |<span data-ttu-id="c2c8e-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="c2c8e-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c2c8e-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="c2c8e-123">Can be empty</span></span>  <br/> |<span data-ttu-id="c2c8e-124">false</span><span class="sxs-lookup"><span data-stu-id="c2c8e-124">false</span></span>  <br/> |
   

