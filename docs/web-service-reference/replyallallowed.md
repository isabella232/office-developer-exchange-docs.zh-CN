---
title: ReplyAllAllowed
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d22f68cf-b18b-45d0-a9ff-414b7db0e67e
description: ReplyAllAllowed 元素指定是否允许对权限托管数据进行全部答复。
ms.openlocfilehash: 56dfe7670ed87581999bfe0a340bcc72c99d04ea
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467912"
---
# <a name="replyallallowed"></a><span data-ttu-id="11892-103">ReplyAllAllowed</span><span class="sxs-lookup"><span data-stu-id="11892-103">ReplyAllAllowed</span></span>

<span data-ttu-id="11892-104">**ReplyAllAllowed**元素指定是否允许对权限托管数据进行全部答复。</span><span class="sxs-lookup"><span data-stu-id="11892-104">The **ReplyAllAllowed** element specifies whether a reply all is allowed for rights managed data.</span></span> 
  
```XML
<ReplyAllAllowed> true | false </ReplyAllAllowed>
```

 <span data-ttu-id="11892-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="11892-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="11892-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="11892-106">Attributes and elements</span></span>

<span data-ttu-id="11892-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="11892-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11892-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="11892-108">Attributes</span></span>

<span data-ttu-id="11892-109">无。</span><span class="sxs-lookup"><span data-stu-id="11892-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="11892-110">子元素</span><span class="sxs-lookup"><span data-stu-id="11892-110">Child elements</span></span>

<span data-ttu-id="11892-111">无。</span><span class="sxs-lookup"><span data-stu-id="11892-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="11892-112">父元素</span><span class="sxs-lookup"><span data-stu-id="11892-112">Parent elements</span></span>

[<span data-ttu-id="11892-113">RightsManagementLicenseData</span><span class="sxs-lookup"><span data-stu-id="11892-113">RightsManagementLicenseData</span></span>](rightsmanagementlicensedata.md)
  
## <a name="text-value"></a><span data-ttu-id="11892-114">文本值</span><span class="sxs-lookup"><span data-stu-id="11892-114">Text value</span></span>

<span data-ttu-id="11892-115">如果**ReplyAllAllowed**元素的文本值为**true** ，则表示允许权限托管数据的全部答复。</span><span class="sxs-lookup"><span data-stu-id="11892-115">A text value of **true** for the **ReplyAllAllowed** element indicates that a reply all is allowed for the rights managed data.</span></span> <span data-ttu-id="11892-116">**如果值为 false** ，则表示不允许全部答复。</span><span class="sxs-lookup"><span data-stu-id="11892-116">A value of **false** indicates that a reply all is not allowed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="11892-117">备注</span><span class="sxs-lookup"><span data-stu-id="11892-117">Remarks</span></span>

<span data-ttu-id="11892-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="11892-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="11892-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="11892-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11892-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="11892-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11892-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="11892-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11892-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="11892-122">Schema name</span></span>  <br/> |<span data-ttu-id="11892-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="11892-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="11892-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="11892-124">Validation file</span></span>  <br/> |<span data-ttu-id="11892-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="11892-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11892-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="11892-126">Can be empty</span></span>  <br/> ||
   

