---
title: 与会者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 837bb372-39eb-48ae-9c09-0d2552511f93
description: 与会者元素指定收件人的会议的邀请。
ms.openlocfilehash: 22d88bb092b416c553144496e133680b53f5d30e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753287"
---
# <a name="attendees"></a><span data-ttu-id="51de8-103">与会者</span><span class="sxs-lookup"><span data-stu-id="51de8-103">Attendees</span></span>

<span data-ttu-id="51de8-104">**与会者**元素指定收件人的会议的邀请。</span><span class="sxs-lookup"><span data-stu-id="51de8-104">The **Attendees** element specifies the recipients of an invitation to a meeting.</span></span> 
  
```XML
<Attendees>
    <EmailUser></EmailUser>
</Attendees>
```

 <span data-ttu-id="51de8-105">**ArrayOfEmailUsersType**</span><span class="sxs-lookup"><span data-stu-id="51de8-105">**ArrayOfEmailUsersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="51de8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="51de8-106">Attributes and elements</span></span>

<span data-ttu-id="51de8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="51de8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51de8-108">属性</span><span class="sxs-lookup"><span data-stu-id="51de8-108">Attributes</span></span>

<span data-ttu-id="51de8-109">无。</span><span class="sxs-lookup"><span data-stu-id="51de8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="51de8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="51de8-110">Child elements</span></span>

|<span data-ttu-id="51de8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="51de8-111">**Element**</span></span>|<span data-ttu-id="51de8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="51de8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51de8-113">EmailUser</span><span class="sxs-lookup"><span data-stu-id="51de8-113">EmailUser</span></span>](emailuser.md) <br/> |<span data-ttu-id="51de8-114">指定电子邮件收件人或 Active Directory 联系人。</span><span class="sxs-lookup"><span data-stu-id="51de8-114">Specifies an email recipient or Active Directory contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="51de8-115">父元素</span><span class="sxs-lookup"><span data-stu-id="51de8-115">Parent elements</span></span>

|<span data-ttu-id="51de8-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="51de8-116">**Element**</span></span>|<span data-ttu-id="51de8-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="51de8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="51de8-118">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="51de8-118">MeetingSuggestion</span></span>](meetingsuggestion.md) <br/> |<span data-ttu-id="51de8-119">指定建议的会议。</span><span class="sxs-lookup"><span data-stu-id="51de8-119">Specifies a proposed meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51de8-120">备注</span><span class="sxs-lookup"><span data-stu-id="51de8-120">Remarks</span></span>

<span data-ttu-id="51de8-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="51de8-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="51de8-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="51de8-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="51de8-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="51de8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51de8-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="51de8-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="51de8-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="51de8-125">Schema Name</span></span>  <br/> |<span data-ttu-id="51de8-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="51de8-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="51de8-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="51de8-127">Validation File</span></span>  <br/> |<span data-ttu-id="51de8-128">types.xsd</span><span class="sxs-lookup"><span data-stu-id="51de8-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="51de8-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="51de8-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="51de8-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="51de8-130">See also</span></span>

- [<span data-ttu-id="51de8-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="51de8-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

