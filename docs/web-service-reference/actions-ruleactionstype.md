---
title: 操作 (RuleActionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2afba70c-65f7-458c-a4e6-a2cd9bccc0f9
description: Actions 元素包含与收件箱规则关联的操作的列表。
ms.openlocfilehash: 8ed8095ca8b41e037c2c0dad319c9c4ab99ed2bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753187"
---
# <a name="actions-ruleactionstype"></a><span data-ttu-id="fec0c-103">操作 (RuleActionsType)</span><span class="sxs-lookup"><span data-stu-id="fec0c-103">Actions (RuleActionsType)</span></span>

<span data-ttu-id="fec0c-104">**Actions**元素包含与收件箱规则关联的操作的列表。</span><span class="sxs-lookup"><span data-stu-id="fec0c-104">The **Actions** element contains a list of actions associated with Inbox rules.</span></span> 
  
```XML
<Actions>
   <AssignCategories/>
   <CopyToFolder/>
   <Delete/>
   <ForwardAsAttachmentToRecipients/>
   <ForwardToRecipients/>
   <MarkImportance/>
   <MarkAsRead/>
   <MoveToFolder/>
   <PermanentDelete/>
   <RedirectToRecipients/>
   <SendSMSAlertToRecipients/>
   <ServerReplyWithMessage/>
   <StopProcessingRules/>
</Actions>
```

 <span data-ttu-id="fec0c-105">**RuleActionsType**</span><span class="sxs-lookup"><span data-stu-id="fec0c-105">**RuleActionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fec0c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fec0c-106">Attributes and elements</span></span>

<span data-ttu-id="fec0c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fec0c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fec0c-108">属性</span><span class="sxs-lookup"><span data-stu-id="fec0c-108">Attributes</span></span>

<span data-ttu-id="fec0c-109">无。</span><span class="sxs-lookup"><span data-stu-id="fec0c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fec0c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fec0c-110">Child elements</span></span>

<span data-ttu-id="fec0c-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [删除](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead](markasread.md)  |  [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md)  |  [StopProcessingRules](stopprocessingrules.md)</span><span class="sxs-lookup"><span data-stu-id="fec0c-111">[AssignCategories](assigncategories.md) | [CopyToFolder](copytofolder.md) | [Delete](delete.md) | [ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) | [ForwardToRecipients](forwardtorecipients.md) | [MarkImportance](markimportance.md) | [MarkAsRead](markasread.md) | [MoveToFolder](movetofolder.md) | [PermanentDelete](permanentdelete.md) | [RedirectToRecipients](redirecttorecipients.md) | [SendSMSAlertToRecipients](sendsmsalerttorecipients.md) | [ServerReplyWithMessage](serverreplywithmessage.md) | [StopProcessingRules](stopprocessingrules.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fec0c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fec0c-112">Parent elements</span></span>

[<span data-ttu-id="fec0c-113">规则 (RuleType)</span><span class="sxs-lookup"><span data-stu-id="fec0c-113">Rule (RuleType)</span></span>](rule-ruletype.md)
  
## <a name="remarks"></a><span data-ttu-id="fec0c-114">备注</span><span class="sxs-lookup"><span data-stu-id="fec0c-114">Remarks</span></span>

<span data-ttu-id="fec0c-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fec0c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fec0c-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fec0c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fec0c-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="fec0c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fec0c-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="fec0c-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fec0c-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="fec0c-119">Schema name</span></span>  <br/> |<span data-ttu-id="fec0c-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="fec0c-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="fec0c-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="fec0c-121">Validation file</span></span>  <br/> |<span data-ttu-id="fec0c-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fec0c-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fec0c-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="fec0c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="fec0c-124">false</span><span class="sxs-lookup"><span data-stu-id="fec0c-124">false</span></span>  <br/> |
   

