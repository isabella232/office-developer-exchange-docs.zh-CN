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
description: IsUMEnabled 元素指示是否将邮箱启用统一消息。
ms.openlocfilehash: 5f4d59c5497158e5afbc8bb5db4900bd129df50b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826113"
---
# <a name="isumenabled-um-web-service"></a><span data-ttu-id="69669-103">IsUMEnabled （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="69669-103">IsUMEnabled (UM web service)</span></span>

<span data-ttu-id="69669-104">**IsUMEnabled**元素指示是否将邮箱启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="69669-104">The **IsUMEnabled** element indicates whether a mailbox is enabled for Unified Messaging.</span></span> 
  
```xml
<IsUMEnabled/>
```

 <span data-ttu-id="69669-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="69669-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69669-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="69669-106">Attributes and elements</span></span>

<span data-ttu-id="69669-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="69669-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69669-108">属性</span><span class="sxs-lookup"><span data-stu-id="69669-108">Attributes</span></span>

<span data-ttu-id="69669-109">无。</span><span class="sxs-lookup"><span data-stu-id="69669-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69669-110">子元素</span><span class="sxs-lookup"><span data-stu-id="69669-110">Child elements</span></span>

<span data-ttu-id="69669-111">无。</span><span class="sxs-lookup"><span data-stu-id="69669-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69669-112">父元素</span><span class="sxs-lookup"><span data-stu-id="69669-112">Parent elements</span></span>

<span data-ttu-id="69669-113">无。</span><span class="sxs-lookup"><span data-stu-id="69669-113">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="69669-114">文本值</span><span class="sxs-lookup"><span data-stu-id="69669-114">Text value</span></span>

<span data-ttu-id="69669-115">如果此元素是包含，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="69669-115">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="69669-116">值为**true**指示邮箱启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="69669-116">A value of **true** indicates that the mailbox is enabled for Unified Messaging.</span></span> <span data-ttu-id="69669-117">如果值为**false**意味着邮箱未启用统一消息。</span><span class="sxs-lookup"><span data-stu-id="69669-117">A value of **false** means that the mailbox is not enabled for Unified Messaging.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="69669-118">注解</span><span class="sxs-lookup"><span data-stu-id="69669-118">Remarks</span></span>

<span data-ttu-id="69669-119">若要确定是否将邮箱启用统一消息，请使用[IsUMEnabled 操作 （UM web 服务）](isumenabled-operation-um-web-service.md)。</span><span class="sxs-lookup"><span data-stu-id="69669-119">To determine whether a mailbox is enabled for Unified Messaging, use the [IsUMEnabled operation (UM web service)](isumenabled-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69669-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="69669-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69669-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="69669-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="69669-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="69669-122">Schema Name</span></span>  <br/> |<span data-ttu-id="69669-123">邮件</span><span class="sxs-lookup"><span data-stu-id="69669-123">Messages</span></span>  <br/> |
|<span data-ttu-id="69669-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="69669-124">Validation File</span></span>  <br/> |<span data-ttu-id="69669-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="69669-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="69669-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="69669-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="69669-127">False</span><span class="sxs-lookup"><span data-stu-id="69669-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69669-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="69669-128">See also</span></span>



[<span data-ttu-id="69669-129">IsUMEnabled 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="69669-129">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)


[<span data-ttu-id="69669-130">Exchange 的统一的消息 web 服务 XML 元素</span><span class="sxs-lookup"><span data-stu-id="69669-130">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

