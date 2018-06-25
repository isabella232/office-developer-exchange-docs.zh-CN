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
description: SetPlayOnPhoneDialString 元素定义一个请求设置 PlayOnPhone 操作 （UM web 服务） 的默认拨号字符串和 PlayOnPhoneGreeting 操作 （UM web 服务） 请求。
ms.openlocfilehash: fd82dc6ef0dd90a2318da93191f657005b7a5c87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827450"
---
# <a name="setplayonphonedialstring-um-web-service"></a><span data-ttu-id="cbe1d-103">SetPlayOnPhoneDialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbe1d-103">SetPlayOnPhoneDialString (UM web service)</span></span>

<span data-ttu-id="cbe1d-104">**SetPlayOnPhoneDialString**元素定义一个请求设置[PlayOnPhone 操作 （UM web 服务）](playonphone-operation-um-web-service.md)和[PlayOnPhoneGreeting 操作 （UM web 服务）](playonphonegreeting-operation-um-web-service.md)请求的默认拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="cbe1d-104">The **SetPlayOnPhoneDialString** element defines a request to set the default dial string for [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md) requests.</span></span> 
  
[<span data-ttu-id="cbe1d-105">SetPlayOnPhoneDialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbe1d-105">SetPlayOnPhoneDialString (UM web service)</span></span>](setplayonphonedialstring-um-web-service.md)
  
```xml
<SetPlayOnPhoneDialString>
  <dialString>   </dialString>
</SetPlayOnPhoneDialString>
```

 <span data-ttu-id="cbe1d-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="cbe1d-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cbe1d-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cbe1d-107">Attributes and elements</span></span>

<span data-ttu-id="cbe1d-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cbe1d-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cbe1d-109">属性</span><span class="sxs-lookup"><span data-stu-id="cbe1d-109">Attributes</span></span>

<span data-ttu-id="cbe1d-110">无。</span><span class="sxs-lookup"><span data-stu-id="cbe1d-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cbe1d-111">子元素</span><span class="sxs-lookup"><span data-stu-id="cbe1d-111">Child elements</span></span>

|<span data-ttu-id="cbe1d-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="cbe1d-112">**Element**</span></span>|<span data-ttu-id="cbe1d-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="cbe1d-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cbe1d-114">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbe1d-114">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="cbe1d-115">要将设置为默认的拨号串的电话号码。</span><span class="sxs-lookup"><span data-stu-id="cbe1d-115">The telephone number to set as the default dial string.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cbe1d-116">父元素</span><span class="sxs-lookup"><span data-stu-id="cbe1d-116">Parent elements</span></span>

<span data-ttu-id="cbe1d-117">无。</span><span class="sxs-lookup"><span data-stu-id="cbe1d-117">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="cbe1d-118">文本值</span><span class="sxs-lookup"><span data-stu-id="cbe1d-118">Text value</span></span>

<span data-ttu-id="cbe1d-119">无。</span><span class="sxs-lookup"><span data-stu-id="cbe1d-119">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cbe1d-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="cbe1d-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cbe1d-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="cbe1d-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cbe1d-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="cbe1d-122">Schema Name</span></span>  <br/> |<span data-ttu-id="cbe1d-123">邮件</span><span class="sxs-lookup"><span data-stu-id="cbe1d-123">Messages</span></span>  <br/> |
|<span data-ttu-id="cbe1d-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="cbe1d-124">Validation File</span></span>  <br/> |<span data-ttu-id="cbe1d-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cbe1d-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cbe1d-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="cbe1d-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="cbe1d-127">False</span><span class="sxs-lookup"><span data-stu-id="cbe1d-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbe1d-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cbe1d-128">See also</span></span>



[<span data-ttu-id="cbe1d-129">SetPlayOnPhoneDialString 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="cbe1d-129">SetPlayOnPhoneDialString operation (UM web service)</span></span>](setplayonphonedialstring-operation-um-web-service.md)

