---
title: FolderChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChanges
api_type:
- schema
ms.assetid: d3f611ed-56a4-43f8-aa65-cbd7844b827f
description: FolderChanges 元素表示的文件夹的更改的集合。
ms.openlocfilehash: 7ab89e79f6babb5e93863974835685c6975d96dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754379"
---
# <a name="folderchanges"></a><span data-ttu-id="d9e2c-103">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="d9e2c-103">FolderChanges</span></span>

<span data-ttu-id="d9e2c-104">**FolderChanges**元素表示的文件夹的更改的集合。</span><span class="sxs-lookup"><span data-stu-id="d9e2c-104">The **FolderChanges** element represents a collection of changes for a folder.</span></span> 
  
[<span data-ttu-id="d9e2c-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="d9e2c-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="d9e2c-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="d9e2c-106">FolderChanges</span></span>](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 <span data-ttu-id="d9e2c-107">**NonEmptyArrayOfFolderChangesType**</span><span class="sxs-lookup"><span data-stu-id="d9e2c-107">**NonEmptyArrayOfFolderChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9e2c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9e2c-108">Attributes and elements</span></span>

<span data-ttu-id="d9e2c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9e2c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9e2c-110">属性</span><span class="sxs-lookup"><span data-stu-id="d9e2c-110">Attributes</span></span>

<span data-ttu-id="d9e2c-111">无。</span><span class="sxs-lookup"><span data-stu-id="d9e2c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9e2c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d9e2c-112">Child elements</span></span>

|<span data-ttu-id="d9e2c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9e2c-113">**Element**</span></span>|<span data-ttu-id="d9e2c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9e2c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9e2c-115">FolderChange</span><span class="sxs-lookup"><span data-stu-id="d9e2c-115">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="d9e2c-116">代表单个更改单个文件夹上执行。</span><span class="sxs-lookup"><span data-stu-id="d9e2c-116">Represents a single change to be performed on a single folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d9e2c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="d9e2c-117">Parent elements</span></span>

|<span data-ttu-id="d9e2c-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9e2c-118">**Element**</span></span>|<span data-ttu-id="d9e2c-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9e2c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9e2c-120">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="d9e2c-120">UpdateFolder</span></span>](updatefolder.md) <br/> |<span data-ttu-id="d9e2c-121">表示用于更新的文件夹的属性的操作。</span><span class="sxs-lookup"><span data-stu-id="d9e2c-121">Represents the operation that is used to update properties for a folder.</span></span>  <br/> <span data-ttu-id="d9e2c-122">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="d9e2c-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d9e2c-123">备注</span><span class="sxs-lookup"><span data-stu-id="d9e2c-123">Remarks</span></span>

<span data-ttu-id="d9e2c-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d9e2c-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9e2c-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="d9e2c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9e2c-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9e2c-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d9e2c-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="d9e2c-127">Schema Name</span></span>  <br/> |<span data-ttu-id="d9e2c-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="d9e2c-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d9e2c-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="d9e2c-129">Validation File</span></span>  <br/> |<span data-ttu-id="d9e2c-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d9e2c-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d9e2c-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="d9e2c-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9e2c-132">False</span><span class="sxs-lookup"><span data-stu-id="d9e2c-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9e2c-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9e2c-133">See also</span></span>



[<span data-ttu-id="d9e2c-134">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="d9e2c-134">UpdateFolder operation</span></span>](updatefolder-operation.md)

