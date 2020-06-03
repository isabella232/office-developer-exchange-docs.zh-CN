---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: GetServiceConfiguration 元素定义 GetServiceConfiguration 请求。
ms.openlocfilehash: e9357a9e3be22e129c4910c01231f9dbd22a2dbe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457870"
---
# <a name="getserviceconfiguration"></a><span data-ttu-id="0afa3-103">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afa3-103">GetServiceConfiguration</span></span>

<span data-ttu-id="0afa3-104">**GetServiceConfiguration**元素定义 GetServiceConfiguration 请求。</span><span class="sxs-lookup"><span data-stu-id="0afa3-104">The **GetServiceConfiguration** element defines a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 <span data-ttu-id="0afa3-105">**GetServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="0afa3-105">**GetServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0afa3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0afa3-106">Attributes and elements</span></span>

<span data-ttu-id="0afa3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0afa3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0afa3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="0afa3-108">Attributes</span></span>

<span data-ttu-id="0afa3-109">无。</span><span class="sxs-lookup"><span data-stu-id="0afa3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0afa3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0afa3-110">Child elements</span></span>

|<span data-ttu-id="0afa3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0afa3-111">**Element**</span></span>|<span data-ttu-id="0afa3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0afa3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0afa3-113">ActingAs</span><span class="sxs-lookup"><span data-stu-id="0afa3-113">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="0afa3-114">标识呼叫者发送的人。</span><span class="sxs-lookup"><span data-stu-id="0afa3-114">Identifies who the caller is sending as.</span></span> <span data-ttu-id="0afa3-115">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="0afa3-115">This element is optional.</span></span> <span data-ttu-id="0afa3-116">如果此元素不存在，则假定已通过身份验证的用户成为发件人。</span><span class="sxs-lookup"><span data-stu-id="0afa3-116">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="0afa3-117">若要请求发件人提示，必须包含**ActingAs**元素。</span><span class="sxs-lookup"><span data-stu-id="0afa3-117">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="0afa3-118">如果**ActingAs**元素缺失、不包含路由类型、不包含电子邮件地址、包含无效的电子邮件地址、不会解析为 Active Directory 域服务（AD ds）中的用户或解析为 AD ds 中的多个用户，则会在响应中返回 ErrorInvalidArgument 错误。</span><span class="sxs-lookup"><span data-stu-id="0afa3-118">An ErrorInvalidArgument error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span>  <br/> |
|[<span data-ttu-id="0afa3-119">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="0afa3-119">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="0afa3-120">包含请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="0afa3-120">Contains the requested service configurations.</span></span> <span data-ttu-id="0afa3-121">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0afa3-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0afa3-122">父元素</span><span class="sxs-lookup"><span data-stu-id="0afa3-122">Parent elements</span></span>

<span data-ttu-id="0afa3-123">无。</span><span class="sxs-lookup"><span data-stu-id="0afa3-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="0afa3-124">文本值</span><span class="sxs-lookup"><span data-stu-id="0afa3-124">Text value</span></span>

<span data-ttu-id="0afa3-125">无。</span><span class="sxs-lookup"><span data-stu-id="0afa3-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0afa3-126">说明</span><span class="sxs-lookup"><span data-stu-id="0afa3-126">Remarks</span></span>

<span data-ttu-id="0afa3-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0afa3-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0afa3-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="0afa3-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0afa3-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="0afa3-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0afa3-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="0afa3-130">Schema Name</span></span>  <br/> |<span data-ttu-id="0afa3-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="0afa3-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0afa3-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="0afa3-132">Validation File</span></span>  <br/> |<span data-ttu-id="0afa3-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0afa3-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0afa3-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="0afa3-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="0afa3-135">False</span><span class="sxs-lookup"><span data-stu-id="0afa3-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0afa3-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0afa3-136">See also</span></span>



- [<span data-ttu-id="0afa3-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0afa3-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

