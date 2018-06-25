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
description: HasPicture 元素指示联系人项目是否有代表联系人的图片的文件附件。
ms.openlocfilehash: 8f6890ec2bcc9a961f69331fb20f5cad8a59bf38
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825806"
---
# <a name="haspicture"></a><span data-ttu-id="d8c2d-103">HasPicture</span><span class="sxs-lookup"><span data-stu-id="d8c2d-103">HasPicture</span></span>

<span data-ttu-id="d8c2d-104">**HasPicture**元素指示联系人项目是否有代表联系人的图片的文件附件。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-104">The **HasPicture** element indicates whether the contact item has a file attachment that represents the contact's picture.</span></span> 
  
[<span data-ttu-id="d8c2d-105">Contact</span><span class="sxs-lookup"><span data-stu-id="d8c2d-105">Contact</span></span>](contact.md)
  
[<span data-ttu-id="d8c2d-106">HasPicture</span><span class="sxs-lookup"><span data-stu-id="d8c2d-106">HasPicture</span></span>](haspicture.md)
  
```xml
<HasPicture>true or false</HasPicture>
```

 <span data-ttu-id="d8c2d-107">**boolean**</span><span class="sxs-lookup"><span data-stu-id="d8c2d-107">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d8c2d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d8c2d-108">Attributes and elements</span></span>

<span data-ttu-id="d8c2d-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d8c2d-110">属性</span><span class="sxs-lookup"><span data-stu-id="d8c2d-110">Attributes</span></span>

<span data-ttu-id="d8c2d-111">无。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d8c2d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d8c2d-112">Child elements</span></span>

<span data-ttu-id="d8c2d-113">无。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d8c2d-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d8c2d-114">Parent elements</span></span>

|<span data-ttu-id="d8c2d-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="d8c2d-115">**Element**</span></span>|<span data-ttu-id="d8c2d-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="d8c2d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d8c2d-117">联系人</span><span class="sxs-lookup"><span data-stu-id="d8c2d-117">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="d8c2d-118">表示对 Exchange 存储中的联系人项目。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-118">Represents a contact item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d8c2d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="d8c2d-119">Text value</span></span>

<span data-ttu-id="d8c2d-120">**HasPicture**元素的文本值可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-120">The text value of the **HasPicture** element can be either **true** or **false**.</span></span> <span data-ttu-id="d8c2d-121">默认值为 **false** 。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-121">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8c2d-122">备注</span><span class="sxs-lookup"><span data-stu-id="d8c2d-122">Remarks</span></span>

<span data-ttu-id="d8c2d-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d8c2d-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d8c2d-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="d8c2d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8c2d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="d8c2d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d8c2d-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="d8c2d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="d8c2d-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="d8c2d-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="d8c2d-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="d8c2d-128">Validation File</span></span>  <br/> |<span data-ttu-id="d8c2d-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d8c2d-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d8c2d-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="d8c2d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="d8c2d-131">False</span><span class="sxs-lookup"><span data-stu-id="d8c2d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d8c2d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d8c2d-132">See also</span></span>



- [<span data-ttu-id="d8c2d-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d8c2d-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

