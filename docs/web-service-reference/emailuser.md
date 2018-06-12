---
title: EmailUser
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc8133ff-c34e-4921-bb56-06e79aee0a8a
description: EmailUser 元素指定电子邮件收件人。
ms.openlocfilehash: e724b3996d37a42527ec1183cef9bb6b312b8c93
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754092"
---
# <a name="emailuser"></a><span data-ttu-id="6f9bd-103">EmailUser</span><span class="sxs-lookup"><span data-stu-id="6f9bd-103">EmailUser</span></span>

<span data-ttu-id="6f9bd-104">**EmailUser**元素指定电子邮件收件人。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-104">The **EmailUser** element specifies an email recipient.</span></span> 
  
```XML
<EmailUser>
    <Name/>
    <UserId/>
</EmailUser>
```

 <span data-ttu-id="6f9bd-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="6f9bd-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f9bd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f9bd-106">Attributes and elements</span></span>

<span data-ttu-id="6f9bd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f9bd-108">属性</span><span class="sxs-lookup"><span data-stu-id="6f9bd-108">Attributes</span></span>

<span data-ttu-id="6f9bd-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f9bd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f9bd-110">Child elements</span></span>

|<span data-ttu-id="6f9bd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f9bd-111">**Element**</span></span>|<span data-ttu-id="6f9bd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f9bd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f9bd-113">名称 （字符串）</span><span class="sxs-lookup"><span data-stu-id="6f9bd-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="6f9bd-114">指定搜索精简条件名称或键或电子邮件用户的名称。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="6f9bd-115">UserId （字符串）</span><span class="sxs-lookup"><span data-stu-id="6f9bd-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="6f9bd-116">指定电子邮件用户的用户的标识符。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6f9bd-117">父元素</span><span class="sxs-lookup"><span data-stu-id="6f9bd-117">Parent elements</span></span>

|<span data-ttu-id="6f9bd-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f9bd-118">**Element**</span></span>|<span data-ttu-id="6f9bd-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f9bd-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f9bd-120">与会者</span><span class="sxs-lookup"><span data-stu-id="6f9bd-120">Attendees</span></span>](attendees.md) <br/> |<span data-ttu-id="6f9bd-121">指定收件人的会议的邀请。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-121">Specifies the recipients of an invitation to a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f9bd-122">备注</span><span class="sxs-lookup"><span data-stu-id="6f9bd-122">Remarks</span></span>

<span data-ttu-id="6f9bd-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6f9bd-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f9bd-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f9bd-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f9bd-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f9bd-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f9bd-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f9bd-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f9bd-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6f9bd-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="6f9bd-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="6f9bd-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f9bd-129">Validation File</span></span>  <br/> |<span data-ttu-id="6f9bd-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f9bd-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f9bd-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f9bd-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="6f9bd-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f9bd-132">See also</span></span>



- [<span data-ttu-id="6f9bd-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f9bd-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

