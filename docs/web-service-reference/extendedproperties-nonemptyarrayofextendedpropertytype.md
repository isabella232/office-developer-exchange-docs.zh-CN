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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754238"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a><span data-ttu-id="b90d8-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="b90d8-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span></span>

<span data-ttu-id="b90d8-104">**ExtendedProperties**元素指定其他属性的数组。</span><span class="sxs-lookup"><span data-stu-id="b90d8-104">The **ExtendedProperties** element specifies an array of additional properties.</span></span> 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 <span data-ttu-id="b90d8-105">**NonEmptyArrayOfExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="b90d8-105">**NonEmptyArrayOfExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b90d8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b90d8-106">Attributes and elements</span></span>

<span data-ttu-id="b90d8-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b90d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b90d8-108">属性</span><span class="sxs-lookup"><span data-stu-id="b90d8-108">Attributes</span></span>

<span data-ttu-id="b90d8-109">无。</span><span class="sxs-lookup"><span data-stu-id="b90d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b90d8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b90d8-110">Child elements</span></span>

|<span data-ttu-id="b90d8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b90d8-111">**Element**</span></span>|<span data-ttu-id="b90d8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b90d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b90d8-113">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="b90d8-113">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="b90d8-114">标识文件夹和项扩展的 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="b90d8-114">Identifies extended MAPI properties on folders and items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b90d8-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b90d8-115">Parent elements</span></span>

|<span data-ttu-id="b90d8-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b90d8-116">**Element**</span></span>|<span data-ttu-id="b90d8-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b90d8-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b90d8-118">ImGroup</span><span class="sxs-lookup"><span data-stu-id="b90d8-118">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="b90d8-119">代表一个即时消息的组。</span><span class="sxs-lookup"><span data-stu-id="b90d8-119">Represents an instant messaging group.</span></span>  <br/> |
|[<span data-ttu-id="b90d8-120">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="b90d8-120">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="b90d8-121">指定预览邮箱项目的前 256 个字符，而无需打开项目。</span><span class="sxs-lookup"><span data-stu-id="b90d8-121">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b90d8-122">备注</span><span class="sxs-lookup"><span data-stu-id="b90d8-122">Remarks</span></span>

<span data-ttu-id="b90d8-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b90d8-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b90d8-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b90d8-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b90d8-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="b90d8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b90d8-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="b90d8-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b90d8-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="b90d8-127">Schema Name</span></span>  <br/> |<span data-ttu-id="b90d8-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="b90d8-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="b90d8-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="b90d8-129">Validation File</span></span>  <br/> |<span data-ttu-id="b90d8-130">types.xsd</span><span class="sxs-lookup"><span data-stu-id="b90d8-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="b90d8-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="b90d8-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="b90d8-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b90d8-132">See also</span></span>



- [<span data-ttu-id="b90d8-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b90d8-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

