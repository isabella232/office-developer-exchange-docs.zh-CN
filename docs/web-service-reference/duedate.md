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
description: DueDate 元素均表示项目的到期日期。
ms.openlocfilehash: b24891972f240bc6ee5d0fe868445b96abdc089a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753995"
---
# <a name="duedate"></a><span data-ttu-id="9e796-103">DueDate</span><span class="sxs-lookup"><span data-stu-id="9e796-103">DueDate</span></span>

<span data-ttu-id="9e796-104">**DueDate**元素均表示项目的到期日期。</span><span class="sxs-lookup"><span data-stu-id="9e796-104">The **DueDate** element represents the date an item is due.</span></span> 
  
```xml
<DueDate/>
```

 <span data-ttu-id="9e796-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="9e796-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e796-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9e796-106">Attributes and elements</span></span>

<span data-ttu-id="9e796-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9e796-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e796-108">属性</span><span class="sxs-lookup"><span data-stu-id="9e796-108">Attributes</span></span>

<span data-ttu-id="9e796-109">无。</span><span class="sxs-lookup"><span data-stu-id="9e796-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9e796-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9e796-110">Child elements</span></span>

<span data-ttu-id="9e796-111">无。</span><span class="sxs-lookup"><span data-stu-id="9e796-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9e796-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9e796-112">Parent elements</span></span>

|<span data-ttu-id="9e796-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9e796-113">**Element**</span></span>|<span data-ttu-id="9e796-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9e796-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e796-115">任务</span><span class="sxs-lookup"><span data-stu-id="9e796-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="9e796-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="9e796-116">Represents a task in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9e796-117">Flag</span><span class="sxs-lookup"><span data-stu-id="9e796-117">Flag</span></span>](flag.md) <br/> |<span data-ttu-id="9e796-118">邮箱项目上指定的标志。</span><span class="sxs-lookup"><span data-stu-id="9e796-118">Specifies a flag on a mailbox item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9e796-119">文本值</span><span class="sxs-lookup"><span data-stu-id="9e796-119">Text value</span></span>

<span data-ttu-id="9e796-120">如果使用此元素，则需要一个文本值，表示的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="9e796-120">A text value that represents the date and time is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e796-121">备注</span><span class="sxs-lookup"><span data-stu-id="9e796-121">Remarks</span></span>

<span data-ttu-id="9e796-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9e796-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e796-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="9e796-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e796-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="9e796-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e796-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="9e796-125">Schema name</span></span>  <br/> |<span data-ttu-id="9e796-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="9e796-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e796-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="9e796-127">Validation file</span></span>  <br/> |<span data-ttu-id="9e796-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9e796-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e796-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="9e796-129">Can be empty</span></span>  <br/> |<span data-ttu-id="9e796-130">False</span><span class="sxs-lookup"><span data-stu-id="9e796-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e796-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9e796-131">See also</span></span>

- [<span data-ttu-id="9e796-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9e796-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

