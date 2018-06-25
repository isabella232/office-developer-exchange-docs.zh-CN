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
description: 上次修改时间： 2015 年 9 月 17 日
ms.openlocfilehash: 3895095ed4e469cdb9fec489ba6b6e228779a9c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753054"
---
# <a name="agent"></a><span data-ttu-id="ca2c9-103">代理</span><span class="sxs-lookup"><span data-stu-id="ca2c9-103">agent</span></span>
  
<span data-ttu-id="ca2c9-104">**适用于：** Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca2c9-104">**Applies to:** Exchange Server 2013</span></span>
  
<span data-ttu-id="ca2c9-105">**代理**元素包含安装代理的配置信息。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-105">The **agent** element contains configuration information about an installed agent.</span></span> 
  
- [<span data-ttu-id="ca2c9-106">configuration</span><span class="sxs-lookup"><span data-stu-id="ca2c9-106">configuration</span></span>](configuration.md) 
- [<span data-ttu-id="ca2c9-107">mexRuntime</span><span class="sxs-lookup"><span data-stu-id="ca2c9-107">mexRuntime</span></span>](mexruntime.md)
- [<span data-ttu-id="ca2c9-108">agentList</span><span class="sxs-lookup"><span data-stu-id="ca2c9-108">agentList</span></span>](agentlist.md)
- [<span data-ttu-id="ca2c9-109">代理</span><span class="sxs-lookup"><span data-stu-id="ca2c9-109">agent</span></span>](agent.md)
  
```XML
<agent
        name=""
        baseType=""
        classFactory=""
        assemblyPath=""
        enabled="" />
</agent>
```

<span data-ttu-id="ca2c9-110">**agentType （复杂类型）**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-110">**agentType (complexType)**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="ca2c9-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ca2c9-111">Attributes and elements</span></span>

<span data-ttu-id="ca2c9-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca2c9-113">属性</span><span class="sxs-lookup"><span data-stu-id="ca2c9-113">Attributes</span></span>

|<span data-ttu-id="ca2c9-114">**属性**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-114">**Attribute**</span></span>|<span data-ttu-id="ca2c9-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ca2c9-116">**name**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-116">**name**</span></span> <br/> |<span data-ttu-id="ca2c9-117">代理安装时指定的名称。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-117">The name that was specified when the agent was installed.</span></span> <span data-ttu-id="ca2c9-118">此属性需要包含超过 64 个字符的非空字符串值。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-118">This attribute requires a nonempty string value that contains a maximum of 64 characters.</span></span>  <br/> |
|<span data-ttu-id="ca2c9-119">**baseType**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-119">**baseType**</span></span> <br/> |<span data-ttu-id="ca2c9-120">完整名称，包括代理从中派生的类的命名空间。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-120">The full name, including the namespace, of the class from which the agent derives.</span></span> <span data-ttu-id="ca2c9-121">此属性需要一个非空的 string 值，包含至少一个字符。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-121">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="ca2c9-122">**classFactory**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-122">**classFactory**</span></span> <br/> |<span data-ttu-id="ca2c9-123">包括的命名空间的类的实现代理工厂创建代理的实例的完整名称。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-123">The full name, including the namespace, of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="ca2c9-124">此属性必须包含实现代理工厂创建代理的实例的类的完全限定的名称。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-124">This attribute must contain the fully qualified name of the class that implements the agent factory that creates instances of the agent.</span></span> <span data-ttu-id="ca2c9-125">此类必须从[SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx)或[RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx)类。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-125">This class must derive from either the [SmtpReceiveAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Smtp.SmtpReceiveAgentFactory.aspx) or [RoutingAgentFactory](https://msdn.microsoft.com/library/Microsoft.Exchange.Data.Transport.Routing.RoutingAgentFactory.aspx) class.</span></span>  <br/> |
|<span data-ttu-id="ca2c9-126">**assemblyPath**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-126">**assemblyPath**</span></span> <br/> |<span data-ttu-id="ca2c9-127">包括的代理的包含代码的程序集的文件名的完全限定的路径。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-127">The fully qualified path, including the file name, of the assembly that contains the code for the agent.</span></span> <span data-ttu-id="ca2c9-128">此属性需要一个非空的 string 值，包含至少一个字符。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-128">This attribute requires a nonempty string value that contains at least one character.</span></span>  <br/> |
|<span data-ttu-id="ca2c9-129">**启用**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-129">**enabled**</span></span> <br/> |<span data-ttu-id="ca2c9-130">一个布尔值，该值指示是否启用代理。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-130">A Boolean value that indicates whether the agent is enabled.</span></span> <span data-ttu-id="ca2c9-131">如果启用代理，则值为**true**否则，值为**false**。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-131">The value is **true** if the agent is enabled; otherwise, the value is **false**.</span></span> <span data-ttu-id="ca2c9-132">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-132">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ca2c9-133">子元素</span><span class="sxs-lookup"><span data-stu-id="ca2c9-133">Child elements</span></span>

<span data-ttu-id="ca2c9-134">无。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-134">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca2c9-135">父元素</span><span class="sxs-lookup"><span data-stu-id="ca2c9-135">Parent elements</span></span>

|<span data-ttu-id="ca2c9-136">**元素**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-136">**Element**</span></span>|<span data-ttu-id="ca2c9-137">**说明**</span><span class="sxs-lookup"><span data-stu-id="ca2c9-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca2c9-138">agentList</span><span class="sxs-lookup"><span data-stu-id="ca2c9-138">agentList</span></span>](agentlist.md) <br/> |<span data-ttu-id="ca2c9-139">包含的每个安装代理**代理**元素。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-139">Contains an **agent** element for each installed agent.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="ca2c9-140">元素信息</span><span class="sxs-lookup"><span data-stu-id="ca2c9-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca2c9-141">命名空间</span><span class="sxs-lookup"><span data-stu-id="ca2c9-141">Namespace</span></span>  <br/> |<span data-ttu-id="ca2c9-142">此文件不定义命名空间。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-142">This file does not define a namespace.</span></span>  <br/> |
|<span data-ttu-id="ca2c9-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="ca2c9-143">Schema Name</span></span>  <br/> |<span data-ttu-id="ca2c9-144">不可用。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-144">Not available.</span></span>  <br/> |
|<span data-ttu-id="ca2c9-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="ca2c9-145">Validation File</span></span>  <br/> |<span data-ttu-id="ca2c9-146">不可用。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-146">Not available.</span></span>  <br/> |
|<span data-ttu-id="ca2c9-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="ca2c9-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca2c9-148">False。</span><span class="sxs-lookup"><span data-stu-id="ca2c9-148">False.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca2c9-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ca2c9-149">See also</span></span>

- [<span data-ttu-id="ca2c9-150">Exchange 2013 的代理配置文件元素</span><span class="sxs-lookup"><span data-stu-id="ca2c9-150">Agents configuration file elements for Exchange 2013</span></span>](agents-configuration-file-elements-for-exchange-2013.md)

