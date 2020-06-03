---
title: 与会者
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 837bb372-39eb-48ae-9c09-0d2552511f93
description: "\"与会者\" 元素指定会议邀请的收件人。"
ms.openlocfilehash: 3a63bdf7e49309697ac503be5f4c95eb805b9635
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460328"
---
# <a name="attendees"></a><span data-ttu-id="a1bde-103">与会者</span><span class="sxs-lookup"><span data-stu-id="a1bde-103">Attendees</span></span>

<span data-ttu-id="a1bde-104">"**与会者**" 元素指定会议邀请的收件人。</span><span class="sxs-lookup"><span data-stu-id="a1bde-104">The **Attendees** element specifies the recipients of an invitation to a meeting.</span></span> 
  
```XML
<Attendees>
    <EmailUser></EmailUser>
</Attendees>
```

 <span data-ttu-id="a1bde-105">**ArrayOfEmailUsersType**</span><span class="sxs-lookup"><span data-stu-id="a1bde-105">**ArrayOfEmailUsersType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a1bde-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a1bde-106">Attributes and elements</span></span>

<span data-ttu-id="a1bde-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a1bde-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1bde-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a1bde-108">Attributes</span></span>

<span data-ttu-id="a1bde-109">无。</span><span class="sxs-lookup"><span data-stu-id="a1bde-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1bde-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a1bde-110">Child elements</span></span>

|<span data-ttu-id="a1bde-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a1bde-111">**Element**</span></span>|<span data-ttu-id="a1bde-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a1bde-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1bde-113">Emailuser.displayname</span><span class="sxs-lookup"><span data-stu-id="a1bde-113">EmailUser</span></span>](emailuser.md) <br/> |<span data-ttu-id="a1bde-114">指定电子邮件收件人或 Active Directory 联系人。</span><span class="sxs-lookup"><span data-stu-id="a1bde-114">Specifies an email recipient or Active Directory contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a1bde-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a1bde-115">Parent elements</span></span>

|<span data-ttu-id="a1bde-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a1bde-116">**Element**</span></span>|<span data-ttu-id="a1bde-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a1bde-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a1bde-118">MeetingSuggestion</span><span class="sxs-lookup"><span data-stu-id="a1bde-118">MeetingSuggestion</span></span>](meetingsuggestion.md) <br/> |<span data-ttu-id="a1bde-119">指定建议的会议。</span><span class="sxs-lookup"><span data-stu-id="a1bde-119">Specifies a proposed meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1bde-120">备注</span><span class="sxs-lookup"><span data-stu-id="a1bde-120">Remarks</span></span>

<span data-ttu-id="a1bde-121">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a1bde-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a1bde-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a1bde-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1bde-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="a1bde-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1bde-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="a1bde-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a1bde-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="a1bde-125">Schema Name</span></span>  <br/> |<span data-ttu-id="a1bde-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="a1bde-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="a1bde-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="a1bde-127">Validation File</span></span>  <br/> |<span data-ttu-id="a1bde-128">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="a1bde-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a1bde-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="a1bde-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a1bde-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a1bde-130">See also</span></span>

- [<span data-ttu-id="a1bde-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a1bde-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

