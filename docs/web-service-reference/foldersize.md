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
description: FolderSize 元素描述托管文件夹中所有内容的总大小。
ms.openlocfilehash: 8ed493cfb0c2cabd02d28354c115a73662992473
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461336"
---
# <a name="foldersize"></a><span data-ttu-id="ced37-103">FolderSize</span><span class="sxs-lookup"><span data-stu-id="ced37-103">FolderSize</span></span>

<span data-ttu-id="ced37-104">**FolderSize**元素描述托管文件夹中所有内容的总大小。</span><span class="sxs-lookup"><span data-stu-id="ced37-104">The **FolderSize** element describes the total size of all the contents of a managed folder.</span></span> 
  
```xml
<FolderSize/>
```

 <span data-ttu-id="ced37-105">**int**</span><span class="sxs-lookup"><span data-stu-id="ced37-105">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ced37-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ced37-106">Attributes and elements</span></span>

<span data-ttu-id="ced37-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ced37-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ced37-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ced37-108">Attributes</span></span>

<span data-ttu-id="ced37-109">无。</span><span class="sxs-lookup"><span data-stu-id="ced37-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ced37-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ced37-110">Child elements</span></span>

<span data-ttu-id="ced37-111">无。</span><span class="sxs-lookup"><span data-stu-id="ced37-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ced37-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ced37-112">Parent elements</span></span>

|<span data-ttu-id="ced37-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ced37-113">**Element**</span></span>|<span data-ttu-id="ced37-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ced37-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ced37-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="ced37-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="ced37-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="ced37-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ced37-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ced37-117">Text value</span></span>

<span data-ttu-id="ced37-118">该文本值表示文件夹的总大小（以 mb 为单位）。</span><span class="sxs-lookup"><span data-stu-id="ced37-118">The text value represents the total size of the folder in megabytes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ced37-119">说明</span><span class="sxs-lookup"><span data-stu-id="ced37-119">Remarks</span></span>

<span data-ttu-id="ced37-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ced37-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ced37-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="ced37-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ced37-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="ced37-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ced37-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="ced37-123">Schema name</span></span>  <br/> |<span data-ttu-id="ced37-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="ced37-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="ced37-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="ced37-125">Validation file</span></span>  <br/> |<span data-ttu-id="ced37-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ced37-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ced37-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="ced37-127">Can be empty</span></span>  <br/> |<span data-ttu-id="ced37-128">False</span><span class="sxs-lookup"><span data-stu-id="ced37-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ced37-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ced37-129">See also</span></span>



[<span data-ttu-id="ced37-130">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="ced37-130">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="ced37-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ced37-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

