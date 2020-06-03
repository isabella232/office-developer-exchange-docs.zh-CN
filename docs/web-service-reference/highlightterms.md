---
title: HighlightTerms
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ce4a2978-fd0c-41a4-ae65-aa6f5dc9a0f9
description: HighlightTerms 元素标识 FindItem 操作中返回的突出显示的术语和 FindConversation 操作响应。
ms.openlocfilehash: c55ffc010dc0cfb09403433aaf8a0809a26f71a3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457632"
---
# <a name="highlightterms"></a><span data-ttu-id="9ecac-103">HighlightTerms</span><span class="sxs-lookup"><span data-stu-id="9ecac-103">HighlightTerms</span></span>

<span data-ttu-id="9ecac-104">**HighlightTerms**元素标识**FindItem**操作中返回的突出显示的术语和**FindConversation**操作响应。</span><span class="sxs-lookup"><span data-stu-id="9ecac-104">The **HighlightTerms** element identifies the highlighted terms returned in a **FindItem** operation and a **FindConversation** operation response.</span></span> 
  
```XML
<HighlightTerms>
   <Term/>
</HighlightTerms>
```

 <span data-ttu-id="9ecac-105">**ArrayOfHighlightTermsType**</span><span class="sxs-lookup"><span data-stu-id="9ecac-105">**ArrayOfHighlightTermsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9ecac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9ecac-106">Attributes and elements</span></span>

<span data-ttu-id="9ecac-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9ecac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ecac-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9ecac-108">Attributes</span></span>

<span data-ttu-id="9ecac-109">无。</span><span class="sxs-lookup"><span data-stu-id="9ecac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9ecac-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9ecac-110">Child elements</span></span>

<span data-ttu-id="9ecac-111">术语</span><span class="sxs-lookup"><span data-stu-id="9ecac-111">Term</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9ecac-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9ecac-112">Parent elements</span></span>

<span data-ttu-id="9ecac-113">[FindConversationResponse](findconversationresponse.md)  | [FindItemResponseMessage](finditemresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="9ecac-113">[FindConversationResponse](findconversationresponse.md) | [FindItemResponseMessage](finditemresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9ecac-114">备注</span><span class="sxs-lookup"><span data-stu-id="9ecac-114">Remarks</span></span>

<span data-ttu-id="9ecac-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9ecac-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9ecac-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9ecac-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ecac-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="9ecac-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ecac-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="9ecac-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9ecac-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="9ecac-119">Schema name</span></span>  <br/> |<span data-ttu-id="9ecac-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="9ecac-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9ecac-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="9ecac-121">Validation file</span></span>  <br/> |<span data-ttu-id="9ecac-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9ecac-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9ecac-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="9ecac-123">Can be empty</span></span>  <br/> ||
   

