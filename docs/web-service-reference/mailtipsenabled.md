---
title: MailTipsEnabled
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailTipsEnabled
api_type:
- schema
ms.assetid: 737388b3-7b73-42af-94d3-3dbb0659718f
description: MailTipsEnabled 元素指示是否可以使用邮件提示服务。
ms.openlocfilehash: 6be923733f1cbd584010ce5f8ee5b96178d5c2c0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468010"
---
# <a name="mailtipsenabled"></a><span data-ttu-id="07fb7-103">MailTipsEnabled</span><span class="sxs-lookup"><span data-stu-id="07fb7-103">MailTipsEnabled</span></span>

<span data-ttu-id="07fb7-104">**MailTipsEnabled**元素指示是否可以使用邮件提示服务。</span><span class="sxs-lookup"><span data-stu-id="07fb7-104">The **MailTipsEnabled** element indicates whether the mail tips service is available.</span></span> 
  
```xml
<MailTipsEnabled>true | false</MailTipsEnabled>
```

 <span data-ttu-id="07fb7-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="07fb7-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07fb7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="07fb7-106">Attributes and elements</span></span>

<span data-ttu-id="07fb7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="07fb7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07fb7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="07fb7-108">Attributes</span></span>

<span data-ttu-id="07fb7-109">无。</span><span class="sxs-lookup"><span data-stu-id="07fb7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07fb7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="07fb7-110">Child elements</span></span>

<span data-ttu-id="07fb7-111">无。</span><span class="sxs-lookup"><span data-stu-id="07fb7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="07fb7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="07fb7-112">Parent elements</span></span>

|<span data-ttu-id="07fb7-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="07fb7-113">**Element**</span></span>|<span data-ttu-id="07fb7-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="07fb7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07fb7-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="07fb7-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="07fb7-116">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="07fb7-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="07fb7-117">文本值</span><span class="sxs-lookup"><span data-stu-id="07fb7-117">Text value</span></span>

<span data-ttu-id="07fb7-118">如果邮件提示服务可用，则此元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="07fb7-118">The text value of this element is **true** if the mail tips service is available.</span></span> <span data-ttu-id="07fb7-119">如果 "邮件提示" 服务不可用，则该值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="07fb7-119">The value is **false** if the mail tips service is not available.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07fb7-120">说明</span><span class="sxs-lookup"><span data-stu-id="07fb7-120">Remarks</span></span>

<span data-ttu-id="07fb7-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="07fb7-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07fb7-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="07fb7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07fb7-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="07fb7-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07fb7-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="07fb7-124">Schema Name</span></span>  <br/> |<span data-ttu-id="07fb7-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="07fb7-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="07fb7-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="07fb7-126">Validation File</span></span>  <br/> |<span data-ttu-id="07fb7-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07fb7-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07fb7-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="07fb7-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="07fb7-129">False</span><span class="sxs-lookup"><span data-stu-id="07fb7-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07fb7-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="07fb7-130">See also</span></span>



- [<span data-ttu-id="07fb7-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="07fb7-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

