---
title: Mileage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Mileage
api_type:
- schema
ms.assetid: 461ba447-1b04-4115-9919-dc378fd3bf24
description: 里程元素表示任务或联系人项目的里程。
ms.openlocfilehash: 20cbed08d41599a433f3e2aa6e4a662018fbdc48
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465777"
---
# <a name="mileage"></a><span data-ttu-id="1630c-103">Mileage</span><span class="sxs-lookup"><span data-stu-id="1630c-103">Mileage</span></span>

<span data-ttu-id="1630c-104">**里程**元素表示任务或联系人项目的里程。</span><span class="sxs-lookup"><span data-stu-id="1630c-104">The **Mileage** element represents mileage for a task or contact item.</span></span> 
  
```xml
<Mileage/>
```

 <span data-ttu-id="1630c-105">**string**</span><span class="sxs-lookup"><span data-stu-id="1630c-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1630c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1630c-106">Attributes and elements</span></span>

<span data-ttu-id="1630c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1630c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1630c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1630c-108">Attributes</span></span>

<span data-ttu-id="1630c-109">无。</span><span class="sxs-lookup"><span data-stu-id="1630c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1630c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1630c-110">Child elements</span></span>

<span data-ttu-id="1630c-111">无。</span><span class="sxs-lookup"><span data-stu-id="1630c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1630c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1630c-112">Parent elements</span></span>

|<span data-ttu-id="1630c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1630c-113">**Element**</span></span>|<span data-ttu-id="1630c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1630c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1630c-115">联系人</span><span class="sxs-lookup"><span data-stu-id="1630c-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="1630c-116">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="1630c-116">Represents a contact item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1630c-117">任务</span><span class="sxs-lookup"><span data-stu-id="1630c-117">Task</span></span>](task.md) <br/> |<span data-ttu-id="1630c-118">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="1630c-118">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1630c-119">文本值</span><span class="sxs-lookup"><span data-stu-id="1630c-119">Text value</span></span>

<span data-ttu-id="1630c-120">如果使用此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="1630c-120">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1630c-121">说明</span><span class="sxs-lookup"><span data-stu-id="1630c-121">Remarks</span></span>

<span data-ttu-id="1630c-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1630c-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1630c-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="1630c-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1630c-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="1630c-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1630c-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="1630c-125">Schema name</span></span>  <br/> |<span data-ttu-id="1630c-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="1630c-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="1630c-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="1630c-127">Validation file</span></span>  <br/> |<span data-ttu-id="1630c-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1630c-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1630c-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="1630c-129">Can be empty</span></span>  <br/> |<span data-ttu-id="1630c-130">False</span><span class="sxs-lookup"><span data-stu-id="1630c-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1630c-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1630c-131">See also</span></span>



- [<span data-ttu-id="1630c-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1630c-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

