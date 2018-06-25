---
title: SuppressReadReceipts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f0805560-7a2f-455b-94d2-ec4f1e3652c3
description: 应禁止显示 SuppressReadReceipts 元素指示是否读回执。
ms.openlocfilehash: 794252da6b3e6b6e6f36181c1811a2a001bfaf53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838166"
---
# <a name="suppressreadreceipts"></a><span data-ttu-id="80864-103">SuppressReadReceipts</span><span class="sxs-lookup"><span data-stu-id="80864-103">SuppressReadReceipts</span></span>

<span data-ttu-id="80864-104">**SuppressReadReceipts**元素指示是否读取应禁止显示回执。</span><span class="sxs-lookup"><span data-stu-id="80864-104">The **SuppressReadReceipts** element indicates whether read receipts should be suppressed.</span></span> 
  
```XML
<SuppressReadReceipts>true | false</SuppressReadReceipts>
```

 <span data-ttu-id="80864-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="80864-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="80864-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80864-106">Attributes and elements</span></span>

<span data-ttu-id="80864-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80864-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80864-108">属性</span><span class="sxs-lookup"><span data-stu-id="80864-108">Attributes</span></span>

<span data-ttu-id="80864-109">无。</span><span class="sxs-lookup"><span data-stu-id="80864-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80864-110">子元素</span><span class="sxs-lookup"><span data-stu-id="80864-110">Child elements</span></span>

<span data-ttu-id="80864-111">无。</span><span class="sxs-lookup"><span data-stu-id="80864-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80864-112">父元素</span><span class="sxs-lookup"><span data-stu-id="80864-112">Parent elements</span></span>

<span data-ttu-id="80864-113">[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)</span><span class="sxs-lookup"><span data-stu-id="80864-113">[ConversationAction](conversationaction.md) | [MarkAllItemsAsRead](markallitemsasread.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="80864-114">文本值</span><span class="sxs-lookup"><span data-stu-id="80864-114">Text value</span></span>

<span data-ttu-id="80864-115">文本值为**true**的**SuppressReadReciepts**元素指示的 read 回执被禁止。</span><span class="sxs-lookup"><span data-stu-id="80864-115">A text value of **true** for the **SuppressReadReciepts** element indicates that read receipts are suppressed.</span></span> <span data-ttu-id="80864-116">如果值为**false**指示的 read 将向发件人发送回执。</span><span class="sxs-lookup"><span data-stu-id="80864-116">A value of **false** indicates that read receipts will be sent to the sender.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="80864-117">备注</span><span class="sxs-lookup"><span data-stu-id="80864-117">Remarks</span></span>

<span data-ttu-id="80864-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="80864-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="80864-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="80864-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80864-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="80864-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80864-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="80864-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="80864-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="80864-122">Schema name</span></span>  <br/> |<span data-ttu-id="80864-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="80864-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="80864-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="80864-124">Validation file</span></span>  <br/> |<span data-ttu-id="80864-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="80864-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="80864-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="80864-126">Can be empty</span></span>  <br/> ||
   

