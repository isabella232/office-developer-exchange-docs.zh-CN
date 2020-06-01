---
title: UserSettingError （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: abb175c5-4f38-4dcc-81e3-b511686862eb
description: UserSettingError 元素表示因尝试获取用户设置而返回的错误。
ms.openlocfilehash: 61603038ce93780f690d72226b1356b239d2002d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468605"
---
# <a name="usersettingerror-soap"></a><span data-ttu-id="14927-103">UserSettingError （SOAP）</span><span class="sxs-lookup"><span data-stu-id="14927-103">UserSettingError (SOAP)</span></span>

<span data-ttu-id="14927-104">**UserSettingError**元素表示因尝试获取用户设置而返回的错误。</span><span class="sxs-lookup"><span data-stu-id="14927-104">The **UserSettingError** element represents an error that is returned as a result of an attempt to get a user setting.</span></span> 
  
```XML
<UserSettingError>
    <ErrorCode/>
    <ErrorMessage/>
    <SettingName/>
</UserSettingError>
```

 <span data-ttu-id="14927-105">**UserSettingError**</span><span class="sxs-lookup"><span data-stu-id="14927-105">**UserSettingError**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="14927-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="14927-106">Attributes and elements</span></span>

<span data-ttu-id="14927-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="14927-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14927-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="14927-108">Attributes</span></span>

<span data-ttu-id="14927-109">无。</span><span class="sxs-lookup"><span data-stu-id="14927-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="14927-110">子元素</span><span class="sxs-lookup"><span data-stu-id="14927-110">Child elements</span></span>

|<span data-ttu-id="14927-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="14927-111">**Element**</span></span>|<span data-ttu-id="14927-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="14927-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14927-113">ErrorCode （SOAP）</span><span class="sxs-lookup"><span data-stu-id="14927-113">ErrorCode (SOAP)</span></span>](errorcode-soap.md) <br/> |<span data-ttu-id="14927-114">表示自动发现服务返回的错误代码。</span><span class="sxs-lookup"><span data-stu-id="14927-114">Represents an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="14927-115">ErrorMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="14927-115">ErrorMessage (SOAP)</span></span>](errormessage-soap.md) <br/> |<span data-ttu-id="14927-116">Respresents 与自动发现服务返回的错误代码相关联的消息。</span><span class="sxs-lookup"><span data-stu-id="14927-116">Respresents a message associated with an error code that is returned by the Autodiscover service.</span></span>  <br/> |
|[<span data-ttu-id="14927-117">SettingName （SOAP）</span><span class="sxs-lookup"><span data-stu-id="14927-117">SettingName (SOAP)</span></span>](settingname-soap.md) <br/> |<span data-ttu-id="14927-118">代表用户设置的名称。</span><span class="sxs-lookup"><span data-stu-id="14927-118">Represents the name of a user setting.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="14927-119">父元素</span><span class="sxs-lookup"><span data-stu-id="14927-119">Parent elements</span></span>

|<span data-ttu-id="14927-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="14927-120">**Element**</span></span>|<span data-ttu-id="14927-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="14927-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="14927-122">UserSettingErrors （SOAP）</span><span class="sxs-lookup"><span data-stu-id="14927-122">UserSettingErrors (SOAP)</span></span>](usersettingerrors-soap.md) <br/> |<span data-ttu-id="14927-123">表示有关无法返回的设置的信息的集合。</span><span class="sxs-lookup"><span data-stu-id="14927-123">Represents a collection of information about settings that could not be returned.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="14927-124">文本值</span><span class="sxs-lookup"><span data-stu-id="14927-124">Text value</span></span>

<span data-ttu-id="14927-125">无。</span><span class="sxs-lookup"><span data-stu-id="14927-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14927-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="14927-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14927-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="14927-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="14927-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="14927-128">Schema Name</span></span>  <br/> |<span data-ttu-id="14927-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="14927-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="14927-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="14927-130">Validation File</span></span>  <br/> |<span data-ttu-id="14927-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="14927-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="14927-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="14927-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="14927-133">True</span><span class="sxs-lookup"><span data-stu-id="14927-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14927-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="14927-134">See also</span></span>



[<span data-ttu-id="14927-135">Exchange 2013 的 SOAP 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="14927-135">SOAP Autodiscover XML elements for Exchange 2013</span></span>](soap-autodiscover-xml-elements-for-exchange-2013.md)

