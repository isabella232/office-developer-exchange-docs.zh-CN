---
title: ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessages
api_type:
- schema
ms.assetid: c7cfa0d1-fcb2-441f-8489-3a549da33b34
description: ResponseMessages 元素包含一组服务配置响应消息。
ms.openlocfilehash: cf271224141ffeb6dc00069abf430ab33d3ca2fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457450"
---
# <a name="responsemessages-arrayofserviceconfigurationresponsemessagetype"></a><span data-ttu-id="ce093-103">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span><span class="sxs-lookup"><span data-stu-id="ce093-103">ResponseMessages (ArrayOfServiceConfigurationResponseMessageType)</span></span>

<span data-ttu-id="ce093-104">**ResponseMessages**元素包含一组服务配置响应消息。</span><span class="sxs-lookup"><span data-stu-id="ce093-104">The **ResponseMessages** element contains an array of service configuration response messages.</span></span> 
  
```XML
<ResponseMessages>
   <ServiceConfigurationResponseMessageType/>
</ResponseMessages>
```

 <span data-ttu-id="ce093-105">**ArrayOfServiceConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ce093-105">**ArrayOfServiceConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ce093-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ce093-106">Attributes and elements</span></span>

<span data-ttu-id="ce093-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ce093-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ce093-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ce093-108">Attributes</span></span>

<span data-ttu-id="ce093-109">无。</span><span class="sxs-lookup"><span data-stu-id="ce093-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ce093-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ce093-110">Child elements</span></span>

|<span data-ttu-id="ce093-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce093-111">**Element**</span></span>|<span data-ttu-id="ce093-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce093-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce093-113">ServiceConfigurationResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="ce093-113">ServiceConfigurationResponseMessageType</span></span>](serviceconfigurationresponsemessagetype.md) <br/> |<span data-ttu-id="ce093-114">包含服务配置设置。</span><span class="sxs-lookup"><span data-stu-id="ce093-114">Contains service configuration settings.</span></span> <span data-ttu-id="ce093-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="ce093-115">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ce093-116">父元素</span><span class="sxs-lookup"><span data-stu-id="ce093-116">Parent elements</span></span>

|<span data-ttu-id="ce093-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="ce093-117">**Element**</span></span>|<span data-ttu-id="ce093-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="ce093-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce093-119">GetServiceConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="ce093-119">GetServiceConfigurationResponse</span></span>](getserviceconfigurationresponse.md) <br/> |<span data-ttu-id="ce093-120">定义对 GetServiceConfiguration 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ce093-120">Defines a response to a GetServiceConfiguration request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ce093-121">文本值</span><span class="sxs-lookup"><span data-stu-id="ce093-121">Text value</span></span>

<span data-ttu-id="ce093-122">无。</span><span class="sxs-lookup"><span data-stu-id="ce093-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ce093-123">说明</span><span class="sxs-lookup"><span data-stu-id="ce093-123">Remarks</span></span>

<span data-ttu-id="ce093-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ce093-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ce093-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="ce093-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce093-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="ce093-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ce093-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="ce093-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ce093-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="ce093-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ce093-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="ce093-129">Validation File</span></span>  <br/> |<span data-ttu-id="ce093-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ce093-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ce093-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="ce093-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ce093-132">False</span><span class="sxs-lookup"><span data-stu-id="ce093-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce093-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ce093-133">See also</span></span>



- [<span data-ttu-id="ce093-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ce093-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

