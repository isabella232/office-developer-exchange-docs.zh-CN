---
title: DeleteItemField
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteItemField
api_type:
- schema
ms.assetid: 3893be6a-49a7-49f6-bf53-c7f819ec3f87
description: DeleteItemField 元素均表示 UpdateItem 呼叫期间，从项目中删除给定的属性的操作。
ms.openlocfilehash: 2388bd10379211a31890b7c4f27920431ce444c8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753812"
---
# <a name="deleteitemfield"></a><span data-ttu-id="a13fe-103">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="a13fe-103">DeleteItemField</span></span>

<span data-ttu-id="a13fe-104">**DeleteItemField**元素均表示 UpdateItem 呼叫期间，从项目中删除给定的属性的操作。</span><span class="sxs-lookup"><span data-stu-id="a13fe-104">The **DeleteItemField** element represents an operation to delete a given property from an item during an UpdateItem call.</span></span> 
 
- [<span data-ttu-id="a13fe-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="a13fe-105">UpdateItem</span></span>](updateitem.md)  
- [<span data-ttu-id="a13fe-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="a13fe-106">ItemChanges</span></span>](itemchanges.md) 
- [<span data-ttu-id="a13fe-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="a13fe-107">ItemChange</span></span>](itemchange.md) 
- [<span data-ttu-id="a13fe-108">更新 （项）</span><span class="sxs-lookup"><span data-stu-id="a13fe-108">Updates (Item)</span></span>](updates-item.md) 
- [<span data-ttu-id="a13fe-109">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="a13fe-109">DeleteItemField</span></span>](deleteitemfield.md)
  
```xml
<DeleteItemField>
   <FieldURI/>
</DeleteItemField>
```

 <span data-ttu-id="a13fe-110">**DeleteItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="a13fe-110">**DeleteItemFieldType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a13fe-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a13fe-111">Attributes and elements</span></span>

<span data-ttu-id="a13fe-112">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a13fe-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a13fe-113">属性</span><span class="sxs-lookup"><span data-stu-id="a13fe-113">Attributes</span></span>

<span data-ttu-id="a13fe-114">无。</span><span class="sxs-lookup"><span data-stu-id="a13fe-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a13fe-115">子元素</span><span class="sxs-lookup"><span data-stu-id="a13fe-115">Child elements</span></span>

|<span data-ttu-id="a13fe-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="a13fe-116">**Element**</span></span>|<span data-ttu-id="a13fe-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a13fe-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a13fe-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="a13fe-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="a13fe-119">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="a13fe-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="a13fe-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a13fe-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="a13fe-121">标识字典属性中的各个成员。</span><span class="sxs-lookup"><span data-stu-id="a13fe-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="a13fe-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="a13fe-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="a13fe-123">标识扩展的 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="a13fe-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a13fe-124">父元素</span><span class="sxs-lookup"><span data-stu-id="a13fe-124">Parent elements</span></span>

|<span data-ttu-id="a13fe-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="a13fe-125">**Element**</span></span>|<span data-ttu-id="a13fe-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="a13fe-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a13fe-127">更新 （项）</span><span class="sxs-lookup"><span data-stu-id="a13fe-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="a13fe-128">包含一组定义的元素的 append、 设置和删除项目属性更改。</span><span class="sxs-lookup"><span data-stu-id="a13fe-128">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/><br/><span data-ttu-id="a13fe-129">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="a13fe-129">The following is the XPath expression to this element:</span></span><br/>`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a13fe-130">备注</span><span class="sxs-lookup"><span data-stu-id="a13fe-130">Remarks</span></span>

<span data-ttu-id="a13fe-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a13fe-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a13fe-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="a13fe-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a13fe-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="a13fe-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a13fe-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="a13fe-134">Schema Name</span></span>  <br/> |<span data-ttu-id="a13fe-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="a13fe-135">types schema</span></span>  <br/> |
|<span data-ttu-id="a13fe-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="a13fe-136">Validation File</span></span>  <br/> |<span data-ttu-id="a13fe-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a13fe-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a13fe-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="a13fe-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="a13fe-139">False</span><span class="sxs-lookup"><span data-stu-id="a13fe-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a13fe-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a13fe-140">See also</span></span>

- [<span data-ttu-id="a13fe-141">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="a13fe-141">UpdateItem operation</span></span>](updateitem-operation.md)

