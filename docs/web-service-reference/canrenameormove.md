---
title: CanRenameOrMove
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanRenameOrMove
api_type:
- schema
ms.assetid: fe0cdb04-5f2b-4f1d-9d12-7ace0883cd86
description: CanRenameOrMove 元素指示是否可以重命名或移动客户的托管的文件夹。
ms.openlocfilehash: 0303499f5cd54d4a52222e43c2c5f0b389fbcf53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753439"
---
# <a name="canrenameormove"></a><span data-ttu-id="82298-103">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="82298-103">CanRenameOrMove</span></span>

<span data-ttu-id="82298-104">**CanRenameOrMove**元素指示是否可以重命名或移动客户的托管的文件夹。</span><span class="sxs-lookup"><span data-stu-id="82298-104">The **CanRenameOrMove** element indicates whether a managed folder can be renamed or moved by the customer.</span></span> 
  
```xml
<CanRenameOrMove/>
```

 <span data-ttu-id="82298-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="82298-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="82298-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="82298-106">Attributes and elements</span></span>

<span data-ttu-id="82298-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="82298-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="82298-108">属性</span><span class="sxs-lookup"><span data-stu-id="82298-108">Attributes</span></span>

<span data-ttu-id="82298-109">无。</span><span class="sxs-lookup"><span data-stu-id="82298-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="82298-110">子元素</span><span class="sxs-lookup"><span data-stu-id="82298-110">Child elements</span></span>

<span data-ttu-id="82298-111">无。</span><span class="sxs-lookup"><span data-stu-id="82298-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="82298-112">父元素</span><span class="sxs-lookup"><span data-stu-id="82298-112">Parent elements</span></span>

|<span data-ttu-id="82298-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="82298-113">**Element**</span></span>|<span data-ttu-id="82298-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="82298-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="82298-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="82298-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="82298-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="82298-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="82298-117">文本值</span><span class="sxs-lookup"><span data-stu-id="82298-117">Text value</span></span>

<span data-ttu-id="82298-118">文本值表示的布尔值。</span><span class="sxs-lookup"><span data-stu-id="82298-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="82298-119">值为**true**指示的文件夹可以重命名或移动;如果值为**false**指示无法重命名或移动的文件夹。</span><span class="sxs-lookup"><span data-stu-id="82298-119">A value of **true** indicates that the folder can be renamed or moved; a value of **false** indicates that the folder cannot be renamed or moved.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="82298-120">备注</span><span class="sxs-lookup"><span data-stu-id="82298-120">Remarks</span></span>

<span data-ttu-id="82298-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="82298-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="82298-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="82298-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="82298-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="82298-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="82298-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="82298-124">Schema name</span></span>  <br/> |<span data-ttu-id="82298-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="82298-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="82298-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="82298-126">Validation file</span></span>  <br/> |<span data-ttu-id="82298-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="82298-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="82298-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="82298-128">Can be empty</span></span>  <br/> |<span data-ttu-id="82298-129">False</span><span class="sxs-lookup"><span data-stu-id="82298-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="82298-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="82298-130">See also</span></span>



- [<span data-ttu-id="82298-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="82298-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

