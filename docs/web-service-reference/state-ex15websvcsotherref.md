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
description: State 元素表示联系人项目的居住状态。
ms.openlocfilehash: 123aa0db83f58996924baadb0a87946db6934450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459999"
---
# <a name="state"></a><span data-ttu-id="26f00-103">状态</span><span class="sxs-lookup"><span data-stu-id="26f00-103">State</span></span>

<span data-ttu-id="26f00-104">**State**元素表示联系人项目的居住状态。</span><span class="sxs-lookup"><span data-stu-id="26f00-104">The **State** element represents the state of residence for a contact item.</span></span> 
  
```xml
<State/>
```

<span data-ttu-id="26f00-105">**string**</span><span class="sxs-lookup"><span data-stu-id="26f00-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="26f00-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="26f00-106">Attributes and elements</span></span>

<span data-ttu-id="26f00-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="26f00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="26f00-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="26f00-108">Attributes</span></span>

<span data-ttu-id="26f00-109">无。</span><span class="sxs-lookup"><span data-stu-id="26f00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="26f00-110">子元素</span><span class="sxs-lookup"><span data-stu-id="26f00-110">Child elements</span></span>

<span data-ttu-id="26f00-111">无。</span><span class="sxs-lookup"><span data-stu-id="26f00-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="26f00-112">父元素</span><span class="sxs-lookup"><span data-stu-id="26f00-112">Parent elements</span></span>

|<span data-ttu-id="26f00-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="26f00-113">**Element**</span></span>|<span data-ttu-id="26f00-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="26f00-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="26f00-115">条目（PhysicalAddress）</span><span class="sxs-lookup"><span data-stu-id="26f00-115">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md) <br/> |<span data-ttu-id="26f00-116">描述联系人项目的单个物理地址。</span><span class="sxs-lookup"><span data-stu-id="26f00-116">Describes a single physical address for a contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="26f00-117">文本值</span><span class="sxs-lookup"><span data-stu-id="26f00-117">Text value</span></span>

<span data-ttu-id="26f00-118">如果使用此元素，则为表示 state 的名称的 string 值。</span><span class="sxs-lookup"><span data-stu-id="26f00-118">A string value that represents the name of a state is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="26f00-119">说明</span><span class="sxs-lookup"><span data-stu-id="26f00-119">Remarks</span></span>

<span data-ttu-id="26f00-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="26f00-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="26f00-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="26f00-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="26f00-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="26f00-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="26f00-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="26f00-123">Schema name</span></span>  <br/> |<span data-ttu-id="26f00-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="26f00-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="26f00-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="26f00-125">Validation file</span></span>  <br/> |<span data-ttu-id="26f00-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="26f00-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="26f00-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="26f00-127">Can be empty</span></span>  <br/> |<span data-ttu-id="26f00-128">False</span><span class="sxs-lookup"><span data-stu-id="26f00-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="26f00-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="26f00-129">See also</span></span>

- [<span data-ttu-id="26f00-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="26f00-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="26f00-131">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="26f00-131">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
- [<span data-ttu-id="26f00-132">更新联系人</span><span class="sxs-lookup"><span data-stu-id="26f00-132">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
- [<span data-ttu-id="26f00-133">删除联系人</span><span class="sxs-lookup"><span data-stu-id="26f00-133">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

