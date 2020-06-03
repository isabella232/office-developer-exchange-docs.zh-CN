---
title: Organizer
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Organizer
api_type:
- schema
ms.assetid: 63892b57-3805-4d60-b9f7-20552a69c241
description: 组织者元素表示会议的组织者。
ms.openlocfilehash: c1188c9b3a894e86a08b8869045c3647e394f506
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462414"
---
# <a name="organizer"></a><span data-ttu-id="d28ea-103">Organizer</span><span class="sxs-lookup"><span data-stu-id="d28ea-103">Organizer</span></span>

<span data-ttu-id="d28ea-104">**组织者**元素表示会议的组织者。</span><span class="sxs-lookup"><span data-stu-id="d28ea-104">The **Organizer** element represents the organizer of a meeting.</span></span> 
  
```xml
<Organizer>
   <Mailbox/>
</Organizer>
```

<span data-ttu-id="d28ea-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="d28ea-105">**SingleRecipientType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d28ea-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d28ea-106">Attributes and elements</span></span>

<span data-ttu-id="d28ea-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d28ea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d28ea-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d28ea-108">Attributes</span></span>

<span data-ttu-id="d28ea-109">无。</span><span class="sxs-lookup"><span data-stu-id="d28ea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d28ea-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d28ea-110">Child elements</span></span>

|<span data-ttu-id="d28ea-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d28ea-111">**Element**</span></span>|<span data-ttu-id="d28ea-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d28ea-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d28ea-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="d28ea-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="d28ea-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="d28ea-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d28ea-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d28ea-115">Parent elements</span></span>

|<span data-ttu-id="d28ea-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d28ea-116">**Element**</span></span>|<span data-ttu-id="d28ea-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d28ea-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d28ea-118">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="d28ea-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="d28ea-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="d28ea-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="d28ea-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d28ea-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d28ea-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="d28ea-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d28ea-122">说明</span><span class="sxs-lookup"><span data-stu-id="d28ea-122">Remarks</span></span>

<span data-ttu-id="d28ea-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d28ea-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d28ea-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="d28ea-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d28ea-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="d28ea-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d28ea-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="d28ea-126">Schema name</span></span>  <br/> |<span data-ttu-id="d28ea-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="d28ea-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d28ea-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="d28ea-128">Validation file</span></span>  <br/> |<span data-ttu-id="d28ea-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d28ea-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d28ea-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="d28ea-130">Can be empty</span></span>  <br/> |<span data-ttu-id="d28ea-131">False</span><span class="sxs-lookup"><span data-stu-id="d28ea-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d28ea-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d28ea-132">See also</span></span>

- [<span data-ttu-id="d28ea-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d28ea-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

