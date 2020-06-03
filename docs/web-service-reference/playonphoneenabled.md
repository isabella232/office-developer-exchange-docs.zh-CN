---
title: PlayOnPhoneEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhoneEnabled
api_type:
- schema
ms.assetid: 6f800912-be4c-46f9-aa1e-dff0bbf877c5
description: PlayOnPhoneEnabled 元素指示是否启用 "电话上播放" 功能。
ms.openlocfilehash: 8342e2bcc9c767903e0f6c180000a0f00eccc311
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529929"
---
# <a name="playonphoneenabled"></a><span data-ttu-id="f7394-103">PlayOnPhoneEnabled</span><span class="sxs-lookup"><span data-stu-id="f7394-103">PlayOnPhoneEnabled</span></span>

<span data-ttu-id="f7394-104">**PlayOnPhoneEnabled**元素指示是否启用 "电话上播放" 功能。</span><span class="sxs-lookup"><span data-stu-id="f7394-104">The **PlayOnPhoneEnabled** element indicates whether the Play-on-Phone feature is enabled.</span></span> 
  
```XML
<PlayOnPhoneEnabled>true | false</PlayOnPhoneEnabled>
```

 <span data-ttu-id="f7394-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f7394-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7394-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7394-106">Attributes and elements</span></span>

<span data-ttu-id="f7394-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7394-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7394-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f7394-108">Attributes</span></span>

<span data-ttu-id="f7394-109">无。</span><span class="sxs-lookup"><span data-stu-id="f7394-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7394-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f7394-110">Child elements</span></span>

<span data-ttu-id="f7394-111">无。</span><span class="sxs-lookup"><span data-stu-id="f7394-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7394-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f7394-112">Parent elements</span></span>

|<span data-ttu-id="f7394-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7394-113">**Element**</span></span>|<span data-ttu-id="f7394-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7394-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7394-115">UnifiedMessagingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7394-115">UnifiedMessagingConfiguration</span></span>](unifiedmessagingconfiguration.md) <br/> |<span data-ttu-id="f7394-116">包含统一消息服务的配置信息。</span><span class="sxs-lookup"><span data-stu-id="f7394-116">Contains configuration information for the Unified Messaging service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f7394-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f7394-117">Text value</span></span>

<span data-ttu-id="f7394-118">如果为帐户启用了 "在电话上播放"，则**PlayOnPhoneEnabled**元素的值为**true** ; 否则为 false。否则，该值为**false**。</span><span class="sxs-lookup"><span data-stu-id="f7394-118">The **PlayOnPhoneEnabled** element has a value of **true** if play-on-phone is enabled for the account; otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f7394-119">备注</span><span class="sxs-lookup"><span data-stu-id="f7394-119">Remarks</span></span>

<span data-ttu-id="f7394-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="f7394-120">This element is required.</span></span>
  
<span data-ttu-id="f7394-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f7394-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7394-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7394-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7394-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7394-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f7394-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7394-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f7394-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="f7394-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f7394-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7394-126">Validation File</span></span>  <br/> |<span data-ttu-id="f7394-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f7394-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f7394-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7394-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7394-129">False</span><span class="sxs-lookup"><span data-stu-id="f7394-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f7394-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f7394-130">See also</span></span>



- [<span data-ttu-id="f7394-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f7394-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

