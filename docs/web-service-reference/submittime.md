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
description: SubmitTime 元素表示邮件发送到服务器的时间。
ms.openlocfilehash: e4409d962988ee308e0c0b461f9448ef68067fe8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467051"
---
# <a name="submittime"></a><span data-ttu-id="8a279-103">SubmitTime</span><span class="sxs-lookup"><span data-stu-id="8a279-103">SubmitTime</span></span>

<span data-ttu-id="8a279-104">**SubmitTime**元素表示邮件发送到服务器的时间。</span><span class="sxs-lookup"><span data-stu-id="8a279-104">The **SubmitTime** element represents the time at which the message was sent to the server.</span></span> 
  
```XML
<SubmitTime/>
```

 <span data-ttu-id="8a279-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="8a279-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a279-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a279-106">Attributes and elements</span></span>

<span data-ttu-id="8a279-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a279-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a279-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8a279-108">Attributes</span></span>

<span data-ttu-id="8a279-109">无。</span><span class="sxs-lookup"><span data-stu-id="8a279-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a279-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8a279-110">Child elements</span></span>

<span data-ttu-id="8a279-111">无。</span><span class="sxs-lookup"><span data-stu-id="8a279-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a279-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8a279-112">Parent elements</span></span>

|<span data-ttu-id="8a279-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8a279-113">**Element**</span></span>|<span data-ttu-id="8a279-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a279-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a279-115">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="8a279-115">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="8a279-116">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="8a279-116">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8a279-117">文本值</span><span class="sxs-lookup"><span data-stu-id="8a279-117">Text value</span></span>

<span data-ttu-id="8a279-118">如果使用此元素，则表示日期/时间的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="8a279-118">A text value that represents a date/time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a279-119">说明</span><span class="sxs-lookup"><span data-stu-id="8a279-119">Remarks</span></span>

<span data-ttu-id="8a279-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a279-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a279-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a279-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a279-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a279-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8a279-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a279-123">Schema Name</span></span>  <br/> |<span data-ttu-id="8a279-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="8a279-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="8a279-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a279-125">Validation File</span></span>  <br/> |<span data-ttu-id="8a279-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8a279-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8a279-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a279-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a279-128">False</span><span class="sxs-lookup"><span data-stu-id="8a279-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a279-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a279-129">See also</span></span>



[<span data-ttu-id="8a279-130">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="8a279-130">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="8a279-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8a279-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

