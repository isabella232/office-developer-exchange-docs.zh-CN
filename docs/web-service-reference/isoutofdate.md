---
title: IsOutOfDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsOutOfDate
api_type:
- schema
ms.assetid: 2b6005a6-56a9-4848-b998-32908c13e2e2
description: IsOutOfDate 元素指示会议消息、 请求、 响应或取消是否过期。
ms.openlocfilehash: 0a6b2670cc3eb260002821bab31d652177902de1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826110"
---
# <a name="isoutofdate"></a><span data-ttu-id="faa07-103">IsOutOfDate</span><span class="sxs-lookup"><span data-stu-id="faa07-103">IsOutOfDate</span></span>

<span data-ttu-id="faa07-104">**IsOutOfDate**元素指示会议消息、 请求、 响应或取消是否过期。</span><span class="sxs-lookup"><span data-stu-id="faa07-104">The **IsOutOfDate** element indicates whether a meeting message, request, response, or cancellation is out-of-date.</span></span> 
  
```xml
<IsOutOfDate/>
```

 <span data-ttu-id="faa07-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="faa07-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="faa07-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="faa07-106">Attributes and elements</span></span>

<span data-ttu-id="faa07-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="faa07-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="faa07-108">属性</span><span class="sxs-lookup"><span data-stu-id="faa07-108">Attributes</span></span>

<span data-ttu-id="faa07-109">无。</span><span class="sxs-lookup"><span data-stu-id="faa07-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="faa07-110">子元素</span><span class="sxs-lookup"><span data-stu-id="faa07-110">Child elements</span></span>

<span data-ttu-id="faa07-111">无。</span><span class="sxs-lookup"><span data-stu-id="faa07-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="faa07-112">父元素</span><span class="sxs-lookup"><span data-stu-id="faa07-112">Parent elements</span></span>

|<span data-ttu-id="faa07-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="faa07-113">**Element**</span></span>|<span data-ttu-id="faa07-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="faa07-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="faa07-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="faa07-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="faa07-116">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="faa07-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="faa07-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="faa07-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="faa07-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="faa07-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="faa07-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="faa07-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="faa07-120">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="faa07-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="faa07-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="faa07-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="faa07-122">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="faa07-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="faa07-123">文本值</span><span class="sxs-lookup"><span data-stu-id="faa07-123">Text value</span></span>

<span data-ttu-id="faa07-124">文本值为**true**指示会议项目已过期。</span><span class="sxs-lookup"><span data-stu-id="faa07-124">A text value of **true** indicates that the meeting item is out-of-date.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="faa07-125">备注</span><span class="sxs-lookup"><span data-stu-id="faa07-125">Remarks</span></span>

<span data-ttu-id="faa07-126">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="faa07-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="faa07-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="faa07-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="faa07-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="faa07-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="faa07-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="faa07-129">Schema Name</span></span>  <br/> |<span data-ttu-id="faa07-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="faa07-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="faa07-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="faa07-131">Validation File</span></span>  <br/> |<span data-ttu-id="faa07-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="faa07-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="faa07-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="faa07-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="faa07-134">False</span><span class="sxs-lookup"><span data-stu-id="faa07-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="faa07-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="faa07-135">See also</span></span>



- [<span data-ttu-id="faa07-136">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="faa07-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

