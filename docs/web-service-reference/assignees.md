---
title: 代理人
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: "\"代理人\" 元素指定向其分配任务的人员。"
ms.openlocfilehash: 3e98273e859dbe2128b0ad3b4df42c8016fd3bc5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464712"
---
# <a name="assignees"></a><span data-ttu-id="fa80e-103">代理人</span><span class="sxs-lookup"><span data-stu-id="fa80e-103">Assignees</span></span>

<span data-ttu-id="fa80e-104">"**代理人**" 元素指定向其分配任务的人员。</span><span class="sxs-lookup"><span data-stu-id="fa80e-104">The **Assignees** element specifies the people to whom a task is assigned.</span></span> 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 <span data-ttu-id="fa80e-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="fa80e-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fa80e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fa80e-106">Attributes and elements</span></span>

<span data-ttu-id="fa80e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fa80e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fa80e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fa80e-108">Attributes</span></span>

<span data-ttu-id="fa80e-109">无。</span><span class="sxs-lookup"><span data-stu-id="fa80e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa80e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fa80e-110">Child elements</span></span>

|<span data-ttu-id="fa80e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa80e-111">**Element**</span></span>|<span data-ttu-id="fa80e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa80e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa80e-113">名称（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="fa80e-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="fa80e-114">表示邮箱用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="fa80e-114">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="fa80e-115">UserId （string）</span><span class="sxs-lookup"><span data-stu-id="fa80e-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="fa80e-116">指定电子邮件用户的用户标识符。</span><span class="sxs-lookup"><span data-stu-id="fa80e-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fa80e-117">父元素</span><span class="sxs-lookup"><span data-stu-id="fa80e-117">Parent elements</span></span>

|<span data-ttu-id="fa80e-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="fa80e-118">**Element**</span></span>|<span data-ttu-id="fa80e-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="fa80e-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fa80e-120">TaskSuggestion</span><span class="sxs-lookup"><span data-stu-id="fa80e-120">TaskSuggestion</span></span>](tasksuggestion.md) <br/> |<span data-ttu-id="fa80e-121">指定建议的任务。</span><span class="sxs-lookup"><span data-stu-id="fa80e-121">Specifies a proposed task.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa80e-122">备注</span><span class="sxs-lookup"><span data-stu-id="fa80e-122">Remarks</span></span>

<span data-ttu-id="fa80e-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fa80e-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fa80e-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fa80e-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fa80e-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="fa80e-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa80e-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="fa80e-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fa80e-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="fa80e-127">Schema Name</span></span>  <br/> |<span data-ttu-id="fa80e-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="fa80e-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="fa80e-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="fa80e-129">Validation File</span></span>  <br/> |<span data-ttu-id="fa80e-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="fa80e-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="fa80e-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="fa80e-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="fa80e-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fa80e-132">See also</span></span>

- [<span data-ttu-id="fa80e-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fa80e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

