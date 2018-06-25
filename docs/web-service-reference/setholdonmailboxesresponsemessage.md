---
title: SetHoldOnMailboxesResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d61de0f3-24e0-434a-946a-c53d393b7d04
description: SetHoldOnMailboxesResponseMessage 元素指定 SetHoldOnMailboxes 请求的响应消息。
ms.openlocfilehash: b7cb890a71d27340e328e39c1c463fefa080b8cb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827420"
---
# <a name="setholdonmailboxesresponsemessage"></a><span data-ttu-id="ef9d0-103">SetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ef9d0-103">SetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="ef9d0-104">**SetHoldOnMailboxesResponseMessage**元素指定**SetHoldOnMailboxes**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="ef9d0-104">The **SetHoldOnMailboxesResponseMessage** element specifies the response message for a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxesResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="ef9d0-105">**SetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ef9d0-105">**SetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ef9d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ef9d0-106">Attributes and elements</span></span>

<span data-ttu-id="ef9d0-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ef9d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ef9d0-108">属性</span><span class="sxs-lookup"><span data-stu-id="ef9d0-108">Attributes</span></span>

<span data-ttu-id="ef9d0-109">无。</span><span class="sxs-lookup"><span data-stu-id="ef9d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ef9d0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ef9d0-110">Child elements</span></span>

<span data-ttu-id="ef9d0-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span><span class="sxs-lookup"><span data-stu-id="ef9d0-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ef9d0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ef9d0-112">Parent elements</span></span>

[<span data-ttu-id="ef9d0-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ef9d0-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="ef9d0-114">备注</span><span class="sxs-lookup"><span data-stu-id="ef9d0-114">Remarks</span></span>

<span data-ttu-id="ef9d0-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ef9d0-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ef9d0-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ef9d0-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ef9d0-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="ef9d0-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ef9d0-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="ef9d0-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ef9d0-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="ef9d0-119">Schema name</span></span>  <br/> |<span data-ttu-id="ef9d0-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="ef9d0-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ef9d0-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="ef9d0-121">Validation file</span></span>  <br/> |<span data-ttu-id="ef9d0-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ef9d0-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ef9d0-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="ef9d0-123">Can be empty</span></span>  <br/> ||
   

