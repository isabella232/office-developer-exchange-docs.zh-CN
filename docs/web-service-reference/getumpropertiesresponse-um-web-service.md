---
title: GetUMPropertiesResponse （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMPropertiesResponse
api_type:
- schema
ms.assetid: fcd93ce5-7403-46a9-b46e-56d2ebdd2f79
description: GetUMPropertiesResponse 元素定义对 GetUMProperties 操作（UM web 服务）请求的响应。
ms.openlocfilehash: 3247489a305c694c10764d7a0c6f02b1fad51ebf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459123"
---
# <a name="getumpropertiesresponse-um-web-service"></a><span data-ttu-id="0d416-103">GetUMPropertiesResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d416-103">GetUMPropertiesResponse (UM web service)</span></span>

<span data-ttu-id="0d416-104">**GetUMPropertiesResponse**元素定义对[GETUMPROPERTIES 操作（UM web 服务）](getumproperties-operation-um-web-service.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="0d416-104">The **GetUMPropertiesResponse** element defines a response to a [GetUMProperties operation (UM web service)](getumproperties-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="0d416-105">GetUMPropertiesResponse （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d416-105">GetUMPropertiesResponse (UM web service)</span></span>](getumpropertiesresponse-um-web-service.md)
  
```xml
<GetUMPropertiesResponse>
  <OofStatus/>
  <MissedCallNotificationEnabled/>
  <PlayOnPhoneDialString/>
  <TelephoneAccessNumbers/>
  <TelephoneAccessFolderEmail/>
</GetUMPropertiesResponse>
```

 <span data-ttu-id="0d416-106">**UMProperties**</span><span class="sxs-lookup"><span data-stu-id="0d416-106">**UMProperties**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d416-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0d416-107">Attributes and elements</span></span>

<span data-ttu-id="0d416-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0d416-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d416-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="0d416-109">Attributes</span></span>

<span data-ttu-id="0d416-110">无。</span><span class="sxs-lookup"><span data-stu-id="0d416-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d416-111">子元素</span><span class="sxs-lookup"><span data-stu-id="0d416-111">Child elements</span></span>

|<span data-ttu-id="0d416-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d416-112">**Element**</span></span>|<span data-ttu-id="0d416-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d416-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d416-114">MissedCallNotificationEnabled （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d416-114">MissedCallNotificationEnabled (UM web service)</span></span>](missedcallnotificationenabled-um-web-service.md) <br/> |<span data-ttu-id="0d416-115">指示是否启用未接来电通知。</span><span class="sxs-lookup"><span data-stu-id="0d416-115">Indicates whether missed call notifications are enabled.</span></span>  <br/> |
|[<span data-ttu-id="0d416-116">PlayOnPhoneDialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d416-116">PlayOnPhoneDialString (UM web service)</span></span>](playonphonedialstring-um-web-service.md) <br/> |<span data-ttu-id="0d416-117">包含用于[PlayOnPhone 操作（um web 服务）](playonphone-operation-um-web-service.md)和[PLAYONPHONEGREETING 操作（um web 服务）](playonphonegreeting-operation-um-web-service.md)的默认拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="0d416-117">Contains the default dial string to use for the [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) and [PlayOnPhoneGreeting operation (UM web service)](playonphonegreeting-operation-um-web-service.md).</span></span>  <br/> |
|[<span data-ttu-id="0d416-118">TelephoneAccessNumbers （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d416-118">TelephoneAccessNumbers (UM web service)</span></span>](telephoneaccessnumbers-um-web-service.md) <br/> |<span data-ttu-id="0d416-119">包含用户通过电话访问统一消息时可使用的电话号码列表。</span><span class="sxs-lookup"><span data-stu-id="0d416-119">Contains the list of telephone numbers the user can use to access Unified Messaging via a telephone.</span></span>  <br/> |
|[<span data-ttu-id="0d416-120">TelephoneAccessFolderEmail （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d416-120">TelephoneAccessFolderEmail (UM web service)</span></span>](telephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="0d416-121">包含电子邮件文件夹的标识符，统一消息将通过电话读取邮件。</span><span class="sxs-lookup"><span data-stu-id="0d416-121">Contains the identifier for the e-mail folder from which Unified Messaging will read messages over the telephone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d416-122">父元素</span><span class="sxs-lookup"><span data-stu-id="0d416-122">Parent elements</span></span>

<span data-ttu-id="0d416-123">无。</span><span class="sxs-lookup"><span data-stu-id="0d416-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0d416-124">文本值</span><span class="sxs-lookup"><span data-stu-id="0d416-124">Text value</span></span>

<span data-ttu-id="0d416-125">无。</span><span class="sxs-lookup"><span data-stu-id="0d416-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d416-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="0d416-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d416-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="0d416-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d416-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="0d416-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0d416-129">邮件</span><span class="sxs-lookup"><span data-stu-id="0d416-129">Messages</span></span>  <br/> |
|<span data-ttu-id="0d416-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="0d416-130">Validation File</span></span>  <br/> |<span data-ttu-id="0d416-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0d416-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d416-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="0d416-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d416-133">False</span><span class="sxs-lookup"><span data-stu-id="0d416-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d416-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d416-134">See also</span></span>



[<span data-ttu-id="0d416-135">GetUMProperties 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="0d416-135">GetUMProperties operation (UM web service)</span></span>](getumproperties-operation-um-web-service.md)

