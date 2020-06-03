---
title: BaseOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BaseOffset
api_type:
- schema
ms.assetid: 0ffad7a6-8e1b-452b-9d87-8e0f6c77f0a6
description: BaseOffset元素表示当前时区的偏移与协调通用时间 (UTC) 每小时。
ms.openlocfilehash: 1e29f123dfac2e29807e0a2077d47adb14844f4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460258"
---
# <a name="baseoffset"></a><span data-ttu-id="c1fe5-103">BaseOffset</span><span class="sxs-lookup"><span data-stu-id="c1fe5-103">BaseOffset</span></span>

<span data-ttu-id="c1fe5-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **BaseOffset**元素表示当前时区的偏移与协调通用时间 (UTC) 每小时。</span><span class="sxs-lookup"><span data-stu-id="c1fe5-104">The **BaseOffset** element represents the hourly offset from Coordinated Universal Time (UTC) for the current time zone.</span></span> 
  
```xml
<BaseOffset/>
```

 <span data-ttu-id="c1fe5-105">**duration**</span><span class="sxs-lookup"><span data-stu-id="c1fe5-105">**duration**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1fe5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c1fe5-106">Attributes and elements</span></span>

<span data-ttu-id="c1fe5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1fe5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1fe5-108">属性</span><span class="sxs-lookup"><span data-stu-id="c1fe5-108">Attributes</span></span>

<span data-ttu-id="c1fe5-109">无</span><span class="sxs-lookup"><span data-stu-id="c1fe5-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1fe5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c1fe5-110">Child elements</span></span>

<span data-ttu-id="c1fe5-111">无。</span><span class="sxs-lookup"><span data-stu-id="c1fe5-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1fe5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c1fe5-112">Parent elements</span></span>

|<span data-ttu-id="c1fe5-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1fe5-113">**Element**</span></span>|<span data-ttu-id="c1fe5-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1fe5-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1fe5-115">MeetingTimeZone</span><span class="sxs-lookup"><span data-stu-id="c1fe5-115">MeetingTimeZone</span></span>](meetingtimezone.md) <br/> |<span data-ttu-id="c1fe5-116">表示时区的会议所在的位置。</span><span class="sxs-lookup"><span data-stu-id="c1fe5-116">Represents the time zone of the location where the meeting is hosted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1fe5-117">说明</span><span class="sxs-lookup"><span data-stu-id="c1fe5-117">Remarks</span></span>

<span data-ttu-id="c1fe5-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c1fe5-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1fe5-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="c1fe5-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1fe5-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="c1fe5-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c1fe5-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="c1fe5-121">Schema Name</span></span>  <br/> |<span data-ttu-id="c1fe5-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="c1fe5-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="c1fe5-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="c1fe5-123">Validation File</span></span>  <br/> |<span data-ttu-id="c1fe5-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c1fe5-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c1fe5-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="c1fe5-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1fe5-126">False</span><span class="sxs-lookup"><span data-stu-id="c1fe5-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1fe5-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c1fe5-127">See also</span></span>



- [<span data-ttu-id="c1fe5-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c1fe5-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

