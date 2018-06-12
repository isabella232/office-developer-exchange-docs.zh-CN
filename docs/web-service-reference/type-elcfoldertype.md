---
title: 类型 (ElcFolderType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: Type 元素指定文件夹中保留策略使用的类型。
ms.openlocfilehash: f679a9237a577d26d4b28e1b25f3e135f7193903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838292"
---
# <a name="type-elcfoldertype"></a><span data-ttu-id="fe6b9-103">类型 (ElcFolderType)</span><span class="sxs-lookup"><span data-stu-id="fe6b9-103">Type (ElcFolderType)</span></span>

<span data-ttu-id="fe6b9-104">**Type**元素指定文件夹中保留策略使用的类型。</span><span class="sxs-lookup"><span data-stu-id="fe6b9-104">The **Type** element specifies the type of folder used in a retention policy.</span></span> 
  
```XML
<Type> Calendar | Contacts | DeletedItems | Drafts | Inbox | JunkEmail | Journal | Notes | Outbox | SentItems | Tasks | All | ManagedCustomFolder | RssSubscriptions | SyncIssues | ConversationHistory | Personal | RecoverableItems | NonIpmRoot <Type>
```

 <span data-ttu-id="fe6b9-105">**ElcFolderType**</span><span class="sxs-lookup"><span data-stu-id="fe6b9-105">**ElcFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fe6b9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fe6b9-106">Attributes and elements</span></span>

<span data-ttu-id="fe6b9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fe6b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fe6b9-108">属性</span><span class="sxs-lookup"><span data-stu-id="fe6b9-108">Attributes</span></span>

<span data-ttu-id="fe6b9-109">无。</span><span class="sxs-lookup"><span data-stu-id="fe6b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fe6b9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fe6b9-110">Child elements</span></span>

<span data-ttu-id="fe6b9-111">无。</span><span class="sxs-lookup"><span data-stu-id="fe6b9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fe6b9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fe6b9-112">Parent elements</span></span>

[<span data-ttu-id="fe6b9-113">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="fe6b9-113">RetentionPolicyTag</span></span>](retentionpolicytag.md)
  
## <a name="text-value"></a><span data-ttu-id="fe6b9-114">文本值</span><span class="sxs-lookup"><span data-stu-id="fe6b9-114">Text value</span></span>

<span data-ttu-id="fe6b9-115">**Type**元素的文本值是保留策略中使用的文件夹类型。</span><span class="sxs-lookup"><span data-stu-id="fe6b9-115">The text value of the **Type** element is the folder type used in a retention policy.</span></span> <span data-ttu-id="fe6b9-116">文本值可以是下列值表示默认文件夹类型之一： 日历、 联系人、 DeletedItems、 草稿、 收件箱、 JunkEmail、 日志、 注释、 发件箱、 SentItems、 任务所有，ManagedCustomFolder RssSubscriptions、 SyncIssues，ConversationHistory、 个人、 RecoverableItems，或 NonIpmRoot</span><span class="sxs-lookup"><span data-stu-id="fe6b9-116">The text value can be one of the following values that represent a default folder type: Calendar, Contacts, DeletedItems, Drafts, Inbox, JunkEmail, Journal, Notes, Outbox, SentItems, Tasks, All, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, Personal, RecoverableItems, or NonIpmRoot</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fe6b9-117">备注</span><span class="sxs-lookup"><span data-stu-id="fe6b9-117">Remarks</span></span>

<span data-ttu-id="fe6b9-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fe6b9-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fe6b9-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fe6b9-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fe6b9-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="fe6b9-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe6b9-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="fe6b9-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fe6b9-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="fe6b9-122">Schema name</span></span>  <br/> |<span data-ttu-id="fe6b9-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="fe6b9-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="fe6b9-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="fe6b9-124">Validation file</span></span>  <br/> |<span data-ttu-id="fe6b9-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fe6b9-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fe6b9-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="fe6b9-126">Can be empty</span></span>  <br/> |<span data-ttu-id="fe6b9-127">false</span><span class="sxs-lookup"><span data-stu-id="fe6b9-127">false</span></span>  <br/> |
   

