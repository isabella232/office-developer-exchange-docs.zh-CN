---
title: IsManagedFoldersRoot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsManagedFoldersRoot
api_type:
- schema
ms.assetid: 00823fb9-bf8b-49bb-8e1b-d698c6d4063f
description: IsManagedFoldersRoot 元素指示托管文件夹是否为所有托管文件夹的根。
ms.openlocfilehash: 4373dba9dce92de8e175948d889f0806e100fa6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466022"
---
# <a name="ismanagedfoldersroot"></a><span data-ttu-id="113dc-103">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="113dc-103">IsManagedFoldersRoot</span></span>

<span data-ttu-id="113dc-104">**IsManagedFoldersRoot**元素指示托管文件夹是否为所有托管文件夹的根。</span><span class="sxs-lookup"><span data-stu-id="113dc-104">The **IsManagedFoldersRoot** element indicates whether the managed folder is the root for all managed folders.</span></span> 
  
```xml
<IsManagedFoldersRoot/>
```

 <span data-ttu-id="113dc-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="113dc-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="113dc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="113dc-106">Attributes and elements</span></span>

<span data-ttu-id="113dc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="113dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="113dc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="113dc-108">Attributes</span></span>

<span data-ttu-id="113dc-109">无。</span><span class="sxs-lookup"><span data-stu-id="113dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="113dc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="113dc-110">Child elements</span></span>

<span data-ttu-id="113dc-111">无。</span><span class="sxs-lookup"><span data-stu-id="113dc-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="113dc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="113dc-112">Parent elements</span></span>

|<span data-ttu-id="113dc-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="113dc-113">**Element**</span></span>|<span data-ttu-id="113dc-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="113dc-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="113dc-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="113dc-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="113dc-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="113dc-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="113dc-117">文本值</span><span class="sxs-lookup"><span data-stu-id="113dc-117">Text value</span></span>

<span data-ttu-id="113dc-118">如果存在此元素，则需要一个表示布尔值的文本值。</span><span class="sxs-lookup"><span data-stu-id="113dc-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="113dc-119">**如果值为 true** ，则表示该文件夹是托管文件夹的根文件夹;**如果值为 false** ，则表示该文件夹不是托管文件夹的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="113dc-119">A value of **true** indicates that the folder is the root folder of the managed folder; a value of **false** indicates that the folder is not the root folder of the managed folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="113dc-120">说明</span><span class="sxs-lookup"><span data-stu-id="113dc-120">Remarks</span></span>

<span data-ttu-id="113dc-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="113dc-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="113dc-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="113dc-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="113dc-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="113dc-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="113dc-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="113dc-124">Schema name</span></span>  <br/> |<span data-ttu-id="113dc-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="113dc-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="113dc-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="113dc-126">Validation file</span></span>  <br/> |<span data-ttu-id="113dc-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="113dc-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="113dc-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="113dc-128">Can be empty</span></span>  <br/> |<span data-ttu-id="113dc-129">False</span><span class="sxs-lookup"><span data-stu-id="113dc-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="113dc-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="113dc-130">See also</span></span>



- [<span data-ttu-id="113dc-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="113dc-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

