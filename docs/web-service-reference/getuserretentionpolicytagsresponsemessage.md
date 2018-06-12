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
ms.openlocfilehash: db73cb7f1922d845c9565753ff8d4917b82b1259
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825701"
---
# <a name="getuserretentionpolicytagsresponsemessage"></a><span data-ttu-id="1d1cb-103">GetUserRetentionPolicyTagsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1d1cb-103">GetUserRetentionPolicyTagsResponseMessage</span></span>

<span data-ttu-id="1d1cb-104">**GetUserRetentionPolicyTagsResponseMessage**元素指定**GetUserRetentionPolicyTags**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="1d1cb-104">The **GetUserRetentionPolicyTagsResponseMessage** element specifies the response message for a **GetUserRetentionPolicyTags** request.</span></span> 
  
```XML
<GetUserRetentionPolicyTagsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <RetentionPolicyTags/>
</GetUserRetentionPolicyTagsResponseMessage>
```

 <span data-ttu-id="1d1cb-105">**GetUserRetentionPolicyTagsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1d1cb-105">**GetUserRetentionPolicyTagsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d1cb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d1cb-106">Attributes and elements</span></span>

<span data-ttu-id="1d1cb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d1cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d1cb-108">属性</span><span class="sxs-lookup"><span data-stu-id="1d1cb-108">Attributes</span></span>

<span data-ttu-id="1d1cb-109">无。</span><span class="sxs-lookup"><span data-stu-id="1d1cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d1cb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1d1cb-110">Child elements</span></span>

<span data-ttu-id="1d1cb-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span><span class="sxs-lookup"><span data-stu-id="1d1cb-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [RetentionPolicyTags](retentionpolicytags.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d1cb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1d1cb-112">Parent elements</span></span>

[<span data-ttu-id="1d1cb-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1d1cb-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="1d1cb-114">备注</span><span class="sxs-lookup"><span data-stu-id="1d1cb-114">Remarks</span></span>

<span data-ttu-id="1d1cb-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1d1cb-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1d1cb-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1d1cb-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d1cb-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d1cb-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d1cb-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d1cb-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1d1cb-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d1cb-119">Schema name</span></span>  <br/> |<span data-ttu-id="1d1cb-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="1d1cb-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1d1cb-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d1cb-121">Validation file</span></span>  <br/> |<span data-ttu-id="1d1cb-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1d1cb-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d1cb-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d1cb-123">Can be empty</span></span>  <br/> |<span data-ttu-id="1d1cb-124">false</span><span class="sxs-lookup"><span data-stu-id="1d1cb-124">false</span></span>  <br/> |
   

