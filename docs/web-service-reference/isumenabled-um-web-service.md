---
title: IsUMEnabled （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: IsUMEnabled 元素指示是否为邮箱启用统一消息。
ms.openlocfilehash: ea5bde677c62664acad8afd5c8142e96d82b7a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458227"
---
# <a name="isumenabled-um-web-service"></a><span data-ttu-id="d1b9b-103">IsUMEnabled （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="d1b9b-103">IsUMEnabled (UM web service)</span></span>

<span data-ttu-id="d1b9b-104">**IsUMEnabled**元素指示是否为邮箱启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-104">The **IsUMEnabled** element indicates whether a mailbox is enabled for Unified Messaging.</span></span> 
  
```xml
<IsUMEnabled/>
```

 <span data-ttu-id="d1b9b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="d1b9b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1b9b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d1b9b-106">Attributes and elements</span></span>

<span data-ttu-id="d1b9b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1b9b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d1b9b-108">Attributes</span></span>

<span data-ttu-id="d1b9b-109">无。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1b9b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d1b9b-110">Child elements</span></span>

<span data-ttu-id="d1b9b-111">无。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d1b9b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d1b9b-112">Parent elements</span></span>

<span data-ttu-id="d1b9b-113">无。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-113">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d1b9b-114">文本值</span><span class="sxs-lookup"><span data-stu-id="d1b9b-114">Text value</span></span>

<span data-ttu-id="d1b9b-115">如果包含此元素，则需要一个表示布尔值的文本值。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-115">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="d1b9b-116">**如果值为 true** ，则表示已为邮箱启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-116">A value of **true** indicates that the mailbox is enabled for Unified Messaging.</span></span> <span data-ttu-id="d1b9b-117">**如果值为 false** ，则表示没有为邮箱启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-117">A value of **false** means that the mailbox is not enabled for Unified Messaging.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1b9b-118">备注</span><span class="sxs-lookup"><span data-stu-id="d1b9b-118">Remarks</span></span>

<span data-ttu-id="d1b9b-119">若要确定是否为统一消息启用了邮箱，请使用[IsUMEnabled 操作（UM web 服务）](isumenabled-operation-um-web-service.md)。</span><span class="sxs-lookup"><span data-stu-id="d1b9b-119">To determine whether a mailbox is enabled for Unified Messaging, use the [IsUMEnabled operation (UM web service)](isumenabled-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1b9b-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="d1b9b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1b9b-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="d1b9b-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d1b9b-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="d1b9b-122">Schema Name</span></span>  <br/> |<span data-ttu-id="d1b9b-123">邮件</span><span class="sxs-lookup"><span data-stu-id="d1b9b-123">Messages</span></span>  <br/> |
|<span data-ttu-id="d1b9b-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="d1b9b-124">Validation File</span></span>  <br/> |<span data-ttu-id="d1b9b-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d1b9b-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d1b9b-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="d1b9b-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1b9b-127">False</span><span class="sxs-lookup"><span data-stu-id="d1b9b-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1b9b-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d1b9b-128">See also</span></span>



[<span data-ttu-id="d1b9b-129">IsUMEnabled 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="d1b9b-129">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)


[<span data-ttu-id="d1b9b-130">Exchange 的统一消息 web 服务 XML 元素</span><span class="sxs-lookup"><span data-stu-id="d1b9b-130">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

