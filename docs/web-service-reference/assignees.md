---
title: Assignees
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20ef18c2-daa0-4f65-a515-e84e9993a77f
description: Assignees 元素指定为其分配任务的人员。
ms.openlocfilehash: 5fc301cd77268213e95fd33a2a2f36dbe218b512
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753269"
---
# <a name="assignees"></a><span data-ttu-id="acce4-103">Assignees</span><span class="sxs-lookup"><span data-stu-id="acce4-103">Assignees</span></span>

<span data-ttu-id="acce4-104">**Assignees**元素指定为其分配任务的人员。</span><span class="sxs-lookup"><span data-stu-id="acce4-104">The **Assignees** element specifies the people to whom a task is assigned.</span></span> 
  
```XML
<Assignees>
    <Name></Name>
    <UserID></UserID>
</Assignees>
```

 <span data-ttu-id="acce4-105">**EmailUserType**</span><span class="sxs-lookup"><span data-stu-id="acce4-105">**EmailUserType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="acce4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="acce4-106">Attributes and elements</span></span>

<span data-ttu-id="acce4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="acce4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="acce4-108">属性</span><span class="sxs-lookup"><span data-stu-id="acce4-108">Attributes</span></span>

<span data-ttu-id="acce4-109">无。</span><span class="sxs-lookup"><span data-stu-id="acce4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="acce4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="acce4-110">Child elements</span></span>

|<span data-ttu-id="acce4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="acce4-111">**Element**</span></span>|<span data-ttu-id="acce4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="acce4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acce4-113">名称 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="acce4-113">Name (EmailAddress)</span></span>](name-emailaddress.md) <br/> |<span data-ttu-id="acce4-114">代表邮箱用户的显示名称。</span><span class="sxs-lookup"><span data-stu-id="acce4-114">Represents the display name of the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="acce4-115">UserId （字符串）</span><span class="sxs-lookup"><span data-stu-id="acce4-115">UserId (string)</span></span>](userid-string.md) <br/> |<span data-ttu-id="acce4-116">指定电子邮件用户的用户的标识符。</span><span class="sxs-lookup"><span data-stu-id="acce4-116">Specifies the user identifier of an email user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="acce4-117">父元素</span><span class="sxs-lookup"><span data-stu-id="acce4-117">Parent elements</span></span>

|<span data-ttu-id="acce4-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="acce4-118">**Element**</span></span>|<span data-ttu-id="acce4-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="acce4-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="acce4-120">TaskSuggestion</span><span class="sxs-lookup"><span data-stu-id="acce4-120">TaskSuggestion</span></span>](tasksuggestion.md) <br/> |<span data-ttu-id="acce4-121">指定建议的任务。</span><span class="sxs-lookup"><span data-stu-id="acce4-121">Specifies a proposed task.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="acce4-122">备注</span><span class="sxs-lookup"><span data-stu-id="acce4-122">Remarks</span></span>

<span data-ttu-id="acce4-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="acce4-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="acce4-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="acce4-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="acce4-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="acce4-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="acce4-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="acce4-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="acce4-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="acce4-127">Schema Name</span></span>  <br/> |<span data-ttu-id="acce4-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="acce4-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="acce4-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="acce4-129">Validation File</span></span>  <br/> |<span data-ttu-id="acce4-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="acce4-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="acce4-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="acce4-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="acce4-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="acce4-132">See also</span></span>

- [<span data-ttu-id="acce4-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="acce4-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

