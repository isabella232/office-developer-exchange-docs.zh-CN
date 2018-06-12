---
title: MakeItemImmutable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de1d2a60-aeeb-4625-8b11-23c42e1e7bae
description: MakeItemImmutable 元素指定一个布尔值，该值指示是否应只读进行项目。
ms.openlocfilehash: 63c05fd3572c7b4ab93fe098d9165a117849ef02
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826337"
---
# <a name="makeitemimmutable"></a><span data-ttu-id="2d055-103">MakeItemImmutable</span><span class="sxs-lookup"><span data-stu-id="2d055-103">MakeItemImmutable</span></span>

<span data-ttu-id="2d055-104">**MakeItemImmutable**元素指定一个布尔值，该值指示是否应只读进行项目。</span><span class="sxs-lookup"><span data-stu-id="2d055-104">The **MakeItemImmutable** element specifies a Boolean value that indicates whether an item should be made read-only.</span></span> 
  
```XML
<MakeItemImmutable>true | false</MakeItemImmutable>
```

 <span data-ttu-id="2d055-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2d055-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2d055-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2d055-106">Attributes and elements</span></span>

<span data-ttu-id="2d055-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2d055-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2d055-108">属性</span><span class="sxs-lookup"><span data-stu-id="2d055-108">Attributes</span></span>

<span data-ttu-id="2d055-109">无。</span><span class="sxs-lookup"><span data-stu-id="2d055-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2d055-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2d055-110">Child elements</span></span>

<span data-ttu-id="2d055-111">无。</span><span class="sxs-lookup"><span data-stu-id="2d055-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2d055-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2d055-112">Parent elements</span></span>

[<span data-ttu-id="2d055-113">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="2d055-113">UpdateItemInRecoverableItems</span></span>](updateiteminrecoverableitems.md)
  
## <a name="text-value"></a><span data-ttu-id="2d055-114">文本值</span><span class="sxs-lookup"><span data-stu-id="2d055-114">Text value</span></span>

<span data-ttu-id="2d055-115">文本值为**true**的**MakeItemImmutable**元素指示项目应只读的。</span><span class="sxs-lookup"><span data-stu-id="2d055-115">A text value of **true** for the **MakeItemImmutable** element indicates that the item should be made read-only.</span></span> <span data-ttu-id="2d055-116">如果值为**false**指示项允许读写访问权限。</span><span class="sxs-lookup"><span data-stu-id="2d055-116">A value of **false** indicates that the item allows read-write access.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2d055-117">备注</span><span class="sxs-lookup"><span data-stu-id="2d055-117">Remarks</span></span>

<span data-ttu-id="2d055-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2d055-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2d055-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2d055-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2d055-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="2d055-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2d055-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="2d055-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2d055-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="2d055-122">Schema name</span></span>  <br/> |<span data-ttu-id="2d055-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="2d055-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2d055-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="2d055-124">Validation file</span></span>  <br/> |<span data-ttu-id="2d055-125">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2d055-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2d055-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="2d055-126">Can be empty</span></span>  <br/> ||
   

