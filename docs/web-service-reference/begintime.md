---
title: BeginTime
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2a60c89c-9c21-4041-9593-b244ac1608ef
description: BeginTime 元素指定要查询提醒的时间范围的开始时间。
ms.openlocfilehash: 4f926b8e4931c187cd4d5b97d6182d609bc15a1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463375"
---
# <a name="begintime"></a><span data-ttu-id="53d7f-103">BeginTime</span><span class="sxs-lookup"><span data-stu-id="53d7f-103">BeginTime</span></span>

<span data-ttu-id="53d7f-104">**BeginTime**元素指定要查询提醒的时间范围的开始时间。</span><span class="sxs-lookup"><span data-stu-id="53d7f-104">The **BeginTime** element specifies the beginning of the time span to query for reminders.</span></span> 
  
```XML
<BeginTime/>
```

 <span data-ttu-id="53d7f-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="53d7f-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="53d7f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="53d7f-106">Attributes and elements</span></span>

<span data-ttu-id="53d7f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="53d7f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="53d7f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="53d7f-108">Attributes</span></span>

<span data-ttu-id="53d7f-109">无。</span><span class="sxs-lookup"><span data-stu-id="53d7f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="53d7f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="53d7f-110">Child elements</span></span>

<span data-ttu-id="53d7f-111">无。</span><span class="sxs-lookup"><span data-stu-id="53d7f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="53d7f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="53d7f-112">Parent elements</span></span>

[<span data-ttu-id="53d7f-113">GetReminders</span><span class="sxs-lookup"><span data-stu-id="53d7f-113">GetReminders</span></span>](getreminders.md)
  
## <a name="text-value"></a><span data-ttu-id="53d7f-114">文本值</span><span class="sxs-lookup"><span data-stu-id="53d7f-114">Text value</span></span>

<span data-ttu-id="53d7f-115">**BeginTime**元素的文本值是提醒所针对的项目的开始时间。</span><span class="sxs-lookup"><span data-stu-id="53d7f-115">The text value of the **BeginTime** element is the beginning time of the item the reminder is for.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="53d7f-116">备注</span><span class="sxs-lookup"><span data-stu-id="53d7f-116">Remarks</span></span>

<span data-ttu-id="53d7f-117">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="53d7f-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="53d7f-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="53d7f-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="53d7f-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="53d7f-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53d7f-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="53d7f-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="53d7f-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="53d7f-121">Schema Name</span></span>  <br/> |<span data-ttu-id="53d7f-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="53d7f-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="53d7f-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="53d7f-123">Validation File</span></span>  <br/> |<span data-ttu-id="53d7f-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="53d7f-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="53d7f-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="53d7f-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="53d7f-126">False</span><span class="sxs-lookup"><span data-stu-id="53d7f-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="53d7f-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="53d7f-127">See also</span></span>



[<span data-ttu-id="53d7f-128">GetReminders</span><span class="sxs-lookup"><span data-stu-id="53d7f-128">GetReminders</span></span>](getreminders.md)


- [<span data-ttu-id="53d7f-129">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="53d7f-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

