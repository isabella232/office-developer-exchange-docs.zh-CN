---
title: 修改
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Modify
api_type:
- schema
ms.assetid: 7a51e9e1-addb-4343-8a22-78f23763c0a8
description: Modify 元素指示客户端是否可以修改文件夹或项目。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: e7712644ac9c32afab06be49b438ad83bbb31058
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530413"
---
# <a name="modify"></a><span data-ttu-id="d9c89-104">修改</span><span class="sxs-lookup"><span data-stu-id="d9c89-104">Modify</span></span>

<span data-ttu-id="d9c89-105">**Modify**元素指示客户端是否可以修改文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="d9c89-105">The **Modify** element indicates whether a client can modify a folder or item.</span></span> <span data-ttu-id="d9c89-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d9c89-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Modify>true or false</Modify>
```

 <span data-ttu-id="d9c89-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="d9c89-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d9c89-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d9c89-108">Attributes and elements</span></span>

<span data-ttu-id="d9c89-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d9c89-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9c89-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d9c89-110">Attributes</span></span>

<span data-ttu-id="d9c89-111">无。</span><span class="sxs-lookup"><span data-stu-id="d9c89-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9c89-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d9c89-112">Child elements</span></span>

<span data-ttu-id="d9c89-113">无。</span><span class="sxs-lookup"><span data-stu-id="d9c89-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d9c89-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d9c89-114">Parent elements</span></span>

|<span data-ttu-id="d9c89-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="d9c89-115">**Element**</span></span>|<span data-ttu-id="d9c89-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="d9c89-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d9c89-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="d9c89-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="d9c89-118">基于项目或文件夹的权限设置，包含客户端的权限。</span><span class="sxs-lookup"><span data-stu-id="d9c89-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="d9c89-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d9c89-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d9c89-120">文本值</span><span class="sxs-lookup"><span data-stu-id="d9c89-120">Text value</span></span>

<span data-ttu-id="d9c89-121">如果文本值为**true，则**表示客户端可以修改项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="d9c89-121">A text value of **true** indicates that a client can modify an item or folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d9c89-122">说明</span><span class="sxs-lookup"><span data-stu-id="d9c89-122">Remarks</span></span>

<span data-ttu-id="d9c89-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d9c89-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9c89-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="d9c89-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9c89-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="d9c89-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d9c89-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="d9c89-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d9c89-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="d9c89-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d9c89-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="d9c89-128">Validation File</span></span>  <br/> |<span data-ttu-id="d9c89-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d9c89-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d9c89-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="d9c89-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d9c89-131">False</span><span class="sxs-lookup"><span data-stu-id="d9c89-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9c89-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d9c89-132">See also</span></span>



- [<span data-ttu-id="d9c89-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d9c89-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="d9c89-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="d9c89-134">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

