---
title: RetentionPolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f46679d0-9236-41e2-8624-72300079c67c
description: RetentionPolicyTag 元素指定的邮箱项目的保留策略。
ms.openlocfilehash: 2525f6d7a0ca583342d28dd9f4857a69b3a8c05a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827226"
---
# <a name="retentionpolicytag"></a><span data-ttu-id="c0b8e-103">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="c0b8e-103">RetentionPolicyTag</span></span>

<span data-ttu-id="c0b8e-104">**RetentionPolicyTag**元素指定的邮箱项目的保留策略。</span><span class="sxs-lookup"><span data-stu-id="c0b8e-104">The **RetentionPolicyTag** element specifies the retention policy for a mailbox item.</span></span> 
  
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

 <span data-ttu-id="c0b8e-105">**RetentionPolicyTagType**</span><span class="sxs-lookup"><span data-stu-id="c0b8e-105">**RetentionPolicyTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0b8e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0b8e-106">Attributes and elements</span></span>

<span data-ttu-id="c0b8e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0b8e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0b8e-108">属性</span><span class="sxs-lookup"><span data-stu-id="c0b8e-108">Attributes</span></span>

<span data-ttu-id="c0b8e-109">无。</span><span class="sxs-lookup"><span data-stu-id="c0b8e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0b8e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c0b8e-110">Child elements</span></span>

<span data-ttu-id="c0b8e-111">[DisplayName （字符串）](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [类型 (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [说明](description.md) | [IsVisible](isvisible.md)  |  [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span><span class="sxs-lookup"><span data-stu-id="c0b8e-111">[DisplayName (string)](displayname-string.md) | [RetentionId](retentionid.md) | [RetentionPeriod](retentionperiod.md) | [Type (ElcFolderType)](type-elcfoldertype.md) | [RetentionAction](retentionaction.md) | [Description](description.md) | [IsVisible](isvisible.md) | [OptedInto](optedinto.md) | [IsArchive](isarchive.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0b8e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c0b8e-112">Parent elements</span></span>

[<span data-ttu-id="c0b8e-113">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="c0b8e-113">RetentionPolicyTags</span></span>](retentionpolicytags.md)
  
## <a name="remarks"></a><span data-ttu-id="c0b8e-114">备注</span><span class="sxs-lookup"><span data-stu-id="c0b8e-114">Remarks</span></span>

<span data-ttu-id="c0b8e-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c0b8e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c0b8e-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c0b8e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0b8e-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0b8e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0b8e-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0b8e-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0b8e-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0b8e-119">Schema name</span></span>  <br/> |<span data-ttu-id="c0b8e-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="c0b8e-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="c0b8e-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0b8e-121">Validation file</span></span>  <br/> |<span data-ttu-id="c0b8e-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c0b8e-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0b8e-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0b8e-123">Can be empty</span></span>  <br/> ||
   

