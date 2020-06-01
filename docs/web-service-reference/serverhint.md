---
title: ServerHint
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerHint
api_type:
- schema
ms.assetid: 5ac60472-a565-43d1-a5fb-8be0c9511f82
description: ServerHint 元素表示跟踪远程站点或林中的邮件的起始点。
ms.openlocfilehash: 76a719901f4e4d1da67ce377ab8b73e4a4592dc4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461987"
---
# <a name="serverhint"></a><span data-ttu-id="d2d6e-103">ServerHint</span><span class="sxs-lookup"><span data-stu-id="d2d6e-103">ServerHint</span></span>

<span data-ttu-id="d2d6e-104">**ServerHint**元素表示跟踪远程站点或林中的邮件的起始点。</span><span class="sxs-lookup"><span data-stu-id="d2d6e-104">The **ServerHint** element represents the starting point for tracking a message in a remote site or forest.</span></span> 
  
```xml
<ServerHint/>
```

 <span data-ttu-id="d2d6e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="d2d6e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d2d6e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d2d6e-106">Attributes and elements</span></span>

<span data-ttu-id="d2d6e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d2d6e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d2d6e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d2d6e-108">Attributes</span></span>

<span data-ttu-id="d2d6e-109">无。</span><span class="sxs-lookup"><span data-stu-id="d2d6e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d2d6e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d2d6e-110">Child elements</span></span>

<span data-ttu-id="d2d6e-111">无。</span><span class="sxs-lookup"><span data-stu-id="d2d6e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d2d6e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d2d6e-112">Parent elements</span></span>

|<span data-ttu-id="d2d6e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d2d6e-113">**Element**</span></span>|<span data-ttu-id="d2d6e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d2d6e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d2d6e-115">FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="d2d6e-115">FindMessageTrackingReport</span></span>](findmessagetrackingreport.md) <br/> |<span data-ttu-id="d2d6e-116">指定要查找的邮件类型的条件。</span><span class="sxs-lookup"><span data-stu-id="d2d6e-116">Specifies criteria for the types of messages to find.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d2d6e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="d2d6e-117">Text value</span></span>

<span data-ttu-id="d2d6e-118">无。</span><span class="sxs-lookup"><span data-stu-id="d2d6e-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2d6e-119">说明</span><span class="sxs-lookup"><span data-stu-id="d2d6e-119">Remarks</span></span>

<span data-ttu-id="d2d6e-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d2d6e-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d2d6e-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="d2d6e-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d2d6e-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="d2d6e-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d2d6e-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="d2d6e-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d2d6e-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="d2d6e-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d2d6e-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="d2d6e-125">Validation File</span></span>  <br/> |<span data-ttu-id="d2d6e-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d2d6e-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d2d6e-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="d2d6e-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d2d6e-128">False</span><span class="sxs-lookup"><span data-stu-id="d2d6e-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d2d6e-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2d6e-129">See also</span></span>



[<span data-ttu-id="d2d6e-130">FindMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="d2d6e-130">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)


- [<span data-ttu-id="d2d6e-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d2d6e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

