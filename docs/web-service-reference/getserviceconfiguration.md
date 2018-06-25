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
ms.openlocfilehash: 7ff7124ff062f21a02fc69b86b7cc7367ba3fcb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825666"
---
# <a name="getserviceconfiguration"></a><span data-ttu-id="b4e52-103">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4e52-103">GetServiceConfiguration</span></span>

<span data-ttu-id="b4e52-104">**GetServiceConfiguration**元素定义 GetServiceConfiguration 请求。</span><span class="sxs-lookup"><span data-stu-id="b4e52-104">The **GetServiceConfiguration** element defines a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 <span data-ttu-id="b4e52-105">**GetServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="b4e52-105">**GetServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4e52-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b4e52-106">Attributes and elements</span></span>

<span data-ttu-id="b4e52-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b4e52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4e52-108">属性</span><span class="sxs-lookup"><span data-stu-id="b4e52-108">Attributes</span></span>

<span data-ttu-id="b4e52-109">无。</span><span class="sxs-lookup"><span data-stu-id="b4e52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4e52-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b4e52-110">Child elements</span></span>

|<span data-ttu-id="b4e52-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b4e52-111">**Element**</span></span>|<span data-ttu-id="b4e52-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b4e52-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4e52-113">ActingAs</span><span class="sxs-lookup"><span data-stu-id="b4e52-113">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="b4e52-114">标识用户呼叫者发送为。</span><span class="sxs-lookup"><span data-stu-id="b4e52-114">Identifies who the caller is sending as.</span></span> <span data-ttu-id="b4e52-115">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="b4e52-115">This element is optional.</span></span> <span data-ttu-id="b4e52-116">如果此元素不存在，则假定为经过身份验证的用户为发件人。</span><span class="sxs-lookup"><span data-stu-id="b4e52-116">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="b4e52-117">**ActingAs**元素必须包含针对请求发件人提示。</span><span class="sxs-lookup"><span data-stu-id="b4e52-117">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="b4e52-118">如果**ActingAs**元素缺少，不包括路由类型，不包括电子邮件地址、 包含无效的电子邮件地址，不能解决 Active Directory 域中的用户，可以在响应中返回 ErrorInvalidArgument 错误服务 (AD DS)，或将解析为 AD DS 中的多个用户。</span><span class="sxs-lookup"><span data-stu-id="b4e52-118">An ErrorInvalidArgument error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span>  <br/> |
|[<span data-ttu-id="b4e52-119">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="b4e52-119">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="b4e52-120">包含请求的服务配置。</span><span class="sxs-lookup"><span data-stu-id="b4e52-120">Contains the requested service configurations.</span></span> <span data-ttu-id="b4e52-121">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b4e52-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b4e52-122">父元素</span><span class="sxs-lookup"><span data-stu-id="b4e52-122">Parent elements</span></span>

<span data-ttu-id="b4e52-123">无。</span><span class="sxs-lookup"><span data-stu-id="b4e52-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="b4e52-124">文本值</span><span class="sxs-lookup"><span data-stu-id="b4e52-124">Text value</span></span>

<span data-ttu-id="b4e52-125">无。</span><span class="sxs-lookup"><span data-stu-id="b4e52-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4e52-126">备注</span><span class="sxs-lookup"><span data-stu-id="b4e52-126">Remarks</span></span>

<span data-ttu-id="b4e52-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b4e52-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4e52-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="b4e52-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4e52-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="b4e52-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b4e52-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="b4e52-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b4e52-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="b4e52-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b4e52-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="b4e52-132">Validation File</span></span>  <br/> |<span data-ttu-id="b4e52-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b4e52-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b4e52-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="b4e52-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4e52-135">False</span><span class="sxs-lookup"><span data-stu-id="b4e52-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4e52-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b4e52-136">See also</span></span>



- [<span data-ttu-id="b4e52-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b4e52-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

