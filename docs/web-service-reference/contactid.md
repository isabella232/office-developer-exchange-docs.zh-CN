---
title: ContactId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86f66275-1e39-48ed-bd89-ac3bffc465a7
description: ContactId 元素唯一标识一个联系人。
ms.openlocfilehash: 17e8012283078d5d6e2cd1d2e88eef37b008be42
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463179"
---
# <a name="contactid"></a><span data-ttu-id="3e165-103">ContactId</span><span class="sxs-lookup"><span data-stu-id="3e165-103">ContactId</span></span>

<span data-ttu-id="3e165-104">**ContactId**元素唯一标识一个联系人。</span><span class="sxs-lookup"><span data-stu-id="3e165-104">The **ContactId** element uniquely identifies a contact.</span></span> 
  
```XML
<ContactId Id="" ChangeKey=""/>
```

 <span data-ttu-id="3e165-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="3e165-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e165-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3e165-106">Attributes and elements</span></span>

<span data-ttu-id="3e165-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3e165-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e165-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3e165-108">Attributes</span></span>

|<span data-ttu-id="3e165-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="3e165-109">**Attribute**</span></span>|<span data-ttu-id="3e165-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="3e165-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3e165-111">Id</span><span class="sxs-lookup"><span data-stu-id="3e165-111">Id</span></span>  <br/> |<span data-ttu-id="3e165-112">**Id**属性的文本值是联系人项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="3e165-112">The text value of the **Id** attribute is the identifier of the contact item.</span></span>  <br/> |
|<span data-ttu-id="3e165-113">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="3e165-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="3e165-114">**ChangeKey**属性的文本值是联系人项目的更改键。</span><span class="sxs-lookup"><span data-stu-id="3e165-114">The text value of the **ChangeKey** attribute is the change key of the contact item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3e165-115">子元素</span><span class="sxs-lookup"><span data-stu-id="3e165-115">Child elements</span></span>

<span data-ttu-id="3e165-116">无。</span><span class="sxs-lookup"><span data-stu-id="3e165-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e165-117">父元素</span><span class="sxs-lookup"><span data-stu-id="3e165-117">Parent elements</span></span>

<span data-ttu-id="3e165-118">[AddImContactToGroup](addimcontacttogroup.md)  | [RemoveContactFromImList](removecontactfromimlist.md)  | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span><span class="sxs-lookup"><span data-stu-id="3e165-118">[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3e165-119">备注</span><span class="sxs-lookup"><span data-stu-id="3e165-119">Remarks</span></span>

<span data-ttu-id="3e165-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3e165-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3e165-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3e165-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e165-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="3e165-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e165-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="3e165-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e165-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="3e165-124">Schema name</span></span>  <br/> |<span data-ttu-id="3e165-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="3e165-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="3e165-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="3e165-126">Validation file</span></span>  <br/> |<span data-ttu-id="3e165-127">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="3e165-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e165-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="3e165-128">Can be empty</span></span>  <br/> |<span data-ttu-id="3e165-129">false</span><span class="sxs-lookup"><span data-stu-id="3e165-129">false</span></span>  <br/> |
   

