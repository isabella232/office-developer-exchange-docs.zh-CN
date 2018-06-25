---
title: 组织者
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
description: 组织者元素均表示会议组织的者。
ms.openlocfilehash: b723578a1b52cd5f6e9bd869a15430453adfa291
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826662"
---
# <a name="organizer"></a><span data-ttu-id="c79b2-103">组织者</span><span class="sxs-lookup"><span data-stu-id="c79b2-103">Organizer</span></span>

<span data-ttu-id="c79b2-104">**组织者**元素均表示会议组织的者。</span><span class="sxs-lookup"><span data-stu-id="c79b2-104">The **Organizer** element represents the organizer of a meeting.</span></span> 
  
```xml
<Organizer>
   <Mailbox/>
</Organizer>
```

<span data-ttu-id="c79b2-105">**SingleRecipientType**</span><span class="sxs-lookup"><span data-stu-id="c79b2-105">**SingleRecipientType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c79b2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c79b2-106">Attributes and elements</span></span>

<span data-ttu-id="c79b2-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c79b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c79b2-108">属性</span><span class="sxs-lookup"><span data-stu-id="c79b2-108">Attributes</span></span>

<span data-ttu-id="c79b2-109">无。</span><span class="sxs-lookup"><span data-stu-id="c79b2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c79b2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c79b2-110">Child elements</span></span>

|<span data-ttu-id="c79b2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c79b2-111">**Element**</span></span>|<span data-ttu-id="c79b2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c79b2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c79b2-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="c79b2-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="c79b2-114">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="c79b2-114">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c79b2-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c79b2-115">Parent elements</span></span>

|<span data-ttu-id="c79b2-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c79b2-116">**Element**</span></span>|<span data-ttu-id="c79b2-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c79b2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c79b2-118">日历项目</span><span class="sxs-lookup"><span data-stu-id="c79b2-118">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="c79b2-119">表示 Exchange 日历项。</span><span class="sxs-lookup"><span data-stu-id="c79b2-119">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="c79b2-120">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="c79b2-120">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="c79b2-121">表示 Exchange 存储中的会议请求。</span><span class="sxs-lookup"><span data-stu-id="c79b2-121">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c79b2-122">备注</span><span class="sxs-lookup"><span data-stu-id="c79b2-122">Remarks</span></span>

<span data-ttu-id="c79b2-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c79b2-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c79b2-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c79b2-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c79b2-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c79b2-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c79b2-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c79b2-126">Schema name</span></span>  <br/> |<span data-ttu-id="c79b2-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c79b2-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c79b2-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c79b2-128">Validation file</span></span>  <br/> |<span data-ttu-id="c79b2-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c79b2-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c79b2-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c79b2-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c79b2-131">False</span><span class="sxs-lookup"><span data-stu-id="c79b2-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c79b2-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c79b2-132">See also</span></span>

- [<span data-ttu-id="c79b2-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c79b2-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

