---
title: 状态
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- State
api_type:
- schema
ms.assetid: bcce7b0e-d504-4a1f-a530-db80b207f201
description: 状态元素表示为联系人项居住地所在的状态。
ms.openlocfilehash: caa9541d30eaa04cc3f2dda0ebbf687b156c4f64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827565"
---
# <a name="state"></a><span data-ttu-id="409c3-103">状态</span><span class="sxs-lookup"><span data-stu-id="409c3-103">State</span></span>

<span data-ttu-id="409c3-104">**状态**元素表示为联系人项居住地所在的状态。</span><span class="sxs-lookup"><span data-stu-id="409c3-104">The **State** element represents the state of residence for a contact item.</span></span> 
  
```xml
<State/>
```

<span data-ttu-id="409c3-105">**string**</span><span class="sxs-lookup"><span data-stu-id="409c3-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="409c3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="409c3-106">Attributes and elements</span></span>

<span data-ttu-id="409c3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="409c3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="409c3-108">属性</span><span class="sxs-lookup"><span data-stu-id="409c3-108">Attributes</span></span>

<span data-ttu-id="409c3-109">无。</span><span class="sxs-lookup"><span data-stu-id="409c3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="409c3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="409c3-110">Child elements</span></span>

<span data-ttu-id="409c3-111">无。</span><span class="sxs-lookup"><span data-stu-id="409c3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="409c3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="409c3-112">Parent elements</span></span>

|<span data-ttu-id="409c3-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="409c3-113">**Element**</span></span>|<span data-ttu-id="409c3-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="409c3-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="409c3-115">条目 (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="409c3-115">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md) <br/> |<span data-ttu-id="409c3-116">描述单个物理地址的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="409c3-116">Describes a single physical address for a contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="409c3-117">文本值</span><span class="sxs-lookup"><span data-stu-id="409c3-117">Text value</span></span>

<span data-ttu-id="409c3-118">如果使用此元素，则需要一个 string 值，该值代表状态的名称。</span><span class="sxs-lookup"><span data-stu-id="409c3-118">A string value that represents the name of a state is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="409c3-119">备注</span><span class="sxs-lookup"><span data-stu-id="409c3-119">Remarks</span></span>

<span data-ttu-id="409c3-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="409c3-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="409c3-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="409c3-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="409c3-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="409c3-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="409c3-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="409c3-123">Schema name</span></span>  <br/> |<span data-ttu-id="409c3-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="409c3-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="409c3-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="409c3-125">Validation file</span></span>  <br/> |<span data-ttu-id="409c3-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="409c3-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="409c3-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="409c3-127">Can be empty</span></span>  <br/> |<span data-ttu-id="409c3-128">False</span><span class="sxs-lookup"><span data-stu-id="409c3-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="409c3-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="409c3-129">See also</span></span>

- [<span data-ttu-id="409c3-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="409c3-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="409c3-131">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="409c3-131">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
- [<span data-ttu-id="409c3-132">更新联系人</span><span class="sxs-lookup"><span data-stu-id="409c3-132">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="409c3-133">删除联系人</span><span class="sxs-lookup"><span data-stu-id="409c3-133">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

