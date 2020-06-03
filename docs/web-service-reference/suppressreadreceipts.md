---
title: SuppressReadReceipts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: SuppressReadReceipts 元素指示是否应禁止显示已读回执。
ms.openlocfilehash: aa604d4907582bd73727ba664958a589a222f9cb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455931"
---
# <a name="suppressreadreceipts"></a><span data-ttu-id="44830-103">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="44830-103">SuppressReadReceipts</span></span>

<span data-ttu-id="44830-104">**SuppressReadReceipts**元素指示是否应禁止显示已读回执。</span><span class="sxs-lookup"><span data-stu-id="44830-104">The **SuppressReadReceipts** element indicates whether read receipts should be suppressed.</span></span> 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 <span data-ttu-id="44830-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="44830-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44830-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="44830-106">Attributes and elements</span></span>

<span data-ttu-id="44830-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="44830-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44830-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="44830-108">Attributes</span></span>

<span data-ttu-id="44830-109">无。</span><span class="sxs-lookup"><span data-stu-id="44830-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44830-110">子元素</span><span class="sxs-lookup"><span data-stu-id="44830-110">Child elements</span></span>

<span data-ttu-id="44830-111">无。</span><span class="sxs-lookup"><span data-stu-id="44830-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="44830-112">父元素</span><span class="sxs-lookup"><span data-stu-id="44830-112">Parent elements</span></span>

<span data-ttu-id="44830-113">[ConversationAction](conversationaction.md)  | [MarkAllItemsAsRead](markallitemsasread.md)</span><span class="sxs-lookup"><span data-stu-id="44830-113">[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="44830-114">文本值</span><span class="sxs-lookup"><span data-stu-id="44830-114">Text value</span></span>

<span data-ttu-id="44830-115">如果**SuppressReadReciepts**元素的文本值为**true** ，则表示已取消阅读回执。</span><span class="sxs-lookup"><span data-stu-id="44830-115">A text value of **true** for the **SuppressReadReciepts** element indicates that read receipts are suppressed.</span></span> <span data-ttu-id="44830-116">**如果值为 false** ，则表示已读回执将发送给发件人。</span><span class="sxs-lookup"><span data-stu-id="44830-116">A value of **false** indicates that read receipts will be sent to the sender.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="44830-117">备注</span><span class="sxs-lookup"><span data-stu-id="44830-117">Remarks</span></span>

<span data-ttu-id="44830-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="44830-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="44830-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="44830-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44830-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="44830-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44830-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="44830-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="44830-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="44830-122">Schema name</span></span>  <br/> |<span data-ttu-id="44830-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="44830-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="44830-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="44830-124">Validation file</span></span>  <br/> |<span data-ttu-id="44830-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="44830-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="44830-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="44830-126">Can be empty</span></span>  <br/> ||
   

