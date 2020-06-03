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
description: CanRenameOrMove 元素指示客户是否可以重命名或移动托管文件夹。
ms.openlocfilehash: eb6aaeb8b0edcab5b67212c426a44daf32a0cf73
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463361"
---
# <a name="canrenameormove"></a><span data-ttu-id="7dc1a-103">CanRenameOrMove</span><span class="sxs-lookup"><span data-stu-id="7dc1a-103">CanRenameOrMove</span></span>

<span data-ttu-id="7dc1a-104">**CanRenameOrMove**元素指示客户是否可以重命名或移动托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-104">The **CanRenameOrMove** element indicates whether a managed folder can be renamed or moved by the customer.</span></span> 
  
```xml
<CanRenameOrMove/>
```

 <span data-ttu-id="7dc1a-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="7dc1a-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7dc1a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7dc1a-106">Attributes and elements</span></span>

<span data-ttu-id="7dc1a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7dc1a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7dc1a-108">Attributes</span></span>

<span data-ttu-id="7dc1a-109">无。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7dc1a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7dc1a-110">Child elements</span></span>

<span data-ttu-id="7dc1a-111">无。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7dc1a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7dc1a-112">Parent elements</span></span>

|<span data-ttu-id="7dc1a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7dc1a-113">**Element**</span></span>|<span data-ttu-id="7dc1a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7dc1a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7dc1a-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="7dc1a-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="7dc1a-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7dc1a-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7dc1a-117">Text value</span></span>

<span data-ttu-id="7dc1a-118">该文本值表示一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="7dc1a-119">**如果值为 true** ，则表示可以重命名或移动文件夹;**如果值为 false** ，则表示无法重命名或移动文件夹。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-119">A value of **true** indicates that the folder can be renamed or moved; a value of **false** indicates that the folder cannot be renamed or moved.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7dc1a-120">说明</span><span class="sxs-lookup"><span data-stu-id="7dc1a-120">Remarks</span></span>

<span data-ttu-id="7dc1a-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7dc1a-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7dc1a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="7dc1a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7dc1a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="7dc1a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7dc1a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="7dc1a-124">Schema name</span></span>  <br/> |<span data-ttu-id="7dc1a-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="7dc1a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="7dc1a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="7dc1a-126">Validation file</span></span>  <br/> |<span data-ttu-id="7dc1a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7dc1a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7dc1a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="7dc1a-128">Can be empty</span></span>  <br/> |<span data-ttu-id="7dc1a-129">False</span><span class="sxs-lookup"><span data-stu-id="7dc1a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7dc1a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7dc1a-130">See also</span></span>



- [<span data-ttu-id="7dc1a-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7dc1a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

