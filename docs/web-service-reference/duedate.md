---
title: DueDate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DueDate
api_type:
- schema
ms.assetid: dd9b6c43-a512-4b3b-a071-4abde02ed55f
description: DueDate 元素表示项目的截止日期。
ms.openlocfilehash: b88bb5c64ee48e02b1600c6865ce650e7bcdaa3b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463557"
---
# <a name="duedate"></a><span data-ttu-id="159be-103">DueDate</span><span class="sxs-lookup"><span data-stu-id="159be-103">DueDate</span></span>

<span data-ttu-id="159be-104">**DueDate**元素表示项目的截止日期。</span><span class="sxs-lookup"><span data-stu-id="159be-104">The **DueDate** element represents the date an item is due.</span></span> 
  
```xml
<DueDate/>
```

 <span data-ttu-id="159be-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="159be-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="159be-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="159be-106">Attributes and elements</span></span>

<span data-ttu-id="159be-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="159be-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="159be-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="159be-108">Attributes</span></span>

<span data-ttu-id="159be-109">无。</span><span class="sxs-lookup"><span data-stu-id="159be-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="159be-110">子元素</span><span class="sxs-lookup"><span data-stu-id="159be-110">Child elements</span></span>

<span data-ttu-id="159be-111">无。</span><span class="sxs-lookup"><span data-stu-id="159be-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="159be-112">父元素</span><span class="sxs-lookup"><span data-stu-id="159be-112">Parent elements</span></span>

|<span data-ttu-id="159be-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="159be-113">**Element**</span></span>|<span data-ttu-id="159be-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="159be-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="159be-115">任务</span><span class="sxs-lookup"><span data-stu-id="159be-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="159be-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="159be-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="159be-117">Flag</span><span class="sxs-lookup"><span data-stu-id="159be-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="159be-118">指定邮箱项目的标志。</span><span class="sxs-lookup"><span data-stu-id="159be-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="159be-119">文本值</span><span class="sxs-lookup"><span data-stu-id="159be-119">Text value</span></span>

<span data-ttu-id="159be-120">如果使用此元素，则表示日期和时间的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="159be-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="159be-121">说明</span><span class="sxs-lookup"><span data-stu-id="159be-121">Remarks</span></span>

<span data-ttu-id="159be-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="159be-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="159be-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="159be-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="159be-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="159be-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="159be-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="159be-125">Schema name</span></span>  <br/> |<span data-ttu-id="159be-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="159be-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="159be-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="159be-127">Validation file</span></span>  <br/> |<span data-ttu-id="159be-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="159be-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="159be-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="159be-129">Can be empty</span></span>  <br/> |<span data-ttu-id="159be-130">False</span><span class="sxs-lookup"><span data-stu-id="159be-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="159be-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="159be-131">See also</span></span>

- [<span data-ttu-id="159be-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="159be-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

