---
title: ApplicationRoles
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 00003b9b-f8f1-4452-a0af-157f789f8892
description: ApplicationRoles 元素指定当前呼叫的呼叫的合作伙伴应用程序使用的应用程序角色。
ms.openlocfilehash: ff32b693dae573416263bcb7c0fbb552a933b8d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753160"
---
# <a name="applicationroles"></a><span data-ttu-id="2292a-103">ApplicationRoles</span><span class="sxs-lookup"><span data-stu-id="2292a-103">ApplicationRoles</span></span>

<span data-ttu-id="2292a-104">**ApplicationRoles**元素指定当前呼叫的呼叫的合作伙伴应用程序使用的应用程序角色。</span><span class="sxs-lookup"><span data-stu-id="2292a-104">The **ApplicationRoles** element specifies the application roles that the calling partner application uses for the current call.</span></span> 
  
```XML
<ApplicationRoles>
    <Role></Role>
</ApplicationRoles>
```

 <span data-ttu-id="2292a-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="2292a-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2292a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2292a-106">Attributes and elements</span></span>

<span data-ttu-id="2292a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2292a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2292a-108">属性</span><span class="sxs-lookup"><span data-stu-id="2292a-108">Attributes</span></span>

<span data-ttu-id="2292a-109">无。</span><span class="sxs-lookup"><span data-stu-id="2292a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2292a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2292a-110">Child elements</span></span>

|<span data-ttu-id="2292a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="2292a-111">**Element**</span></span>|<span data-ttu-id="2292a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="2292a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2292a-113">Role</span><span class="sxs-lookup"><span data-stu-id="2292a-113">Role</span></span>](role.md) <br/> |<span data-ttu-id="2292a-114">指定一个字符串，表示管理角色。</span><span class="sxs-lookup"><span data-stu-id="2292a-114">Specifies a string that represents a management role.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="2292a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="2292a-115">Parent elements</span></span>

|<span data-ttu-id="2292a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="2292a-116">**Element**</span></span>|<span data-ttu-id="2292a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="2292a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2292a-118">ManagementRole</span><span class="sxs-lookup"><span data-stu-id="2292a-118">ManagementRole</span></span>](managementrole.md) <br/> |<span data-ttu-id="2292a-119">指定的管理角色。</span><span class="sxs-lookup"><span data-stu-id="2292a-119">Specifies the management role.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2292a-120">备注</span><span class="sxs-lookup"><span data-stu-id="2292a-120">Remarks</span></span>

<span data-ttu-id="2292a-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2292a-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2292a-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2292a-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2292a-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="2292a-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2292a-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="2292a-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2292a-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="2292a-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2292a-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="2292a-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="2292a-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="2292a-127">Validation File</span></span>  <br/> |<span data-ttu-id="2292a-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="2292a-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="2292a-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="2292a-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2292a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2292a-130">See also</span></span>

- [<span data-ttu-id="2292a-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2292a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

