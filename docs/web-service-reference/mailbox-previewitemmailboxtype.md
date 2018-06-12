---
title: 邮箱 (PreviewItemMailboxType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: 邮箱元素包含邮箱标识符和用户的主要简单邮件传输协议 (SMTP) 地址。
ms.openlocfilehash: 1b6669928015bc880806479d294a4063034a559f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826255"
---
# <a name="mailbox-previewitemmailboxtype"></a><span data-ttu-id="633ae-103">邮箱 (PreviewItemMailboxType)</span><span class="sxs-lookup"><span data-stu-id="633ae-103">Mailbox (PreviewItemMailboxType)</span></span>

<span data-ttu-id="633ae-104">**邮箱**元素包含邮箱标识符和用户的主要简单邮件传输协议 (SMTP) 地址。</span><span class="sxs-lookup"><span data-stu-id="633ae-104">The **Mailbox** element contains the mailbox identifier and the user's primary Simple Mail Transfer Protocol (SMTP) address.</span></span> 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

<span data-ttu-id="633ae-105">**PreviewItemMailboxType**</span><span class="sxs-lookup"><span data-stu-id="633ae-105">**PreviewItemMailboxType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="633ae-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="633ae-106">Attributes and elements</span></span>

<span data-ttu-id="633ae-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="633ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="633ae-108">属性</span><span class="sxs-lookup"><span data-stu-id="633ae-108">Attributes</span></span>

<span data-ttu-id="633ae-109">无。</span><span class="sxs-lookup"><span data-stu-id="633ae-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="633ae-110">子元素</span><span class="sxs-lookup"><span data-stu-id="633ae-110">Child elements</span></span>

<span data-ttu-id="633ae-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress （字符串）](primarysmtpaddress-string.md)</span><span class="sxs-lookup"><span data-stu-id="633ae-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="633ae-112">父元素</span><span class="sxs-lookup"><span data-stu-id="633ae-112">Parent elements</span></span>

[<span data-ttu-id="633ae-113">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="633ae-113">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="633ae-114">备注</span><span class="sxs-lookup"><span data-stu-id="633ae-114">Remarks</span></span>

<span data-ttu-id="633ae-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="633ae-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="633ae-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="633ae-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="633ae-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="633ae-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="633ae-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="633ae-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="633ae-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="633ae-119">Schema name</span></span>  <br/> |<span data-ttu-id="633ae-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="633ae-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="633ae-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="633ae-121">Validation file</span></span>  <br/> |<span data-ttu-id="633ae-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="633ae-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="633ae-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="633ae-123">Can be empty</span></span>  <br/> |<span data-ttu-id="633ae-124">false</span><span class="sxs-lookup"><span data-stu-id="633ae-124">false</span></span>  <br/> |
   

