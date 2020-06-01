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
ms.openlocfilehash: a6af4181218391bc9d3c177467295d771cce4c89
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456407"
---
# <a name="setholdonmailboxesresponsemessage"></a><span data-ttu-id="15e23-103">SetHoldOnMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="15e23-103">SetHoldOnMailboxesResponseMessage</span></span>

<span data-ttu-id="15e23-104">**SetHoldOnMailboxesResponseMessage**元素指定**SetHoldOnMailboxes**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="15e23-104">The **SetHoldOnMailboxesResponseMessage** element specifies the response message for a **SetHoldOnMailboxes** request.</span></span> 
  
```XML
<SetHoldOnMailboxesResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MailboxHoldResult/>
</SetHoldOnMailboxesResponseMessage>
```

 <span data-ttu-id="15e23-105">**SetHoldOnMailboxesResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="15e23-105">**SetHoldOnMailboxesResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="15e23-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="15e23-106">Attributes and elements</span></span>

<span data-ttu-id="15e23-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="15e23-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="15e23-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="15e23-108">Attributes</span></span>

<span data-ttu-id="15e23-109">无。</span><span class="sxs-lookup"><span data-stu-id="15e23-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="15e23-110">子元素</span><span class="sxs-lookup"><span data-stu-id="15e23-110">Child elements</span></span>

<span data-ttu-id="15e23-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [MailboxHoldResult](mailboxholdresult.md)</span><span class="sxs-lookup"><span data-stu-id="15e23-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MailboxHoldResult](mailboxholdresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="15e23-112">父元素</span><span class="sxs-lookup"><span data-stu-id="15e23-112">Parent elements</span></span>

[<span data-ttu-id="15e23-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="15e23-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="15e23-114">备注</span><span class="sxs-lookup"><span data-stu-id="15e23-114">Remarks</span></span>

<span data-ttu-id="15e23-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="15e23-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="15e23-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="15e23-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="15e23-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="15e23-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="15e23-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="15e23-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="15e23-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="15e23-119">Schema name</span></span>  <br/> |<span data-ttu-id="15e23-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="15e23-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="15e23-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="15e23-121">Validation file</span></span>  <br/> |<span data-ttu-id="15e23-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="15e23-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="15e23-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="15e23-123">Can be empty</span></span>  <br/> ||
   

