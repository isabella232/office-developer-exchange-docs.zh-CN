---
title: GroupId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 656d9b9a-8a65-4a75-8466-5b0d96512dab
description: GroupId 元素唯一标识一个组。
ms.openlocfilehash: 3b8de4d0fef95e2caff4db0d90bb303830022d36
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530090"
---
# <a name="groupid"></a><span data-ttu-id="fd520-103">GroupId</span><span class="sxs-lookup"><span data-stu-id="fd520-103">GroupId</span></span>

<span data-ttu-id="fd520-104">**GroupId**元素唯一标识一个组。</span><span class="sxs-lookup"><span data-stu-id="fd520-104">The **GroupId** element uniquely identifies a group.</span></span> 
  
```XML
<GroupId Id="" ChangeKey=""/>
```

 <span data-ttu-id="fd520-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="fd520-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd520-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fd520-106">Attributes and elements</span></span>

<span data-ttu-id="fd520-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fd520-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd520-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fd520-108">Attributes</span></span>

|<span data-ttu-id="fd520-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="fd520-109">**Attribute**</span></span>|<span data-ttu-id="fd520-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="fd520-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fd520-111">Id</span><span class="sxs-lookup"><span data-stu-id="fd520-111">Id</span></span>  <br/> |<span data-ttu-id="fd520-112">**Id**属性的文本值是组的标识符。</span><span class="sxs-lookup"><span data-stu-id="fd520-112">The text value of the **Id** attribute is the identifier of the group.</span></span>  <br/> |
|<span data-ttu-id="fd520-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="fd520-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="fd520-114">**ChangeKey**属性的文本值是组的更改键。</span><span class="sxs-lookup"><span data-stu-id="fd520-114">The text value of the **ChangeKey** attribute is the change key of the group.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fd520-115">子元素</span><span class="sxs-lookup"><span data-stu-id="fd520-115">Child elements</span></span>

<span data-ttu-id="fd520-116">无。</span><span class="sxs-lookup"><span data-stu-id="fd520-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd520-117">父元素</span><span class="sxs-lookup"><span data-stu-id="fd520-117">Parent elements</span></span>

<span data-ttu-id="fd520-118">[AddNewImContactToGroup](addnewimcontacttogroup.md)  | [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md)  | [AddImContactToGroup](addimcontacttogroup.md)  | [RemoveContactFromImList](removecontactfromimlist.md)  | [RemoveImContactFromGroup](removeimcontactfromgroup.md)  | [RemoveImGroup](removeimgroup.md)  | [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)  | [SetImGroup](setimgroup.md)</span><span class="sxs-lookup"><span data-stu-id="fd520-118">[AddNewImContactToGroup](addnewimcontacttogroup.md) | [AddNewTelUriContactToGroup](addnewteluricontacttogroup.md) | [AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md) | [RemoveImGroup](removeimgroup.md) | [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md) | [SetImGroup](setimgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd520-119">备注</span><span class="sxs-lookup"><span data-stu-id="fd520-119">Remarks</span></span>

<span data-ttu-id="fd520-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fd520-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fd520-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fd520-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd520-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="fd520-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd520-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="fd520-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fd520-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="fd520-124">Schema name</span></span>  <br/> |<span data-ttu-id="fd520-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="fd520-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fd520-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="fd520-126">Validation file</span></span>  <br/> |<span data-ttu-id="fd520-127">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="fd520-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fd520-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="fd520-128">Can be empty</span></span>  <br/> ||
   

