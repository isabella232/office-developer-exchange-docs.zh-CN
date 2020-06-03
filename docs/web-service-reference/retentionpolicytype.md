---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: RetentionPolicyType 元素指定应用于会话中的项目的保留策略类型。
ms.openlocfilehash: 3900718f10e1e11d5864ebf7e64a3e1e22aa45c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462869"
---
# <a name="retentionpolicytype"></a><span data-ttu-id="a47b9-103">RetentionPolicyType</span><span class="sxs-lookup"><span data-stu-id="a47b9-103">RetentionPolicyType</span></span>

<span data-ttu-id="a47b9-104">**RetentionPolicyType**元素指定应用于会话中的项目的保留策略类型。</span><span class="sxs-lookup"><span data-stu-id="a47b9-104">The **RetentionPolicyType** element specifies the retention policy type applied to items in a conversation.</span></span> 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 <span data-ttu-id="a47b9-105">**RetentionType**</span><span class="sxs-lookup"><span data-stu-id="a47b9-105">**RetentionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a47b9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a47b9-106">Attributes and elements</span></span>

<span data-ttu-id="a47b9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a47b9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a47b9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a47b9-108">Attributes</span></span>

<span data-ttu-id="a47b9-109">无。</span><span class="sxs-lookup"><span data-stu-id="a47b9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a47b9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a47b9-110">Child elements</span></span>

<span data-ttu-id="a47b9-111">无。</span><span class="sxs-lookup"><span data-stu-id="a47b9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a47b9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a47b9-112">Parent elements</span></span>

[<span data-ttu-id="a47b9-113">ConversationAction</span><span class="sxs-lookup"><span data-stu-id="a47b9-113">ConversationAction</span></span>](conversationaction.md)
  
## <a name="text-value"></a><span data-ttu-id="a47b9-114">文本值</span><span class="sxs-lookup"><span data-stu-id="a47b9-114">Text value</span></span>

<span data-ttu-id="a47b9-115">**RetentionPolicyType**元素的文本值是应用于会话中的项目的保留类型。</span><span class="sxs-lookup"><span data-stu-id="a47b9-115">The text value of the **RetentionPolicyType** element is the retention type applied to items in a conversation.</span></span> <span data-ttu-id="a47b9-116">"**删除**" 的文本值表示当保留挂起过期时，会话中的项目将被删除。</span><span class="sxs-lookup"><span data-stu-id="a47b9-116">The text value of **Delete** indicates that the items in the conversation are deleted when the retention hold expires.</span></span> <span data-ttu-id="a47b9-117">**存档**的文本值表示在保留挂起过期时，会话中的项目将移动到存档邮箱中。</span><span class="sxs-lookup"><span data-stu-id="a47b9-117">The text value of **Archive** indicates that the items in the conversation are moved to the archive mailbox when the retention hold expires.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a47b9-118">备注</span><span class="sxs-lookup"><span data-stu-id="a47b9-118">Remarks</span></span>

<span data-ttu-id="a47b9-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a47b9-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a47b9-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a47b9-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a47b9-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="a47b9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a47b9-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="a47b9-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a47b9-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="a47b9-123">Schema name</span></span>  <br/> |<span data-ttu-id="a47b9-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="a47b9-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="a47b9-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="a47b9-125">Validation file</span></span>  <br/> |<span data-ttu-id="a47b9-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a47b9-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a47b9-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="a47b9-127">Can be empty</span></span>  <br/> ||
   

