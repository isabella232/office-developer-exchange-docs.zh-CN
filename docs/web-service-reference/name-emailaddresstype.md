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
description: Name 元素表示邮箱用户的名称。
ms.openlocfilehash: db6eb547b5c848dc31bbaa377692989b16771673
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466925"
---
# <a name="name-emailaddresstype"></a><span data-ttu-id="955f8-103">名称 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="955f8-103">Name (EmailAddressType)</span></span>

<span data-ttu-id="955f8-104">**Name**元素表示邮箱用户的名称。</span><span class="sxs-lookup"><span data-stu-id="955f8-104">The **Name** element represents the name of a mailbox user.</span></span> 
  
```xml
<Name/>
```

<span data-ttu-id="955f8-105">**string**</span><span class="sxs-lookup"><span data-stu-id="955f8-105">**string**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="955f8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="955f8-106">Attributes and elements</span></span>

<span data-ttu-id="955f8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="955f8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="955f8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="955f8-108">Attributes</span></span>

<span data-ttu-id="955f8-109">无。</span><span class="sxs-lookup"><span data-stu-id="955f8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="955f8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="955f8-110">Child elements</span></span>

<span data-ttu-id="955f8-111">无。</span><span class="sxs-lookup"><span data-stu-id="955f8-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="955f8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="955f8-112">Parent elements</span></span>

|<span data-ttu-id="955f8-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="955f8-113">**Element**</span></span>|<span data-ttu-id="955f8-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="955f8-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="955f8-115">Mailbox</span><span class="sxs-lookup"><span data-stu-id="955f8-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="955f8-116">标识完全解析的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="955f8-116">Identifies a fully resolved e-mail address.</span></span>  <br/> |
|[<span data-ttu-id="955f8-117">RoomList</span><span class="sxs-lookup"><span data-stu-id="955f8-117">RoomList</span></span>](roomlist.md) <br/> |<span data-ttu-id="955f8-118">标识会议室列表。</span><span class="sxs-lookup"><span data-stu-id="955f8-118">Identifies a list of meeting rooms.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="955f8-119">文本值</span><span class="sxs-lookup"><span data-stu-id="955f8-119">Text value</span></span>

<span data-ttu-id="955f8-120">如果使用此元素，则需要一个表示字符串的文本值。</span><span class="sxs-lookup"><span data-stu-id="955f8-120">A text value that represents a string is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="955f8-121">说明</span><span class="sxs-lookup"><span data-stu-id="955f8-121">Remarks</span></span>

<span data-ttu-id="955f8-122">此元素为可选。</span><span class="sxs-lookup"><span data-stu-id="955f8-122">This element is optional.</span></span> <span data-ttu-id="955f8-123">**Name**元素存在于**AttachmentType**、 **EmailAddressType**和**EmailAddress**类型中。</span><span class="sxs-lookup"><span data-stu-id="955f8-123">The **Name** element exists in the **AttachmentType**, **EmailAddressType**, and **EmailAddress** types.</span></span> <span data-ttu-id="955f8-124">"[名称" （EmailAddress）](name-emailaddress.md)元素主题中介绍了**EmailAddress**类型中的**name**元素。</span><span class="sxs-lookup"><span data-stu-id="955f8-124">The **Name** element in the **EmailAddress** type is described in the [Name (EmailAddress)](name-emailaddress.md) element topic.</span></span> 
  
<span data-ttu-id="955f8-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="955f8-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="955f8-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="955f8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="955f8-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="955f8-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="955f8-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="955f8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="955f8-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="955f8-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="955f8-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="955f8-130">Validation File</span></span>  <br/> |<span data-ttu-id="955f8-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="955f8-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="955f8-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="955f8-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="955f8-133">False</span><span class="sxs-lookup"><span data-stu-id="955f8-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="955f8-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="955f8-134">See also</span></span>

- [<span data-ttu-id="955f8-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="955f8-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

