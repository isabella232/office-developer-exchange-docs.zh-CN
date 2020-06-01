---
title: RoutingType （EmailAddressType）
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
ms.openlocfilehash: d4229f2857a5c99cc9bb7ff9b9b103de099a0055
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465084"
---
# <a name="routingtype-emailaddresstype"></a><span data-ttu-id="9491c-103">RoutingType （EmailAddressType）</span><span class="sxs-lookup"><span data-stu-id="9491c-103">RoutingType (EmailAddressType)</span></span>

<span data-ttu-id="9491c-104">**RoutingType**元素定义邮箱的地址类型。</span><span class="sxs-lookup"><span data-stu-id="9491c-104">The **RoutingType** element defines the address type for the mailbox.</span></span> 
  
```XML
<RoutingType/>
```

 <span data-ttu-id="9491c-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="9491c-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9491c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9491c-106">Attributes and elements</span></span>

<span data-ttu-id="9491c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9491c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9491c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9491c-108">Attributes</span></span>

<span data-ttu-id="9491c-109">无。</span><span class="sxs-lookup"><span data-stu-id="9491c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9491c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9491c-110">Child elements</span></span>

<span data-ttu-id="9491c-111">无。</span><span class="sxs-lookup"><span data-stu-id="9491c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9491c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9491c-112">Parent elements</span></span>

|<span data-ttu-id="9491c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9491c-113">**Element**</span></span>|<span data-ttu-id="9491c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9491c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9491c-115">ActingAs</span><span class="sxs-lookup"><span data-stu-id="9491c-115">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="9491c-116">标识呼叫者发送的人。</span><span class="sxs-lookup"><span data-stu-id="9491c-116">Identifies who the caller is sending as.</span></span>  <br/> |
|[<span data-ttu-id="9491c-117">邮箱</span><span class="sxs-lookup"><span data-stu-id="9491c-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="9491c-118">标识完全解析的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="9491c-118">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="9491c-119">RoomList</span><span class="sxs-lookup"><span data-stu-id="9491c-119">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="9491c-120">标识会议室列表。</span><span class="sxs-lookup"><span data-stu-id="9491c-120">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9491c-121">文本值</span><span class="sxs-lookup"><span data-stu-id="9491c-121">Text value</span></span>

<span data-ttu-id="9491c-122">该文本值表示路由类型。</span><span class="sxs-lookup"><span data-stu-id="9491c-122">The text value represents a routing type.</span></span> <span data-ttu-id="9491c-123">SMTP 是此元素的典型文本值。</span><span class="sxs-lookup"><span data-stu-id="9491c-123">SMTP is the typical text value for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9491c-124">备注</span><span class="sxs-lookup"><span data-stu-id="9491c-124">Remarks</span></span>

<span data-ttu-id="9491c-125">此元素在[邮箱](mailbox.md)元素中是可选的。</span><span class="sxs-lookup"><span data-stu-id="9491c-125">This element is optional in the [Mailbox](mailbox.md) element.</span></span> <span data-ttu-id="9491c-126">另一个[RoutingType （EmailAddress）](routingtype-emailaddress.md)元素用于可用性操作。</span><span class="sxs-lookup"><span data-stu-id="9491c-126">Another [RoutingType (EmailAddress)](routingtype-emailaddress.md) element is used for Availability operations.</span></span> 
  
<span data-ttu-id="9491c-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9491c-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9491c-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="9491c-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9491c-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="9491c-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9491c-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="9491c-130">Schema Name</span></span>  <br/> |<span data-ttu-id="9491c-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="9491c-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="9491c-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="9491c-132">Validation File</span></span>  <br/> |<span data-ttu-id="9491c-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9491c-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9491c-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="9491c-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="9491c-135">False</span><span class="sxs-lookup"><span data-stu-id="9491c-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9491c-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9491c-136">See also</span></span>



- [<span data-ttu-id="9491c-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9491c-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

