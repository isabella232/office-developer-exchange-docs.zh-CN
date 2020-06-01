---
title: Member
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Member
api_type:
- schema
ms.assetid: af9c5ff8-02a4-41fc-876d-14ac05f1ee77
description: Member 元素表示通讯组列表成员。
ms.openlocfilehash: e84223b7c41846ca2f174293bff46a8825777a0e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457303"
---
# <a name="member"></a><span data-ttu-id="11104-103">成员</span><span class="sxs-lookup"><span data-stu-id="11104-103">Member</span></span>

<span data-ttu-id="11104-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Member** 元素表示通讯组列表成员。</span><span class="sxs-lookup"><span data-stu-id="11104-104">The **Member** element represents a member of a distribution list.</span></span> 
  
```xml
<Member Key="">
   <Mailbox/>
   <Status/>
</Member>
```

<span data-ttu-id="11104-105">**MemberType**</span><span class="sxs-lookup"><span data-stu-id="11104-105">**MemberType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="11104-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="11104-106">Attributes and elements</span></span>

<span data-ttu-id="11104-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="11104-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="11104-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="11104-108">Attributes</span></span>

|<span data-ttu-id="11104-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="11104-109">**Attribute**</span></span>|<span data-ttu-id="11104-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="11104-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11104-111">键</span><span class="sxs-lookup"><span data-stu-id="11104-111">Key</span></span>  <br/> |<span data-ttu-id="11104-p101">为通讯组列表成员提供的唯一标识符。此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="11104-p101">Provides a unique identifier for the distribution list member. This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="11104-114">子元素</span><span class="sxs-lookup"><span data-stu-id="11104-114">Child elements</span></span>

|<span data-ttu-id="11104-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="11104-115">**Element**</span></span>|<span data-ttu-id="11104-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="11104-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11104-117">Mailbox</span><span class="sxs-lookup"><span data-stu-id="11104-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="11104-p102">代表通讯组列表成员的电子邮件地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="11104-p102">Represents the e-mail address of the distribution list member. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="11104-120">状态 (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="11104-120">Status (MemberStatusType)</span></span>](status-memberstatustype.md) <br/> |<span data-ttu-id="11104-p103">提供有关通讯组列表成员状态的信息。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="11104-p103">Provides information about the status of a distribution list member. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="11104-123">父元素</span><span class="sxs-lookup"><span data-stu-id="11104-123">Parent elements</span></span>

|<span data-ttu-id="11104-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="11104-124">**Element**</span></span>|<span data-ttu-id="11104-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="11104-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="11104-126">成员 (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="11104-126">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="11104-127">包含通讯组列表成员的列表。</span><span class="sxs-lookup"><span data-stu-id="11104-127">Contains a list of distribution list members.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11104-128">说明</span><span class="sxs-lookup"><span data-stu-id="11104-128">Remarks</span></span>

<span data-ttu-id="11104-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="11104-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="11104-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="11104-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="11104-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="11104-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="11104-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="11104-132">Schema Name</span></span>  <br/> |<span data-ttu-id="11104-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="11104-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="11104-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="11104-134">Validation File</span></span>  <br/> |<span data-ttu-id="11104-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="11104-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="11104-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="11104-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="11104-137">False</span><span class="sxs-lookup"><span data-stu-id="11104-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11104-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="11104-138">See also</span></span>

- [<span data-ttu-id="11104-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="11104-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

