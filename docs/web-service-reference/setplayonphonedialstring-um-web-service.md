---
title: SetPlayOnPhoneDialString （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: 513a5072-c3ac-405f-98c2-0ab982d0a360
description: SetPlayOnPhoneDialString 元素定义一个请求，用于设置 PlayOnPhone 操作（UM web 服务）和 PlayOnPhoneGreeting 操作（UM web 服务）请求的默认拨号字符串。
ms.openlocfilehash: 40021e9dedafb5fafda91bf3612d8a6485dae8e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458626"
---
# <a name="setplayonphonedialstring-um-web-service"></a><span data-ttu-id="e67dd-103">SetPlayOnPhoneDialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e67dd-103">SetPlayOnPhoneDialString (UM web service)</span></span>

<span data-ttu-id="e67dd-104">**SetPlayOnPhoneDialString**元素定义一个请求，用于设置[PLAYONPHONE 操作（um web 服务）](playonphone-operation-um-web-service.md)和[PlayOnPhoneGreeting 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)请求的默认拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="e67dd-104">The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests.</span></span> 
  
[<span data-ttu-id="e67dd-105">SetPlayOnPhoneDialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e67dd-105">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 <span data-ttu-id="e67dd-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="e67dd-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e67dd-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e67dd-107">Attributes and elements</span></span>

<span data-ttu-id="e67dd-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e67dd-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e67dd-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="e67dd-109">Attributes</span></span>

<span data-ttu-id="e67dd-110">无。</span><span class="sxs-lookup"><span data-stu-id="e67dd-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e67dd-111">子元素</span><span class="sxs-lookup"><span data-stu-id="e67dd-111">Child elements</span></span>

|<span data-ttu-id="e67dd-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="e67dd-112">**Element**</span></span>|<span data-ttu-id="e67dd-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="e67dd-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e67dd-114">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e67dd-114">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="e67dd-115">要设置为默认拨号字符串的电话号码。</span><span class="sxs-lookup"><span data-stu-id="e67dd-115">The telephone number to set as the default dial string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e67dd-116">父元素</span><span class="sxs-lookup"><span data-stu-id="e67dd-116">Parent elements</span></span>

<span data-ttu-id="e67dd-117">无。</span><span class="sxs-lookup"><span data-stu-id="e67dd-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e67dd-118">文本值</span><span class="sxs-lookup"><span data-stu-id="e67dd-118">Text value</span></span>

<span data-ttu-id="e67dd-119">无。</span><span class="sxs-lookup"><span data-stu-id="e67dd-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e67dd-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="e67dd-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e67dd-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="e67dd-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e67dd-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="e67dd-122">Schema Name</span></span>  <br/> |<span data-ttu-id="e67dd-123">邮件</span><span class="sxs-lookup"><span data-stu-id="e67dd-123">Messages</span></span>  <br/> |
|<span data-ttu-id="e67dd-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="e67dd-124">Validation File</span></span>  <br/> |<span data-ttu-id="e67dd-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e67dd-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e67dd-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="e67dd-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="e67dd-127">False</span><span class="sxs-lookup"><span data-stu-id="e67dd-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e67dd-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e67dd-128">See also</span></span>



[<span data-ttu-id="e67dd-129">SetPlayOnPhoneDialString 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="e67dd-129">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)

