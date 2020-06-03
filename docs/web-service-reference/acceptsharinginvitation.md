---
title: AcceptSharingInvitation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AcceptSharingInvitation
api_type:
- schema
ms.assetid: 3c2a47d6-490d-425b-8893-089a4f8882cd
description: AcceptSharingInvitation 元素用于接受允许访问其他用户的 "日历" 或 "联系人" 数据的邀请。
ms.openlocfilehash: c8cdae707bd122e74fa0e284163d1540d857c3de
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461707"
---
# <a name="acceptsharinginvitation"></a><span data-ttu-id="9988e-103">AcceptSharingInvitation</span><span class="sxs-lookup"><span data-stu-id="9988e-103">AcceptSharingInvitation</span></span>

<span data-ttu-id="9988e-104">**AcceptSharingInvitation**元素用于接受允许访问其他用户的 "日历" 或 "联系人" 数据的邀请。</span><span class="sxs-lookup"><span data-stu-id="9988e-104">The **AcceptSharingInvitation** element is used to accept an invitation that allows access to another user's calendar or contacts data.</span></span> 
  
```xml
<AcceptSharingInvitation>
   <ReferenceItemId/>
</AcceptSharingInvitation>
```

 <span data-ttu-id="9988e-105">**AcceptSharingInvitationType**</span><span class="sxs-lookup"><span data-stu-id="9988e-105">**AcceptSharingInvitationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9988e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9988e-106">Attributes and elements</span></span>

<span data-ttu-id="9988e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9988e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9988e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9988e-108">Attributes</span></span>

<span data-ttu-id="9988e-109">无。</span><span class="sxs-lookup"><span data-stu-id="9988e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9988e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9988e-110">Child elements</span></span>

|<span data-ttu-id="9988e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9988e-111">**Element**</span></span>|<span data-ttu-id="9988e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9988e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9988e-113">ReferenceItemId</span><span class="sxs-lookup"><span data-stu-id="9988e-113">ReferenceItemId</span></span>](referenceitemid.md) <br/> |<span data-ttu-id="9988e-114">标识 response 对象引用的项。</span><span class="sxs-lookup"><span data-stu-id="9988e-114">Identifies the item to which the response object refers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9988e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9988e-115">Parent elements</span></span>

|<span data-ttu-id="9988e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="9988e-116">**Element**</span></span>|<span data-ttu-id="9988e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="9988e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9988e-118">ResponseObjects</span><span class="sxs-lookup"><span data-stu-id="9988e-118">ResponseObjects</span></span>](responseobjects.md) <br/> |<span data-ttu-id="9988e-119">包含与 Exchange 存储中的项目关联的所有响应对象的集合。</span><span class="sxs-lookup"><span data-stu-id="9988e-119">Contains a collection of all the response objects that are associated with an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="9988e-120">项目（NonEmptyArrayOfAllItemsType）</span><span class="sxs-lookup"><span data-stu-id="9988e-120">Items (NonEmptyArrayOfAllItemsType)</span></span>](items-nonemptyarrayofallitemstype.md) <br/> |<span data-ttu-id="9988e-121">包含要在由[ParentFolderId （TargetFolderIdType）](parentfolderid-targetfolderidtype.md)元素标识的文件夹中创建的项的数组。</span><span class="sxs-lookup"><span data-stu-id="9988e-121">Contains an array of items to create in the folder that is identified by the [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) element.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9988e-122">说明</span><span class="sxs-lookup"><span data-stu-id="9988e-122">Remarks</span></span>

<span data-ttu-id="9988e-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9988e-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9988e-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="9988e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9988e-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="9988e-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9988e-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="9988e-126">Schema Name</span></span>  <br/> |<span data-ttu-id="9988e-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="9988e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="9988e-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="9988e-128">Validation File</span></span>  <br/> |<span data-ttu-id="9988e-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9988e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9988e-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="9988e-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="9988e-131">False</span><span class="sxs-lookup"><span data-stu-id="9988e-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9988e-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9988e-132">See also</span></span>

- [<span data-ttu-id="9988e-133">CreateItem （AcceptSharingInvitation）</span><span class="sxs-lookup"><span data-stu-id="9988e-133">CreateItem (AcceptSharingInvitation)</span></span>](createitem-acceptsharinginvitation.md)
- [<span data-ttu-id="9988e-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9988e-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

