---
title: 已阅读
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
description: 读取元素指示客户端是否可以读取文件夹或项目。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: cd9c2c9802c78b202418e3947f5b5718b0f676cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826948"
---
# <a name="read"></a><span data-ttu-id="c6239-104">已阅读</span><span class="sxs-lookup"><span data-stu-id="c6239-104">Read</span></span>

<span data-ttu-id="c6239-105">**读取**元素指示客户端是否可以读取文件夹或项目。</span><span class="sxs-lookup"><span data-stu-id="c6239-105">The **Read** element indicates whether a client can read a folder or item.</span></span> <span data-ttu-id="c6239-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c6239-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<Read>true or false</Read>
```

 <span data-ttu-id="c6239-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="c6239-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c6239-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c6239-108">Attributes and elements</span></span>

<span data-ttu-id="c6239-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c6239-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c6239-110">属性</span><span class="sxs-lookup"><span data-stu-id="c6239-110">Attributes</span></span>

<span data-ttu-id="c6239-111">无。</span><span class="sxs-lookup"><span data-stu-id="c6239-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c6239-112">子元素</span><span class="sxs-lookup"><span data-stu-id="c6239-112">Child elements</span></span>

<span data-ttu-id="c6239-113">无。</span><span class="sxs-lookup"><span data-stu-id="c6239-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c6239-114">父元素</span><span class="sxs-lookup"><span data-stu-id="c6239-114">Parent elements</span></span>

|<span data-ttu-id="c6239-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="c6239-115">**Element**</span></span>|<span data-ttu-id="c6239-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="c6239-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c6239-117">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="c6239-117">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="c6239-118">包含客户端基于的项目或文件夹的权限设置的权限。</span><span class="sxs-lookup"><span data-stu-id="c6239-118">Contains the rights of the client based on the permission settings for the item or folder.</span></span> <span data-ttu-id="c6239-119">在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c6239-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c6239-120">文本值</span><span class="sxs-lookup"><span data-stu-id="c6239-120">Text value</span></span>

<span data-ttu-id="c6239-121">文本值为**true**指示客户端可以读取文件夹的项目。</span><span class="sxs-lookup"><span data-stu-id="c6239-121">A text value of **true** indicates that a client can read an item of folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c6239-122">备注</span><span class="sxs-lookup"><span data-stu-id="c6239-122">Remarks</span></span>

<span data-ttu-id="c6239-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c6239-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c6239-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c6239-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c6239-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c6239-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c6239-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c6239-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c6239-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c6239-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c6239-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c6239-128">Validation File</span></span>  <br/> |<span data-ttu-id="c6239-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c6239-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c6239-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c6239-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c6239-131">False</span><span class="sxs-lookup"><span data-stu-id="c6239-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c6239-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c6239-132">See also</span></span>



- [<span data-ttu-id="c6239-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c6239-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c6239-134">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="c6239-134">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

