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
description: LargeAudienceThreshold 元素表示客户端的大型访问群体阈值。
ms.openlocfilehash: 6d85f9eaf8b7723713877d376876461befa92324
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466386"
---
# <a name="largeaudiencethreshold"></a><span data-ttu-id="5abb1-103">LargeAudienceThreshold</span><span class="sxs-lookup"><span data-stu-id="5abb1-103">LargeAudienceThreshold</span></span>

<span data-ttu-id="5abb1-104">**LargeAudienceThreshold**元素表示客户端的大型访问群体阈值。</span><span class="sxs-lookup"><span data-stu-id="5abb1-104">The **LargeAudienceThreshold** element represents the large audience threshold for a client.</span></span> 
  
```XML
<LargeAudienceThreshold/>
```

 <span data-ttu-id="5abb1-105">**int**</span><span class="sxs-lookup"><span data-stu-id="5abb1-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5abb1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5abb1-106">Attributes and elements</span></span>

<span data-ttu-id="5abb1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5abb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5abb1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5abb1-108">Attributes</span></span>

<span data-ttu-id="5abb1-109">无。</span><span class="sxs-lookup"><span data-stu-id="5abb1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5abb1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5abb1-110">Child elements</span></span>

<span data-ttu-id="5abb1-111">无。</span><span class="sxs-lookup"><span data-stu-id="5abb1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5abb1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5abb1-112">Parent elements</span></span>

|<span data-ttu-id="5abb1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5abb1-113">**Element**</span></span>|<span data-ttu-id="5abb1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5abb1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5abb1-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="5abb1-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="5abb1-116">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="5abb1-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5abb1-117">文本值</span><span class="sxs-lookup"><span data-stu-id="5abb1-117">Text value</span></span>

<span data-ttu-id="5abb1-118">Text 值是一个代表访问群体阈值的整数，表示该邮件将发送给多个用户。</span><span class="sxs-lookup"><span data-stu-id="5abb1-118">The text value is an integer that represents the audience threshold that indicates that the message is going to more than one person.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5abb1-119">说明</span><span class="sxs-lookup"><span data-stu-id="5abb1-119">Remarks</span></span>

<span data-ttu-id="5abb1-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5abb1-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5abb1-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="5abb1-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5abb1-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="5abb1-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5abb1-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="5abb1-123">Schema Name</span></span>  <br/> |<span data-ttu-id="5abb1-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="5abb1-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="5abb1-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="5abb1-125">Validation File</span></span>  <br/> |<span data-ttu-id="5abb1-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5abb1-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5abb1-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="5abb1-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="5abb1-128">False</span><span class="sxs-lookup"><span data-stu-id="5abb1-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5abb1-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5abb1-129">See also</span></span>



- [<span data-ttu-id="5abb1-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5abb1-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

