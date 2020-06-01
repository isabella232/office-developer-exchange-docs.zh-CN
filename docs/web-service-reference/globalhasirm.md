---
title: GlobalHasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 425272b2-7a4e-4376-aea9-d9b10c1ad6ee
description: GlobalHasIrm 元素指定会话中和所有文件夹中是否至少有一封邮件是受 IRM 保护的邮件。
ms.openlocfilehash: 10b99c9a6421a89a549b69e918087f3e542ffa09
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459467"
---
# <a name="globalhasirm"></a><span data-ttu-id="63fb0-103">GlobalHasIrm</span><span class="sxs-lookup"><span data-stu-id="63fb0-103">GlobalHasIrm</span></span>

<span data-ttu-id="63fb0-104">**GlobalHasIrm**元素指定会话中和所有文件夹中是否至少有一封邮件是受 IRM 保护的邮件。</span><span class="sxs-lookup"><span data-stu-id="63fb0-104">The **GlobalHasIrm** element specifies whether at least one message in the conversation and across all folders is an IRM protected message.</span></span> 
  
```XML
<GlobalHasIrm> true | false </GlobalHasIrm>
```

 <span data-ttu-id="63fb0-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="63fb0-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63fb0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="63fb0-106">Attributes and elements</span></span>

<span data-ttu-id="63fb0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="63fb0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63fb0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="63fb0-108">Attributes</span></span>

<span data-ttu-id="63fb0-109">无。</span><span class="sxs-lookup"><span data-stu-id="63fb0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63fb0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="63fb0-110">Child elements</span></span>

<span data-ttu-id="63fb0-111">无。</span><span class="sxs-lookup"><span data-stu-id="63fb0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="63fb0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="63fb0-112">Parent elements</span></span>

[<span data-ttu-id="63fb0-113">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="63fb0-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="63fb0-114">文本值</span><span class="sxs-lookup"><span data-stu-id="63fb0-114">Text value</span></span>

<span data-ttu-id="63fb0-115">如果对话中和所有文件夹中的至少一封邮件是受 IRM 保护的邮件，则**GlobalHasIrm**元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="63fb0-115">The text value of the **GlobalHasIrm** element is **true** if at least one message in the conversation and across all folders is an IRM protected message.</span></span> <span data-ttu-id="63fb0-116">否则，该值为**false**。</span><span class="sxs-lookup"><span data-stu-id="63fb0-116">Otherwise the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63fb0-117">说明</span><span class="sxs-lookup"><span data-stu-id="63fb0-117">Remarks</span></span>

<span data-ttu-id="63fb0-118">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="63fb0-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="63fb0-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="63fb0-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63fb0-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="63fb0-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63fb0-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="63fb0-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63fb0-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="63fb0-122">Schema Name</span></span>  <br/> |<span data-ttu-id="63fb0-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="63fb0-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="63fb0-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="63fb0-124">Validation File</span></span>  <br/> |<span data-ttu-id="63fb0-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="63fb0-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63fb0-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="63fb0-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="63fb0-127">True</span><span class="sxs-lookup"><span data-stu-id="63fb0-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63fb0-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="63fb0-128">See also</span></span>



[<span data-ttu-id="63fb0-129">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="63fb0-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="63fb0-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="63fb0-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

