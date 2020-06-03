---
title: MaxItems
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4ddba6b8-0f38-42cd-96a1-0d4283f6375b
description: MaxItems 元素指定要在请求中返回的最大项目数。
ms.openlocfilehash: f16e9d46b59c0f562aabd5383f7f445d93414f68
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461742"
---
# <a name="maxitems"></a><span data-ttu-id="71544-103">MaxItems</span><span class="sxs-lookup"><span data-stu-id="71544-103">MaxItems</span></span>

<span data-ttu-id="71544-104">**MaxItems**元素指定要在请求中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="71544-104">The **MaxItems** element specifies the maximum number of items to return in the request.</span></span> 
  
```XML
<MaxItems/>
```

 <span data-ttu-id="71544-105">**int**</span><span class="sxs-lookup"><span data-stu-id="71544-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="71544-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="71544-106">Attributes and elements</span></span>

<span data-ttu-id="71544-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="71544-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="71544-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="71544-108">Attributes</span></span>

<span data-ttu-id="71544-109">无。</span><span class="sxs-lookup"><span data-stu-id="71544-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="71544-110">子元素</span><span class="sxs-lookup"><span data-stu-id="71544-110">Child elements</span></span>

<span data-ttu-id="71544-111">无。</span><span class="sxs-lookup"><span data-stu-id="71544-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="71544-112">父元素</span><span class="sxs-lookup"><span data-stu-id="71544-112">Parent elements</span></span>

[<span data-ttu-id="71544-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="71544-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="71544-114">文本值</span><span class="sxs-lookup"><span data-stu-id="71544-114">Text value</span></span>

<span data-ttu-id="71544-115">**MaxItems**元素的文本值是请求中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="71544-115">The text value of the **MaxItems** element is the maximum number of items to return in the request.</span></span> <span data-ttu-id="71544-116">此数字不能小于零或大于200。</span><span class="sxs-lookup"><span data-stu-id="71544-116">This number cannot be less than zero or greater than 200.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="71544-117">备注</span><span class="sxs-lookup"><span data-stu-id="71544-117">Remarks</span></span>

<span data-ttu-id="71544-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="71544-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="71544-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="71544-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="71544-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="71544-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71544-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="71544-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="71544-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="71544-122">Schema Name</span></span>  <br/> |<span data-ttu-id="71544-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="71544-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="71544-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="71544-124">Validation File</span></span>  <br/> |<span data-ttu-id="71544-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="71544-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="71544-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="71544-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="71544-127">False</span><span class="sxs-lookup"><span data-stu-id="71544-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71544-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="71544-128">See also</span></span>



[<span data-ttu-id="71544-129">GetReminders</span><span class="sxs-lookup"><span data-stu-id="71544-129">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="71544-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="71544-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

