---
title: CanCreateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanCreateItems
api_type:
- schema
ms.assetid: c4574e9a-3c42-40a1-a5f9-79b6560e9b30
description: CanCreateItems 元素指示用户是否有权文件夹中创建项目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 313699a15ef3038dd9114c18b76b29aba15e5ab7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753437"
---
# <a name="cancreateitems"></a><span data-ttu-id="ca05b-104">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="ca05b-104">CanCreateItems</span></span>

<span data-ttu-id="ca05b-105">**CanCreateItems**元素指示用户是否有权文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="ca05b-105">The **CanCreateItems** element indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="ca05b-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ca05b-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CanCreateItems/>
```

 <span data-ttu-id="ca05b-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ca05b-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca05b-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ca05b-108">Attributes and elements</span></span>

<span data-ttu-id="ca05b-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ca05b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca05b-110">属性</span><span class="sxs-lookup"><span data-stu-id="ca05b-110">Attributes</span></span>

<span data-ttu-id="ca05b-111">无。</span><span class="sxs-lookup"><span data-stu-id="ca05b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca05b-112">子元素</span><span class="sxs-lookup"><span data-stu-id="ca05b-112">Child elements</span></span>

<span data-ttu-id="ca05b-113">无。</span><span class="sxs-lookup"><span data-stu-id="ca05b-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca05b-114">父元素</span><span class="sxs-lookup"><span data-stu-id="ca05b-114">Parent elements</span></span>

|<span data-ttu-id="ca05b-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="ca05b-115">**Element**</span></span>|<span data-ttu-id="ca05b-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="ca05b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ca05b-117">权限</span><span class="sxs-lookup"><span data-stu-id="ca05b-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="ca05b-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ca05b-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ca05b-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ca05b-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ca05b-p104">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ca05b-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ca05b-123">文本值</span><span class="sxs-lookup"><span data-stu-id="ca05b-123">Text value</span></span>

<span data-ttu-id="ca05b-124">文本值为**true**指示用户可以创建的文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="ca05b-124">A text value of **true** indicates that the user can create items in the folder.</span></span> <span data-ttu-id="ca05b-125">如果值为**false**指示用户无法创建文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="ca05b-125">A value of **false** indicates that the user cannot create items in the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ca05b-126">备注</span><span class="sxs-lookup"><span data-stu-id="ca05b-126">Remarks</span></span>

<span data-ttu-id="ca05b-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ca05b-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca05b-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="ca05b-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca05b-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="ca05b-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ca05b-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="ca05b-130">Schema Name</span></span>  <br/> |<span data-ttu-id="ca05b-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="ca05b-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ca05b-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="ca05b-132">Validation File</span></span>  <br/> |<span data-ttu-id="ca05b-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ca05b-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ca05b-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="ca05b-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ca05b-135">False</span><span class="sxs-lookup"><span data-stu-id="ca05b-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ca05b-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ca05b-136">See also</span></span>



- [<span data-ttu-id="ca05b-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ca05b-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ca05b-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ca05b-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

