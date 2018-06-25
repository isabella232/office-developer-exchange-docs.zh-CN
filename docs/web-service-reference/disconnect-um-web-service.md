---
title: 断开连接 （UM web 服务）
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
description: 断开元素定义要断开呼叫的请求。
ms.openlocfilehash: 764532bdadd69caaa68406c84277197def3160af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753919"
---
# <a name="disconnect-um-web-service"></a><span data-ttu-id="5d84b-103">断开连接 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d84b-103">Disconnect (UM web service)</span></span>

<span data-ttu-id="5d84b-104">**断开**元素定义要断开呼叫的请求。</span><span class="sxs-lookup"><span data-stu-id="5d84b-104">The **Disconnect** element defines a request to disconnect a call.</span></span> 
  
- [<span data-ttu-id="5d84b-105">断开连接 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d84b-105">Disconnect (UM web service)</span></span>](disconnect-um-web-service.md)
  
```xml
<Disconnect>
  <CallId>   </CallId>
</Disconnect>
```

 <span data-ttu-id="5d84b-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="5d84b-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d84b-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5d84b-107">Attributes and elements</span></span>

<span data-ttu-id="5d84b-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5d84b-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d84b-109">属性</span><span class="sxs-lookup"><span data-stu-id="5d84b-109">Attributes</span></span>

<span data-ttu-id="5d84b-110">无。</span><span class="sxs-lookup"><span data-stu-id="5d84b-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d84b-111">子元素</span><span class="sxs-lookup"><span data-stu-id="5d84b-111">Child elements</span></span>

|<span data-ttu-id="5d84b-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d84b-112">**Element**</span></span>|<span data-ttu-id="5d84b-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d84b-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d84b-114">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d84b-114">CallId (UM web service)</span></span>](callid-um-web-service.md) <br/> |<span data-ttu-id="5d84b-115">要断开连接的呼叫的标识符。</span><span class="sxs-lookup"><span data-stu-id="5d84b-115">The identifier of the call to disconnect.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d84b-116">父元素</span><span class="sxs-lookup"><span data-stu-id="5d84b-116">Parent elements</span></span>

<span data-ttu-id="5d84b-117">无。</span><span class="sxs-lookup"><span data-stu-id="5d84b-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5d84b-118">文本值</span><span class="sxs-lookup"><span data-stu-id="5d84b-118">Text value</span></span>

<span data-ttu-id="5d84b-119">无。</span><span class="sxs-lookup"><span data-stu-id="5d84b-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d84b-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="5d84b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d84b-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="5d84b-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5d84b-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="5d84b-122">Schema Name</span></span>  <br/> |<span data-ttu-id="5d84b-123">邮件</span><span class="sxs-lookup"><span data-stu-id="5d84b-123">Messages</span></span>  <br/> |
|<span data-ttu-id="5d84b-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="5d84b-124">Validation File</span></span>  <br/> |<span data-ttu-id="5d84b-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5d84b-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5d84b-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="5d84b-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d84b-127">False</span><span class="sxs-lookup"><span data-stu-id="5d84b-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d84b-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d84b-128">See also</span></span>

- [<span data-ttu-id="5d84b-129">断开连接操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d84b-129">Disconnect operation (UM web service)</span></span>](disconnect-operation-um-web-service.md)  
- [<span data-ttu-id="5d84b-130">PlayOnPhone 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d84b-130">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md) 
- [<span data-ttu-id="5d84b-131">PlayOnPhoneGreeting 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d84b-131">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)  
- [<span data-ttu-id="5d84b-132">CallId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d84b-132">CallId (UM web service)</span></span>](callid-um-web-service.md)

