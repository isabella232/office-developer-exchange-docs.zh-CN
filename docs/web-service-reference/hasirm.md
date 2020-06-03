---
title: HasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fedc04e0-cfd2-4652-a2a8-51de859ae847
description: HasIrm 元素指定会话中是否至少有一封邮件，以及当前文件夹是否为受 IRM 保护的邮件。
ms.openlocfilehash: 1596610ed5f6b2bac353900624fbec9140aaa693
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462778"
---
# <a name="hasirm"></a><span data-ttu-id="85f2c-103">HasIrm</span><span class="sxs-lookup"><span data-stu-id="85f2c-103">HasIrm</span></span>

<span data-ttu-id="85f2c-104">**HasIrm**元素指定会话中是否至少有一封邮件，以及当前文件夹是否为受 IRM 保护的邮件。</span><span class="sxs-lookup"><span data-stu-id="85f2c-104">The **HasIrm** element specifies whether at least one message in the conversation and the current folder is an IRM protected message.</span></span> 
  
```XML
<HasIrm> true | false </HasIrm>
```

 <span data-ttu-id="85f2c-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="85f2c-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85f2c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85f2c-106">Attributes and elements</span></span>

<span data-ttu-id="85f2c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85f2c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85f2c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="85f2c-108">Attributes</span></span>

<span data-ttu-id="85f2c-109">无。</span><span class="sxs-lookup"><span data-stu-id="85f2c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85f2c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="85f2c-110">Child elements</span></span>

<span data-ttu-id="85f2c-111">无。</span><span class="sxs-lookup"><span data-stu-id="85f2c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85f2c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="85f2c-112">Parent elements</span></span>

[<span data-ttu-id="85f2c-113">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="85f2c-113">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
## <a name="text-value"></a><span data-ttu-id="85f2c-114">文本值</span><span class="sxs-lookup"><span data-stu-id="85f2c-114">Text value</span></span>

<span data-ttu-id="85f2c-115">如果对话中至少有一封邮件，并且当前文件夹中有 IRM，则**HasIrm**元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="85f2c-115">The text value of the **HasIrm** element is **true** if at least one message in the conversation and the current folder has IRM.</span></span> <span data-ttu-id="85f2c-116">否则，该值为**false**。</span><span class="sxs-lookup"><span data-stu-id="85f2c-116">Otherwise, the value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85f2c-117">说明</span><span class="sxs-lookup"><span data-stu-id="85f2c-117">Remarks</span></span>

<span data-ttu-id="85f2c-118">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="85f2c-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="85f2c-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="85f2c-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85f2c-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="85f2c-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85f2c-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="85f2c-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85f2c-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="85f2c-122">Schema Name</span></span>  <br/> |<span data-ttu-id="85f2c-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="85f2c-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="85f2c-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="85f2c-124">Validation File</span></span>  <br/> |<span data-ttu-id="85f2c-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85f2c-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85f2c-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="85f2c-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="85f2c-127">True</span><span class="sxs-lookup"><span data-stu-id="85f2c-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85f2c-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85f2c-128">See also</span></span>



[<span data-ttu-id="85f2c-129">对话 (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="85f2c-129">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)


- [<span data-ttu-id="85f2c-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="85f2c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

