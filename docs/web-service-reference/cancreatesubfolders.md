---
title: CanCreateSubFolders
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanCreateSubFolders
api_type:
- schema
ms.assetid: 4404a1cc-6d3f-4996-9647-58a740e8f883
description: CanCreateSubFolders元素指示用户是否有权限的文件夹中创建子文件夹。在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 234cbf604a3f0f5aa6e7fa896b7b6735516bd9ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753435"
---
# <a name="cancreatesubfolders"></a><span data-ttu-id="871c1-104">CanCreateSubFolders</span><span class="sxs-lookup"><span data-stu-id="871c1-104">CanCreateSubFolders</span></span>

<span data-ttu-id="871c1-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CanCreateSubFolders**元素指示用户是否有权限的文件夹中创建子文件夹。在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="871c1-p102">The **CanCreateSubFolders** element indicates whether a user has permission to create subfolders in a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CanCreateSubFolders/>
```

 <span data-ttu-id="871c1-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="871c1-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="871c1-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="871c1-108">Attributes and elements</span></span>

<span data-ttu-id="871c1-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="871c1-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="871c1-110">属性</span><span class="sxs-lookup"><span data-stu-id="871c1-110">Attributes</span></span>

<span data-ttu-id="871c1-111">无。</span><span class="sxs-lookup"><span data-stu-id="871c1-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="871c1-112">子元素</span><span class="sxs-lookup"><span data-stu-id="871c1-112">Child elements</span></span>

<span data-ttu-id="871c1-113">无。</span><span class="sxs-lookup"><span data-stu-id="871c1-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="871c1-114">父元素</span><span class="sxs-lookup"><span data-stu-id="871c1-114">Parent elements</span></span>

|<span data-ttu-id="871c1-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="871c1-115">**Element**</span></span>|<span data-ttu-id="871c1-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="871c1-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="871c1-117">权限</span><span class="sxs-lookup"><span data-stu-id="871c1-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="871c1-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="871c1-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="871c1-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="871c1-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="871c1-p104">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="871c1-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="871c1-123">文本值</span><span class="sxs-lookup"><span data-stu-id="871c1-123">Text value</span></span>

<span data-ttu-id="871c1-p105">**true**的一个文字值指示用户可以在该文件夹中创建子文件夹。 **false**表示用户不能在文件夹中创建子文件夹。</span><span class="sxs-lookup"><span data-stu-id="871c1-p105">A text value of **true** indicates that the user can create subfolders in the folder. A value of **false** indicates that the user cannot create subfolders in the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="871c1-126">备注</span><span class="sxs-lookup"><span data-stu-id="871c1-126">Remarks</span></span>

<span data-ttu-id="871c1-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="871c1-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="871c1-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="871c1-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="871c1-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="871c1-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="871c1-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="871c1-130">Schema Name</span></span>  <br/> |<span data-ttu-id="871c1-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="871c1-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="871c1-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="871c1-132">Validation File</span></span>  <br/> |<span data-ttu-id="871c1-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="871c1-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="871c1-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="871c1-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="871c1-135">False</span><span class="sxs-lookup"><span data-stu-id="871c1-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="871c1-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="871c1-136">See also</span></span>



- [<span data-ttu-id="871c1-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="871c1-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="871c1-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="871c1-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

