---
title: 类型（ElcFolderType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: Type 元素指定保留策略中使用的文件夹的类型。
ms.openlocfilehash: f6fcc7942a530ada2d6e72c3e38286a7595b09ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465105"
---
# <a name="type-elcfoldertype"></a><span data-ttu-id="d0d42-103">类型（ElcFolderType）</span><span class="sxs-lookup"><span data-stu-id="d0d42-103">Type (ElcFolderType)</span></span>

<span data-ttu-id="d0d42-104">**Type**元素指定保留策略中使用的文件夹的类型。</span><span class="sxs-lookup"><span data-stu-id="d0d42-104">The **Type** element specifies the type of folder used in a retention policy.</span></span> 
  
```XML
<Type> Calendar | Contacts | DeletedItems | Drafts | Inbox | JunkEmail | Journal | Notes | Outbox | SentItems | Tasks | All | ManagedCustomFolder | RssSubscriptions | SyncIssues | ConversationHistory | Personal | RecoverableItems | NonIpmRoot <Type>
```

 <span data-ttu-id="d0d42-105">**ElcFolderType**</span><span class="sxs-lookup"><span data-stu-id="d0d42-105">**ElcFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0d42-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d0d42-106">Attributes and elements</span></span>

<span data-ttu-id="d0d42-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0d42-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0d42-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d0d42-108">Attributes</span></span>

<span data-ttu-id="d0d42-109">无。</span><span class="sxs-lookup"><span data-stu-id="d0d42-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0d42-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d0d42-110">Child elements</span></span>

<span data-ttu-id="d0d42-111">无。</span><span class="sxs-lookup"><span data-stu-id="d0d42-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d0d42-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d0d42-112">Parent elements</span></span>

[<span data-ttu-id="d0d42-113">Get-retentionpolicytag</span><span class="sxs-lookup"><span data-stu-id="d0d42-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="d0d42-114">文本值</span><span class="sxs-lookup"><span data-stu-id="d0d42-114">Text value</span></span>

<span data-ttu-id="d0d42-115">**Type**元素的文本值是在保留策略中使用的文件夹类型。</span><span class="sxs-lookup"><span data-stu-id="d0d42-115">The text value of the **Type** element is the folder type used in a retention policy.</span></span> <span data-ttu-id="d0d42-116">Text 值可以是下列值之一：日历、联系人、DeletedItems、草稿、收件箱、JunkEmail、日记、便笺、发件箱、已发送邮件、任务、全部、ManagedCustomFolder、RssSubscriptions、SyncIssues、ConversationHistory、个人、RecoverableItems 或 NonIpmRoot</span><span class="sxs-lookup"><span data-stu-id="d0d42-116">The text value can be one of the following values that represent a default folder type: Calendar, Contacts, DeletedItems, Drafts, Inbox, JunkEmail, Journal, Notes, Outbox, SentItems, Tasks, All, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, Personal, RecoverableItems, or NonIpmRoot</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0d42-117">备注</span><span class="sxs-lookup"><span data-stu-id="d0d42-117">Remarks</span></span>

<span data-ttu-id="d0d42-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d0d42-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d0d42-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d0d42-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0d42-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="d0d42-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0d42-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="d0d42-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0d42-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="d0d42-122">Schema name</span></span>  <br/> |<span data-ttu-id="d0d42-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="d0d42-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0d42-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="d0d42-124">Validation file</span></span>  <br/> |<span data-ttu-id="d0d42-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d0d42-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0d42-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="d0d42-126">Can be empty</span></span>  <br/> |<span data-ttu-id="d0d42-127">false</span><span class="sxs-lookup"><span data-stu-id="d0d42-127">false</span></span>  <br/> |
   

