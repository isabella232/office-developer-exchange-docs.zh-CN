---
title: Emailuser.displayname
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dc8133ff-c34e-4921-bb56-06e79aee0a8a
description: Emailuser.displayname 元素指定电子邮件收件人。
ms.openlocfilehash: c090106a536f4f40908d364cc3c9c43f6fe42beb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456533"
---
# <a name="emailuser"></a><span data-ttu-id="fb729-103">Emailuser.displayname</span><span class="sxs-lookup"><span data-stu-id="fb729-103">EmailUser</span></span>

<span data-ttu-id="fb729-104">**Emailuser.displayname**元素指定电子邮件收件人。</span><span class="sxs-lookup"><span data-stu-id="fb729-104">The **EmailUser** element specifies an email recipient.</span></span> 
  
```XML
<EmailUser>
    <Name/>
    <UserId/>
</EmailUser>
```

 <span data-ttu-id="fb729-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="fb729-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fb729-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fb729-106">Attributes and elements</span></span>

<span data-ttu-id="fb729-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fb729-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fb729-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fb729-108">Attributes</span></span>

<span data-ttu-id="fb729-109">无。</span><span class="sxs-lookup"><span data-stu-id="fb729-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fb729-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fb729-110">Child elements</span></span>

|<span data-ttu-id="fb729-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb729-111">**Element**</span></span>|<span data-ttu-id="fb729-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb729-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb729-113">名称（字符串）</span><span class="sxs-lookup"><span data-stu-id="fb729-113">Name (string)</span></span>](name-string.md) <br/> |<span data-ttu-id="fb729-114">指定一个搜索精简程序名称或密钥或电子邮件用户的名称。</span><span class="sxs-lookup"><span data-stu-id="fb729-114">Specifies a search refiner name or key or the name of an email user.</span></span>  <br/> |
|[<span data-ttu-id="fb729-115">UserId （string）</span><span class="sxs-lookup"><span data-stu-id="fb729-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="fb729-116">指定电子邮件用户的用户标识符。</span><span class="sxs-lookup"><span data-stu-id="fb729-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fb729-117">父元素</span><span class="sxs-lookup"><span data-stu-id="fb729-117">Parent elements</span></span>

|<span data-ttu-id="fb729-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="fb729-118">**Element**</span></span>|<span data-ttu-id="fb729-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="fb729-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fb729-120">者</span><span class="sxs-lookup"><span data-stu-id="fb729-120">Attendees</span></span>](attendees.md) <br/> |<span data-ttu-id="fb729-121">指定会议邀请的收件人。</span><span class="sxs-lookup"><span data-stu-id="fb729-121">Specifies the recipients of an invitation to a meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb729-122">备注</span><span class="sxs-lookup"><span data-stu-id="fb729-122">Remarks</span></span>

<span data-ttu-id="fb729-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fb729-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fb729-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fb729-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fb729-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="fb729-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fb729-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="fb729-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fb729-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="fb729-127">Schema Name</span></span>  <br/> |<span data-ttu-id="fb729-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="fb729-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="fb729-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="fb729-129">Validation File</span></span>  <br/> |<span data-ttu-id="fb729-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="fb729-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fb729-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="fb729-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fb729-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fb729-132">See also</span></span>



- [<span data-ttu-id="fb729-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fb729-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

