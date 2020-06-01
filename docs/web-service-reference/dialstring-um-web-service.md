---
title: dialString （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- dialString
api_type:
- schema
ms.assetid: d1e3cd23-48fe-4ebc-a5c5-2226d223f800
description: DialString 元素包含要拨打的电话号码的值。
ms.openlocfilehash: 028ea789efabf49a64bc1d5022d9eb2d8df61c51
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467821"
---
# <a name="dialstring-um-web-service"></a><span data-ttu-id="0be23-103">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-103">dialString (UM web service)</span></span>

<span data-ttu-id="0be23-104">**DialString**元素包含要拨打的电话号码的值。</span><span class="sxs-lookup"><span data-stu-id="0be23-104">The **dialString** element contains the value for the telephone number to dial.</span></span> 
  
- [<span data-ttu-id="0be23-105">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-105">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md) 
- [<span data-ttu-id="0be23-106">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-106">dialString (UM web service)</span></span>](dialstring-um-web-service.md) 
- [<span data-ttu-id="0be23-107">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-107">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md) 
- [<span data-ttu-id="0be23-108">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-108">dialString (UM web service)</span></span>](dialstring-um-web-service.md)
  
```xml
<dialString/>
```

 <span data-ttu-id="0be23-109">**string**</span><span class="sxs-lookup"><span data-stu-id="0be23-109">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0be23-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0be23-110">Attributes and elements</span></span>

<span data-ttu-id="0be23-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0be23-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0be23-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="0be23-112">Attributes</span></span>

<span data-ttu-id="0be23-113">无。</span><span class="sxs-lookup"><span data-stu-id="0be23-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0be23-114">子元素</span><span class="sxs-lookup"><span data-stu-id="0be23-114">Child elements</span></span>

<span data-ttu-id="0be23-115">无。</span><span class="sxs-lookup"><span data-stu-id="0be23-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0be23-116">父元素</span><span class="sxs-lookup"><span data-stu-id="0be23-116">Parent elements</span></span>

|<span data-ttu-id="0be23-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="0be23-117">**Element**</span></span>|<span data-ttu-id="0be23-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="0be23-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0be23-119">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-119">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md) <br/> |<span data-ttu-id="0be23-120">定义在电话上播放邮件的请求。</span><span class="sxs-lookup"><span data-stu-id="0be23-120">Defines a request to play a message on a telephone.</span></span>  <br/> |
|[<span data-ttu-id="0be23-121">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-121">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md) <br/> |<span data-ttu-id="0be23-122">定义在电话上播放问候语的请求。</span><span class="sxs-lookup"><span data-stu-id="0be23-122">Defines a request to play a greeting on a telephone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0be23-123">文本值</span><span class="sxs-lookup"><span data-stu-id="0be23-123">Text value</span></span>

<span data-ttu-id="0be23-124">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="0be23-124">A text value is required.</span></span> <span data-ttu-id="0be23-125">文本值必须包含有效的拨号号码。</span><span class="sxs-lookup"><span data-stu-id="0be23-125">The text value must contain a valid dialing number.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0be23-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="0be23-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0be23-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="0be23-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0be23-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="0be23-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0be23-129">邮件</span><span class="sxs-lookup"><span data-stu-id="0be23-129">Messages</span></span>  <br/> |
|<span data-ttu-id="0be23-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="0be23-130">Validation File</span></span>  <br/> |<span data-ttu-id="0be23-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0be23-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0be23-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="0be23-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0be23-133">False</span><span class="sxs-lookup"><span data-stu-id="0be23-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0be23-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0be23-134">See also</span></span>

- [<span data-ttu-id="0be23-135">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-135">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md)  
- [<span data-ttu-id="0be23-136">PlayOnPhone 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-136">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)  
- [<span data-ttu-id="0be23-137">PlayOnPhoneGreeting （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-137">PlayOnPhoneGreeting (UM web service)</span></span>](playonphonegreeting-um-web-service.md)  
- [<span data-ttu-id="0be23-138">PlayOnPhoneGreeting 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0be23-138">PlayOnPhoneGreeting operation (UM web service)</span></span>](playonphonegreeting-operation-um-web-service.md)

