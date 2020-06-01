---
title: MailboxFull
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxFull
api_type:
- schema
ms.assetid: 38b28c9b-9da2-4d6a-9cda-9c393986575b
description: MailboxFull 元素指示收件人的邮箱是否已满。
ms.openlocfilehash: f336f1eda122bb170aafb22a028e3faf84f4d782
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465973"
---
# <a name="mailboxfull"></a><span data-ttu-id="8fc1f-103">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="8fc1f-103">MailboxFull</span></span>

<span data-ttu-id="8fc1f-104">**MailboxFull**元素指示收件人的邮箱是否已满。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-104">The **MailboxFull** element indicates whether the mailbox for the recipient is full.</span></span> 
  
```XML
<MailboxFull>true | false</MailboxFull>
```

<span data-ttu-id="8fc1f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="8fc1f-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8fc1f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8fc1f-106">Attributes and elements</span></span>

<span data-ttu-id="8fc1f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8fc1f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8fc1f-108">Attributes</span></span>

<span data-ttu-id="8fc1f-109">无。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8fc1f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8fc1f-110">Child elements</span></span>

<span data-ttu-id="8fc1f-111">无。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8fc1f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8fc1f-112">Parent elements</span></span>

|<span data-ttu-id="8fc1f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8fc1f-113">**Element**</span></span>|<span data-ttu-id="8fc1f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="8fc1f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8fc1f-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="8fc1f-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="8fc1f-116">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8fc1f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="8fc1f-117">Text value</span></span>

<span data-ttu-id="8fc1f-118">此元素可以是**true** ，也可以是**false**。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="8fc1f-119">**如果值为 true** ，则表示邮箱已达到其容量;**如果值为 false** ，则表示没有达到容量。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-119">A value of **true** indicates that the mailbox has reached its capacity; a value of **false** indicates that it has not reached capacity.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8fc1f-120">说明</span><span class="sxs-lookup"><span data-stu-id="8fc1f-120">Remarks</span></span>

<span data-ttu-id="8fc1f-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8fc1f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8fc1f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8fc1f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8fc1f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8fc1f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8fc1f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8fc1f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="8fc1f-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="8fc1f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="8fc1f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8fc1f-126">Validation File</span></span>  <br/> |<span data-ttu-id="8fc1f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8fc1f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8fc1f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8fc1f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="8fc1f-129">False</span><span class="sxs-lookup"><span data-stu-id="8fc1f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8fc1f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8fc1f-130">See also</span></span>

- [<span data-ttu-id="8fc1f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8fc1f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

