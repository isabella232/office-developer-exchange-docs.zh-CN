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
description: CanCreateItems 元素指示用户是否有权在文件夹中创建项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 73d3d967774d9fcff53722d0936462025e02b659
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458780"
---
# <a name="cancreateitems"></a><span data-ttu-id="ec079-104">CanCreateItems</span><span class="sxs-lookup"><span data-stu-id="ec079-104">CanCreateItems</span></span>

<span data-ttu-id="ec079-105">**CanCreateItems**元素指示用户是否有权在文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="ec079-105">The **CanCreateItems** element indicates whether a user has permission to create items in a folder.</span></span> <span data-ttu-id="ec079-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ec079-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CanCreateItems/>
```

 <span data-ttu-id="ec079-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ec079-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ec079-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ec079-108">Attributes and elements</span></span>

<span data-ttu-id="ec079-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ec079-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ec079-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="ec079-110">Attributes</span></span>

<span data-ttu-id="ec079-111">无。</span><span class="sxs-lookup"><span data-stu-id="ec079-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ec079-112">子元素</span><span class="sxs-lookup"><span data-stu-id="ec079-112">Child elements</span></span>

<span data-ttu-id="ec079-113">无。</span><span class="sxs-lookup"><span data-stu-id="ec079-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ec079-114">父元素</span><span class="sxs-lookup"><span data-stu-id="ec079-114">Parent elements</span></span>

|<span data-ttu-id="ec079-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="ec079-115">**Element**</span></span>|<span data-ttu-id="ec079-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="ec079-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ec079-117">权限</span><span class="sxs-lookup"><span data-stu-id="ec079-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="ec079-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ec079-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="ec079-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="ec079-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="ec079-p104">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ec079-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ec079-123">文本值</span><span class="sxs-lookup"><span data-stu-id="ec079-123">Text value</span></span>

<span data-ttu-id="ec079-124">如果文本值为**true** ，则表示用户可以在文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="ec079-124">A text value of **true** indicates that the user can create items in the folder.</span></span> <span data-ttu-id="ec079-125">**如果值为 false** ，则表示用户无法在文件夹中创建项目。</span><span class="sxs-lookup"><span data-stu-id="ec079-125">A value of **false** indicates that the user cannot create items in the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ec079-126">说明</span><span class="sxs-lookup"><span data-stu-id="ec079-126">Remarks</span></span>

<span data-ttu-id="ec079-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ec079-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ec079-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="ec079-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec079-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="ec079-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ec079-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="ec079-130">Schema Name</span></span>  <br/> |<span data-ttu-id="ec079-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="ec079-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="ec079-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="ec079-132">Validation File</span></span>  <br/> |<span data-ttu-id="ec079-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ec079-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ec079-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="ec079-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="ec079-135">False</span><span class="sxs-lookup"><span data-stu-id="ec079-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ec079-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ec079-136">See also</span></span>



- [<span data-ttu-id="ec079-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ec079-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ec079-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ec079-138">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

