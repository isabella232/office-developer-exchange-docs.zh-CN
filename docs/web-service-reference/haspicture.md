---
title: HasPicture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HasPicture
api_type:
- schema
ms.assetid: 922a43fe-01bd-49f2-9261-e00e4699b8da
description: HasPicture 元素指示联系人项目是否具有表示联系人图片的文件附件。
ms.openlocfilehash: 0f0758e38807587d47b9469f40b10bd9c6ea5012
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462435"
---
# <a name="haspicture"></a><span data-ttu-id="a4ed0-103">HasPicture</span><span class="sxs-lookup"><span data-stu-id="a4ed0-103">HasPicture</span></span>

<span data-ttu-id="a4ed0-104">**HasPicture**元素指示联系人项目是否具有表示联系人图片的文件附件。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-104">The **HasPicture** element indicates whether the contact item has a file attachment that represents the contact's picture.</span></span> 
  
[<span data-ttu-id="a4ed0-105">联系人</span><span class="sxs-lookup"><span data-stu-id="a4ed0-105">Contact</span></span>](contact.md)
  
[<span data-ttu-id="a4ed0-106">HasPicture</span><span class="sxs-lookup"><span data-stu-id="a4ed0-106">HasPicture</span></span>](haspicture.md)
  
```xml
<HasPicture>true or false</HasPicture>
```

 <span data-ttu-id="a4ed0-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="a4ed0-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4ed0-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a4ed0-108">Attributes and elements</span></span>

<span data-ttu-id="a4ed0-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4ed0-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="a4ed0-110">Attributes</span></span>

<span data-ttu-id="a4ed0-111">无。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4ed0-112">子元素</span><span class="sxs-lookup"><span data-stu-id="a4ed0-112">Child elements</span></span>

<span data-ttu-id="a4ed0-113">无。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a4ed0-114">父元素</span><span class="sxs-lookup"><span data-stu-id="a4ed0-114">Parent elements</span></span>

|<span data-ttu-id="a4ed0-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="a4ed0-115">**Element**</span></span>|<span data-ttu-id="a4ed0-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="a4ed0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4ed0-117">联系人</span><span class="sxs-lookup"><span data-stu-id="a4ed0-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="a4ed0-118">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a4ed0-119">文本值</span><span class="sxs-lookup"><span data-stu-id="a4ed0-119">Text value</span></span>

<span data-ttu-id="a4ed0-120">**HasPicture**元素的文本值可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-120">The text value of the **HasPicture** element can be either **true** or **false**.</span></span> <span data-ttu-id="a4ed0-121">默认值为 **false**。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4ed0-122">说明</span><span class="sxs-lookup"><span data-stu-id="a4ed0-122">Remarks</span></span>

<span data-ttu-id="a4ed0-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a4ed0-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4ed0-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="a4ed0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4ed0-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="a4ed0-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a4ed0-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="a4ed0-126">Schema Name</span></span>  <br/> |<span data-ttu-id="a4ed0-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="a4ed0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="a4ed0-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="a4ed0-128">Validation File</span></span>  <br/> |<span data-ttu-id="a4ed0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a4ed0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a4ed0-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="a4ed0-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4ed0-131">False</span><span class="sxs-lookup"><span data-stu-id="a4ed0-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4ed0-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a4ed0-132">See also</span></span>



- [<span data-ttu-id="a4ed0-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a4ed0-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

