---
title: IsDelegated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsDelegated
api_type:
- schema
ms.assetid: c12907db-be80-4924-9469-8e58612cf42c
description: IsDelegated 元素指示会议是否由具有代理访问权限的帐户进行处理。
ms.openlocfilehash: 2c62b59665431d5ea203e972a506aa90afc76601
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456442"
---
# <a name="isdelegated"></a><span data-ttu-id="923bc-103">IsDelegated</span><span class="sxs-lookup"><span data-stu-id="923bc-103">IsDelegated</span></span>

<span data-ttu-id="923bc-104">**IsDelegated**元素指示会议是否由具有代理访问权限的帐户进行处理。</span><span class="sxs-lookup"><span data-stu-id="923bc-104">The **IsDelegated** element indicates whether a meeting was handled by an account that has delegate access.</span></span> 
  
```xml
<IsDelegated/>
```

 <span data-ttu-id="923bc-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="923bc-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="923bc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="923bc-106">Attributes and elements</span></span>

<span data-ttu-id="923bc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="923bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="923bc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="923bc-108">Attributes</span></span>

<span data-ttu-id="923bc-109">无。</span><span class="sxs-lookup"><span data-stu-id="923bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="923bc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="923bc-110">Child elements</span></span>

<span data-ttu-id="923bc-111">无。</span><span class="sxs-lookup"><span data-stu-id="923bc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="923bc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="923bc-112">Parent elements</span></span>

|<span data-ttu-id="923bc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="923bc-113">**Element**</span></span>|<span data-ttu-id="923bc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="923bc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="923bc-115">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="923bc-115">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="923bc-116">表示 Exchange 存储中的会议取消。</span><span class="sxs-lookup"><span data-stu-id="923bc-116">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="923bc-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="923bc-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="923bc-118">表示 Exchange 存储中的会议。</span><span class="sxs-lookup"><span data-stu-id="923bc-118">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="923bc-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="923bc-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="923bc-120">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="923bc-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="923bc-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="923bc-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="923bc-122">表示 Exchange 存储中的会议响应。</span><span class="sxs-lookup"><span data-stu-id="923bc-122">Represents a meeting response in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="923bc-123">文本值</span><span class="sxs-lookup"><span data-stu-id="923bc-123">Text value</span></span>

<span data-ttu-id="923bc-124">如果文本值**为 true** ，则表示该会议由具有代理访问权限的帐户进行处理。</span><span class="sxs-lookup"><span data-stu-id="923bc-124">A text value of **true** indicates that the meeting was handled by an account that has delegate access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="923bc-125">说明</span><span class="sxs-lookup"><span data-stu-id="923bc-125">Remarks</span></span>

<span data-ttu-id="923bc-126">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="923bc-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="923bc-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="923bc-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="923bc-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="923bc-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="923bc-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="923bc-129">Schema Name</span></span>  <br/> |<span data-ttu-id="923bc-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="923bc-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="923bc-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="923bc-131">Validation File</span></span>  <br/> |<span data-ttu-id="923bc-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="923bc-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="923bc-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="923bc-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="923bc-134">False</span><span class="sxs-lookup"><span data-stu-id="923bc-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="923bc-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="923bc-135">See also</span></span>



- [<span data-ttu-id="923bc-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="923bc-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

