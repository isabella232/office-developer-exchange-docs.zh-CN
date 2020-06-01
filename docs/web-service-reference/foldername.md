---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: 文件夹名元素标识要添加到邮箱中的单个托管自定义文件夹。
ms.openlocfilehash: 1bb63e50c06e81337d1142a6624213fb2db12457
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461350"
---
# <a name="foldername"></a><span data-ttu-id="a6424-103">FolderName</span><span class="sxs-lookup"><span data-stu-id="a6424-103">FolderName</span></span>

<span data-ttu-id="a6424-104">**文件夹**名元素标识要添加到邮箱中的单个托管自定义文件夹。</span><span class="sxs-lookup"><span data-stu-id="a6424-104">The **FolderName** element identifies a single managed custom folder to add to a mailbox.</span></span> 
  
[<span data-ttu-id="a6424-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="a6424-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="a6424-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="a6424-106">FolderNames</span></span>](foldernames.md)
  
[<span data-ttu-id="a6424-107">FolderName</span><span class="sxs-lookup"><span data-stu-id="a6424-107">FolderName</span></span>](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 <span data-ttu-id="a6424-108">**string**</span><span class="sxs-lookup"><span data-stu-id="a6424-108">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a6424-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a6424-109">Attributes and elements</span></span>

<span data-ttu-id="a6424-110">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a6424-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a6424-111">Attributes</span><span class="sxs-lookup"><span data-stu-id="a6424-111">Attributes</span></span>

<span data-ttu-id="a6424-112">无。</span><span class="sxs-lookup"><span data-stu-id="a6424-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a6424-113">子元素</span><span class="sxs-lookup"><span data-stu-id="a6424-113">Child elements</span></span>

<span data-ttu-id="a6424-114">无。</span><span class="sxs-lookup"><span data-stu-id="a6424-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a6424-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a6424-115">Parent elements</span></span>

|<span data-ttu-id="a6424-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a6424-116">**Element**</span></span>|<span data-ttu-id="a6424-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a6424-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6424-118">FolderNames</span><span class="sxs-lookup"><span data-stu-id="a6424-118">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="a6424-119">包含要添加到邮箱中的已命名托管自定义文件夹的数组。</span><span class="sxs-lookup"><span data-stu-id="a6424-119">Contains an array of named managed custom folders to add to a mailbox.</span></span>  <br/> <span data-ttu-id="a6424-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="a6424-120">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a6424-121">文本值</span><span class="sxs-lookup"><span data-stu-id="a6424-121">Text value</span></span>

<span data-ttu-id="a6424-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="a6424-122">A text value is required.</span></span> <span data-ttu-id="a6424-123">该文本值表示文件夹的名称。</span><span class="sxs-lookup"><span data-stu-id="a6424-123">The text value represents a folder name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a6424-124">备注</span><span class="sxs-lookup"><span data-stu-id="a6424-124">Remarks</span></span>

<span data-ttu-id="a6424-125">虽然您可以使用 Exchange Web 服务将托管自定义文件夹添加到邮箱中，但不能使用相同的技术来访问可用的托管自定义文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="a6424-125">Although you can use Exchange Web Services to add managed custom folders to a mailbox, you cannot use the same technology to access the list of available managed custom folders.</span></span> <span data-ttu-id="a6424-126">您可以通过使用 Exchange 命令行管理程序命令或通过使用与 Active Directory 目录服务接口的 API，获取托管自定义文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="a6424-126">You can obtain a list of managed custom folders by using an Exchange Management Shell command or by using an API that interfaces with the Active Directory directory service.</span></span> <span data-ttu-id="a6424-127">文件夹名称是对应的 Active Directory 对象的名称。</span><span class="sxs-lookup"><span data-stu-id="a6424-127">The folder name is the name of the corresponding Active Directory object.</span></span>
  
<span data-ttu-id="a6424-128">您可以使用[FindFolder 操作](findfolder-operation.md)查找托管自定义文件夹。</span><span class="sxs-lookup"><span data-stu-id="a6424-128">You can use the [FindFolder operation](findfolder-operation.md) to find managed custom folders.</span></span> <span data-ttu-id="a6424-129">使用[DeleteFolder 操作](deletefolder-operation.md)可删除托管自定义文件夹。</span><span class="sxs-lookup"><span data-stu-id="a6424-129">Use the [DeleteFolder operation](deletefolder-operation.md) to delete managed custom folders.</span></span> 
  
<span data-ttu-id="a6424-130">请务必注意，**文件夹**名称是组织中现有托管自定义文件夹的名称。</span><span class="sxs-lookup"><span data-stu-id="a6424-130">It is important to note that **FolderName** is the name of an existing managed custom folder in the organization.</span></span> <span data-ttu-id="a6424-131">尝试添加不在组织中的文件夹将导致错误响应。</span><span class="sxs-lookup"><span data-stu-id="a6424-131">An attempt to add a folder that is not in the organization will result in an error response.</span></span> 
  
<span data-ttu-id="a6424-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a6424-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a6424-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="a6424-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a6424-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="a6424-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a6424-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="a6424-135">Schema Name</span></span>  <br/> |<span data-ttu-id="a6424-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="a6424-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="a6424-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="a6424-137">Validation File</span></span>  <br/> |<span data-ttu-id="a6424-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a6424-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a6424-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="a6424-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="a6424-140">False</span><span class="sxs-lookup"><span data-stu-id="a6424-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6424-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a6424-141">See also</span></span>



[<span data-ttu-id="a6424-142">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="a6424-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="a6424-143">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="a6424-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="a6424-144">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="a6424-144">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

