---
title: DeploymentId （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: DeploymentId 元素唯一标识 Microsoft Exchange Server 2007 林。
ms.openlocfilehash: 4986a3404763e88fb3e84d52a5d30d54c810f93a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467919"
---
# <a name="deploymentid-pox"></a><span data-ttu-id="78f2f-103">DeploymentId （POX）</span><span class="sxs-lookup"><span data-stu-id="78f2f-103">DeploymentId (POX)</span></span>

<span data-ttu-id="78f2f-104">**DeploymentId**元素唯一标识 Microsoft Exchange Server 2007 林。</span><span class="sxs-lookup"><span data-stu-id="78f2f-104">The **DeploymentId** element uniquely identifies the Microsoft Exchange Server 2007 forest.</span></span> 
  
- [<span data-ttu-id="78f2f-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="78f2f-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)  
- [<span data-ttu-id="78f2f-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="78f2f-106">Response (POX)</span></span>](response-pox.md) 
- [<span data-ttu-id="78f2f-107">User （POX）</span><span class="sxs-lookup"><span data-stu-id="78f2f-107">User (POX)</span></span>](user-pox.md)  
- [<span data-ttu-id="78f2f-108">DeploymentId （POX）</span><span class="sxs-lookup"><span data-stu-id="78f2f-108">DeploymentId (POX)</span></span>](deploymentid-pox.md)
  
```xml
<DeploymentId/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="78f2f-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="78f2f-109">Attributes and elements</span></span>

<span data-ttu-id="78f2f-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="78f2f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78f2f-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="78f2f-111">Attributes</span></span>

<span data-ttu-id="78f2f-112">无。</span><span class="sxs-lookup"><span data-stu-id="78f2f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78f2f-113">子元素</span><span class="sxs-lookup"><span data-stu-id="78f2f-113">Child elements</span></span>

<span data-ttu-id="78f2f-114">无。</span><span class="sxs-lookup"><span data-stu-id="78f2f-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="78f2f-115">父元素</span><span class="sxs-lookup"><span data-stu-id="78f2f-115">Parent elements</span></span>

|<span data-ttu-id="78f2f-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="78f2f-116">**Element**</span></span>|<span data-ttu-id="78f2f-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="78f2f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78f2f-118">User （POX）</span><span class="sxs-lookup"><span data-stu-id="78f2f-118">User (POX)</span></span>](user-pox.md) <br/> |<span data-ttu-id="78f2f-119">提供用户特定的信息。</span><span class="sxs-lookup"><span data-stu-id="78f2f-119">Provides user-specific information.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="78f2f-120">文本值</span><span class="sxs-lookup"><span data-stu-id="78f2f-120">Text value</span></span>

<span data-ttu-id="78f2f-121">该文本值唯一标识采用 GUID 格式的 Exchange 2007 林。</span><span class="sxs-lookup"><span data-stu-id="78f2f-121">The text value uniquely identifies the Exchange 2007 forest in GUID format.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78f2f-122">备注</span><span class="sxs-lookup"><span data-stu-id="78f2f-122">Remarks</span></span>

<span data-ttu-id="78f2f-123">如果您卸载然后重新安装 Exchange 2007 并使用相同的服务器名称，则**DeploymentId**值将更改。</span><span class="sxs-lookup"><span data-stu-id="78f2f-123">If you uninstall and then reinstall Exchange 2007 and you use the same server name, the **DeploymentId** value changes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78f2f-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="78f2f-124">See also</span></span>

- [<span data-ttu-id="78f2f-125">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="78f2f-125">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

