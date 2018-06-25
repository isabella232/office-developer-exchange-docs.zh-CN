---
title: UnknownEntries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UnknownEntries
api_type:
- schema
ms.assetid: 107ec73e-083a-4956-9d37-33d4734cc157
description: UnknownEntries 元素包含一个数组无法解析针对 Active Directory 目录服务的未知的权限条目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 306e5f226a56694bb1ff32362f77e7dff80865ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838344"
---
# <a name="unknownentries"></a><span data-ttu-id="21429-104">UnknownEntries</span><span class="sxs-lookup"><span data-stu-id="21429-104">UnknownEntries</span></span>

<span data-ttu-id="21429-105">**UnknownEntries**元素包含一个数组无法解析针对 Active Directory 目录服务的未知的权限条目。</span><span class="sxs-lookup"><span data-stu-id="21429-105">The **UnknownEntries** element contains an array of unknown permission entries that cannot be resolved against the Active Directory directory service.</span></span> <span data-ttu-id="21429-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21429-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<UnknownEntries>
   <UnknownEntry/>
</UnknownEntries>
```

 <span data-ttu-id="21429-107">**ArrayOfUnknownEntriesType**</span><span class="sxs-lookup"><span data-stu-id="21429-107">**ArrayOfUnknownEntriesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="21429-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="21429-108">Attributes and elements</span></span>

<span data-ttu-id="21429-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="21429-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="21429-110">属性</span><span class="sxs-lookup"><span data-stu-id="21429-110">Attributes</span></span>

<span data-ttu-id="21429-111">无。</span><span class="sxs-lookup"><span data-stu-id="21429-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21429-112">子元素</span><span class="sxs-lookup"><span data-stu-id="21429-112">Child elements</span></span>

|<span data-ttu-id="21429-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="21429-113">**Element**</span></span>|<span data-ttu-id="21429-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="21429-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21429-115">UnknownEntry</span><span class="sxs-lookup"><span data-stu-id="21429-115">UnknownEntry</span></span>](unknownentry.md) <br/> |<span data-ttu-id="21429-116">表示无法解析的 Active directory 的单个未知的权限条目。</span><span class="sxs-lookup"><span data-stu-id="21429-116">Represents a single unknown permission entry that cannot be resolved against Active Directory.</span></span> <span data-ttu-id="21429-117">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21429-117">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="21429-118">父元素</span><span class="sxs-lookup"><span data-stu-id="21429-118">Parent elements</span></span>

|<span data-ttu-id="21429-119">**元素**</span><span class="sxs-lookup"><span data-stu-id="21429-119">**Element**</span></span>|<span data-ttu-id="21429-120">**说明**</span><span class="sxs-lookup"><span data-stu-id="21429-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="21429-121">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="21429-121">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="21429-122">包含所有配置的文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="21429-122">Contains all the permissions that are configured for a folder.</span></span> <span data-ttu-id="21429-123">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21429-123">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="21429-124">PermissionSet (CalendarPermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="21429-124">PermissionSet (CalendarPermissionSetType)</span></span>](permissionset-calendarpermissionsettype.md) <br/> |<span data-ttu-id="21429-125">包含所有配置的日历文件夹的权限。</span><span class="sxs-lookup"><span data-stu-id="21429-125">Contains all the permissions that are configured for a calendar folder.</span></span> <span data-ttu-id="21429-126">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="21429-126">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21429-127">注解</span><span class="sxs-lookup"><span data-stu-id="21429-127">Remarks</span></span>

<span data-ttu-id="21429-128">可以通过使用[SetFolderField](setfolderfield.md)元素 UpdateFolder 操作从文件夹中删除未知的条目。</span><span class="sxs-lookup"><span data-stu-id="21429-128">You can delete unknown entries from a folder by using the UpdateFolder operation with the [SetFolderField](setfolderfield.md) element.</span></span> <span data-ttu-id="21429-129">通过使用 UpdateFolder 操作的 SetFolderField 选项重置 PermissionSet 时，将删除未知的条目。</span><span class="sxs-lookup"><span data-stu-id="21429-129">The unknown entries are deleted when you reset the PermissionSet by using the SetFolderField option of the UpdateFolder operation.</span></span> <span data-ttu-id="21429-130">Exchange Web 服务不支持各项的删除。</span><span class="sxs-lookup"><span data-stu-id="21429-130">Exchange Web Services does not support the deletion of individual entries.</span></span> 
  
<span data-ttu-id="21429-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="21429-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="21429-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="21429-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21429-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="21429-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="21429-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="21429-134">Schema Name</span></span>  <br/> |<span data-ttu-id="21429-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="21429-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="21429-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="21429-136">Validation File</span></span>  <br/> |<span data-ttu-id="21429-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="21429-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="21429-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="21429-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="21429-139">False</span><span class="sxs-lookup"><span data-stu-id="21429-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="21429-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="21429-140">See also</span></span>



[<span data-ttu-id="21429-141">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="21429-141">UpdateFolder operation</span></span>](updatefolder-operation.md)


- [<span data-ttu-id="21429-142">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="21429-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="21429-143">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="21429-143">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

