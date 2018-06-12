---
title: HighlightTerms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce4a2978-fd0c-41a4-ae65-aa6f5dc9a0f9
description: HighlightTerms 元素标识 FindItem 操作和 FindConversation 操作响应中返回的突出显示的术语。
ms.openlocfilehash: c075e63674bc08773925a2a540a1c2434423926d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825808"
---
# <a name="highlightterms"></a><span data-ttu-id="b1be4-103">HighlightTerms</span><span class="sxs-lookup"><span data-stu-id="b1be4-103">HighlightTerms</span></span>

<span data-ttu-id="b1be4-104">**HighlightTerms**元素标识**FindItem**操作和**FindConversation**操作响应中返回的突出显示的术语。</span><span class="sxs-lookup"><span data-stu-id="b1be4-104">The **HighlightTerms** element identifies the highlighted terms returned in a **FindItem** operation and a **FindConversation** operation response.</span></span> 
  
```XML
<HighlightTerms>
   <Term/>
</HighlightTerms>
```

 <span data-ttu-id="b1be4-105">**ArrayOfHighlightTermsType**</span><span class="sxs-lookup"><span data-stu-id="b1be4-105">**ArrayOfHighlightTermsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1be4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b1be4-106">Attributes and elements</span></span>

<span data-ttu-id="b1be4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b1be4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1be4-108">属性</span><span class="sxs-lookup"><span data-stu-id="b1be4-108">Attributes</span></span>

<span data-ttu-id="b1be4-109">无。</span><span class="sxs-lookup"><span data-stu-id="b1be4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1be4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b1be4-110">Child elements</span></span>

<span data-ttu-id="b1be4-111">术语</span><span class="sxs-lookup"><span data-stu-id="b1be4-111">Term</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b1be4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b1be4-112">Parent elements</span></span>

<span data-ttu-id="b1be4-113">[FindConversationResponse](findconversationresponse.md) | [FindItemResponseMessage](finditemresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="b1be4-113">[FindConversationResponse](findconversationresponse.md) | [FindItemResponseMessage](finditemresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1be4-114">备注</span><span class="sxs-lookup"><span data-stu-id="b1be4-114">Remarks</span></span>

<span data-ttu-id="b1be4-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b1be4-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b1be4-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b1be4-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1be4-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="b1be4-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1be4-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="b1be4-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b1be4-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="b1be4-119">Schema name</span></span>  <br/> |<span data-ttu-id="b1be4-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="b1be4-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b1be4-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="b1be4-121">Validation file</span></span>  <br/> |<span data-ttu-id="b1be4-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b1be4-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b1be4-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="b1be4-123">Can be empty</span></span>  <br/> ||
   

