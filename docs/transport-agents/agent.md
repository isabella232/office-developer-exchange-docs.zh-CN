---
title: 代理
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- agent
api_type:
- schema
ms.assetid: 0bf744a5-9d79-4c82-8ea7-45fdb3f55300
description: 上次修改时间：2015年9月17日
ms.openlocfilehash: a810bb229015054e0f244773760235114655a982
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455679"
---
# <a name="agent"></a><span data-ttu-id="fe8d7-103">代理</span><span class="sxs-lookup"><span data-stu-id="fe8d7-103">agent</span></span>
  
<span data-ttu-id="fe8d7-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="fe8d7-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="fe8d7-105">**Agent**元素包含有关已安装的代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-105">The **agent** element contains configuration information about an installed agent.</span></span> 
  
- [<span data-ttu-id="fe8d7-106">configuration</span><span class="sxs-lookup"><span data-stu-id="fe8d7-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="fe8d7-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="fe8d7-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="fe8d7-108">agentList</span><span class="sxs-lookup"><span data-stu-id="fe8d7-108">agentList</span></span>](agentlist.md)
- [<span data-ttu-id="fe8d7-109">代理</span><span class="sxs-lookup"><span data-stu-id="fe8d7-109">agent</span></span>](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

<span data-ttu-id="fe8d7-110">**agentType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-110">**agentType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fe8d7-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe8d7-111">Attributes and elements</span></span>

<span data-ttu-id="fe8d7-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe8d7-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="fe8d7-113">Attributes</span></span>

|<span data-ttu-id="fe8d7-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-114">**Attribute**</span></span>|<span data-ttu-id="fe8d7-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fe8d7-116">**name**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-116">**name**</span></span> <br/> |<span data-ttu-id="fe8d7-117">安装代理时指定的名称。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-117">The name that was specified when the agent was installed.</span></span> <span data-ttu-id="fe8d7-118">此属性需要一个非空字符串值，最多包含64个字符。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-118">This attribute requires a nonempty string value that contains a maximum of 64 characters.</span></span>  <br/> |
|<span data-ttu-id="fe8d7-119">**#c1**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-119">**baseType**</span></span> <br/> |<span data-ttu-id="fe8d7-120">代理派生的类的完整名称（包括命名空间）。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-120">The full name, including the namespace, of the class from which the agent derives.</span></span> <span data-ttu-id="fe8d7-121">此属性需要一个不包含至少一个字符的非空字符串值。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-121">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="fe8d7-122">**classFactory**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-122">**classFactory**</span></span> <br/> |<span data-ttu-id="fe8d7-123">实现代理工厂创建代理实例的类的完整名称（包括命名空间）。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-123">The full name, including the namespace, of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="fe8d7-124">此属性必须包含实现代理工厂创建代理实例的类的完全限定名称。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-124">This attribute must contain the fully qualified name of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="fe8d7-125">此类必须派生自[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)或[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-125">This class must derive from either the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) or [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span>  <br/> |
|<span data-ttu-id="fe8d7-126">**assemblyPath**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-126">**assemblyPath**</span></span> <br/> |<span data-ttu-id="fe8d7-127">包含代理代码的程序集的完全限定路径（包括文件名）。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-127">The fully qualified path, including the file name, of the assembly that contains the code for the agent.</span></span> <span data-ttu-id="fe8d7-128">此属性需要一个不包含至少一个字符的非空字符串值。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-128">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="fe8d7-129">**enabled**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-129">**enabled**</span></span> <br/> |<span data-ttu-id="fe8d7-130">一个布尔值，该值指示是否已启用代理。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-130">A Boolean value that indicates whether the agent is enabled.</span></span> <span data-ttu-id="fe8d7-131">如果启用了代理，则此值为**true** ; 否则为 false。否则，该值为**false**。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-131">The value is **true** if the agent is enabled; otherwise, the value is **false**.</span></span> <span data-ttu-id="fe8d7-132">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-132">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fe8d7-133">子元素</span><span class="sxs-lookup"><span data-stu-id="fe8d7-133">Child elements</span></span>

<span data-ttu-id="fe8d7-134">无。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-134">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe8d7-135">父元素</span><span class="sxs-lookup"><span data-stu-id="fe8d7-135">Parent elements</span></span>

|<span data-ttu-id="fe8d7-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-136">**Element**</span></span>|<span data-ttu-id="fe8d7-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="fe8d7-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fe8d7-138">agentList</span><span class="sxs-lookup"><span data-stu-id="fe8d7-138">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="fe8d7-139">包含每个已安装代理的**代理**元素。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-139">Contains an **agent** element for each installed agent.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="fe8d7-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe8d7-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe8d7-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe8d7-141">Namespace</span></span>  <br/> |<span data-ttu-id="fe8d7-142">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-142">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="fe8d7-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe8d7-143">Schema Name</span></span>  <br/> |<span data-ttu-id="fe8d7-144">不可用。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-144">Not available.</span></span>  <br/> |
|<span data-ttu-id="fe8d7-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe8d7-145">Validation File</span></span>  <br/> |<span data-ttu-id="fe8d7-146">不可用。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-146">Not available.</span></span>  <br/> |
|<span data-ttu-id="fe8d7-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe8d7-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="fe8d7-148">不正确。</span><span class="sxs-lookup"><span data-stu-id="fe8d7-148">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fe8d7-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fe8d7-149">See also</span></span>

- [<span data-ttu-id="fe8d7-150">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="fe8d7-150">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

