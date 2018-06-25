---
title: UserSettingError (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: abb175c5-4f38-4dcc-81e3-b511686862eb
description: UserSettingError 元素表示由于尝试获取用户设置返回的错误。
ms.openlocfilehash: 886e0be0aa900ce3a00902c21cc115e866d0cd99
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838490"
---
# <a name="usersettingerror-soap"></a><span data-ttu-id="b3ed5-103">UserSettingError (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b3ed5-103">UserSettingError (SOAP)</span></span>

<span data-ttu-id="b3ed5-104">**UserSettingError**元素表示由于尝试获取用户设置返回的错误。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-104">The **UserSettingError** element represents an error that is returned as a result of an attempt to get a user setting.</span></span> 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 <span data-ttu-id="b3ed5-105">**UserSettingError**</span><span class="sxs-lookup"><span data-stu-id="b3ed5-105">**UserSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b3ed5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b3ed5-106">Attributes and elements</span></span>

<span data-ttu-id="b3ed5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b3ed5-108">属性</span><span class="sxs-lookup"><span data-stu-id="b3ed5-108">Attributes</span></span>

<span data-ttu-id="b3ed5-109">无。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b3ed5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b3ed5-110">Child elements</span></span>

|<span data-ttu-id="b3ed5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b3ed5-111">**Element**</span></span>|<span data-ttu-id="b3ed5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b3ed5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3ed5-113">ErrorCode (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b3ed5-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="b3ed5-114">代表由自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b3ed5-115">ErrorMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b3ed5-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="b3ed5-116">表示与错误代码返回的自动发现服务关联的消息。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-116">Respresents a message associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="b3ed5-117">SettingName (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b3ed5-117">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="b3ed5-118">代表用户设置的名称。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-118">Represents the name of a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b3ed5-119">父元素</span><span class="sxs-lookup"><span data-stu-id="b3ed5-119">Parent elements</span></span>

|<span data-ttu-id="b3ed5-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="b3ed5-120">**Element**</span></span>|<span data-ttu-id="b3ed5-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="b3ed5-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b3ed5-122">UserSettingErrors (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b3ed5-122">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="b3ed5-123">表示不会返回的设置的信息的集合。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-123">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b3ed5-124">文本值</span><span class="sxs-lookup"><span data-stu-id="b3ed5-124">Text value</span></span>

<span data-ttu-id="b3ed5-125">无。</span><span class="sxs-lookup"><span data-stu-id="b3ed5-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b3ed5-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="b3ed5-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b3ed5-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="b3ed5-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b3ed5-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="b3ed5-128">Schema Name</span></span>  <br/> |<span data-ttu-id="b3ed5-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="b3ed5-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b3ed5-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="b3ed5-130">Validation File</span></span>  <br/> |<span data-ttu-id="b3ed5-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b3ed5-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b3ed5-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="b3ed5-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="b3ed5-133">True</span><span class="sxs-lookup"><span data-stu-id="b3ed5-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b3ed5-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b3ed5-134">See also</span></span>



[<span data-ttu-id="b3ed5-135">SOAP Exchange 2013 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="b3ed5-135">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

