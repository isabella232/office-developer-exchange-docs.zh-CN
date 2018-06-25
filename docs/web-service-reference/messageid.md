---
title: MessageId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MessageId
api_type:
- schema
ms.assetid: 3b038ad5-7752-4ed8-9769-a9f1d86c8fef
description: MessageId 元素均表示要搜索的邮件标识。
ms.openlocfilehash: 66a7298db2d0052e5653742f781aa3f423b427d5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826455"
---
# <a name="messageid"></a><span data-ttu-id="ef4b1-103">MessageId</span><span class="sxs-lookup"><span data-stu-id="ef4b1-103">MessageId</span></span>

<span data-ttu-id="ef4b1-104">**MessageId**元素均表示要搜索的邮件标识。</span><span class="sxs-lookup"><span data-stu-id="ef4b1-104">The **MessageId** element represents the message identification to search for.</span></span> 
  
```XML
<MessageId/>
```

 <span data-ttu-id="ef4b1-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef4b1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ef4b1-106">Attributes and elements</span></span>

<span data-ttu-id="ef4b1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ef4b1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef4b1-108">属性</span><span class="sxs-lookup"><span data-stu-id="ef4b1-108">Attributes</span></span>

<span data-ttu-id="ef4b1-109">无。</span><span class="sxs-lookup"><span data-stu-id="ef4b1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef4b1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ef4b1-110">Child elements</span></span>

<span data-ttu-id="ef4b1-111">无。</span><span class="sxs-lookup"><span data-stu-id="ef4b1-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef4b1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ef4b1-112">Parent elements</span></span>

|<span data-ttu-id="ef4b1-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-113">**Element**</span></span>|<span data-ttu-id="ef4b1-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ef4b1-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ef4b1-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="ef4b1-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="ef4b1-116">指定条件的邮件，以查找的类型。</span><span class="sxs-lookup"><span data-stu-id="ef4b1-116">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ef4b1-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ef4b1-117">Text value</span></span>

<span data-ttu-id="ef4b1-118">如果使用此元素，则需要用于表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="ef4b1-118">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef4b1-119">备注</span><span class="sxs-lookup"><span data-stu-id="ef4b1-119">Remarks</span></span>

<span data-ttu-id="ef4b1-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ef4b1-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef4b1-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="ef4b1-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef4b1-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="ef4b1-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef4b1-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="ef4b1-123">Schema Name</span></span>  <br/> |<span data-ttu-id="ef4b1-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="ef4b1-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef4b1-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="ef4b1-125">Validation File</span></span>  <br/> |<span data-ttu-id="ef4b1-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef4b1-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef4b1-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="ef4b1-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="ef4b1-128">False</span><span class="sxs-lookup"><span data-stu-id="ef4b1-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef4b1-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ef4b1-129">See also</span></span>



- [<span data-ttu-id="ef4b1-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ef4b1-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

