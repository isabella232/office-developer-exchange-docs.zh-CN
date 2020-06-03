---
title: ApplicationRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00003b9b-f8f1-4452-a0af-157f789f8892
description: ApplicationRoles 元素指定调用合作伙伴应用程序对当前呼叫使用的应用程序角色。
ms.openlocfilehash: 8dfe5c745896d02217cbf91375d355954a4e22eb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464698"
---
# <a name="applicationroles"></a><span data-ttu-id="911fd-103">ApplicationRoles</span><span class="sxs-lookup"><span data-stu-id="911fd-103">ApplicationRoles</span></span>

<span data-ttu-id="911fd-104">**ApplicationRoles**元素指定调用合作伙伴应用程序对当前呼叫使用的应用程序角色。</span><span class="sxs-lookup"><span data-stu-id="911fd-104">The **ApplicationRoles** element specifies the application roles that the calling partner application uses for the current call.</span></span> 
  
```XML
<ApplicationRoles>
    <Role></Role>
</ApplicationRoles>
```

 <span data-ttu-id="911fd-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="911fd-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="911fd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="911fd-106">Attributes and elements</span></span>

<span data-ttu-id="911fd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="911fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="911fd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="911fd-108">Attributes</span></span>

<span data-ttu-id="911fd-109">无。</span><span class="sxs-lookup"><span data-stu-id="911fd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="911fd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="911fd-110">Child elements</span></span>

|<span data-ttu-id="911fd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="911fd-111">**Element**</span></span>|<span data-ttu-id="911fd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="911fd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="911fd-113">角色</span><span class="sxs-lookup"><span data-stu-id="911fd-113">Role</span></span>](role.md) <br/> |<span data-ttu-id="911fd-114">指定一个表示管理角色的字符串。</span><span class="sxs-lookup"><span data-stu-id="911fd-114">Specifies a string that represents a management role.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="911fd-115">父元素</span><span class="sxs-lookup"><span data-stu-id="911fd-115">Parent elements</span></span>

|<span data-ttu-id="911fd-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="911fd-116">**Element**</span></span>|<span data-ttu-id="911fd-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="911fd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="911fd-118">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="911fd-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="911fd-119">指定管理角色。</span><span class="sxs-lookup"><span data-stu-id="911fd-119">Specifies the management role.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="911fd-120">备注</span><span class="sxs-lookup"><span data-stu-id="911fd-120">Remarks</span></span>

<span data-ttu-id="911fd-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="911fd-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="911fd-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="911fd-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="911fd-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="911fd-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="911fd-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="911fd-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="911fd-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="911fd-125">Schema Name</span></span>  <br/> |<span data-ttu-id="911fd-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="911fd-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="911fd-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="911fd-127">Validation File</span></span>  <br/> |<span data-ttu-id="911fd-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="911fd-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="911fd-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="911fd-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="911fd-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="911fd-130">See also</span></span>

- [<span data-ttu-id="911fd-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="911fd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

