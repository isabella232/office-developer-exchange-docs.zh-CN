---
title: ItemChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChanges
api_type:
- schema
ms.assetid: cd307892-2f69-4494-8325-219bdb5c3ad5
description: ItemChanges 元素包含 ItemChange 元素的数组，这些元素标识项目以及要应用于这些项目的更新。
ms.openlocfilehash: ea6fb2023b88360f9558057e80c7fe0d855173b5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459908"
---
# <a name="itemchanges"></a><span data-ttu-id="73eff-103">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="73eff-103">ItemChanges</span></span>

<span data-ttu-id="73eff-104">**ItemChanges**元素包含[ItemChange](itemchange.md)元素的数组，这些元素标识项目以及要应用于这些项目的更新。</span><span class="sxs-lookup"><span data-stu-id="73eff-104">The **ItemChanges** element contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span> 
  
[<span data-ttu-id="73eff-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="73eff-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="73eff-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="73eff-106">ItemChanges</span></span>](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 <span data-ttu-id="73eff-107">**NonEmptyArrayOfItemChangesType**</span><span class="sxs-lookup"><span data-stu-id="73eff-107">**NonEmptyArrayOfItemChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73eff-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="73eff-108">Attributes and elements</span></span>

<span data-ttu-id="73eff-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="73eff-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73eff-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="73eff-110">Attributes</span></span>

<span data-ttu-id="73eff-111">无。</span><span class="sxs-lookup"><span data-stu-id="73eff-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="73eff-112">子元素</span><span class="sxs-lookup"><span data-stu-id="73eff-112">Child elements</span></span>

|<span data-ttu-id="73eff-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="73eff-113">**Element**</span></span>|<span data-ttu-id="73eff-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="73eff-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73eff-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="73eff-115">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="73eff-116">包含项目标识符和要应用于项目的更新。</span><span class="sxs-lookup"><span data-stu-id="73eff-116">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73eff-117">父元素</span><span class="sxs-lookup"><span data-stu-id="73eff-117">Parent elements</span></span>

|<span data-ttu-id="73eff-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="73eff-118">**Element**</span></span>|<span data-ttu-id="73eff-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="73eff-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73eff-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="73eff-120">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="73eff-121">定义对邮箱中的项目的更新请求。</span><span class="sxs-lookup"><span data-stu-id="73eff-121">Defines a request to update items in a mailbox.</span></span>  <br/> <span data-ttu-id="73eff-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="73eff-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73eff-123">说明</span><span class="sxs-lookup"><span data-stu-id="73eff-123">Remarks</span></span>

<span data-ttu-id="73eff-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="73eff-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73eff-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="73eff-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73eff-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="73eff-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="73eff-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="73eff-127">Schema Name</span></span>  <br/> |<span data-ttu-id="73eff-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="73eff-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="73eff-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="73eff-129">Validation File</span></span>  <br/> |<span data-ttu-id="73eff-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="73eff-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="73eff-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="73eff-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="73eff-132">False</span><span class="sxs-lookup"><span data-stu-id="73eff-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73eff-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="73eff-133">See also</span></span>



[<span data-ttu-id="73eff-134">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="73eff-134">UpdateItem operation</span></span>](updateitem-operation.md)

