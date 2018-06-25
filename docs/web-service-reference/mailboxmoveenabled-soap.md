---
title: MailboxMoveEnabled (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 73d09137-d3bd-46b3-954a-a358ead07c91
description: MailBoxMoveEnabled 元素均表示 MailboxMoveEnabled() 标志。 MailBoxMoveEnabled 元素是仅供内部使用。 客户端不使用此元素。
ms.openlocfilehash: 9ba4f49cbd43ab8ca24d9597f69b55c448fd9263
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826292"
---
# <a name="mailboxmoveenabled-soap"></a><span data-ttu-id="71e8c-105">MailboxMoveEnabled (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71e8c-105">MailboxMoveEnabled (SOAP)</span></span>

<span data-ttu-id="71e8c-106">**MailBoxMoveEnabled**元素均表示**MailboxMoveEnabled()** 标志。</span><span class="sxs-lookup"><span data-stu-id="71e8c-106">The **MailBoxMoveEnabled** element represents the **MailboxMoveEnabled()** flag.</span></span> <span data-ttu-id="71e8c-107">**MailBoxMoveEnabled**元素是仅供内部使用。</span><span class="sxs-lookup"><span data-stu-id="71e8c-107">The **MailBoxMoveEnabled** element is for internal use only.</span></span> <span data-ttu-id="71e8c-108">客户端不使用此元素。</span><span class="sxs-lookup"><span data-stu-id="71e8c-108">This element is not used by clients.</span></span> 
  
```XML
<MailBoxMoveEnabled>true | false</MailBoxMoveEnabled>
```

<span data-ttu-id="71e8c-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="71e8c-109">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="71e8c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="71e8c-110">Attributes and elements</span></span>

<span data-ttu-id="71e8c-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="71e8c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="71e8c-112">属性</span><span class="sxs-lookup"><span data-stu-id="71e8c-112">Attributes</span></span>

<span data-ttu-id="71e8c-113">无。</span><span class="sxs-lookup"><span data-stu-id="71e8c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="71e8c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="71e8c-114">Child elements</span></span>

<span data-ttu-id="71e8c-115">无。</span><span class="sxs-lookup"><span data-stu-id="71e8c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="71e8c-116">父元素</span><span class="sxs-lookup"><span data-stu-id="71e8c-116">Parent elements</span></span>

|<span data-ttu-id="71e8c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="71e8c-117">**Element**</span></span>|<span data-ttu-id="71e8c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="71e8c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="71e8c-119">OrganizationRelationshipSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71e8c-119">OrganizationRelationshipSettings (SOAP)</span></span>](organizationrelationshipsettings-soap.md) <br/> |<span data-ttu-id="71e8c-120">代表单个组织的组织关系的列表。</span><span class="sxs-lookup"><span data-stu-id="71e8c-120">Represents a list of organization relationships for a single organization.</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="71e8c-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="71e8c-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="71e8c-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="71e8c-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="71e8c-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="71e8c-123">Schema Name</span></span>  <br/> |<span data-ttu-id="71e8c-124">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="71e8c-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="71e8c-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="71e8c-125">Validation File</span></span>  <br/> |<span data-ttu-id="71e8c-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="71e8c-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="71e8c-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="71e8c-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="71e8c-128">True</span><span class="sxs-lookup"><span data-stu-id="71e8c-128">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="71e8c-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="71e8c-129">See also</span></span>

- [<span data-ttu-id="71e8c-130">GetOrganizationRelationshipSettings 操作 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="71e8c-130">GetOrganizationRelationshipSettings operation (SOAP)</span></span>](getorganizationrelationshipsettings-operation-soap.md)

