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
ms.openlocfilehash: c38e2ed24e78b5199d4d65cce27a00a8e6704037
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2018
ms.locfileid: "19826434"
---
# <a name="member"></a><span data-ttu-id="8c6dd-103">Member</span><span class="sxs-lookup"><span data-stu-id="8c6dd-103">Member</span></span>

<span data-ttu-id="8c6dd-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Member** 元素表示通讯组列表成员。</span><span class="sxs-lookup"><span data-stu-id="8c6dd-104">The **Member** element represents a member of a distribution list.</span></span> 
  
```xml
<Member Key="">
   <Mailbox/>
   <Status/>
</Member>
```

<span data-ttu-id="8c6dd-105">**MemberType**</span><span class="sxs-lookup"><span data-stu-id="8c6dd-105">**MemberType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8c6dd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8c6dd-106">Attributes and elements</span></span>

<span data-ttu-id="8c6dd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8c6dd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8c6dd-108">属性</span><span class="sxs-lookup"><span data-stu-id="8c6dd-108">Attributes</span></span>

|<span data-ttu-id="8c6dd-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8c6dd-109">**Attribute**</span></span>|<span data-ttu-id="8c6dd-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8c6dd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8c6dd-111">项</span><span class="sxs-lookup"><span data-stu-id="8c6dd-111">Key</span></span>  <br/> |<span data-ttu-id="8c6dd-p101">为通讯组列表成员提供的唯一标识符。此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="8c6dd-p101">Provides a unique identifier for the distribution list member. This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8c6dd-114">子元素</span><span class="sxs-lookup"><span data-stu-id="8c6dd-114">Child elements</span></span>

|<span data-ttu-id="8c6dd-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="8c6dd-115">**Element**</span></span>|<span data-ttu-id="8c6dd-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="8c6dd-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c6dd-117">Mailbox</span><span class="sxs-lookup"><span data-stu-id="8c6dd-117">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="8c6dd-p102">代表通讯组列表成员的电子邮件地址。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8c6dd-p102">Represents the e-mail address of the distribution list member. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="8c6dd-120">状态 (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="8c6dd-120">Status (MemberStatusType)</span></span>](status-memberstatustype.md) <br/> |<span data-ttu-id="8c6dd-p103">提供有关通讯组列表成员状态的信息。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="8c6dd-p103">Provides information about the status of a distribution list member. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8c6dd-123">父元素</span><span class="sxs-lookup"><span data-stu-id="8c6dd-123">Parent elements</span></span>

|<span data-ttu-id="8c6dd-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="8c6dd-124">**Element**</span></span>|<span data-ttu-id="8c6dd-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="8c6dd-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8c6dd-126">成员 (MemberListType)</span><span class="sxs-lookup"><span data-stu-id="8c6dd-126">Members (MemberListType)</span></span>](members-memberlisttype.md) <br/> |<span data-ttu-id="8c6dd-127">包含通讯组列表成员的列表。</span><span class="sxs-lookup"><span data-stu-id="8c6dd-127">Contains a list of distribution list members.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c6dd-128">备注</span><span class="sxs-lookup"><span data-stu-id="8c6dd-128">Remarks</span></span>

<span data-ttu-id="8c6dd-129">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8c6dd-129">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8c6dd-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="8c6dd-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c6dd-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="8c6dd-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8c6dd-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="8c6dd-132">Schema Name</span></span>  <br/> |<span data-ttu-id="8c6dd-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="8c6dd-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="8c6dd-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="8c6dd-134">Validation File</span></span>  <br/> |<span data-ttu-id="8c6dd-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8c6dd-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8c6dd-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="8c6dd-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="8c6dd-137">False</span><span class="sxs-lookup"><span data-stu-id="8c6dd-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8c6dd-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8c6dd-138">See also</span></span>

- [<span data-ttu-id="8c6dd-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8c6dd-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

