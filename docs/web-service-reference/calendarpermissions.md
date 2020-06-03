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
description: CalendarPermissions 元素包含一个文件夹的日历权限数组。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: f072339212d0fdff3983fbfb6bc8f53c272350c8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529467"
---
# <a name="calendarpermissions"></a><span data-ttu-id="9b390-104">CalendarPermissions</span><span class="sxs-lookup"><span data-stu-id="9b390-104">CalendarPermissions</span></span>

<span data-ttu-id="9b390-105">**CalendarPermissions**元素包含一个文件夹的日历权限数组。</span><span class="sxs-lookup"><span data-stu-id="9b390-105">The **CalendarPermissions** element contains an array of calendar permissions for a folder.</span></span> <span data-ttu-id="9b390-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9b390-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CalendarPermissions>
   <PermissionSet/>
</CalendarPermissions>
```

 <span data-ttu-id="9b390-107">**ArrayOfCalendarPermissionsType**</span><span class="sxs-lookup"><span data-stu-id="9b390-107">**ArrayOfCalendarPermissionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b390-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b390-108">Attributes and elements</span></span>

<span data-ttu-id="9b390-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b390-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b390-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="9b390-110">Attributes</span></span>

<span data-ttu-id="9b390-111">无。</span><span class="sxs-lookup"><span data-stu-id="9b390-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b390-112">子元素</span><span class="sxs-lookup"><span data-stu-id="9b390-112">Child elements</span></span>

|<span data-ttu-id="9b390-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b390-113">**Element**</span></span>|<span data-ttu-id="9b390-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b390-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b390-115">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="9b390-115">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="9b390-116">定义代理用户对 "日历" 文件夹的访问权限。</span><span class="sxs-lookup"><span data-stu-id="9b390-116">Defines the access that a delegate user has to a calendar folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9b390-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9b390-117">Parent elements</span></span>

|<span data-ttu-id="9b390-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="9b390-118">**Element**</span></span>|<span data-ttu-id="9b390-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="9b390-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9b390-120">PermissionSet （CalendarPermissionSetType）</span><span class="sxs-lookup"><span data-stu-id="9b390-120">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="9b390-121">包含日历文件夹的所有已配置的权限。</span><span class="sxs-lookup"><span data-stu-id="9b390-121">Contains all the configured permissions for a calendar folder.</span></span> <span data-ttu-id="9b390-122">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9b390-122">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b390-123">说明</span><span class="sxs-lookup"><span data-stu-id="9b390-123">Remarks</span></span>

<span data-ttu-id="9b390-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9b390-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b390-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b390-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b390-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b390-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b390-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b390-127">Schema Name</span></span>  <br/> |<span data-ttu-id="9b390-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="9b390-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="9b390-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b390-129">Validation File</span></span>  <br/> |<span data-ttu-id="9b390-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b390-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b390-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b390-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="9b390-132">False</span><span class="sxs-lookup"><span data-stu-id="9b390-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b390-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9b390-133">See also</span></span>



- [<span data-ttu-id="9b390-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9b390-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="9b390-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="9b390-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

