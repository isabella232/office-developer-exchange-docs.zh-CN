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
description: DeleteItemField 元素表示在 UpdateItem 调用过程中从项中删除给定属性的操作。
ms.openlocfilehash: e6f5ee8a1130d7c040f3ddd94021eff6d4a758b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455672"
---
# <a name="deleteitemfield"></a><span data-ttu-id="18092-103">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="18092-103">DeleteItemField</span></span>

<span data-ttu-id="18092-104">**DeleteItemField**元素表示在 UpdateItem 调用过程中从项中删除给定属性的操作。</span><span class="sxs-lookup"><span data-stu-id="18092-104">The **DeleteItemField** element represents an operation to delete a given property from an item during an UpdateItem call.</span></span> 
 
- [<span data-ttu-id="18092-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="18092-105">UpdateItem</span></span>](updateitem.md)  
- [<span data-ttu-id="18092-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="18092-106">ItemChanges</span></span>](itemchanges.md) 
- [<span data-ttu-id="18092-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="18092-107">ItemChange</span></span>](itemchange.md) 
- [<span data-ttu-id="18092-108">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="18092-108">Updates (Item)</span></span>](updates-item.md) 
- [<span data-ttu-id="18092-109">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="18092-109">DeleteItemField</span></span>](deleteitemfield.md)
  
```xml
<DeleteItemField>
   <FieldURI/>
</DeleteItemField>
```

```xml
<DeleteItemField>
   <IndexedFieldURI/> 
</DeleteItemField>
```

```xml
<DeleteItemField>
   <ExtendedFieldURI/>
</DeleteItemField>
```

<span data-ttu-id="18092-110">**DeleteItemFieldType**</span><span class="sxs-lookup"><span data-stu-id="18092-110">**DeleteItemFieldType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="18092-111">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18092-111">Attributes and elements</span></span>

<span data-ttu-id="18092-112">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18092-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18092-113">Attributes</span><span class="sxs-lookup"><span data-stu-id="18092-113">Attributes</span></span>

<span data-ttu-id="18092-114">无。</span><span class="sxs-lookup"><span data-stu-id="18092-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18092-115">子元素</span><span class="sxs-lookup"><span data-stu-id="18092-115">Child elements</span></span>

|<span data-ttu-id="18092-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="18092-116">**Element**</span></span>|<span data-ttu-id="18092-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="18092-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18092-118">FieldURI</span><span class="sxs-lookup"><span data-stu-id="18092-118">FieldURI</span></span>](fielduri.md) <br/> |<span data-ttu-id="18092-119">标识由 URI 频繁引用的属性。</span><span class="sxs-lookup"><span data-stu-id="18092-119">Identifies frequently referenced properties by URI.</span></span>  <br/> |
|[<span data-ttu-id="18092-120">IndexedFieldURI</span><span class="sxs-lookup"><span data-stu-id="18092-120">IndexedFieldURI</span></span>](indexedfielduri.md) <br/> |<span data-ttu-id="18092-121">标识 dictionary 属性的各个成员。</span><span class="sxs-lookup"><span data-stu-id="18092-121">Identifies individual members of a dictionary property.</span></span>  <br/> |
|[<span data-ttu-id="18092-122">ExtendedFieldURI</span><span class="sxs-lookup"><span data-stu-id="18092-122">ExtendedFieldURI</span></span>](extendedfielduri.md) <br/> |<span data-ttu-id="18092-123">标识扩展 MAPI 属性。</span><span class="sxs-lookup"><span data-stu-id="18092-123">Identifies extended MAPI properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="18092-124">父元素</span><span class="sxs-lookup"><span data-stu-id="18092-124">Parent elements</span></span>

|<span data-ttu-id="18092-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="18092-125">**Element**</span></span>|<span data-ttu-id="18092-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="18092-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18092-127">更新（项目）</span><span class="sxs-lookup"><span data-stu-id="18092-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="18092-128">包含一组元素，这些元素定义追加、设置和删除对项目属性所做的更改。</span><span class="sxs-lookup"><span data-stu-id="18092-128">Contains a set of elements that define append, set, and delete changes to item properties.</span></span>  <br/><br/><span data-ttu-id="18092-129">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="18092-129">The following is the XPath expression to this element:</span></span><br/>`/UpdateItem/ItemChanges/ItemChange[i]/Updates` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18092-130">说明</span><span class="sxs-lookup"><span data-stu-id="18092-130">Remarks</span></span>

<span data-ttu-id="18092-131">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18092-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18092-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="18092-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18092-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="18092-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18092-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="18092-134">Schema Name</span></span>  <br/> |<span data-ttu-id="18092-135">类型架构</span><span class="sxs-lookup"><span data-stu-id="18092-135">types schema</span></span>  <br/> |
|<span data-ttu-id="18092-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="18092-136">Validation File</span></span>  <br/> |<span data-ttu-id="18092-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="18092-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="18092-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="18092-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="18092-139">False</span><span class="sxs-lookup"><span data-stu-id="18092-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18092-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18092-140">See also</span></span>

- [<span data-ttu-id="18092-141">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="18092-141">UpdateItem operation</span></span>](updateitem-operation.md)

