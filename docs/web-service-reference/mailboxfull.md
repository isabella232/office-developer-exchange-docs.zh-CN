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
description: MailboxFull 元素指示是否已满的收件人的邮箱。
ms.openlocfilehash: 8e2c9e01b93af03e875834724a942cd9b17a73f3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826286"
---
# <a name="mailboxfull"></a><span data-ttu-id="a8e2d-103">MailboxFull</span><span class="sxs-lookup"><span data-stu-id="a8e2d-103">MailboxFull</span></span>

<span data-ttu-id="a8e2d-104">**MailboxFull**元素指示是否已满的收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-104">The **MailboxFull** element indicates whether the mailbox for the recipient is full.</span></span> 
  
```XML
<MailboxFull>true | false</MailboxFull>
```

<span data-ttu-id="a8e2d-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a8e2d-105">**Boolean**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a8e2d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a8e2d-106">Attributes and elements</span></span>

<span data-ttu-id="a8e2d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8e2d-108">属性</span><span class="sxs-lookup"><span data-stu-id="a8e2d-108">Attributes</span></span>

<span data-ttu-id="a8e2d-109">无。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8e2d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a8e2d-110">Child elements</span></span>

<span data-ttu-id="a8e2d-111">无。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a8e2d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a8e2d-112">Parent elements</span></span>

|<span data-ttu-id="a8e2d-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a8e2d-113">**Element**</span></span>|<span data-ttu-id="a8e2d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a8e2d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8e2d-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="a8e2d-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="a8e2d-116">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a8e2d-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a8e2d-117">Text value</span></span>

<span data-ttu-id="a8e2d-118">此元素可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="a8e2d-119">值为**true**指示邮箱已达到其容量;如果值为**false**指示它不已达到容量。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-119">A value of **true** indicates that the mailbox has reached its capacity; a value of **false** indicates that it has not reached capacity.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a8e2d-120">备注</span><span class="sxs-lookup"><span data-stu-id="a8e2d-120">Remarks</span></span>

<span data-ttu-id="a8e2d-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a8e2d-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8e2d-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="a8e2d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8e2d-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="a8e2d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8e2d-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="a8e2d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="a8e2d-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="a8e2d-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8e2d-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="a8e2d-126">Validation File</span></span>  <br/> |<span data-ttu-id="a8e2d-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a8e2d-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8e2d-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="a8e2d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="a8e2d-129">False</span><span class="sxs-lookup"><span data-stu-id="a8e2d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8e2d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a8e2d-130">See also</span></span>

- [<span data-ttu-id="a8e2d-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a8e2d-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

