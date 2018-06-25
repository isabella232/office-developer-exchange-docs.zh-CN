---
title: GetSearchableMailboxesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0fcc2f53-742b-46ae-bbab-c3295a3d69e7
description: GetSearchableMailboxesResponse 元素包含对 GetSearchableMailboxes 请求的响应。
ms.openlocfilehash: 35a671cd534d1b48b29ef836c24d97d7cbd52401
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754682"
---
# <a name="getsearchablemailboxesresponse"></a><span data-ttu-id="6cfc7-103">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="6cfc7-103">GetSearchableMailboxesResponse</span></span>

<span data-ttu-id="6cfc7-104">**GetSearchableMailboxesResponse**元素包含对**GetSearchableMailboxes**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-104">The **GetSearchableMailboxesResponse** element contains the response to a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<GetSearchableMailboxesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <SearchableMailboxes/>
   <FailedMailboxes/>
</GetSearchableMailboxesResponse>
```

 <span data-ttu-id="6cfc7-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6cfc7-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6cfc7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6cfc7-106">Attributes and elements</span></span>

<span data-ttu-id="6cfc7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6cfc7-108">属性</span><span class="sxs-lookup"><span data-stu-id="6cfc7-108">Attributes</span></span>

<span data-ttu-id="6cfc7-109">无。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6cfc7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6cfc7-110">Child elements</span></span>

<span data-ttu-id="6cfc7-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [SearchableMailboxes](searchablemailboxes.md) | [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="6cfc7-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [SearchableMailboxes](searchablemailboxes.md) | [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6cfc7-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6cfc7-112">Parent elements</span></span>

<span data-ttu-id="6cfc7-113">无。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6cfc7-114">备注</span><span class="sxs-lookup"><span data-stu-id="6cfc7-114">Remarks</span></span>

<span data-ttu-id="6cfc7-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6cfc7-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6cfc7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6cfc7-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="6cfc7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6cfc7-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="6cfc7-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6cfc7-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="6cfc7-119">Schema name</span></span>  <br/> |<span data-ttu-id="6cfc7-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="6cfc7-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6cfc7-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="6cfc7-121">Validation file</span></span>  <br/> |<span data-ttu-id="6cfc7-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6cfc7-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6cfc7-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="6cfc7-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6cfc7-124">false</span><span class="sxs-lookup"><span data-stu-id="6cfc7-124">false</span></span>  <br/> |
   

