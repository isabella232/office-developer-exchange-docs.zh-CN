---
title: ContactId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86f66275-1e39-48ed-bd89-ac3bffc465a7
description: ContactId 元素唯一地标识联系人。
ms.openlocfilehash: 4fd3693ed89194c85e5f1770f1db3903d835f43e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753508"
---
# <a name="contactid"></a><span data-ttu-id="9c688-103">ContactId</span><span class="sxs-lookup"><span data-stu-id="9c688-103">ContactId</span></span>

<span data-ttu-id="9c688-104">**ContactId**元素唯一地标识联系人。</span><span class="sxs-lookup"><span data-stu-id="9c688-104">The **ContactId** element uniquely identifies a contact.</span></span> 
  
```XML
<ContactId Id="" ChangeKey=""/>
```

 <span data-ttu-id="9c688-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="9c688-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9c688-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9c688-106">Attributes and elements</span></span>

<span data-ttu-id="9c688-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9c688-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c688-108">属性</span><span class="sxs-lookup"><span data-stu-id="9c688-108">Attributes</span></span>

|<span data-ttu-id="9c688-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="9c688-109">**Attribute**</span></span>|<span data-ttu-id="9c688-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c688-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c688-111">Id</span><span class="sxs-lookup"><span data-stu-id="9c688-111">Id</span></span>  <br/> |<span data-ttu-id="9c688-112">**Id**属性的文本值是联系人项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="9c688-112">The text value of the **Id** attribute is the identifier of the contact item.</span></span>  <br/> |
|<span data-ttu-id="9c688-113">更改密钥</span><span class="sxs-lookup"><span data-stu-id="9c688-113">ChangeKey</span></span>  <br/> |<span data-ttu-id="9c688-114">**更改密钥**属性的文本值为联系人项目的更改键。</span><span class="sxs-lookup"><span data-stu-id="9c688-114">The text value of the **ChangeKey** attribute is the change key of the contact item.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9c688-115">子元素</span><span class="sxs-lookup"><span data-stu-id="9c688-115">Child elements</span></span>

<span data-ttu-id="9c688-116">无。</span><span class="sxs-lookup"><span data-stu-id="9c688-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9c688-117">父元素</span><span class="sxs-lookup"><span data-stu-id="9c688-117">Parent elements</span></span>

<span data-ttu-id="9c688-118">[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span><span class="sxs-lookup"><span data-stu-id="9c688-118">[AddImContactToGroup](addimcontacttogroup.md) | [RemoveContactFromImList](removecontactfromimlist.md) | [RemoveImContactFromGroup](removeimcontactfromgroup.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9c688-119">备注</span><span class="sxs-lookup"><span data-stu-id="9c688-119">Remarks</span></span>

<span data-ttu-id="9c688-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9c688-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9c688-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9c688-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c688-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="9c688-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c688-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="9c688-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c688-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="9c688-124">Schema name</span></span>  <br/> |<span data-ttu-id="9c688-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="9c688-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="9c688-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="9c688-126">Validation file</span></span>  <br/> |<span data-ttu-id="9c688-127">types.xsd</span><span class="sxs-lookup"><span data-stu-id="9c688-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c688-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="9c688-128">Can be empty</span></span>  <br/> |<span data-ttu-id="9c688-129">false</span><span class="sxs-lookup"><span data-stu-id="9c688-129">false</span></span>  <br/> |
   

