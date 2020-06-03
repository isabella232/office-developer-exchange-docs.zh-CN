---
title: 邮箱（PreviewItemMailboxType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: 邮箱元素包含邮箱标识符和用户的主要简单邮件传输协议（SMTP）地址。
ms.openlocfilehash: 4dc5ee45c00945c30a699daa0158c96679189ab1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463893"
---
# <a name="mailbox-previewitemmailboxtype"></a><span data-ttu-id="b4c89-103">邮箱（PreviewItemMailboxType）</span><span class="sxs-lookup"><span data-stu-id="b4c89-103">Mailbox (PreviewItemMailboxType)</span></span>

<span data-ttu-id="b4c89-104">**邮箱**元素包含邮箱标识符和用户的主要简单邮件传输协议（SMTP）地址。</span><span class="sxs-lookup"><span data-stu-id="b4c89-104">The **Mailbox** element contains the mailbox identifier and the user's primary Simple Mail Transfer Protocol (SMTP) address.</span></span> 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

<span data-ttu-id="b4c89-105">**PreviewItemMailboxType**</span><span class="sxs-lookup"><span data-stu-id="b4c89-105">**PreviewItemMailboxType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b4c89-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b4c89-106">Attributes and elements</span></span>

<span data-ttu-id="b4c89-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b4c89-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4c89-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b4c89-108">Attributes</span></span>

<span data-ttu-id="b4c89-109">无。</span><span class="sxs-lookup"><span data-stu-id="b4c89-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4c89-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b4c89-110">Child elements</span></span>

<span data-ttu-id="b4c89-111">[MailboxId](mailboxid.md)  | [PrimarySmtpAddress （字符串）](primarysmtpaddress-string.md)</span><span class="sxs-lookup"><span data-stu-id="b4c89-111">[MailboxId](mailboxid.md) | [PrimarySmtpAddress (string)](primarysmtpaddress-string.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4c89-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b4c89-112">Parent elements</span></span>

[<span data-ttu-id="b4c89-113">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="b4c89-113">SearchPreviewItem</span></span>](searchpreviewitem.md)
  
## <a name="remarks"></a><span data-ttu-id="b4c89-114">备注</span><span class="sxs-lookup"><span data-stu-id="b4c89-114">Remarks</span></span>

<span data-ttu-id="b4c89-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b4c89-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b4c89-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b4c89-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4c89-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="b4c89-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4c89-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="b4c89-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b4c89-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="b4c89-119">Schema name</span></span>  <br/> |<span data-ttu-id="b4c89-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="b4c89-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="b4c89-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="b4c89-121">Validation file</span></span>  <br/> |<span data-ttu-id="b4c89-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b4c89-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b4c89-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="b4c89-123">Can be empty</span></span>  <br/> |<span data-ttu-id="b4c89-124">false</span><span class="sxs-lookup"><span data-stu-id="b4c89-124">false</span></span>  <br/> |
   

