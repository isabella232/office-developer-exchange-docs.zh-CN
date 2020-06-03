---
title: UserSettings （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: ac3b827c-2e46-49ef-8c5a-f88084c0a12c
description: UserSettings 元素表示用户设置的集合。
ms.openlocfilehash: 0e1627d4ef42db4e3bd2f4d841bea29fcf947a82
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530280"
---
# <a name="usersettings-soap"></a><span data-ttu-id="e8a33-103">UserSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="e8a33-103">UserSettings (SOAP)</span></span>

<span data-ttu-id="e8a33-104">**UserSettings**元素表示用户设置的集合。</span><span class="sxs-lookup"><span data-stu-id="e8a33-104">The **UserSettings** element represents a collection of user settings.</span></span> 
  
```XML
<UserSettings>
    <UserSetting/>
</UserSettings>
```

 <span data-ttu-id="e8a33-105">**UserSettings**</span><span class="sxs-lookup"><span data-stu-id="e8a33-105">**UserSettings**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8a33-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e8a33-106">Attributes and elements</span></span>

<span data-ttu-id="e8a33-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e8a33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8a33-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e8a33-108">Attributes</span></span>

<span data-ttu-id="e8a33-109">无。</span><span class="sxs-lookup"><span data-stu-id="e8a33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8a33-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e8a33-110">Child elements</span></span>

|<span data-ttu-id="e8a33-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e8a33-111">**Element**</span></span>|<span data-ttu-id="e8a33-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e8a33-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8a33-113">UserSetting （SOAP）</span><span class="sxs-lookup"><span data-stu-id="e8a33-113">UserSetting (SOAP)</span></span>](usersetting-soap.md) <br/> |<span data-ttu-id="e8a33-114">代表单个用户设置。</span><span class="sxs-lookup"><span data-stu-id="e8a33-114">Represents a single user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e8a33-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e8a33-115">Parent elements</span></span>

|<span data-ttu-id="e8a33-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e8a33-116">**Element**</span></span>|<span data-ttu-id="e8a33-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e8a33-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8a33-118">UserResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="e8a33-118">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="e8a33-119">表示对单个用户的 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e8a33-119">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e8a33-120">文本值</span><span class="sxs-lookup"><span data-stu-id="e8a33-120">Text value</span></span>

<span data-ttu-id="e8a33-121">无。</span><span class="sxs-lookup"><span data-stu-id="e8a33-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8a33-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="e8a33-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8a33-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="e8a33-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="e8a33-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="e8a33-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e8a33-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="e8a33-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="e8a33-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="e8a33-126">Validation File</span></span>  <br/> |<span data-ttu-id="e8a33-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e8a33-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8a33-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="e8a33-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="e8a33-129">True</span><span class="sxs-lookup"><span data-stu-id="e8a33-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e8a33-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8a33-130">See also</span></span>



[<span data-ttu-id="e8a33-131">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="e8a33-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

