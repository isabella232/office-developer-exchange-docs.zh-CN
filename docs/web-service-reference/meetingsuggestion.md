---
title: MeetingSuggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d6012063-eb67-4e83-a4a6-33482685083f
description: MeetingSuggestion 元素指定建议的会议。
ms.openlocfilehash: 132ed907886c0ee9f3c4f46cc835d4b4fc6aa621
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466309"
---
# <a name="meetingsuggestion"></a><span data-ttu-id="1e6d2-103">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="1e6d2-103">MeetingSuggestion</span></span>

<span data-ttu-id="1e6d2-104">**MeetingSuggestion**元素指定建议的会议。</span><span class="sxs-lookup"><span data-stu-id="1e6d2-104">The **MeetingSuggestion** element specifies a proposed meeting.</span></span> 
  
```XML
<MeetingSuggestion>
   <Attendees/>
   <Location/>
   <Subject/>
   <MeetingString/>
   <StartTime/>
   <EndTime/>
</MeetingSuggestion>
```

 <span data-ttu-id="1e6d2-105">**MeetingSuggestionType**</span><span class="sxs-lookup"><span data-stu-id="1e6d2-105">**MeetingSuggestionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e6d2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e6d2-106">Attributes and elements</span></span>

<span data-ttu-id="1e6d2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e6d2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e6d2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1e6d2-108">Attributes</span></span>

<span data-ttu-id="1e6d2-109">无。</span><span class="sxs-lookup"><span data-stu-id="1e6d2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e6d2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1e6d2-110">Child elements</span></span>

<span data-ttu-id="1e6d2-111">[与会者](attendees.md)  | [位置](location.md)  | [主题](subject.md)  | [Meetingsuggestion.meetingstring](meetingstring.md)  | [StartTime](starttime.md)  | [EndTime](endtime.md)</span><span class="sxs-lookup"><span data-stu-id="1e6d2-111">[Attendees](attendees.md) | [Location](location.md) | [Subject](subject.md) | [MeetingString](meetingstring.md) | [StartTime](starttime.md) | [EndTime](endtime.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1e6d2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1e6d2-112">Parent elements</span></span>

[<span data-ttu-id="1e6d2-113">MeetingSuggestions</span><span class="sxs-lookup"><span data-stu-id="1e6d2-113">MeetingSuggestions</span></span>](meetingsuggestions.md)
  
## <a name="remarks"></a><span data-ttu-id="1e6d2-114">备注</span><span class="sxs-lookup"><span data-stu-id="1e6d2-114">Remarks</span></span>

<span data-ttu-id="1e6d2-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1e6d2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1e6d2-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1e6d2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e6d2-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e6d2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e6d2-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e6d2-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e6d2-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e6d2-119">Schema name</span></span>  <br/> |<span data-ttu-id="1e6d2-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="1e6d2-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1e6d2-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e6d2-121">Validation file</span></span>  <br/> |<span data-ttu-id="1e6d2-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1e6d2-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e6d2-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e6d2-123">Can be empty</span></span>  <br/> ||
   

