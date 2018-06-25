---
title: IsOwner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ea0f0afc-32fe-46cb-8530-62a6ce9490f6
description: IsOwner 元素指定指定电子邮件的用户是否所有者。
ms.openlocfilehash: aac3c2a599093282542025468d73c55ec4569e29
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826080"
---
# <a name="isowner"></a><span data-ttu-id="ba9a0-103">IsOwner</span><span class="sxs-lookup"><span data-stu-id="ba9a0-103">IsOwner</span></span>

<span data-ttu-id="ba9a0-104">**IsOwner**元素指定指定电子邮件的用户是否所有者。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-104">The **IsOwner** element specifies whether the specified email user is the owner.</span></span> 
  
```XML
<IsOwner>true | false</IsOwner>
```

 <span data-ttu-id="ba9a0-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ba9a0-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ba9a0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ba9a0-106">Attributes and elements</span></span>

<span data-ttu-id="ba9a0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ba9a0-108">属性</span><span class="sxs-lookup"><span data-stu-id="ba9a0-108">Attributes</span></span>

<span data-ttu-id="ba9a0-109">无。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ba9a0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ba9a0-110">Child elements</span></span>

<span data-ttu-id="ba9a0-111">无。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ba9a0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ba9a0-112">Parent elements</span></span>

|<span data-ttu-id="ba9a0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ba9a0-113">**Element**</span></span>|<span data-ttu-id="ba9a0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ba9a0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ba9a0-115">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="ba9a0-115">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md) <br/> |<span data-ttu-id="ba9a0-116">指定有关权限管理许可证的信息。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-116">Specifies information about the rights management license.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ba9a0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ba9a0-117">Text value</span></span>

<span data-ttu-id="ba9a0-118">文本值为**true**的**IsOwner**元素指示用户是项目上颁发的权限的所有者。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-118">A text value of **true** for the **IsOwner** element indicates that the user is the owner of rights issued on an item.</span></span> <span data-ttu-id="ba9a0-119">如果值为**false**指示用户不是项目上颁发的权限的所有者。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-119">A value of **false** indicates that the user is not the owner of rights issued on an item.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ba9a0-120">备注</span><span class="sxs-lookup"><span data-stu-id="ba9a0-120">Remarks</span></span>

<span data-ttu-id="ba9a0-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ba9a0-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ba9a0-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ba9a0-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="ba9a0-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ba9a0-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="ba9a0-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ba9a0-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="ba9a0-125">Schema Name</span></span>  <br/> |<span data-ttu-id="ba9a0-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="ba9a0-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="ba9a0-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="ba9a0-127">Validation File</span></span>  <br/> |<span data-ttu-id="ba9a0-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="ba9a0-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="ba9a0-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="ba9a0-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="ba9a0-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ba9a0-130">See also</span></span>



- [<span data-ttu-id="ba9a0-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ba9a0-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

