---
title: UserSettingErrors (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a9b94bae-cab9-412d-a811-801e849ed6c5
description: UserSettingErrors 元素表示不会返回的设置的信息的集合。
ms.openlocfilehash: 4477c30145d2cb187a4309d018512537af974ee8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838496"
---
# <a name="usersettingerrors-soap"></a><span data-ttu-id="cf2df-103">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf2df-103">UserSettingErrors (SOAP)</span></span>

<span data-ttu-id="cf2df-104">**UserSettingErrors**元素表示不会返回的设置的信息的集合。</span><span class="sxs-lookup"><span data-stu-id="cf2df-104">The **UserSettingErrors** element represents a collection of information about settings that could not be returned.</span></span> 
  
```XML
<UserSettingErrors>
    <UserSettingError/>
</UserSettingErrors>
```

 <span data-ttu-id="cf2df-105">**UserSettingErrors**</span><span class="sxs-lookup"><span data-stu-id="cf2df-105">**UserSettingErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cf2df-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cf2df-106">Attributes and elements</span></span>

<span data-ttu-id="cf2df-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cf2df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf2df-108">属性</span><span class="sxs-lookup"><span data-stu-id="cf2df-108">Attributes</span></span>

<span data-ttu-id="cf2df-109">无。</span><span class="sxs-lookup"><span data-stu-id="cf2df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cf2df-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cf2df-110">Child elements</span></span>

|<span data-ttu-id="cf2df-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf2df-111">**Element**</span></span>|<span data-ttu-id="cf2df-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf2df-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf2df-113">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf2df-113">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="cf2df-114">代表在检索用户设置时返回的错误。</span><span class="sxs-lookup"><span data-stu-id="cf2df-114">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cf2df-115">父元素</span><span class="sxs-lookup"><span data-stu-id="cf2df-115">Parent elements</span></span>

|<span data-ttu-id="cf2df-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="cf2df-116">**Element**</span></span>|<span data-ttu-id="cf2df-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="cf2df-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cf2df-118">用户回音 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="cf2df-118">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="cf2df-119">代表对单个用户 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="cf2df-119">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cf2df-120">文本值</span><span class="sxs-lookup"><span data-stu-id="cf2df-120">Text value</span></span>

<span data-ttu-id="cf2df-121">无。</span><span class="sxs-lookup"><span data-stu-id="cf2df-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf2df-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="cf2df-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf2df-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="cf2df-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="cf2df-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="cf2df-124">Schema Name</span></span>  <br/> |<span data-ttu-id="cf2df-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="cf2df-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="cf2df-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="cf2df-126">Validation File</span></span>  <br/> |<span data-ttu-id="cf2df-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="cf2df-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="cf2df-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="cf2df-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="cf2df-129">True</span><span class="sxs-lookup"><span data-stu-id="cf2df-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf2df-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cf2df-130">See also</span></span>



[<span data-ttu-id="cf2df-131">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="cf2df-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

