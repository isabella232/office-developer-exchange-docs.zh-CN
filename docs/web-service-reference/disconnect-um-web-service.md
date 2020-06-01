---
title: 断开连接（UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: 2f8c1e8c-3bd4-4988-96b9-735c347b29f7
description: Disconnect 元素定义了断开呼叫连接的请求。
ms.openlocfilehash: a00d957927a7a97d12c0d8c0c662956a18529cde
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458451"
---
# <a name="disconnect-um-web-service"></a><span data-ttu-id="b7dd6-103">断开连接（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7dd6-103">Disconnect (UM web service)</span></span>

<span data-ttu-id="b7dd6-104">**Disconnect**元素定义了断开呼叫连接的请求。</span><span class="sxs-lookup"><span data-stu-id="b7dd6-104">The **Disconnect** element defines a request to disconnect a call.</span></span> 
  
- [<span data-ttu-id="b7dd6-105">断开连接（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7dd6-105">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md)
  
```xml
<Disconnect>
  <CallId>   </CallId>
</Disconnect>
```

 <span data-ttu-id="b7dd6-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="b7dd6-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7dd6-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7dd6-107">Attributes and elements</span></span>

<span data-ttu-id="b7dd6-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7dd6-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7dd6-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7dd6-109">Attributes</span></span>

<span data-ttu-id="b7dd6-110">无。</span><span class="sxs-lookup"><span data-stu-id="b7dd6-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7dd6-111">子元素</span><span class="sxs-lookup"><span data-stu-id="b7dd6-111">Child elements</span></span>

|<span data-ttu-id="b7dd6-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7dd6-112">**Element**</span></span>|<span data-ttu-id="b7dd6-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7dd6-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7dd6-114">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7dd6-114">CallId (UM web service)</span></span>](callid-um-web-service.md) <br/> |<span data-ttu-id="b7dd6-115">要断开连接的呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="b7dd6-115">The identifier of the call to disconnect.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b7dd6-116">父元素</span><span class="sxs-lookup"><span data-stu-id="b7dd6-116">Parent elements</span></span>

<span data-ttu-id="b7dd6-117">无。</span><span class="sxs-lookup"><span data-stu-id="b7dd6-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b7dd6-118">文本值</span><span class="sxs-lookup"><span data-stu-id="b7dd6-118">Text value</span></span>

<span data-ttu-id="b7dd6-119">无。</span><span class="sxs-lookup"><span data-stu-id="b7dd6-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7dd6-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7dd6-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7dd6-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7dd6-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7dd6-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7dd6-122">Schema Name</span></span>  <br/> |<span data-ttu-id="b7dd6-123">邮件</span><span class="sxs-lookup"><span data-stu-id="b7dd6-123">Messages</span></span>  <br/> |
|<span data-ttu-id="b7dd6-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7dd6-124">Validation File</span></span>  <br/> |<span data-ttu-id="b7dd6-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b7dd6-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7dd6-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7dd6-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7dd6-127">False</span><span class="sxs-lookup"><span data-stu-id="b7dd6-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7dd6-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7dd6-128">See also</span></span>

- [<span data-ttu-id="b7dd6-129">断开连接操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7dd6-129">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)  
- [<span data-ttu-id="b7dd6-130">PlayOnPhone 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7dd6-130">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md) 
- [<span data-ttu-id="b7dd6-131">PlayOnPhoneGreeting 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7dd6-131">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)  
- [<span data-ttu-id="b7dd6-132">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="b7dd6-132">CallId (UM web service)</span></span>](callid-um-web-service.md)

