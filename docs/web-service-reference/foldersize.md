---
title: FolderSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderSize
api_type:
- schema
ms.assetid: 27e5f0cd-e23a-4ddd-943a-9f17bf0fd87b
description: FolderSize 元素描述了托管文件夹中的所有内容的总大小。
ms.openlocfilehash: 314c75e6ab824caed4c6a1c6f5b62a43f86ba939
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754405"
---
# <a name="foldersize"></a><span data-ttu-id="33a33-103">FolderSize</span><span class="sxs-lookup"><span data-stu-id="33a33-103">FolderSize</span></span>

<span data-ttu-id="33a33-104">**FolderSize**元素描述了托管文件夹中的所有内容的总大小。</span><span class="sxs-lookup"><span data-stu-id="33a33-104">The **FolderSize** element describes the total size of all the contents of a managed folder.</span></span> 
  
```xml
<FolderSize/>
```

 <span data-ttu-id="33a33-105">**int**</span><span class="sxs-lookup"><span data-stu-id="33a33-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="33a33-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="33a33-106">Attributes and elements</span></span>

<span data-ttu-id="33a33-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="33a33-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="33a33-108">属性</span><span class="sxs-lookup"><span data-stu-id="33a33-108">Attributes</span></span>

<span data-ttu-id="33a33-109">无。</span><span class="sxs-lookup"><span data-stu-id="33a33-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="33a33-110">子元素</span><span class="sxs-lookup"><span data-stu-id="33a33-110">Child elements</span></span>

<span data-ttu-id="33a33-111">无。</span><span class="sxs-lookup"><span data-stu-id="33a33-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="33a33-112">父元素</span><span class="sxs-lookup"><span data-stu-id="33a33-112">Parent elements</span></span>

|<span data-ttu-id="33a33-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="33a33-113">**Element**</span></span>|<span data-ttu-id="33a33-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="33a33-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="33a33-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="33a33-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="33a33-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="33a33-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="33a33-117">文本值</span><span class="sxs-lookup"><span data-stu-id="33a33-117">Text value</span></span>

<span data-ttu-id="33a33-118">文本值表示的文件夹中兆字节为单位的总大小。</span><span class="sxs-lookup"><span data-stu-id="33a33-118">The text value represents the total size of the folder in megabytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33a33-119">备注</span><span class="sxs-lookup"><span data-stu-id="33a33-119">Remarks</span></span>

<span data-ttu-id="33a33-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="33a33-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="33a33-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="33a33-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33a33-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="33a33-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="33a33-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="33a33-123">Schema name</span></span>  <br/> |<span data-ttu-id="33a33-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="33a33-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="33a33-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="33a33-125">Validation file</span></span>  <br/> |<span data-ttu-id="33a33-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="33a33-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="33a33-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="33a33-127">Can be empty</span></span>  <br/> |<span data-ttu-id="33a33-128">False</span><span class="sxs-lookup"><span data-stu-id="33a33-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="33a33-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="33a33-129">See also</span></span>



[<span data-ttu-id="33a33-130">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="33a33-130">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="33a33-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="33a33-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

