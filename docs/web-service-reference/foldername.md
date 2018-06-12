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
description: FolderName 元素标识单个托管自定义文件夹添加到邮箱。
ms.openlocfilehash: 56a7a7d256624c5103c88a333222807519d21501
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754397"
---
# <a name="foldername"></a><span data-ttu-id="5c177-103">FolderName</span><span class="sxs-lookup"><span data-stu-id="5c177-103">FolderName</span></span>

<span data-ttu-id="5c177-104">**FolderName**元素标识单个托管自定义文件夹添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="5c177-104">The **FolderName** element identifies a single managed custom folder to add to a mailbox.</span></span> 
  
[<span data-ttu-id="5c177-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="5c177-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="5c177-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="5c177-106">FolderNames</span></span>](foldernames.md)
  
[<span data-ttu-id="5c177-107">FolderName</span><span class="sxs-lookup"><span data-stu-id="5c177-107">FolderName</span></span>](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 <span data-ttu-id="5c177-108">**string**</span><span class="sxs-lookup"><span data-stu-id="5c177-108">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5c177-109">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5c177-109">Attributes and elements</span></span>

<span data-ttu-id="5c177-110">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5c177-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5c177-111">属性</span><span class="sxs-lookup"><span data-stu-id="5c177-111">Attributes</span></span>

<span data-ttu-id="5c177-112">无。</span><span class="sxs-lookup"><span data-stu-id="5c177-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5c177-113">子元素</span><span class="sxs-lookup"><span data-stu-id="5c177-113">Child elements</span></span>

<span data-ttu-id="5c177-114">无。</span><span class="sxs-lookup"><span data-stu-id="5c177-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5c177-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5c177-115">Parent elements</span></span>

|<span data-ttu-id="5c177-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="5c177-116">**Element**</span></span>|<span data-ttu-id="5c177-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="5c177-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c177-118">FolderNames</span><span class="sxs-lookup"><span data-stu-id="5c177-118">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="5c177-119">包含命名托管的自定义文件夹添加到邮箱的数组。</span><span class="sxs-lookup"><span data-stu-id="5c177-119">Contains an array of named managed custom folders to add to a mailbox.</span></span>  <br/> <span data-ttu-id="5c177-120">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="5c177-120">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5c177-121">文本值</span><span class="sxs-lookup"><span data-stu-id="5c177-121">Text value</span></span>

<span data-ttu-id="5c177-122">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="5c177-122">A text value is required.</span></span> <span data-ttu-id="5c177-123">文本值表示的文件夹名称。</span><span class="sxs-lookup"><span data-stu-id="5c177-123">The text value represents a folder name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c177-124">备注</span><span class="sxs-lookup"><span data-stu-id="5c177-124">Remarks</span></span>

<span data-ttu-id="5c177-125">尽管可以使用 Exchange Web 服务添加到邮箱的托管自定义文件夹，但不能使用相同的技术以访问可用托管自定义文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="5c177-125">Although you can use Exchange Web Services to add managed custom folders to a mailbox, you cannot use the same technology to access the list of available managed custom folders.</span></span> <span data-ttu-id="5c177-126">通过使用 Exchange 命令行管理程序命令或通过使用 Active Directory 目录服务的 API 的接口，您可以获取托管自定义文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="5c177-126">You can obtain a list of managed custom folders by using an Exchange Management Shell command or by using an API that interfaces with the Active Directory directory service.</span></span> <span data-ttu-id="5c177-127">文件夹名称为相应的 Active Directory 对象的名称。</span><span class="sxs-lookup"><span data-stu-id="5c177-127">The folder name is the name of the corresponding Active Directory object.</span></span>
  
<span data-ttu-id="5c177-128">您可以使用[FindFolder 操作](findfolder-operation.md)查找托管自定义文件夹。</span><span class="sxs-lookup"><span data-stu-id="5c177-128">You can use the [FindFolder operation](findfolder-operation.md) to find managed custom folders.</span></span> <span data-ttu-id="5c177-129">使用[DeleteFolder 操作](deletefolder-operation.md)删除托管自定义文件夹。</span><span class="sxs-lookup"><span data-stu-id="5c177-129">Use the [DeleteFolder operation](deletefolder-operation.md) to delete managed custom folders.</span></span> 
  
<span data-ttu-id="5c177-130">请务必注意**FolderName**是组织中现有托管自定义文件夹的名称。</span><span class="sxs-lookup"><span data-stu-id="5c177-130">It is important to note that **FolderName** is the name of an existing managed custom folder in the organization.</span></span> <span data-ttu-id="5c177-131">尝试添加文件夹不在组织中将导致错误响应。</span><span class="sxs-lookup"><span data-stu-id="5c177-131">An attempt to add a folder that is not in the organization will result in an error response.</span></span> 
  
<span data-ttu-id="5c177-132">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5c177-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5c177-133">元素信息</span><span class="sxs-lookup"><span data-stu-id="5c177-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5c177-134">命名空间</span><span class="sxs-lookup"><span data-stu-id="5c177-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5c177-135">架构名称</span><span class="sxs-lookup"><span data-stu-id="5c177-135">Schema Name</span></span>  <br/> |<span data-ttu-id="5c177-136">类型架构</span><span class="sxs-lookup"><span data-stu-id="5c177-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="5c177-137">验证文件</span><span class="sxs-lookup"><span data-stu-id="5c177-137">Validation File</span></span>  <br/> |<span data-ttu-id="5c177-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5c177-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5c177-139">可以为空</span><span class="sxs-lookup"><span data-stu-id="5c177-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="5c177-140">False</span><span class="sxs-lookup"><span data-stu-id="5c177-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5c177-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5c177-141">See also</span></span>



[<span data-ttu-id="5c177-142">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="5c177-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="5c177-143">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="5c177-143">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="5c177-144">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="5c177-144">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

