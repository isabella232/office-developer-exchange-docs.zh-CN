---
title: GetUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfiguration
api_type:
- schema
ms.assetid: 4044c0a1-cd88-41ae-9cc4-a7cf2b279094
description: GetUserConfiguration 元素表示获取用户配置对象的请求。
ms.openlocfilehash: 46a2a5ebbabfc038692a5de83e0a960e05295061
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457709"
---
# <a name="getuserconfiguration"></a><span data-ttu-id="e3f71-103">GetUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="e3f71-103">GetUserConfiguration</span></span>

<span data-ttu-id="e3f71-104">**GetUserConfiguration**元素表示获取用户配置对象的请求。</span><span class="sxs-lookup"><span data-stu-id="e3f71-104">The **GetUserConfiguration** element represent a request to get a user configuration object.</span></span> 
  
```XML
<GetUserConfiguration>
   <UserConfigurationName/>
   <UserConfigurationProperties/>
</GetUserConfiguration>
```

 <span data-ttu-id="e3f71-105">**GetUserConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="e3f71-105">**GetUserConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3f71-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e3f71-106">Attributes and elements</span></span>

<span data-ttu-id="e3f71-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e3f71-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3f71-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e3f71-108">Attributes</span></span>

<span data-ttu-id="e3f71-109">无。</span><span class="sxs-lookup"><span data-stu-id="e3f71-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3f71-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e3f71-110">Child elements</span></span>

|<span data-ttu-id="e3f71-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e3f71-111">**Element**</span></span>|<span data-ttu-id="e3f71-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e3f71-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3f71-113">UserConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e3f71-113">UserConfigurationName</span></span>](userconfigurationname.md) <br/> |<span data-ttu-id="e3f71-114">表示用户配置对象的名称。</span><span class="sxs-lookup"><span data-stu-id="e3f71-114">Represents the name of a user configuration object.</span></span> <span data-ttu-id="e3f71-115">GetUserConfiguration 请求中必须存在此元素。</span><span class="sxs-lookup"><span data-stu-id="e3f71-115">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
|[<span data-ttu-id="e3f71-116">UserConfigurationProperties</span><span class="sxs-lookup"><span data-stu-id="e3f71-116">UserConfigurationProperties</span></span>](userconfigurationproperties.md) <br/> |<span data-ttu-id="e3f71-117">指定要返回的用户配置属性类型。</span><span class="sxs-lookup"><span data-stu-id="e3f71-117">Specifies the user configuration property types to return.</span></span> <span data-ttu-id="e3f71-118">GetUserConfiguration 请求中必须存在此元素。</span><span class="sxs-lookup"><span data-stu-id="e3f71-118">This element must be present in a GetUserConfiguration request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e3f71-119">父元素</span><span class="sxs-lookup"><span data-stu-id="e3f71-119">Parent elements</span></span>

<span data-ttu-id="e3f71-120">无。</span><span class="sxs-lookup"><span data-stu-id="e3f71-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e3f71-121">文本值</span><span class="sxs-lookup"><span data-stu-id="e3f71-121">Text value</span></span>

<span data-ttu-id="e3f71-122">无。</span><span class="sxs-lookup"><span data-stu-id="e3f71-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3f71-123">说明</span><span class="sxs-lookup"><span data-stu-id="e3f71-123">Remarks</span></span>

<span data-ttu-id="e3f71-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e3f71-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3f71-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="e3f71-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3f71-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="e3f71-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e3f71-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="e3f71-127">Schema Name</span></span>  <br/> |<span data-ttu-id="e3f71-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="e3f71-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e3f71-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="e3f71-129">Validation File</span></span>  <br/> |<span data-ttu-id="e3f71-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e3f71-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e3f71-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="e3f71-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="e3f71-132">False</span><span class="sxs-lookup"><span data-stu-id="e3f71-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3f71-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e3f71-133">See also</span></span>



- [<span data-ttu-id="e3f71-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e3f71-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

