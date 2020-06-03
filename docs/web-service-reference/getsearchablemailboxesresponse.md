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
ms.openlocfilehash: 680fde9d9ad34dd0384e00da023796d004b66b1b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458262"
---
# <a name="getsearchablemailboxesresponse"></a><span data-ttu-id="2b6ad-103">GetSearchableMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="2b6ad-103">GetSearchableMailboxesResponse</span></span>

<span data-ttu-id="2b6ad-104">**GetSearchableMailboxesResponse**元素包含对**GetSearchableMailboxes**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="2b6ad-104">The **GetSearchableMailboxesResponse** element contains the response to a **GetSearchableMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="2b6ad-105">**GetSearchableMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2b6ad-105">**GetSearchableMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2b6ad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2b6ad-106">Attributes and elements</span></span>

<span data-ttu-id="2b6ad-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2b6ad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b6ad-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2b6ad-108">Attributes</span></span>

<span data-ttu-id="2b6ad-109">无。</span><span class="sxs-lookup"><span data-stu-id="2b6ad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2b6ad-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2b6ad-110">Child elements</span></span>

<span data-ttu-id="2b6ad-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [SearchableMailboxes](searchablemailboxes.md)  | [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="2b6ad-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [SearchableMailboxes](searchablemailboxes.md) | [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2b6ad-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2b6ad-112">Parent elements</span></span>

<span data-ttu-id="2b6ad-113">无。</span><span class="sxs-lookup"><span data-stu-id="2b6ad-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b6ad-114">说明</span><span class="sxs-lookup"><span data-stu-id="2b6ad-114">Remarks</span></span>

<span data-ttu-id="2b6ad-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2b6ad-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2b6ad-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2b6ad-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b6ad-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2b6ad-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b6ad-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2b6ad-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2b6ad-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2b6ad-119">Schema name</span></span>  <br/> |<span data-ttu-id="2b6ad-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="2b6ad-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2b6ad-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2b6ad-121">Validation file</span></span>  <br/> |<span data-ttu-id="2b6ad-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="2b6ad-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2b6ad-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2b6ad-123">Can be empty</span></span>  <br/> |<span data-ttu-id="2b6ad-124">false</span><span class="sxs-lookup"><span data-stu-id="2b6ad-124">false</span></span>  <br/> |
   

