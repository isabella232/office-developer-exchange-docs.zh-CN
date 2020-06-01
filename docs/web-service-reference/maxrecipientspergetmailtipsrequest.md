---
title: MaxRecipientsPerGetMailTipsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxRecipientsPerGetMailTipsRequest
api_type:
- schema
ms.assetid: 8ff5df18-1989-4217-b4c0-599232911d0c
description: MaxRecipientsPerGetMailTipsRequest 元素指示可传递给 GetMailTips 操作的最大收件人数。
ms.openlocfilehash: cec343182b364fce040d5e32928cbeb569a22124
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468402"
---
# <a name="maxrecipientspergetmailtipsrequest"></a><span data-ttu-id="2aad4-103">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="2aad4-103">MaxRecipientsPerGetMailTipsRequest</span></span>

<span data-ttu-id="2aad4-104">**MaxRecipientsPerGetMailTipsRequest**元素指示可传递给[GetMailTips 操作](getmailtips-operation.md)的最大收件人数。</span><span class="sxs-lookup"><span data-stu-id="2aad4-104">The **MaxRecipientsPerGetMailTipsRequest** element indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 <span data-ttu-id="2aad4-105">**int**</span><span class="sxs-lookup"><span data-stu-id="2aad4-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2aad4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2aad4-106">Attributes and elements</span></span>

<span data-ttu-id="2aad4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2aad4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2aad4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2aad4-108">Attributes</span></span>

<span data-ttu-id="2aad4-109">无。</span><span class="sxs-lookup"><span data-stu-id="2aad4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2aad4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2aad4-110">Child elements</span></span>

<span data-ttu-id="2aad4-111">无。</span><span class="sxs-lookup"><span data-stu-id="2aad4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2aad4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2aad4-112">Parent elements</span></span>

|<span data-ttu-id="2aad4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2aad4-113">**Element**</span></span>|<span data-ttu-id="2aad4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2aad4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2aad4-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="2aad4-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="2aad4-116">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="2aad4-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2aad4-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2aad4-117">Text value</span></span>

<span data-ttu-id="2aad4-118">Text 值是一个整数，表示可传递给[GetMailTips 操作](getmailtips-operation.md)的最大收件人数。</span><span class="sxs-lookup"><span data-stu-id="2aad4-118">The text value is an integer that represents the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2aad4-119">说明</span><span class="sxs-lookup"><span data-stu-id="2aad4-119">Remarks</span></span>

<span data-ttu-id="2aad4-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2aad4-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2aad4-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="2aad4-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2aad4-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="2aad4-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2aad4-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="2aad4-123">Schema Name</span></span>  <br/> |<span data-ttu-id="2aad4-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="2aad4-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="2aad4-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="2aad4-125">Validation File</span></span>  <br/> |<span data-ttu-id="2aad4-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2aad4-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2aad4-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="2aad4-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="2aad4-128">False</span><span class="sxs-lookup"><span data-stu-id="2aad4-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2aad4-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2aad4-129">See also</span></span>



[<span data-ttu-id="2aad4-130">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="2aad4-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="2aad4-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2aad4-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

