---
title: ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: ExtendedProperties 元素指定其他属性的数组。
ms.openlocfilehash: b92108ecde63d4a3ac3cc80861c204c4d1950cc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754238"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a><span data-ttu-id="a73b7-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="a73b7-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span></span>

<span data-ttu-id="a73b7-104">**ExtendedProperties**元素指定其他属性的数组。</span><span class="sxs-lookup"><span data-stu-id="a73b7-104">The **ExtendedProperties** element specifies an array of additional properties.</span></span> 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 <span data-ttu-id="a73b7-105">**NonEmptyArrayOfExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="a73b7-105">**NonEmptyArrayOfExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a73b7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a73b7-106">Attributes and elements</span></span>

<span data-ttu-id="a73b7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a73b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a73b7-108">属性</span><span class="sxs-lookup"><span data-stu-id="a73b7-108">Attributes</span></span>

<span data-ttu-id="a73b7-109">无。</span><span class="sxs-lookup"><span data-stu-id="a73b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a73b7-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a73b7-110">Child elements</span></span>

|<span data-ttu-id="a73b7-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a73b7-111">**Element**</span></span>|<span data-ttu-id="a73b7-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a73b7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a73b7-113">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a73b7-113">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="a73b7-114">标识文件夹和项扩展的 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="a73b7-114">Identifies extended MAPI properties on folders and items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a73b7-115">父元素</span><span class="sxs-lookup"><span data-stu-id="a73b7-115">Parent elements</span></span>

|<span data-ttu-id="a73b7-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a73b7-116">**Element**</span></span>|<span data-ttu-id="a73b7-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a73b7-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a73b7-118">ImGroup</span><span class="sxs-lookup"><span data-stu-id="a73b7-118">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="a73b7-119">代表一个即时消息的组。</span><span class="sxs-lookup"><span data-stu-id="a73b7-119">Represents an instant messaging group.</span></span>  <br/> |
|[<span data-ttu-id="a73b7-120">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="a73b7-120">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="a73b7-121">指定预览邮箱项目的前 256 个字符，而无需打开项目。</span><span class="sxs-lookup"><span data-stu-id="a73b7-121">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a73b7-122">备注</span><span class="sxs-lookup"><span data-stu-id="a73b7-122">Remarks</span></span>

<span data-ttu-id="a73b7-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a73b7-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a73b7-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a73b7-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a73b7-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="a73b7-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a73b7-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="a73b7-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a73b7-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="a73b7-127">Schema Name</span></span>  <br/> |<span data-ttu-id="a73b7-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="a73b7-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="a73b7-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="a73b7-129">Validation File</span></span>  <br/> |<span data-ttu-id="a73b7-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="a73b7-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="a73b7-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="a73b7-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="a73b7-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a73b7-132">See also</span></span>



- [<span data-ttu-id="a73b7-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a73b7-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

