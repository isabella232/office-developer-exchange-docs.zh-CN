---
title: ModifyRecipientsAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f25e673-0df0-4285-bf03-a083a395cdab
description: ModifyRecipientsAllowed 元素指定是否启用收件人的修改。
ms.openlocfilehash: 2b07c7fa8e6b5872621c8b019b60584abbf98e3c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826473"
---
# <a name="modifyrecipientsallowed"></a><span data-ttu-id="790d9-103">ModifyRecipientsAllowed</span><span class="sxs-lookup"><span data-stu-id="790d9-103">ModifyRecipientsAllowed</span></span>

<span data-ttu-id="790d9-104">**ModifyRecipientsAllowed**元素指定是否启用收件人的修改。</span><span class="sxs-lookup"><span data-stu-id="790d9-104">The **ModifyRecipientsAllowed** element specifies whether modification of the recipients is enabled.</span></span> 
  
```XML
<ModifyRecipientsAllowed> true | false </ModifyRecipientsAllowed>
```

 <span data-ttu-id="790d9-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="790d9-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="790d9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="790d9-106">Attributes and elements</span></span>

<span data-ttu-id="790d9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="790d9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="790d9-108">属性</span><span class="sxs-lookup"><span data-stu-id="790d9-108">Attributes</span></span>

<span data-ttu-id="790d9-109">无。</span><span class="sxs-lookup"><span data-stu-id="790d9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="790d9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="790d9-110">Child elements</span></span>

<span data-ttu-id="790d9-111">无。</span><span class="sxs-lookup"><span data-stu-id="790d9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="790d9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="790d9-112">Parent elements</span></span>

[<span data-ttu-id="790d9-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="790d9-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="790d9-114">文本值</span><span class="sxs-lookup"><span data-stu-id="790d9-114">Text value</span></span>

<span data-ttu-id="790d9-115">文本值为**true**的**ModifyRecipientsAllowed**元素指示的项目的收件人列表项可修改使用启用对其的权限管理。</span><span class="sxs-lookup"><span data-stu-id="790d9-115">A text value of **true** for the **ModifyRecipientsAllowed** element indicates that the item recipient list is modifiable for an item with rights management enabled on it.</span></span> <span data-ttu-id="790d9-116">如果值为**false**指示收件人列表不可修改。</span><span class="sxs-lookup"><span data-stu-id="790d9-116">A value of **false** indicates that the recipient list is not modifiable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="790d9-117">备注</span><span class="sxs-lookup"><span data-stu-id="790d9-117">Remarks</span></span>

<span data-ttu-id="790d9-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="790d9-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="790d9-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="790d9-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="790d9-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="790d9-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="790d9-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="790d9-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="790d9-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="790d9-122">Schema name</span></span>  <br/> |<span data-ttu-id="790d9-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="790d9-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="790d9-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="790d9-124">Validation file</span></span>  <br/> |<span data-ttu-id="790d9-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="790d9-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="790d9-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="790d9-126">Can be empty</span></span>  <br/> ||
   

