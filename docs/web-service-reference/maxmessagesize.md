---
title: MaxMessageSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxMessageSize
api_type:
- schema
ms.assetid: bb98ac72-9409-4332-81bb-ee3bebb9a00e
description: MaxMessageSize 元素表示收件人可接受的最大邮件大小。
ms.openlocfilehash: 727eed38a129800b7d38aa49c41cdacfa13e7a36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468409"
---
# <a name="maxmessagesize"></a><span data-ttu-id="122cb-103">MaxMessageSize</span><span class="sxs-lookup"><span data-stu-id="122cb-103">MaxMessageSize</span></span>

<span data-ttu-id="122cb-104">**MaxMessageSize**元素表示收件人可接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="122cb-104">The **MaxMessageSize** element represents the maximum message size a recipient can accept.</span></span> 
  
```XML
<MaxMessageSize/>
```

 <span data-ttu-id="122cb-105">**int**</span><span class="sxs-lookup"><span data-stu-id="122cb-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="122cb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="122cb-106">Attributes and elements</span></span>

<span data-ttu-id="122cb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="122cb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="122cb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="122cb-108">Attributes</span></span>

<span data-ttu-id="122cb-109">无。</span><span class="sxs-lookup"><span data-stu-id="122cb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="122cb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="122cb-110">Child elements</span></span>

<span data-ttu-id="122cb-111">无。</span><span class="sxs-lookup"><span data-stu-id="122cb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="122cb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="122cb-112">Parent elements</span></span>

|<span data-ttu-id="122cb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="122cb-113">**Element**</span></span>|<span data-ttu-id="122cb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="122cb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="122cb-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="122cb-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="122cb-116">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="122cb-116">Represents values for various types of mail tips.</span></span>  <br/> |
|[<span data-ttu-id="122cb-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="122cb-117">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="122cb-118">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="122cb-118">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="122cb-119">文本值</span><span class="sxs-lookup"><span data-stu-id="122cb-119">Text value</span></span>

<span data-ttu-id="122cb-120">Text 值是一个整数，表示收件人可接受的最大邮件大小。</span><span class="sxs-lookup"><span data-stu-id="122cb-120">The text value is an integer that represents the maximum message size a recipient can accept.</span></span> <span data-ttu-id="122cb-121">此值可以以千字节或兆字节为单位。</span><span class="sxs-lookup"><span data-stu-id="122cb-121">This value can be measured in kilobytes or megabytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="122cb-122">说明</span><span class="sxs-lookup"><span data-stu-id="122cb-122">Remarks</span></span>

<span data-ttu-id="122cb-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="122cb-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="122cb-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="122cb-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="122cb-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="122cb-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="122cb-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="122cb-126">Schema Name</span></span>  <br/> |<span data-ttu-id="122cb-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="122cb-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="122cb-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="122cb-128">Validation File</span></span>  <br/> |<span data-ttu-id="122cb-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="122cb-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="122cb-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="122cb-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="122cb-131">False</span><span class="sxs-lookup"><span data-stu-id="122cb-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="122cb-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="122cb-132">See also</span></span>



- [<span data-ttu-id="122cb-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="122cb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

