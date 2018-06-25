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
description: MaxRecipientsPerGetMailTipsRequest 元素指示可以传递给 GetMailTips 操作的收件人的最大数量。
ms.openlocfilehash: 4c873fe534582e582bf5b1c1d5fd2789616e056a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826386"
---
# <a name="maxrecipientspergetmailtipsrequest"></a><span data-ttu-id="bd929-103">MaxRecipientsPerGetMailTipsRequest</span><span class="sxs-lookup"><span data-stu-id="bd929-103">MaxRecipientsPerGetMailTipsRequest</span></span>

<span data-ttu-id="bd929-104">**MaxRecipientsPerGetMailTipsRequest**元素指示可以传递到[GetMailTips 操作](getmailtips-operation.md)的收件人的最大数量。</span><span class="sxs-lookup"><span data-stu-id="bd929-104">The **MaxRecipientsPerGetMailTipsRequest** element indicates the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 <span data-ttu-id="bd929-105">**int**</span><span class="sxs-lookup"><span data-stu-id="bd929-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bd929-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bd929-106">Attributes and elements</span></span>

<span data-ttu-id="bd929-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bd929-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd929-108">属性</span><span class="sxs-lookup"><span data-stu-id="bd929-108">Attributes</span></span>

<span data-ttu-id="bd929-109">无。</span><span class="sxs-lookup"><span data-stu-id="bd929-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bd929-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bd929-110">Child elements</span></span>

<span data-ttu-id="bd929-111">无。</span><span class="sxs-lookup"><span data-stu-id="bd929-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bd929-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bd929-112">Parent elements</span></span>

|<span data-ttu-id="bd929-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="bd929-113">**Element**</span></span>|<span data-ttu-id="bd929-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="bd929-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bd929-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="bd929-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="bd929-116">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="bd929-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bd929-117">文本值</span><span class="sxs-lookup"><span data-stu-id="bd929-117">Text value</span></span>

<span data-ttu-id="bd929-118">文本值是一个整数，表示可以传递到[GetMailTips 操作](getmailtips-operation.md)的收件人的最大数。</span><span class="sxs-lookup"><span data-stu-id="bd929-118">The text value is an integer that represents the maximum number of recipients that can be passed to the [GetMailTips operation](getmailtips-operation.md).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd929-119">备注</span><span class="sxs-lookup"><span data-stu-id="bd929-119">Remarks</span></span>

<span data-ttu-id="bd929-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bd929-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bd929-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="bd929-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd929-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="bd929-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="bd929-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="bd929-123">Schema Name</span></span>  <br/> |<span data-ttu-id="bd929-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="bd929-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="bd929-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="bd929-125">Validation File</span></span>  <br/> |<span data-ttu-id="bd929-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="bd929-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="bd929-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="bd929-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="bd929-128">False</span><span class="sxs-lookup"><span data-stu-id="bd929-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd929-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bd929-129">See also</span></span>



[<span data-ttu-id="bd929-130">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="bd929-130">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="bd929-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bd929-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

