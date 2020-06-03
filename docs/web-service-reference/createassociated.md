---
title: CreateAssociated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAssociated
api_type:
- schema
ms.assetid: 742a6136-6015-4924-bae4-f3868127e966
description: CreateAssociated 元素指示客户端是否可以创建关联的内容表。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: e88d7670fd9ef848221dab8cc145395bcb11e5bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460790"
---
# <a name="createassociated"></a><span data-ttu-id="ff4f6-104">CreateAssociated</span><span class="sxs-lookup"><span data-stu-id="ff4f6-104">CreateAssociated</span></span>

<span data-ttu-id="ff4f6-105">**CreateAssociated**元素指示客户端是否可以创建关联的内容表。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-105">The **CreateAssociated** element indicates whether a client can create an associated contents table.</span></span> <span data-ttu-id="ff4f6-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<CreateAssociated>true or false</CreateAssociated>
```

 <span data-ttu-id="ff4f6-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="ff4f6-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ff4f6-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ff4f6-108">Attributes and elements</span></span>

<span data-ttu-id="ff4f6-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff4f6-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="ff4f6-110">Attributes</span></span>

<span data-ttu-id="ff4f6-111">无。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ff4f6-112">子元素</span><span class="sxs-lookup"><span data-stu-id="ff4f6-112">Child elements</span></span>

<span data-ttu-id="ff4f6-113">无。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ff4f6-114">父元素</span><span class="sxs-lookup"><span data-stu-id="ff4f6-114">Parent elements</span></span>

|<span data-ttu-id="ff4f6-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="ff4f6-115">**Element**</span></span>|<span data-ttu-id="ff4f6-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="ff4f6-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ff4f6-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="ff4f6-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="ff4f6-118">基于项目或文件夹的权限设置，包含客户端的权限。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="ff4f6-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ff4f6-120">文本值</span><span class="sxs-lookup"><span data-stu-id="ff4f6-120">Text value</span></span>

<span data-ttu-id="ff4f6-121">如果文本值为**true，则**表示客户端可以创建关联的内容表。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-121">A text value of **true** indicates that a client can create an associated contents table.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ff4f6-122">备注</span><span class="sxs-lookup"><span data-stu-id="ff4f6-122">Remarks</span></span>

<span data-ttu-id="ff4f6-123">此属性仅用于 folder 对象。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-123">This property is only used on folder objects.</span></span>
  
<span data-ttu-id="ff4f6-124">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ff4f6-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff4f6-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="ff4f6-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff4f6-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="ff4f6-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ff4f6-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="ff4f6-127">Schema Name</span></span>  <br/> |<span data-ttu-id="ff4f6-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="ff4f6-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="ff4f6-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="ff4f6-129">Validation File</span></span>  <br/> |<span data-ttu-id="ff4f6-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ff4f6-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ff4f6-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="ff4f6-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="ff4f6-132">False</span><span class="sxs-lookup"><span data-stu-id="ff4f6-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff4f6-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ff4f6-133">See also</span></span>



- [<span data-ttu-id="ff4f6-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ff4f6-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ff4f6-135">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="ff4f6-135">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

