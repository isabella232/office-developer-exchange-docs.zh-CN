---
title: RoutingType (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RoutingType
api_type:
- schema
ms.assetid: 683216be-9972-4f48-a148-c34bfe7f53e5
description: RoutingType 元素定义邮箱的地址类型。
ms.openlocfilehash: a02c3b5711a657311428d67cccabd9c8c231db67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827256"
---
# <a name="routingtype-emailaddresstype"></a><span data-ttu-id="2e3fe-103">RoutingType (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="2e3fe-103">RoutingType (EmailAddressType)</span></span>

<span data-ttu-id="2e3fe-104">**RoutingType**元素定义邮箱的地址类型。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-104">The **RoutingType** element defines the address type for the mailbox.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="2e3fe-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="2e3fe-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e3fe-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2e3fe-106">Attributes and elements</span></span>

<span data-ttu-id="2e3fe-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e3fe-108">属性</span><span class="sxs-lookup"><span data-stu-id="2e3fe-108">Attributes</span></span>

<span data-ttu-id="2e3fe-109">无。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2e3fe-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2e3fe-110">Child elements</span></span>

<span data-ttu-id="2e3fe-111">无。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2e3fe-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2e3fe-112">Parent elements</span></span>

|<span data-ttu-id="2e3fe-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e3fe-113">**Element**</span></span>|<span data-ttu-id="2e3fe-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e3fe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e3fe-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="2e3fe-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="2e3fe-116">标识用户呼叫者发送为。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="2e3fe-117">Mailbox</span><span class="sxs-lookup"><span data-stu-id="2e3fe-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="2e3fe-118">标识完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-118">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="2e3fe-119">RoomList</span><span class="sxs-lookup"><span data-stu-id="2e3fe-119">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="2e3fe-120">标识会议室的列表。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-120">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2e3fe-121">文本值</span><span class="sxs-lookup"><span data-stu-id="2e3fe-121">Text value</span></span>

<span data-ttu-id="2e3fe-122">文本值表示路由类型。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-122">The text value represents a routing type.</span></span> <span data-ttu-id="2e3fe-123">SMTP 是此元素的典型的文本值。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-123">SMTP is the typical text value for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e3fe-124">注解</span><span class="sxs-lookup"><span data-stu-id="2e3fe-124">Remarks</span></span>

<span data-ttu-id="2e3fe-125">此元素是可选的[邮箱](mailbox.md)元素中。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-125">This element is optional in the [Mailbox](mailbox.md) element.</span></span> <span data-ttu-id="2e3fe-126">可用性操作使用另一个[RoutingType (EmailAddress)](routingtype-emailaddress.md)元素。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-126">Another [RoutingType (EmailAddress)](routingtype-emailaddress.md) element is used for Availability operations.</span></span> 
  
<span data-ttu-id="2e3fe-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2e3fe-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e3fe-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="2e3fe-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e3fe-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="2e3fe-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e3fe-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="2e3fe-130">Schema Name</span></span>  <br/> |<span data-ttu-id="2e3fe-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="2e3fe-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e3fe-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="2e3fe-132">Validation File</span></span>  <br/> |<span data-ttu-id="2e3fe-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2e3fe-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e3fe-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="2e3fe-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e3fe-135">False</span><span class="sxs-lookup"><span data-stu-id="2e3fe-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e3fe-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2e3fe-136">See also</span></span>



- [<span data-ttu-id="2e3fe-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2e3fe-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

