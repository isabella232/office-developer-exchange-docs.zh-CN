---
title: PlayOnPhoneResponse （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneResponse
api_type:
- schema
ms.assetid: 42b16880-1271-4690-abd0-0072d95b04b7
description: PlayOnPhoneResponse 元素定义对 PlayOnPhone 操作（UM web 服务）请求的响应。
ms.openlocfilehash: ddb9cc9a8feaeb476e6502339fdc74d024797b9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459614"
---
# <a name="playonphoneresponse-um-web-service"></a><span data-ttu-id="0d149-103">PlayOnPhoneResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d149-103">PlayOnPhoneResponse (UM web service)</span></span>

<span data-ttu-id="0d149-104">**PlayOnPhoneResponse**元素定义对[PLAYONPHONE 操作（UM web 服务）](playonphone-operation-um-web-service.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="0d149-104">The **PlayOnPhoneResponse** element defines a response to a [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="0d149-105">PlayOnPhoneResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d149-105">PlayOnPhoneResponse (UM web service)</span></span>](playonphoneresponse-um-web-service.md)
  
```xml
<PlayOnPhoneResponse />
```

 <span data-ttu-id="0d149-106">**string**</span><span class="sxs-lookup"><span data-stu-id="0d149-106">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d149-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0d149-107">Attributes and elements</span></span>

<span data-ttu-id="0d149-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0d149-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d149-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="0d149-109">Attributes</span></span>

<span data-ttu-id="0d149-110">无。</span><span class="sxs-lookup"><span data-stu-id="0d149-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d149-111">子元素</span><span class="sxs-lookup"><span data-stu-id="0d149-111">Child elements</span></span>

<span data-ttu-id="0d149-112">无。</span><span class="sxs-lookup"><span data-stu-id="0d149-112">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d149-113">父元素</span><span class="sxs-lookup"><span data-stu-id="0d149-113">Parent elements</span></span>

<span data-ttu-id="0d149-114">无。</span><span class="sxs-lookup"><span data-stu-id="0d149-114">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0d149-115">文本值</span><span class="sxs-lookup"><span data-stu-id="0d149-115">Text value</span></span>

<span data-ttu-id="0d149-116">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="0d149-116">A text value is required.</span></span> <span data-ttu-id="0d149-117">Text 值是用于[GetCallInfo 操作（um web 服务）](getcallinfo-operation-um-web-service.md)请求或[断开连接操作（um web 服务）](disconnect-operation-um-web-service.md)请求中[CallId （um web 服务](callid-um-web-service.md)）的值的调用标识符。</span><span class="sxs-lookup"><span data-stu-id="0d149-117">The text value is the call identifier to use for the value of [CallId (UM web service)](callid-um-web-service.md) in a [GetCallInfo operation (UM web service)](getcallinfo-operation-um-web-service.md) request or a [Disconnect operation (UM web service)](disconnect-operation-um-web-service.md) request.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="0d149-118">元素信息</span><span class="sxs-lookup"><span data-stu-id="0d149-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d149-119">命名空间</span><span class="sxs-lookup"><span data-stu-id="0d149-119">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d149-120">架构名称</span><span class="sxs-lookup"><span data-stu-id="0d149-120">Schema Name</span></span>  <br/> |<span data-ttu-id="0d149-121">邮件</span><span class="sxs-lookup"><span data-stu-id="0d149-121">Messages</span></span>  <br/> |
|<span data-ttu-id="0d149-122">验证文件</span><span class="sxs-lookup"><span data-stu-id="0d149-122">Validation File</span></span>  <br/> |<span data-ttu-id="0d149-123">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="0d149-123">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d149-124">可以为空</span><span class="sxs-lookup"><span data-stu-id="0d149-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d149-125">False</span><span class="sxs-lookup"><span data-stu-id="0d149-125">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d149-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d149-126">See also</span></span>



[<span data-ttu-id="0d149-127">PlayOnPhone 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d149-127">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)

