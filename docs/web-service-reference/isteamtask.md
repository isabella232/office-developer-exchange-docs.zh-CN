---
title: IsTeamTask
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsTeamTask
api_type:
- schema
ms.assetid: af0095da-e5bb-4138-a01c-c203f1a5a33f
description: IsTeamTask 元素指示任务是否归团队。
ms.openlocfilehash: 25a60b44dbdca89d431dc202f06acb3055958a72
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826109"
---
# <a name="isteamtask"></a><span data-ttu-id="0be96-103">IsTeamTask</span><span class="sxs-lookup"><span data-stu-id="0be96-103">IsTeamTask</span></span>

<span data-ttu-id="0be96-104">**IsTeamTask**元素指示任务是否归团队。</span><span class="sxs-lookup"><span data-stu-id="0be96-104">The **IsTeamTask** element indicates whether the task is owned by a team.</span></span> 
  
```xml
<IsTeamTask/>
```

 <span data-ttu-id="0be96-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="0be96-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0be96-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0be96-106">Attributes and elements</span></span>

<span data-ttu-id="0be96-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0be96-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0be96-108">属性</span><span class="sxs-lookup"><span data-stu-id="0be96-108">Attributes</span></span>

<span data-ttu-id="0be96-109">无。</span><span class="sxs-lookup"><span data-stu-id="0be96-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0be96-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0be96-110">Child elements</span></span>

<span data-ttu-id="0be96-111">无。</span><span class="sxs-lookup"><span data-stu-id="0be96-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0be96-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0be96-112">Parent elements</span></span>

|<span data-ttu-id="0be96-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0be96-113">**Element**</span></span>|<span data-ttu-id="0be96-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0be96-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0be96-115">任务</span><span class="sxs-lookup"><span data-stu-id="0be96-115">Task</span></span>](task.md) <br/> |<span data-ttu-id="0be96-116">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="0be96-116">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0be96-117">文本值</span><span class="sxs-lookup"><span data-stu-id="0be96-117">Text value</span></span>

<span data-ttu-id="0be96-118">文本值表示一个布尔值，指示任务是否归团队。</span><span class="sxs-lookup"><span data-stu-id="0be96-118">The text value represents a Boolean value that indicates whether a task is owned by a team.</span></span> <span data-ttu-id="0be96-119">这是只读属性。</span><span class="sxs-lookup"><span data-stu-id="0be96-119">This is a read-only property.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0be96-120">备注</span><span class="sxs-lookup"><span data-stu-id="0be96-120">Remarks</span></span>

<span data-ttu-id="0be96-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0be96-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0be96-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="0be96-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0be96-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="0be96-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0be96-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="0be96-124">Schema Name</span></span>  <br/> |<span data-ttu-id="0be96-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="0be96-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="0be96-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="0be96-126">Validation File</span></span>  <br/> |<span data-ttu-id="0be96-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0be96-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0be96-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="0be96-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="0be96-129">False</span><span class="sxs-lookup"><span data-stu-id="0be96-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0be96-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0be96-130">See also</span></span>



- [<span data-ttu-id="0be96-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0be96-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="0be96-132">创建任务</span><span class="sxs-lookup"><span data-stu-id="0be96-132">Creating Tasks</span></span>](http://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
  
[<span data-ttu-id="0be96-133">删除任务</span><span class="sxs-lookup"><span data-stu-id="0be96-133">Deleting Tasks</span></span>](http://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

