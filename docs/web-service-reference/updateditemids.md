---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: UpdatedItemIds 元素指定更新的提醒项的标识符。
ms.openlocfilehash: 4a87bf50f90e80c0c887ee3a66b9f201ea1c8440
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465034"
---
# <a name="updateditemids"></a><span data-ttu-id="d0b9d-103">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="d0b9d-103">UpdatedItemIds</span></span>

<span data-ttu-id="d0b9d-104">**UpdatedItemIds**元素指定更新的提醒项的标识符。</span><span class="sxs-lookup"><span data-stu-id="d0b9d-104">The **UpdatedItemIds** element specifies the identifiers of updated reminder items.</span></span> 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 <span data-ttu-id="d0b9d-105">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="d0b9d-105">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0b9d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d0b9d-106">Attributes and elements</span></span>

<span data-ttu-id="d0b9d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0b9d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0b9d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d0b9d-108">Attributes</span></span>

<span data-ttu-id="d0b9d-109">无。</span><span class="sxs-lookup"><span data-stu-id="d0b9d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0b9d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d0b9d-110">Child elements</span></span>

[<span data-ttu-id="d0b9d-111">ItemId</span><span class="sxs-lookup"><span data-stu-id="d0b9d-111">ItemId</span></span>](itemid.md)
  
### <a name="parent-elements"></a><span data-ttu-id="d0b9d-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d0b9d-112">Parent elements</span></span>

[<span data-ttu-id="d0b9d-113">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="d0b9d-113">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="d0b9d-114">备注</span><span class="sxs-lookup"><span data-stu-id="d0b9d-114">Remarks</span></span>

<span data-ttu-id="d0b9d-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d0b9d-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d0b9d-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d0b9d-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="d0b9d-117">如果[PerformReminderAction](performreminderaction-operation.md)操作未成功完成，或者服务器上未进行任何更改，则**UpdatedItemIds**元素将作为空值返回。</span><span class="sxs-lookup"><span data-stu-id="d0b9d-117">If the [PerformReminderAction](performreminderaction-operation.md) operation did not complete successfully, or no changes were made on the server, the **UpdatedItemIds** element is returned as an empty value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="d0b9d-118">元素信息</span><span class="sxs-lookup"><span data-stu-id="d0b9d-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0b9d-119">命名空间</span><span class="sxs-lookup"><span data-stu-id="d0b9d-119">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d0b9d-120">架构名称</span><span class="sxs-lookup"><span data-stu-id="d0b9d-120">Schema Name</span></span>  <br/> |<span data-ttu-id="d0b9d-121">消息架构</span><span class="sxs-lookup"><span data-stu-id="d0b9d-121">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d0b9d-122">验证文件</span><span class="sxs-lookup"><span data-stu-id="d0b9d-122">Validation File</span></span>  <br/> |<span data-ttu-id="d0b9d-123">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d0b9d-123">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0b9d-124">可以为空</span><span class="sxs-lookup"><span data-stu-id="d0b9d-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0b9d-125">True</span><span class="sxs-lookup"><span data-stu-id="d0b9d-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0b9d-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0b9d-126">See also</span></span>



[<span data-ttu-id="d0b9d-127">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="d0b9d-127">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)


- [<span data-ttu-id="d0b9d-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d0b9d-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

