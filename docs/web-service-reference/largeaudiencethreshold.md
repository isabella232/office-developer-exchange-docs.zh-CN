---
title: LargeAudienceThreshold
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- LargeAudienceThreshold
api_type:
- schema
ms.assetid: dacd9db7-b8f0-445d-a3d1-3356b8c2bcd1
description: LargeAudienceThreshold 元素表示客户端的大型受众阈值。
ms.openlocfilehash: a222e992ba2d716f6539c7b146277358a76fe552
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826201"
---
# <a name="largeaudiencethreshold"></a><span data-ttu-id="09b72-103">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="09b72-103">LargeAudienceThreshold</span></span>

<span data-ttu-id="09b72-104">**LargeAudienceThreshold**元素表示客户端的大型受众阈值。</span><span class="sxs-lookup"><span data-stu-id="09b72-104">The **LargeAudienceThreshold** element represents the large audience threshold for a client.</span></span> 
  
```XML
<LargeAudienceThreshold/>
```

 <span data-ttu-id="09b72-105">**int**</span><span class="sxs-lookup"><span data-stu-id="09b72-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09b72-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="09b72-106">Attributes and elements</span></span>

<span data-ttu-id="09b72-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="09b72-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09b72-108">属性</span><span class="sxs-lookup"><span data-stu-id="09b72-108">Attributes</span></span>

<span data-ttu-id="09b72-109">无。</span><span class="sxs-lookup"><span data-stu-id="09b72-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09b72-110">子元素</span><span class="sxs-lookup"><span data-stu-id="09b72-110">Child elements</span></span>

<span data-ttu-id="09b72-111">无。</span><span class="sxs-lookup"><span data-stu-id="09b72-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09b72-112">父元素</span><span class="sxs-lookup"><span data-stu-id="09b72-112">Parent elements</span></span>

|<span data-ttu-id="09b72-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="09b72-113">**Element**</span></span>|<span data-ttu-id="09b72-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="09b72-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09b72-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="09b72-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="09b72-116">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="09b72-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09b72-117">文本值</span><span class="sxs-lookup"><span data-stu-id="09b72-117">Text value</span></span>

<span data-ttu-id="09b72-118">文本值为整数类型的值，该值代表指示邮件转到多个用户的访问群体阈值。</span><span class="sxs-lookup"><span data-stu-id="09b72-118">The text value is an integer that represents the audience threshold that indicates that the message is going to more than one person.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="09b72-119">备注</span><span class="sxs-lookup"><span data-stu-id="09b72-119">Remarks</span></span>

<span data-ttu-id="09b72-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="09b72-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="09b72-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="09b72-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09b72-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="09b72-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="09b72-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="09b72-123">Schema Name</span></span>  <br/> |<span data-ttu-id="09b72-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="09b72-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="09b72-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="09b72-125">Validation File</span></span>  <br/> |<span data-ttu-id="09b72-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="09b72-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09b72-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="09b72-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="09b72-128">False</span><span class="sxs-lookup"><span data-stu-id="09b72-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09b72-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="09b72-129">See also</span></span>



- [<span data-ttu-id="09b72-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="09b72-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

