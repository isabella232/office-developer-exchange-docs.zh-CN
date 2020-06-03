---
title: ModifyRecipientsAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f25e673-0df0-4285-bf03-a083a395cdab
description: ModifyRecipientsAllowed 元素指定是否启用对收件人所做的修改。
ms.openlocfilehash: 3154ec3aceb2da7911002d505e0c452bf920d71f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465693"
---
# <a name="modifyrecipientsallowed"></a><span data-ttu-id="a52e0-103">ModifyRecipientsAllowed</span><span class="sxs-lookup"><span data-stu-id="a52e0-103">ModifyRecipientsAllowed</span></span>

<span data-ttu-id="a52e0-104">**ModifyRecipientsAllowed**元素指定是否启用对收件人所做的修改。</span><span class="sxs-lookup"><span data-stu-id="a52e0-104">The **ModifyRecipientsAllowed** element specifies whether modification of the recipients is enabled.</span></span> 
  
```XML
<ModifyRecipientsAllowed> true | false </ModifyRecipientsAllowed>
```

 <span data-ttu-id="a52e0-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="a52e0-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a52e0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a52e0-106">Attributes and elements</span></span>

<span data-ttu-id="a52e0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a52e0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a52e0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a52e0-108">Attributes</span></span>

<span data-ttu-id="a52e0-109">无。</span><span class="sxs-lookup"><span data-stu-id="a52e0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a52e0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a52e0-110">Child elements</span></span>

<span data-ttu-id="a52e0-111">无。</span><span class="sxs-lookup"><span data-stu-id="a52e0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a52e0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a52e0-112">Parent elements</span></span>

[<span data-ttu-id="a52e0-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="a52e0-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="a52e0-114">文本值</span><span class="sxs-lookup"><span data-stu-id="a52e0-114">Text value</span></span>

<span data-ttu-id="a52e0-115">如果**ModifyRecipientsAllowed**元素的文本值为**true** ，则表示项目收件人列表对在其上启用了权限管理的项目是可修改的。</span><span class="sxs-lookup"><span data-stu-id="a52e0-115">A text value of **true** for the **ModifyRecipientsAllowed** element indicates that the item recipient list is modifiable for an item with rights management enabled on it.</span></span> <span data-ttu-id="a52e0-116">**如果值为 false** ，则表示收件人列表不可修改。</span><span class="sxs-lookup"><span data-stu-id="a52e0-116">A value of **false** indicates that the recipient list is not modifiable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a52e0-117">备注</span><span class="sxs-lookup"><span data-stu-id="a52e0-117">Remarks</span></span>

<span data-ttu-id="a52e0-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a52e0-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a52e0-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a52e0-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a52e0-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="a52e0-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a52e0-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="a52e0-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a52e0-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="a52e0-122">Schema name</span></span>  <br/> |<span data-ttu-id="a52e0-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="a52e0-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="a52e0-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="a52e0-124">Validation file</span></span>  <br/> |<span data-ttu-id="a52e0-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a52e0-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a52e0-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="a52e0-126">Can be empty</span></span>  <br/> ||
   

