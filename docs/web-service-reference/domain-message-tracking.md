---
title: 域 （邮件跟踪）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Domain
api_type:
- schema
ms.assetid: 4e8e9efa-8885-4ca5-bf90-424e63768dc3
description: 域元素均表示要搜索的域。
ms.openlocfilehash: dc161557b59acc580d918f2e196457714bce4ba9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753968"
---
# <a name="domain-message-tracking"></a><span data-ttu-id="07b9e-103">域 （邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="07b9e-103">Domain (Message Tracking)</span></span>

<span data-ttu-id="07b9e-104">**域**元素均表示要搜索的域。</span><span class="sxs-lookup"><span data-stu-id="07b9e-104">The **Domain** element represents the domain to search for.</span></span> 
  
```XML
<Domain/>
```

 <span data-ttu-id="07b9e-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="07b9e-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07b9e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="07b9e-106">Attributes and elements</span></span>

<span data-ttu-id="07b9e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="07b9e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07b9e-108">属性</span><span class="sxs-lookup"><span data-stu-id="07b9e-108">Attributes</span></span>

<span data-ttu-id="07b9e-109">无。</span><span class="sxs-lookup"><span data-stu-id="07b9e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07b9e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="07b9e-110">Child elements</span></span>

<span data-ttu-id="07b9e-111">无。</span><span class="sxs-lookup"><span data-stu-id="07b9e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="07b9e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="07b9e-112">Parent elements</span></span>

|<span data-ttu-id="07b9e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="07b9e-113">**Element**</span></span>|<span data-ttu-id="07b9e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="07b9e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07b9e-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="07b9e-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="07b9e-116">包含要查找的邮件的类型的条件。</span><span class="sxs-lookup"><span data-stu-id="07b9e-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="07b9e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="07b9e-117">Text value</span></span>

<span data-ttu-id="07b9e-118">如果使用此元素，则需要用于表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="07b9e-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="07b9e-119">备注</span><span class="sxs-lookup"><span data-stu-id="07b9e-119">Remarks</span></span>

<span data-ttu-id="07b9e-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="07b9e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07b9e-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="07b9e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07b9e-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="07b9e-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="07b9e-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="07b9e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="07b9e-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="07b9e-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="07b9e-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="07b9e-125">Validation File</span></span>  <br/> |<span data-ttu-id="07b9e-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="07b9e-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="07b9e-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="07b9e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="07b9e-128">False</span><span class="sxs-lookup"><span data-stu-id="07b9e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07b9e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="07b9e-129">See also</span></span>

- [<span data-ttu-id="07b9e-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="07b9e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

