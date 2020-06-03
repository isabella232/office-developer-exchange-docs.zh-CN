---
title: UserConfigurationProperties
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UserConfigurationProperties
api_type:
- schema
ms.assetid: c143a6ec-62ad-4d48-b844-b1ad88054bc1
description: UserConfigurationProperties 元素指定要在 GetUserConfiguration 操作中获取的属性类型。
ms.openlocfilehash: af6bee64516a7410d96ecc7581e8e819f550ddc1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466491"
---
# <a name="userconfigurationproperties"></a><span data-ttu-id="4be69-103">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="4be69-103">UserConfigurationProperties</span></span>

<span data-ttu-id="4be69-104">**UserConfigurationProperties**元素指定要在 GetUserConfiguration 操作中获取的属性类型。</span><span class="sxs-lookup"><span data-stu-id="4be69-104">The **UserConfigurationProperties** element specifies the property types to get in a GetUserConfiguration operation.</span></span> 
  
```xml
<UserConfigurationProperties>Id | Dictionary | XmlData | BinaryData | All</UserConfigurationProperties>
```

 <span data-ttu-id="4be69-105">**UserConfigurationPropertyType**</span><span class="sxs-lookup"><span data-stu-id="4be69-105">**UserConfigurationPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4be69-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4be69-106">Attributes and elements</span></span>

<span data-ttu-id="4be69-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4be69-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4be69-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4be69-108">Attributes</span></span>

<span data-ttu-id="4be69-109">无。</span><span class="sxs-lookup"><span data-stu-id="4be69-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4be69-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4be69-110">Child elements</span></span>

<span data-ttu-id="4be69-111">无。</span><span class="sxs-lookup"><span data-stu-id="4be69-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4be69-112">父元素</span><span class="sxs-lookup"><span data-stu-id="4be69-112">Parent elements</span></span>

|<span data-ttu-id="4be69-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="4be69-113">**Element**</span></span>|<span data-ttu-id="4be69-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="4be69-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4be69-115">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="4be69-115">GetUserConfiguration</span></span>](getuserconfiguration.md) <br/> |<span data-ttu-id="4be69-116">指定获取用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="4be69-116">Specifies a request to get a user configuration object.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4be69-117">文本值</span><span class="sxs-lookup"><span data-stu-id="4be69-117">Text value</span></span>

<span data-ttu-id="4be69-118">下表列出了**UserConfigurationProperties**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="4be69-118">The following table lists the possible values for the **UserConfigurationProperties** element.</span></span> 
  
|<span data-ttu-id="4be69-119">**值**</span><span class="sxs-lookup"><span data-stu-id="4be69-119">**Value**</span></span>|<span data-ttu-id="4be69-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="4be69-120">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4be69-121">Id</span><span class="sxs-lookup"><span data-stu-id="4be69-121">Id</span></span>  <br/> |<span data-ttu-id="4be69-122">指定标识符属性。</span><span class="sxs-lookup"><span data-stu-id="4be69-122">Specifies the identifier property.</span></span>  <br/> |
|<span data-ttu-id="4be69-123">Dictionary</span><span class="sxs-lookup"><span data-stu-id="4be69-123">Dictionary</span></span>  <br/> |<span data-ttu-id="4be69-124">指定字典属性类型。</span><span class="sxs-lookup"><span data-stu-id="4be69-124">Specifies dictionary property types.</span></span>  <br/> |
|<span data-ttu-id="4be69-125">XmlData</span><span class="sxs-lookup"><span data-stu-id="4be69-125">XmlData</span></span>  <br/> |<span data-ttu-id="4be69-126">指定 XML 数据属性类型。</span><span class="sxs-lookup"><span data-stu-id="4be69-126">Specifies XML data property types.</span></span>  <br/> |
|<span data-ttu-id="4be69-127">BinaryData</span><span class="sxs-lookup"><span data-stu-id="4be69-127">BinaryData</span></span>  <br/> |<span data-ttu-id="4be69-128">指定二进制数据属性类型。</span><span class="sxs-lookup"><span data-stu-id="4be69-128">Specifies binary data property types.</span></span>  <br/> |
|<span data-ttu-id="4be69-129">所有</span><span class="sxs-lookup"><span data-stu-id="4be69-129">All</span></span>  <br/> |<span data-ttu-id="4be69-130">指定标识符、字典、XML 数据和二进制数据属性类型。</span><span class="sxs-lookup"><span data-stu-id="4be69-130">Specifies the identifier, dictionary, XML data, and binary data property types.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4be69-131">说明</span><span class="sxs-lookup"><span data-stu-id="4be69-131">Remarks</span></span>

<span data-ttu-id="4be69-132">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4be69-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4be69-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="4be69-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4be69-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="4be69-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4be69-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="4be69-135">Schema Name</span></span>  <br/> |<span data-ttu-id="4be69-136">消息架构</span><span class="sxs-lookup"><span data-stu-id="4be69-136">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4be69-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="4be69-137">Validation File</span></span>  <br/> |<span data-ttu-id="4be69-138">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4be69-138">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4be69-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="4be69-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="4be69-140">False</span><span class="sxs-lookup"><span data-stu-id="4be69-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4be69-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4be69-141">See also</span></span>



- [<span data-ttu-id="4be69-142">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4be69-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

