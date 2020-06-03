---
title: 阅读
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Read
api_type:
- schema
ms.assetid: b14637e9-1695-4b7e-b078-ae527c2e4303
description: Read 元素指示客户端是否可以读取文件夹或项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: d75285e0ab14c4f53d73cb7f4349196e07c3c521
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468311"
---
# <a name="read"></a><span data-ttu-id="19c33-104">阅读</span><span class="sxs-lookup"><span data-stu-id="19c33-104">Read</span></span>

<span data-ttu-id="19c33-105">**Read**元素指示客户端是否可以读取文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="19c33-105">The **Read** element indicates whether a client can read a folder or item.</span></span> <span data-ttu-id="19c33-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="19c33-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Read>true or false</Read>
```

 <span data-ttu-id="19c33-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="19c33-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19c33-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="19c33-108">Attributes and elements</span></span>

<span data-ttu-id="19c33-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="19c33-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19c33-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="19c33-110">Attributes</span></span>

<span data-ttu-id="19c33-111">无。</span><span class="sxs-lookup"><span data-stu-id="19c33-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19c33-112">子元素</span><span class="sxs-lookup"><span data-stu-id="19c33-112">Child elements</span></span>

<span data-ttu-id="19c33-113">无。</span><span class="sxs-lookup"><span data-stu-id="19c33-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="19c33-114">父元素</span><span class="sxs-lookup"><span data-stu-id="19c33-114">Parent elements</span></span>

|<span data-ttu-id="19c33-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="19c33-115">**Element**</span></span>|<span data-ttu-id="19c33-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="19c33-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19c33-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="19c33-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="19c33-118">基于项目或文件夹的权限设置，包含客户端的权限。</span><span class="sxs-lookup"><span data-stu-id="19c33-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="19c33-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="19c33-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="19c33-120">文本值</span><span class="sxs-lookup"><span data-stu-id="19c33-120">Text value</span></span>

<span data-ttu-id="19c33-121">如果文本值为**true，则**表示客户端可以读取文件夹的项目。</span><span class="sxs-lookup"><span data-stu-id="19c33-121">A text value of **true** indicates that a client can read an item of folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="19c33-122">说明</span><span class="sxs-lookup"><span data-stu-id="19c33-122">Remarks</span></span>

<span data-ttu-id="19c33-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="19c33-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19c33-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="19c33-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19c33-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="19c33-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19c33-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="19c33-126">Schema Name</span></span>  <br/> |<span data-ttu-id="19c33-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="19c33-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="19c33-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="19c33-128">Validation File</span></span>  <br/> |<span data-ttu-id="19c33-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19c33-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19c33-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="19c33-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="19c33-131">False</span><span class="sxs-lookup"><span data-stu-id="19c33-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19c33-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="19c33-132">See also</span></span>



- [<span data-ttu-id="19c33-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="19c33-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="19c33-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="19c33-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

