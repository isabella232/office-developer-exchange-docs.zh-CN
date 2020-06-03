---
title: ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a7034730-210d-4916-b992-dda342f890f8
description: ExtendedProperties 元素指定其他属性数组。
ms.openlocfilehash: 36011e0252ed391daefab190d4da679fb3a3f856
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463095"
---
# <a name="extendedproperties-nonemptyarrayofextendedpropertytype"></a><span data-ttu-id="45780-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span><span class="sxs-lookup"><span data-stu-id="45780-103">ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)</span></span>

<span data-ttu-id="45780-104">**ExtendedProperties**元素指定其他属性数组。</span><span class="sxs-lookup"><span data-stu-id="45780-104">The **ExtendedProperties** element specifies an array of additional properties.</span></span> 
  
```XML
<ExtendedProperties>
    <ExtendedProperty/>
</ExtendedProperties>
```

 <span data-ttu-id="45780-105">**NonEmptyArrayOfExtendedPropertyType**</span><span class="sxs-lookup"><span data-stu-id="45780-105">**NonEmptyArrayOfExtendedPropertyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="45780-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="45780-106">Attributes and elements</span></span>

<span data-ttu-id="45780-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="45780-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="45780-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="45780-108">Attributes</span></span>

<span data-ttu-id="45780-109">无。</span><span class="sxs-lookup"><span data-stu-id="45780-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="45780-110">子元素</span><span class="sxs-lookup"><span data-stu-id="45780-110">Child elements</span></span>

|<span data-ttu-id="45780-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="45780-111">**Element**</span></span>|<span data-ttu-id="45780-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="45780-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45780-113">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="45780-113">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="45780-114">标识文件夹和项目的扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="45780-114">Identifies extended MAPI properties on folders and items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="45780-115">父元素</span><span class="sxs-lookup"><span data-stu-id="45780-115">Parent elements</span></span>

|<span data-ttu-id="45780-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="45780-116">**Element**</span></span>|<span data-ttu-id="45780-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="45780-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="45780-118">ImGroup</span><span class="sxs-lookup"><span data-stu-id="45780-118">ImGroup</span></span>](imgroup.md) <br/> |<span data-ttu-id="45780-119">表示即时消息组。</span><span class="sxs-lookup"><span data-stu-id="45780-119">Represents an instant messaging group.</span></span>  <br/> |
|[<span data-ttu-id="45780-120">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="45780-120">SearchPreviewItem</span></span>](searchpreviewitem.md) <br/> |<span data-ttu-id="45780-121">指定在不打开项目的情况下预览邮箱项目的前256个字符。</span><span class="sxs-lookup"><span data-stu-id="45780-121">Specifies the first 256 characters of a mailbox item for preview without opening the item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45780-122">备注</span><span class="sxs-lookup"><span data-stu-id="45780-122">Remarks</span></span>

<span data-ttu-id="45780-123">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="45780-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="45780-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="45780-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="45780-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="45780-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="45780-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="45780-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="45780-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="45780-127">Schema Name</span></span>  <br/> |<span data-ttu-id="45780-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="45780-128">Type schema</span></span>  <br/> |
|<span data-ttu-id="45780-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="45780-129">Validation File</span></span>  <br/> |<span data-ttu-id="45780-130">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="45780-130">types.xsd</span></span>  <br/> |
|<span data-ttu-id="45780-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="45780-131">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="45780-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="45780-132">See also</span></span>



- [<span data-ttu-id="45780-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="45780-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

