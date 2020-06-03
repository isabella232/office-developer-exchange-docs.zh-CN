---
title: MailboxMoveEnabled （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 73d09137-d3bd-46b3-954a-a358ead07c91
description: MailBoxMoveEnabled 元素表示 MailboxMoveEnabled （）标志。 MailBoxMoveEnabled 元素仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 4072d1c231e7cf109a39445fc44fbbb624f6f3a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530738"
---
# <a name="mailboxmoveenabled-soap"></a><span data-ttu-id="539b5-105">MailboxMoveEnabled （SOAP）</span><span class="sxs-lookup"><span data-stu-id="539b5-105">MailboxMoveEnabled (SOAP)</span></span>

<span data-ttu-id="539b5-106">**MailBoxMoveEnabled**元素表示**MailBoxMoveEnabled （）** 标志。</span><span class="sxs-lookup"><span data-stu-id="539b5-106">The **MailBoxMoveEnabled** element represents the **MailboxMoveEnabled()** flag.</span></span> <span data-ttu-id="539b5-107">**MailBoxMoveEnabled**元素仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="539b5-107">The **MailBoxMoveEnabled** element is for internal use only.</span></span> <span data-ttu-id="539b5-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="539b5-108">This element is not used by clients.</span></span> 
  
```XML
<MailBoxMoveEnabled>true | false</MailBoxMoveEnabled>
```

<span data-ttu-id="539b5-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="539b5-109">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="539b5-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="539b5-110">Attributes and elements</span></span>

<span data-ttu-id="539b5-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="539b5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="539b5-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="539b5-112">Attributes</span></span>

<span data-ttu-id="539b5-113">无。</span><span class="sxs-lookup"><span data-stu-id="539b5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="539b5-114">子元素</span><span class="sxs-lookup"><span data-stu-id="539b5-114">Child elements</span></span>

<span data-ttu-id="539b5-115">无。</span><span class="sxs-lookup"><span data-stu-id="539b5-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="539b5-116">父元素</span><span class="sxs-lookup"><span data-stu-id="539b5-116">Parent elements</span></span>

|<span data-ttu-id="539b5-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="539b5-117">**Element**</span></span>|<span data-ttu-id="539b5-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="539b5-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="539b5-119">OrganizationRelationshipSettings （SOAP）</span><span class="sxs-lookup"><span data-stu-id="539b5-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="539b5-120">表示单个组织的组织关系列表。</span><span class="sxs-lookup"><span data-stu-id="539b5-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="539b5-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="539b5-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="539b5-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="539b5-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="539b5-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="539b5-123">Schema Name</span></span>  <br/> |<span data-ttu-id="539b5-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="539b5-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="539b5-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="539b5-125">Validation File</span></span>  <br/> |<span data-ttu-id="539b5-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="539b5-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="539b5-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="539b5-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="539b5-128">True</span><span class="sxs-lookup"><span data-stu-id="539b5-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="539b5-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="539b5-129">See also</span></span>

- [<span data-ttu-id="539b5-130">GetOrganizationRelationshipSettings 操作（SOAP）</span><span class="sxs-lookup"><span data-stu-id="539b5-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

