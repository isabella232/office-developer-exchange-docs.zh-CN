---
title: SubmitTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SubmitTime
api_type:
- schema
ms.assetid: 97e4b71e-f45c-4bdb-80f9-805934916c0f
description: SubmitTime 元素均表示邮件已发送到服务器的时间。
ms.openlocfilehash: 3f19e2ac14b412ef8d1ab59eb069f0223cf782ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827617"
---
# <a name="submittime"></a><span data-ttu-id="2c4ab-103">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="2c4ab-103">SubmitTime</span></span>

<span data-ttu-id="2c4ab-104">**SubmitTime**元素均表示邮件已发送到服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="2c4ab-104">The **SubmitTime** element represents the time at which the message was sent to the server.</span></span> 
  
```XML
<SubmitTime/>
```

 <span data-ttu-id="2c4ab-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="2c4ab-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2c4ab-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2c4ab-106">Attributes and elements</span></span>

<span data-ttu-id="2c4ab-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2c4ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2c4ab-108">属性</span><span class="sxs-lookup"><span data-stu-id="2c4ab-108">Attributes</span></span>

<span data-ttu-id="2c4ab-109">无。</span><span class="sxs-lookup"><span data-stu-id="2c4ab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2c4ab-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2c4ab-110">Child elements</span></span>

<span data-ttu-id="2c4ab-111">无。</span><span class="sxs-lookup"><span data-stu-id="2c4ab-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2c4ab-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2c4ab-112">Parent elements</span></span>

|<span data-ttu-id="2c4ab-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2c4ab-113">**Element**</span></span>|<span data-ttu-id="2c4ab-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2c4ab-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2c4ab-115">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="2c4ab-115">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="2c4ab-116">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="2c4ab-116">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2c4ab-117">文本值</span><span class="sxs-lookup"><span data-stu-id="2c4ab-117">Text value</span></span>

<span data-ttu-id="2c4ab-118">如果使用此元素，则需要一个表示日期/时间的文本值。</span><span class="sxs-lookup"><span data-stu-id="2c4ab-118">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c4ab-119">备注</span><span class="sxs-lookup"><span data-stu-id="2c4ab-119">Remarks</span></span>

<span data-ttu-id="2c4ab-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2c4ab-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2c4ab-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="2c4ab-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2c4ab-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="2c4ab-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2c4ab-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="2c4ab-123">Schema Name</span></span>  <br/> |<span data-ttu-id="2c4ab-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="2c4ab-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="2c4ab-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="2c4ab-125">Validation File</span></span>  <br/> |<span data-ttu-id="2c4ab-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2c4ab-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2c4ab-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="2c4ab-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="2c4ab-128">False</span><span class="sxs-lookup"><span data-stu-id="2c4ab-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c4ab-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2c4ab-129">See also</span></span>



[<span data-ttu-id="2c4ab-130">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="2c4ab-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="2c4ab-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2c4ab-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

