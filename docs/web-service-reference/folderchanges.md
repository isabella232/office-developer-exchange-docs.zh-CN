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
description: FolderChanges 元素表示文件夹的更改集合。
ms.openlocfilehash: 5481496100512584fd0b9745ee42d5b9516bd7fb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458381"
---
# <a name="folderchanges"></a><span data-ttu-id="8e226-103">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="8e226-103">FolderChanges</span></span>

<span data-ttu-id="8e226-104">**FolderChanges**元素表示文件夹的更改集合。</span><span class="sxs-lookup"><span data-stu-id="8e226-104">The **FolderChanges** element represents a collection of changes for a folder.</span></span> 
  
[<span data-ttu-id="8e226-105">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="8e226-105">UpdateFolder</span></span>](updatefolder.md)
  
[<span data-ttu-id="8e226-106">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="8e226-106">FolderChanges</span></span>](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 <span data-ttu-id="8e226-107">**NonEmptyArrayOfFolderChangesType**</span><span class="sxs-lookup"><span data-stu-id="8e226-107">**NonEmptyArrayOfFolderChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8e226-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8e226-108">Attributes and elements</span></span>

<span data-ttu-id="8e226-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8e226-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8e226-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="8e226-110">Attributes</span></span>

<span data-ttu-id="8e226-111">无。</span><span class="sxs-lookup"><span data-stu-id="8e226-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8e226-112">子元素</span><span class="sxs-lookup"><span data-stu-id="8e226-112">Child elements</span></span>

|<span data-ttu-id="8e226-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8e226-113">**Element**</span></span>|<span data-ttu-id="8e226-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8e226-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e226-115">FolderChange</span><span class="sxs-lookup"><span data-stu-id="8e226-115">FolderChange</span></span>](folderchange.md) <br/> |<span data-ttu-id="8e226-116">代表要对单个文件夹执行的单个更改。</span><span class="sxs-lookup"><span data-stu-id="8e226-116">Represents a single change to be performed on a single folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8e226-117">父元素</span><span class="sxs-lookup"><span data-stu-id="8e226-117">Parent elements</span></span>

|<span data-ttu-id="8e226-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="8e226-118">**Element**</span></span>|<span data-ttu-id="8e226-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="8e226-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8e226-120">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="8e226-120">UpdateFolder</span></span>](updatefolder.md) <br/> |<span data-ttu-id="8e226-121">表示用于更新文件夹属性的操作。</span><span class="sxs-lookup"><span data-stu-id="8e226-121">Represents the operation that is used to update properties for a folder.</span></span>  <br/> <span data-ttu-id="8e226-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="8e226-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8e226-123">说明</span><span class="sxs-lookup"><span data-stu-id="8e226-123">Remarks</span></span>

<span data-ttu-id="8e226-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8e226-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8e226-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="8e226-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8e226-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="8e226-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8e226-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="8e226-127">Schema Name</span></span>  <br/> |<span data-ttu-id="8e226-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="8e226-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8e226-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="8e226-129">Validation File</span></span>  <br/> |<span data-ttu-id="8e226-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8e226-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8e226-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="8e226-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="8e226-132">False</span><span class="sxs-lookup"><span data-stu-id="8e226-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8e226-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8e226-133">See also</span></span>



[<span data-ttu-id="8e226-134">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="8e226-134">UpdateFolder operation</span></span>](updatefolder-operation.md)

