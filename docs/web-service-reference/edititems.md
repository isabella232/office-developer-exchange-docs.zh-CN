---
title: EditItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EditItems
api_type:
- schema
ms.assetid: 1cb14493-c999-4d66-b82c-ecb410dc1c00
description: EditItems 元素指示用户有权编辑的文件夹中的项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 0c3800b4d242dccb7455e0d0dea74e766db22854
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459249"
---
# <a name="edititems"></a><span data-ttu-id="d4faa-104">EditItems</span><span class="sxs-lookup"><span data-stu-id="d4faa-104">EditItems</span></span>

<span data-ttu-id="d4faa-105">**EditItems**元素指示用户有权编辑的文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="d4faa-105">The **EditItems** element indicates which items in a folder a user has permission to edit.</span></span> <span data-ttu-id="d4faa-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d4faa-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<EditItems>None or Owned or All</EditItems>
```

 <span data-ttu-id="d4faa-107">**PermissionActionType**</span><span class="sxs-lookup"><span data-stu-id="d4faa-107">**PermissionActionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4faa-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d4faa-108">Attributes and elements</span></span>

<span data-ttu-id="d4faa-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d4faa-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4faa-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d4faa-110">Attributes</span></span>

<span data-ttu-id="d4faa-111">无。</span><span class="sxs-lookup"><span data-stu-id="d4faa-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4faa-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d4faa-112">Child elements</span></span>

<span data-ttu-id="d4faa-113">无。</span><span class="sxs-lookup"><span data-stu-id="d4faa-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d4faa-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d4faa-114">Parent elements</span></span>

|<span data-ttu-id="d4faa-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="d4faa-115">**Element**</span></span>|<span data-ttu-id="d4faa-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="d4faa-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4faa-117">权限</span><span class="sxs-lookup"><span data-stu-id="d4faa-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="d4faa-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d4faa-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="d4faa-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="d4faa-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="d4faa-p104">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d4faa-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d4faa-123">文本值</span><span class="sxs-lookup"><span data-stu-id="d4faa-123">Text value</span></span>

<span data-ttu-id="d4faa-124">下表列出了**EditItems**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="d4faa-124">The following table lists the possible values for the **EditItems** element.</span></span> 
  
<span data-ttu-id="d4faa-125">**EditItems 元素文本值**</span><span class="sxs-lookup"><span data-stu-id="d4faa-125">**EditItems element text values**</span></span>

|<span data-ttu-id="d4faa-126">**值**</span><span class="sxs-lookup"><span data-stu-id="d4faa-126">**Value**</span></span>|<span data-ttu-id="d4faa-127">**说明**</span><span class="sxs-lookup"><span data-stu-id="d4faa-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d4faa-128">无</span><span class="sxs-lookup"><span data-stu-id="d4faa-128">None</span></span>  <br/> |<span data-ttu-id="d4faa-129">指示用户不具有编辑文件夹中的项目的权限。</span><span class="sxs-lookup"><span data-stu-id="d4faa-129">Indicates that the user does not have permission to edit items in the folder.</span></span>  <br/> |
|<span data-ttu-id="d4faa-130">所有权</span><span class="sxs-lookup"><span data-stu-id="d4faa-130">Owned</span></span>  <br/> |<span data-ttu-id="d4faa-131">指示用户有权编辑文件夹中的用户所拥有的项目。</span><span class="sxs-lookup"><span data-stu-id="d4faa-131">Indicates that the user has permission to edit the items that the user owns in the folder.</span></span>  <br/> |
|<span data-ttu-id="d4faa-132">所有</span><span class="sxs-lookup"><span data-stu-id="d4faa-132">All</span></span>  <br/> |<span data-ttu-id="d4faa-133">指示用户有权编辑文件夹中的所有项目。</span><span class="sxs-lookup"><span data-stu-id="d4faa-133">Indicates that the user has permission to edit all items in the folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4faa-134">说明</span><span class="sxs-lookup"><span data-stu-id="d4faa-134">Remarks</span></span>

<span data-ttu-id="d4faa-135">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d4faa-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4faa-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="d4faa-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4faa-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="d4faa-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4faa-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="d4faa-138">Schema Name</span></span>  <br/> |<span data-ttu-id="d4faa-139">类型架构</span><span class="sxs-lookup"><span data-stu-id="d4faa-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4faa-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="d4faa-140">Validation File</span></span>  <br/> |<span data-ttu-id="d4faa-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4faa-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4faa-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="d4faa-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4faa-143">False</span><span class="sxs-lookup"><span data-stu-id="d4faa-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4faa-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d4faa-144">See also</span></span>

- [<span data-ttu-id="d4faa-145">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d4faa-145">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="d4faa-146">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="d4faa-146">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

