---
title: MaxItems
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4ddba6b8-0f38-42cd-96a1-0d4283f6375b
description: MaxItems 元素指定要返回在请求中的项的最大数。
ms.openlocfilehash: dffb9ba4e29915a65fe2a57b6e7a7b4468028fa1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826384"
---
# <a name="maxitems"></a><span data-ttu-id="ed4a4-103">MaxItems</span><span class="sxs-lookup"><span data-stu-id="ed4a4-103">MaxItems</span></span>

<span data-ttu-id="ed4a4-104">**MaxItems**元素指定要返回在请求中的项的最大数。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-104">The **MaxItems** element specifies the maximum number of items to return in the request.</span></span> 
  
```XML
<MaxItems/>
```

 <span data-ttu-id="ed4a4-105">**int**</span><span class="sxs-lookup"><span data-stu-id="ed4a4-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ed4a4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ed4a4-106">Attributes and elements</span></span>

<span data-ttu-id="ed4a4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ed4a4-108">属性</span><span class="sxs-lookup"><span data-stu-id="ed4a4-108">Attributes</span></span>

<span data-ttu-id="ed4a4-109">无。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ed4a4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ed4a4-110">Child elements</span></span>

<span data-ttu-id="ed4a4-111">无。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ed4a4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ed4a4-112">Parent elements</span></span>

[<span data-ttu-id="ed4a4-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="ed4a4-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="ed4a4-114">文本值</span><span class="sxs-lookup"><span data-stu-id="ed4a4-114">Text value</span></span>

<span data-ttu-id="ed4a4-115">**MaxItems**元素的文本值是请求中返回的项的最大数目。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-115">The text value of the **MaxItems** element is the maximum number of items to return in the request.</span></span> <span data-ttu-id="ed4a4-116">此号码不能小于 0 或大于 200。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-116">This number cannot be less than zero or greater than 200.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ed4a4-117">备注</span><span class="sxs-lookup"><span data-stu-id="ed4a4-117">Remarks</span></span>

<span data-ttu-id="ed4a4-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ed4a4-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ed4a4-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ed4a4-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="ed4a4-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ed4a4-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="ed4a4-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ed4a4-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="ed4a4-122">Schema Name</span></span>  <br/> |<span data-ttu-id="ed4a4-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="ed4a4-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ed4a4-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="ed4a4-124">Validation File</span></span>  <br/> |<span data-ttu-id="ed4a4-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ed4a4-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ed4a4-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="ed4a4-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="ed4a4-127">False</span><span class="sxs-lookup"><span data-stu-id="ed4a4-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed4a4-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ed4a4-128">See also</span></span>



[<span data-ttu-id="ed4a4-129">GetReminders</span><span class="sxs-lookup"><span data-stu-id="ed4a4-129">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="ed4a4-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ed4a4-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

