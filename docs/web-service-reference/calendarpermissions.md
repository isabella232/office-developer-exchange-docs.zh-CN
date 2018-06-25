---
title: CalendarPermissions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissions
api_type:
- schema
ms.assetid: 9b659d83-45fb-42a2-b052-5bc4dbe3854d
description: CalendarPermissions 元素包含数组的日历文件夹的权限。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 3dee635e4449cbb3717f5d2fab8838f3e43102a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753421"
---
# <a name="calendarpermissions"></a><span data-ttu-id="52752-104">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="52752-104">CalendarPermissions</span></span>

<span data-ttu-id="52752-105">**CalendarPermissions**元素包含数组的日历文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="52752-105">The **CalendarPermissions** element contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="52752-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="52752-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissions>
   <PermissionSet/>
</CalendarPermissions>
```

 <span data-ttu-id="52752-107">**ArrayOfCalendarPermissionsType**</span><span class="sxs-lookup"><span data-stu-id="52752-107">**ArrayOfCalendarPermissionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52752-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52752-108">Attributes and elements</span></span>

<span data-ttu-id="52752-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52752-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52752-110">属性</span><span class="sxs-lookup"><span data-stu-id="52752-110">Attributes</span></span>

<span data-ttu-id="52752-111">无。</span><span class="sxs-lookup"><span data-stu-id="52752-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="52752-112">子元素</span><span class="sxs-lookup"><span data-stu-id="52752-112">Child elements</span></span>

|<span data-ttu-id="52752-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="52752-113">**Element**</span></span>|<span data-ttu-id="52752-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="52752-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52752-115">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="52752-115">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="52752-116">定义日历文件夹代理用户拥有的访问权限。</span><span class="sxs-lookup"><span data-stu-id="52752-116">Defines the access that a delegate user has to a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52752-117">父元素</span><span class="sxs-lookup"><span data-stu-id="52752-117">Parent elements</span></span>

|<span data-ttu-id="52752-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="52752-118">**Element**</span></span>|<span data-ttu-id="52752-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="52752-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52752-120">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="52752-120">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="52752-121">包含日历文件夹的所有已配置的权限。</span><span class="sxs-lookup"><span data-stu-id="52752-121">Contains all the configured permissions for a calendar folder.</span></span> <span data-ttu-id="52752-122">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="52752-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52752-123">备注</span><span class="sxs-lookup"><span data-stu-id="52752-123">Remarks</span></span>

<span data-ttu-id="52752-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="52752-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52752-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="52752-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52752-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="52752-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52752-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="52752-127">Schema Name</span></span>  <br/> |<span data-ttu-id="52752-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="52752-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="52752-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="52752-129">Validation File</span></span>  <br/> |<span data-ttu-id="52752-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52752-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52752-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="52752-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="52752-132">False</span><span class="sxs-lookup"><span data-stu-id="52752-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52752-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52752-133">See also</span></span>



- [<span data-ttu-id="52752-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52752-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="52752-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="52752-135">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

