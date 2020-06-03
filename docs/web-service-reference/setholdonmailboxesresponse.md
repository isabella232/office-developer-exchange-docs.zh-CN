---
title: SetHoldOnMailboxesResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 909194d6-e2b1-4774-bf29-04ed4318df1d
description: SetHoldOnMailboxesResponse 元素表示对 SetHoldOnMailboxes 请求的响应。
ms.openlocfilehash: 37ad5c6e8f880831a98ff2e649a92cee99930889
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44438080"
---
# <a name="setholdonmailboxesresponse"></a><span data-ttu-id="e385d-103">SetHoldOnMailboxesResponse</span><span class="sxs-lookup"><span data-stu-id="e385d-103">SetHoldOnMailboxesResponse</span></span>

<span data-ttu-id="e385d-104">**SetHoldOnMailboxesResponse**元素表示对**SetHoldOnMailboxes**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="e385d-104">The **SetHoldOnMailboxesResponse** element represents a response to a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxesResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponse>
```

 <span data-ttu-id="e385d-105">**SetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e385d-105">**SetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e385d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e385d-106">Attributes and elements</span></span>

<span data-ttu-id="e385d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e385d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e385d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e385d-108">Attributes</span></span>

<span data-ttu-id="e385d-109">无。</span><span class="sxs-lookup"><span data-stu-id="e385d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e385d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e385d-110">Child elements</span></span>

<span data-ttu-id="e385d-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [MailboxHoldResult](mailboxholdresult.md)</span><span class="sxs-lookup"><span data-stu-id="e385d-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e385d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e385d-112">Parent elements</span></span>

<span data-ttu-id="e385d-113">无。</span><span class="sxs-lookup"><span data-stu-id="e385d-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e385d-114">说明</span><span class="sxs-lookup"><span data-stu-id="e385d-114">Remarks</span></span>

<span data-ttu-id="e385d-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e385d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e385d-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e385d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e385d-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="e385d-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e385d-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="e385d-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e385d-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="e385d-119">Schema name</span></span>  <br/> |<span data-ttu-id="e385d-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="e385d-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e385d-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="e385d-121">Validation file</span></span>  <br/> |<span data-ttu-id="e385d-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e385d-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e385d-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="e385d-123">Can be empty</span></span>  <br/> |<span data-ttu-id="e385d-124">false</span><span class="sxs-lookup"><span data-stu-id="e385d-124">false</span></span>  <br/> |
   

