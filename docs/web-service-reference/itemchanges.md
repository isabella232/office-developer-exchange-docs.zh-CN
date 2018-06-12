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
description: ItemChanges 元素包含标识项目和更新以应用于项目的 ItemChange 元素的数组。
ms.openlocfilehash: 38fe112441a8773a2d6b494ed57c63341cab2b58
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826141"
---
# <a name="itemchanges"></a><span data-ttu-id="6c7cf-103">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="6c7cf-103">ItemChanges</span></span>

<span data-ttu-id="6c7cf-104">**ItemChanges**元素包含标识项目和更新以应用于项目的[ItemChange](itemchange.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="6c7cf-104">The **ItemChanges** element contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span> 
  
[<span data-ttu-id="6c7cf-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="6c7cf-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="6c7cf-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="6c7cf-106">ItemChanges</span></span>](itemchanges.md)
  
```xml
<ItemChanges>
   <ItemChange/>
</ItemChanges>
```

 <span data-ttu-id="6c7cf-107">**NonEmptyArrayOfItemChangesType**</span><span class="sxs-lookup"><span data-stu-id="6c7cf-107">**NonEmptyArrayOfItemChangesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c7cf-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c7cf-108">Attributes and elements</span></span>

<span data-ttu-id="6c7cf-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c7cf-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c7cf-110">属性</span><span class="sxs-lookup"><span data-stu-id="6c7cf-110">Attributes</span></span>

<span data-ttu-id="6c7cf-111">无。</span><span class="sxs-lookup"><span data-stu-id="6c7cf-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c7cf-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6c7cf-112">Child elements</span></span>

|<span data-ttu-id="6c7cf-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c7cf-113">**Element**</span></span>|<span data-ttu-id="6c7cf-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c7cf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c7cf-115">ItemChange</span><span class="sxs-lookup"><span data-stu-id="6c7cf-115">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="6c7cf-116">包含项标识符和更新应用到的项。</span><span class="sxs-lookup"><span data-stu-id="6c7cf-116">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c7cf-117">父元素</span><span class="sxs-lookup"><span data-stu-id="6c7cf-117">Parent elements</span></span>

|<span data-ttu-id="6c7cf-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c7cf-118">**Element**</span></span>|<span data-ttu-id="6c7cf-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c7cf-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c7cf-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="6c7cf-120">UpdateItem</span></span>](updateitem.md) <br/> |<span data-ttu-id="6c7cf-121">定义一个请求来更新邮箱中的项。</span><span class="sxs-lookup"><span data-stu-id="6c7cf-121">Defines a request to update items in a mailbox.</span></span>  <br/> <span data-ttu-id="6c7cf-122">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="6c7cf-122">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c7cf-123">备注</span><span class="sxs-lookup"><span data-stu-id="6c7cf-123">Remarks</span></span>

<span data-ttu-id="6c7cf-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6c7cf-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c7cf-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c7cf-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c7cf-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c7cf-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6c7cf-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c7cf-127">Schema Name</span></span>  <br/> |<span data-ttu-id="6c7cf-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="6c7cf-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6c7cf-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c7cf-129">Validation File</span></span>  <br/> |<span data-ttu-id="6c7cf-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6c7cf-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c7cf-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c7cf-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c7cf-132">False</span><span class="sxs-lookup"><span data-stu-id="6c7cf-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c7cf-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c7cf-133">See also</span></span>



[<span data-ttu-id="6c7cf-134">UpdateItem 操作</span><span class="sxs-lookup"><span data-stu-id="6c7cf-134">UpdateItem operation</span></span>](updateitem-operation.md)

