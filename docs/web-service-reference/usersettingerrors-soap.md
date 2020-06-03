---
title: UserSettingErrors （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a9b94bae-cab9-412d-a811-801e849ed6c5
description: UserSettingErrors 元素表示无法返回的设置的相关信息的集合。
ms.openlocfilehash: a6cc0fe114bd511dc4136532986b552c28b0d5c2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467121"
---
# <a name="usersettingerrors-soap"></a><span data-ttu-id="ee22b-103">UserSettingErrors （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ee22b-103">UserSettingErrors (SOAP)</span></span>

<span data-ttu-id="ee22b-104">**UserSettingErrors**元素表示无法返回的设置的相关信息的集合。</span><span class="sxs-lookup"><span data-stu-id="ee22b-104">The **UserSettingErrors** element represents a collection of information about settings that could not be returned.</span></span> 
  
```XML
<UserSettingErrors>
    <UserSettingError/>
</UserSettingErrors>
```

 <span data-ttu-id="ee22b-105">**UserSettingErrors**</span><span class="sxs-lookup"><span data-stu-id="ee22b-105">**UserSettingErrors**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ee22b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ee22b-106">Attributes and elements</span></span>

<span data-ttu-id="ee22b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ee22b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ee22b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ee22b-108">Attributes</span></span>

<span data-ttu-id="ee22b-109">无。</span><span class="sxs-lookup"><span data-stu-id="ee22b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ee22b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ee22b-110">Child elements</span></span>

|<span data-ttu-id="ee22b-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ee22b-111">**Element**</span></span>|<span data-ttu-id="ee22b-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ee22b-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee22b-113">UserSettingError （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ee22b-113">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="ee22b-114">表示检索用户设置时返回的错误。</span><span class="sxs-lookup"><span data-stu-id="ee22b-114">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ee22b-115">父元素</span><span class="sxs-lookup"><span data-stu-id="ee22b-115">Parent elements</span></span>

|<span data-ttu-id="ee22b-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="ee22b-116">**Element**</span></span>|<span data-ttu-id="ee22b-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="ee22b-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ee22b-118">UserResponse （SOAP）</span><span class="sxs-lookup"><span data-stu-id="ee22b-118">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="ee22b-119">表示对单个用户的 GetUserSettings 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ee22b-119">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ee22b-120">文本值</span><span class="sxs-lookup"><span data-stu-id="ee22b-120">Text value</span></span>

<span data-ttu-id="ee22b-121">无。</span><span class="sxs-lookup"><span data-stu-id="ee22b-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ee22b-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="ee22b-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee22b-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="ee22b-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="ee22b-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="ee22b-124">Schema Name</span></span>  <br/> |<span data-ttu-id="ee22b-125">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="ee22b-125">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="ee22b-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="ee22b-126">Validation File</span></span>  <br/> |<span data-ttu-id="ee22b-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ee22b-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ee22b-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="ee22b-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="ee22b-129">True</span><span class="sxs-lookup"><span data-stu-id="ee22b-129">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ee22b-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ee22b-130">See also</span></span>



[<span data-ttu-id="ee22b-131">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="ee22b-131">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

