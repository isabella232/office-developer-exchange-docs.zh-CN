---
title: MailboxStatisticsSearchResult
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 73499df7-3d50-4e39-895d-6e15dd8b2777
description: MailboxStatisticsSearchResult 元素包含关键字搜索的结果。
ms.openlocfilehash: c300c6c2ec9ab3c772709edd3e6a1c7fea19d6e3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44440846"
---
# <a name="mailboxstatisticssearchresult"></a><span data-ttu-id="d5cea-103">MailboxStatisticsSearchResult</span><span class="sxs-lookup"><span data-stu-id="d5cea-103">MailboxStatisticsSearchResult</span></span>

<span data-ttu-id="d5cea-104">**MailboxStatisticsSearchResult**元素包含关键字搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="d5cea-104">The **MailboxStatisticsSearchResult** element contains the results of a keyword search.</span></span> 
  
```XML
<MailboxStatisticsSearchResult>
   <UserMailbox/>
   <KeywordStatisticsSearchResult/>
</MailboxStatisticsSearchResult>
```

<span data-ttu-id="d5cea-105">**MailboxStatisticsSearchResultType**</span><span class="sxs-lookup"><span data-stu-id="d5cea-105">**MailboxStatisticsSearchResultType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d5cea-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d5cea-106">Attributes and elements</span></span>

<span data-ttu-id="d5cea-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d5cea-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5cea-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d5cea-108">Attributes</span></span>

<span data-ttu-id="d5cea-109">无。</span><span class="sxs-lookup"><span data-stu-id="d5cea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5cea-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d5cea-110">Child elements</span></span>

<span data-ttu-id="d5cea-111">[UserMailbox](usermailbox.md)  | [KeywordStatisticsSearchResult](keywordstatisticssearchresult.md)</span><span class="sxs-lookup"><span data-stu-id="d5cea-111">[UserMailbox](usermailbox.md) | [KeywordStatisticsSearchResult](keywordstatisticssearchresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d5cea-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d5cea-112">Parent elements</span></span>

[<span data-ttu-id="d5cea-113">FindMailboxStatisticsByKeywordsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d5cea-113">FindMailboxStatisticsByKeywordsResponseMessage</span></span>](findmailboxstatisticsbykeywordsresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="d5cea-114">备注</span><span class="sxs-lookup"><span data-stu-id="d5cea-114">Remarks</span></span>

<span data-ttu-id="d5cea-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d5cea-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d5cea-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d5cea-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5cea-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="d5cea-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5cea-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="d5cea-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5cea-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="d5cea-119">Schema name</span></span>  <br/> |<span data-ttu-id="d5cea-120">邮件架构</span><span class="sxs-lookup"><span data-stu-id="d5cea-120">messages schema</span></span>  <br/> |
|<span data-ttu-id="d5cea-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="d5cea-121">Validation file</span></span>  <br/> |<span data-ttu-id="d5cea-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="d5cea-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5cea-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="d5cea-123">Can be empty</span></span>  <br/> ||
   

