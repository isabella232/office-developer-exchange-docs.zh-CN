---
title: 名称 (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Name
api_type:
- schema
ms.assetid: 98c58c53-9acc-4e89-9fcf-03f1b05abee1
description: Name 元素表示的邮箱用户的名称。
ms.openlocfilehash: b140fd46608a04f9aaba17f917cc4171c056dcf2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826504"
---
# <a name="name-emailaddresstype"></a><span data-ttu-id="32b81-103">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="32b81-103">Name (EmailAddressType)</span></span>

<span data-ttu-id="32b81-104">**Name**元素表示的邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="32b81-104">The **Name** element represents the name of a mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="32b81-105">**string**</span><span class="sxs-lookup"><span data-stu-id="32b81-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="32b81-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="32b81-106">Attributes and elements</span></span>

<span data-ttu-id="32b81-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="32b81-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32b81-108">属性</span><span class="sxs-lookup"><span data-stu-id="32b81-108">Attributes</span></span>

<span data-ttu-id="32b81-109">无。</span><span class="sxs-lookup"><span data-stu-id="32b81-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32b81-110">子元素</span><span class="sxs-lookup"><span data-stu-id="32b81-110">Child elements</span></span>

<span data-ttu-id="32b81-111">无。</span><span class="sxs-lookup"><span data-stu-id="32b81-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="32b81-112">父元素</span><span class="sxs-lookup"><span data-stu-id="32b81-112">Parent elements</span></span>

|<span data-ttu-id="32b81-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="32b81-113">**Element**</span></span>|<span data-ttu-id="32b81-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="32b81-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32b81-115">Mailbox</span><span class="sxs-lookup"><span data-stu-id="32b81-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="32b81-116">标识完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="32b81-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="32b81-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="32b81-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="32b81-118">标识会议室的列表。</span><span class="sxs-lookup"><span data-stu-id="32b81-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="32b81-119">文本值</span><span class="sxs-lookup"><span data-stu-id="32b81-119">Text value</span></span>

<span data-ttu-id="32b81-120">如果使用此元素，则需要用于表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="32b81-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="32b81-121">备注</span><span class="sxs-lookup"><span data-stu-id="32b81-121">Remarks</span></span>

<span data-ttu-id="32b81-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="32b81-122">This element is optional.</span></span> <span data-ttu-id="32b81-123">**Name**元素存在于**AttachmentType**、 **EmailAddressType**和**电子邮件地址**类型。</span><span class="sxs-lookup"><span data-stu-id="32b81-123">The **Name** element exists in the **AttachmentType**, **EmailAddressType**, and **EmailAddress** types.</span></span> <span data-ttu-id="32b81-124">**Name**元素中的**电子邮件地址**类型[名称 (EmailAddress)](name-emailaddress.md)元素主题所述。</span><span class="sxs-lookup"><span data-stu-id="32b81-124">The **Name** element in the **EmailAddress** type is described in the [Name (EmailAddress)](name-emailaddress.md) element topic.</span></span> 
  
<span data-ttu-id="32b81-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="32b81-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32b81-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="32b81-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32b81-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="32b81-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="32b81-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="32b81-128">Schema Name</span></span>  <br/> |<span data-ttu-id="32b81-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="32b81-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="32b81-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="32b81-130">Validation File</span></span>  <br/> |<span data-ttu-id="32b81-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="32b81-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="32b81-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="32b81-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="32b81-133">False</span><span class="sxs-lookup"><span data-stu-id="32b81-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32b81-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="32b81-134">See also</span></span>

- [<span data-ttu-id="32b81-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="32b81-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

