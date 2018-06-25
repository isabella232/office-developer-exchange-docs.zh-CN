---
title: SetClientExtension
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10d0739c-2591-4768-935c-b131b26e974d
description: SetClientExtension 元素包含一个请求设置客户端扩展。
ms.openlocfilehash: 9e0a2926e25d74657ddf8a50ec88e77af0fc4ea1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827398"
---
# <a name="setclientextension"></a><span data-ttu-id="7e26c-103">SetClientExtension</span><span class="sxs-lookup"><span data-stu-id="7e26c-103">SetClientExtension</span></span>

<span data-ttu-id="7e26c-104">**SetClientExtension**元素包含一个请求设置客户端扩展。</span><span class="sxs-lookup"><span data-stu-id="7e26c-104">The **SetClientExtension** element contains a request to set a client extension.</span></span> 
  
```XML
<SetClientExtension>
   <Actions/>
</SetClientExtension>
```

 <span data-ttu-id="7e26c-105">**SetClientExtensionType**</span><span class="sxs-lookup"><span data-stu-id="7e26c-105">**SetClientExtensionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7e26c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7e26c-106">Attributes and elements</span></span>

<span data-ttu-id="7e26c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7e26c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7e26c-108">属性</span><span class="sxs-lookup"><span data-stu-id="7e26c-108">Attributes</span></span>

<span data-ttu-id="7e26c-109">无。</span><span class="sxs-lookup"><span data-stu-id="7e26c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7e26c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7e26c-110">Child elements</span></span>

[<span data-ttu-id="7e26c-111">操作 (ArrayOfSetClientExtensionActionsType)</span><span class="sxs-lookup"><span data-stu-id="7e26c-111">Actions (ArrayOfSetClientExtensionActionsType)</span></span>](actions-arrayofsetclientextensionactionstype.md)
  
### <a name="parent-elements"></a><span data-ttu-id="7e26c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7e26c-112">Parent elements</span></span>

<span data-ttu-id="7e26c-113">无。</span><span class="sxs-lookup"><span data-stu-id="7e26c-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e26c-114">备注</span><span class="sxs-lookup"><span data-stu-id="7e26c-114">Remarks</span></span>

<span data-ttu-id="7e26c-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7e26c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7e26c-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7e26c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7e26c-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="7e26c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7e26c-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="7e26c-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7e26c-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="7e26c-119">Schema name</span></span>  <br/> |<span data-ttu-id="7e26c-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="7e26c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7e26c-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="7e26c-121">Validation file</span></span>  <br/> |<span data-ttu-id="7e26c-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7e26c-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7e26c-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="7e26c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="7e26c-124">false</span><span class="sxs-lookup"><span data-stu-id="7e26c-124">false</span></span>  <br/> |
   

