---
title: Get-retentionpolicytag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: Get-retentionpolicytag 元素指定邮箱项目的保留策略。
ms.openlocfilehash: 3ece841e14e6cf11ab15e4a4d8b83a778ae32e46
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465175"
---
# <a name="retentionpolicytag"></a><span data-ttu-id="241b7-103">Get-retentionpolicytag</span><span class="sxs-lookup"><span data-stu-id="241b7-103">RetentionPolicyTag</span></span>

<span data-ttu-id="241b7-104">**Get-retentionpolicytag**元素指定邮箱项目的保留策略。</span><span class="sxs-lookup"><span data-stu-id="241b7-104">The **RetentionPolicyTag** element specifies the retention policy for a mailbox item.</span></span> 
  
```XML
<RetentionPolicyTag>
   <DisplayName/>
   <RetentionId/>
   <RetentionPeriod/>
   <Type/>
   <RetentionAction/>
   <Description/>
   <IsVisible/>
   <OptedInto/>
   <IsArchive/>
</RetentionPolicyTag>
```

 <span data-ttu-id="241b7-105">**RetentionPolicyTagType**</span><span class="sxs-lookup"><span data-stu-id="241b7-105">**RetentionPolicyTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="241b7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="241b7-106">Attributes and elements</span></span>

<span data-ttu-id="241b7-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="241b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="241b7-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="241b7-108">Attributes</span></span>

<span data-ttu-id="241b7-109">无。</span><span class="sxs-lookup"><span data-stu-id="241b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="241b7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="241b7-110">Child elements</span></span>

<span data-ttu-id="241b7-111">[DisplayName （string）](displayname-string.md)  | [RetentionId](retentionid.md)  | [RetentionPeriod](retentionperiod.md)  | [类型（ElcFolderType）](type-elcfoldertype.md)  | [RetentionAction](retentionaction.md)  | [说明](description.md)  | [IsVisible](isvisible.md)  | [OptedInto](optedinto.md)  | [IsArchive](isarchive.md)</span><span class="sxs-lookup"><span data-stu-id="241b7-111">[DisplayName (string)](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [Type (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Description](description.md) | [IsVisible](isvisible.md) | [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="241b7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="241b7-112">Parent elements</span></span>

[<span data-ttu-id="241b7-113">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="241b7-113">RetentionPolicyTags</span></span>](retentionpolicytags.md)
  
## <a name="remarks"></a><span data-ttu-id="241b7-114">备注</span><span class="sxs-lookup"><span data-stu-id="241b7-114">Remarks</span></span>

<span data-ttu-id="241b7-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="241b7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="241b7-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="241b7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="241b7-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="241b7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="241b7-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="241b7-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="241b7-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="241b7-119">Schema name</span></span>  <br/> |<span data-ttu-id="241b7-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="241b7-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="241b7-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="241b7-121">Validation file</span></span>  <br/> |<span data-ttu-id="241b7-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="241b7-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="241b7-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="241b7-123">Can be empty</span></span>  <br/> ||
   

