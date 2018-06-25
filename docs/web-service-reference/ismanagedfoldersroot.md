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
description: IsManagedFoldersRoot 元素指示托管的文件夹是否所有托管文件夹的根。
ms.openlocfilehash: 3484a3fef56545a9a8d56af65f56f75205918ec7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826044"
---
# <a name="ismanagedfoldersroot"></a><span data-ttu-id="10534-103">IsManagedFoldersRoot</span><span class="sxs-lookup"><span data-stu-id="10534-103">IsManagedFoldersRoot</span></span>

<span data-ttu-id="10534-104">**IsManagedFoldersRoot**元素指示托管的文件夹是否所有托管文件夹的根。</span><span class="sxs-lookup"><span data-stu-id="10534-104">The **IsManagedFoldersRoot** element indicates whether the managed folder is the root for all managed folders.</span></span> 
  
```xml
<IsManagedFoldersRoot/>
```

 <span data-ttu-id="10534-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="10534-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10534-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="10534-106">Attributes and elements</span></span>

<span data-ttu-id="10534-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="10534-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10534-108">属性</span><span class="sxs-lookup"><span data-stu-id="10534-108">Attributes</span></span>

<span data-ttu-id="10534-109">无。</span><span class="sxs-lookup"><span data-stu-id="10534-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10534-110">子元素</span><span class="sxs-lookup"><span data-stu-id="10534-110">Child elements</span></span>

<span data-ttu-id="10534-111">无。</span><span class="sxs-lookup"><span data-stu-id="10534-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="10534-112">父元素</span><span class="sxs-lookup"><span data-stu-id="10534-112">Parent elements</span></span>

|<span data-ttu-id="10534-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="10534-113">**Element**</span></span>|<span data-ttu-id="10534-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="10534-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10534-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="10534-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="10534-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="10534-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="10534-117">文本值</span><span class="sxs-lookup"><span data-stu-id="10534-117">Text value</span></span>

<span data-ttu-id="10534-118">如果此元素是存在，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="10534-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="10534-119">值为**true**指示文件夹处于托管文件夹; 的根文件夹如果值为**false**指示的文件夹不是托管文件夹的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="10534-119">A value of **true** indicates that the folder is the root folder of the managed folder; a value of **false** indicates that the folder is not the root folder of the managed folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10534-120">备注</span><span class="sxs-lookup"><span data-stu-id="10534-120">Remarks</span></span>

<span data-ttu-id="10534-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="10534-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10534-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="10534-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10534-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="10534-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="10534-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="10534-124">Schema name</span></span>  <br/> |<span data-ttu-id="10534-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="10534-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="10534-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="10534-126">Validation file</span></span>  <br/> |<span data-ttu-id="10534-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="10534-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="10534-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="10534-128">Can be empty</span></span>  <br/> |<span data-ttu-id="10534-129">False</span><span class="sxs-lookup"><span data-stu-id="10534-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10534-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10534-130">See also</span></span>



- [<span data-ttu-id="10534-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="10534-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

