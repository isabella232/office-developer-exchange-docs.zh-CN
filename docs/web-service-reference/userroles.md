---
title: Userroles.xml
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: be003e12-3496-468d-a61c-48af0b819654
description: Userroles.xml 元素指定呼叫用户的用户角色，或调用合作伙伴应用程序所充当的用户要应用于当前呼叫的用户角色。
ms.openlocfilehash: 5155b82781321b16d1b58fdcaffe7b8cf2372717
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467128"
---
# <a name="userroles"></a><span data-ttu-id="e12f6-103">Userroles.xml</span><span class="sxs-lookup"><span data-stu-id="e12f6-103">UserRoles</span></span>

<span data-ttu-id="e12f6-104">**Userroles.xml**元素指定呼叫用户的用户角色，或调用合作伙伴应用程序所充当的用户要应用于当前呼叫的用户角色。</span><span class="sxs-lookup"><span data-stu-id="e12f6-104">The **UserRoles** element specifies the user roles that the calling user, or the user that the calling partner application is acting as, wants to apply to the current call.</span></span> 
  
```XML
<UserRoles>
   <Role/>
</UserRoles>
```

 <span data-ttu-id="e12f6-105">**NonEmptyArrayOfRoleType**</span><span class="sxs-lookup"><span data-stu-id="e12f6-105">**NonEmptyArrayOfRoleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e12f6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e12f6-106">Attributes and elements</span></span>

<span data-ttu-id="e12f6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e12f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e12f6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e12f6-108">Attributes</span></span>

<span data-ttu-id="e12f6-109">无。</span><span class="sxs-lookup"><span data-stu-id="e12f6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e12f6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e12f6-110">Child elements</span></span>

[<span data-ttu-id="e12f6-111">角色</span><span class="sxs-lookup"><span data-stu-id="e12f6-111">Role</span></span>](role.md)
  
### <a name="parent-elements"></a><span data-ttu-id="e12f6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e12f6-112">Parent elements</span></span>

[<span data-ttu-id="e12f6-113">Get-managementrole</span><span class="sxs-lookup"><span data-stu-id="e12f6-113">ManagementRole</span></span>](managementrole.md)
  
## <a name="remarks"></a><span data-ttu-id="e12f6-114">备注</span><span class="sxs-lookup"><span data-stu-id="e12f6-114">Remarks</span></span>

<span data-ttu-id="e12f6-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e12f6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e12f6-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e12f6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e12f6-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="e12f6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e12f6-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="e12f6-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e12f6-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="e12f6-119">Schema name</span></span>  <br/> |<span data-ttu-id="e12f6-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="e12f6-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="e12f6-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="e12f6-121">Validation file</span></span>  <br/> |<span data-ttu-id="e12f6-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e12f6-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e12f6-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="e12f6-123">Can be empty</span></span>  <br/> ||
   

