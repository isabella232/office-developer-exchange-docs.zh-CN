---
title: 域（邮件跟踪）
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
description: Domain 元素表示要搜索的域。
ms.openlocfilehash: 77da9028766881b9bc633e1b3318cd4d70c6b72f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457023"
---
# <a name="domain-message-tracking"></a><span data-ttu-id="7d469-103">域（邮件跟踪）</span><span class="sxs-lookup"><span data-stu-id="7d469-103">Domain (Message Tracking)</span></span>

<span data-ttu-id="7d469-104">**Domain**元素表示要搜索的域。</span><span class="sxs-lookup"><span data-stu-id="7d469-104">The **Domain** element represents the domain to search for.</span></span> 
  
```XML
<Domain/>
```

 <span data-ttu-id="7d469-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="7d469-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d469-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7d469-106">Attributes and elements</span></span>

<span data-ttu-id="7d469-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7d469-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d469-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7d469-108">Attributes</span></span>

<span data-ttu-id="7d469-109">无。</span><span class="sxs-lookup"><span data-stu-id="7d469-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7d469-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7d469-110">Child elements</span></span>

<span data-ttu-id="7d469-111">无。</span><span class="sxs-lookup"><span data-stu-id="7d469-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d469-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7d469-112">Parent elements</span></span>

|<span data-ttu-id="7d469-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7d469-113">**Element**</span></span>|<span data-ttu-id="7d469-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7d469-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d469-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="7d469-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="7d469-116">包含要查找的邮件的类型的条件。</span><span class="sxs-lookup"><span data-stu-id="7d469-116">Contains criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7d469-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7d469-117">Text value</span></span>

<span data-ttu-id="7d469-118">如果使用此元素，则需要一个表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="7d469-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d469-119">说明</span><span class="sxs-lookup"><span data-stu-id="7d469-119">Remarks</span></span>

<span data-ttu-id="7d469-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7d469-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d469-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="7d469-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d469-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="7d469-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7d469-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="7d469-123">Schema Name</span></span>  <br/> |<span data-ttu-id="7d469-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="7d469-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7d469-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="7d469-125">Validation File</span></span>  <br/> |<span data-ttu-id="7d469-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7d469-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7d469-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="7d469-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="7d469-128">False</span><span class="sxs-lookup"><span data-stu-id="7d469-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d469-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7d469-129">See also</span></span>

- [<span data-ttu-id="7d469-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7d469-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

