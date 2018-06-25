---
title: UpdatedItemIds
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9199aeb2-abdf-40c5-8743-40b61853c951
description: UpdatedItemIds 元素指定更新的提醒项目的标识符。
ms.openlocfilehash: b95ebb20823706e68b1fd66dc64f756808bb7375
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838371"
---
# <a name="updateditemids"></a><span data-ttu-id="eb909-103">UpdatedItemIds</span><span class="sxs-lookup"><span data-stu-id="eb909-103">UpdatedItemIds</span></span>

<span data-ttu-id="eb909-104">**UpdatedItemIds**元素指定更新的提醒项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="eb909-104">The **UpdatedItemIds** element specifies the identifiers of updated reminder items.</span></span> 
  
```XML
<UpdatedItemIds>
   <ItemId></ItemId>
</UpdatedItemIds>

```

 <span data-ttu-id="eb909-105">**NonEmptyArrayOfItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="eb909-105">**NonEmptyArrayOfItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="eb909-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="eb909-106">Attributes and elements</span></span>

<span data-ttu-id="eb909-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="eb909-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb909-108">属性</span><span class="sxs-lookup"><span data-stu-id="eb909-108">Attributes</span></span>

<span data-ttu-id="eb909-109">无。</span><span class="sxs-lookup"><span data-stu-id="eb909-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="eb909-110">子元素</span><span class="sxs-lookup"><span data-stu-id="eb909-110">Child elements</span></span>

[<span data-ttu-id="eb909-111">ItemId</span><span class="sxs-lookup"><span data-stu-id="eb909-111">ItemId</span></span>](itemid.md)
  
### <a name="parent-elements"></a><span data-ttu-id="eb909-112">父元素</span><span class="sxs-lookup"><span data-stu-id="eb909-112">Parent elements</span></span>

[<span data-ttu-id="eb909-113">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="eb909-113">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="eb909-114">备注</span><span class="sxs-lookup"><span data-stu-id="eb909-114">Remarks</span></span>

<span data-ttu-id="eb909-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="eb909-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="eb909-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="eb909-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
<span data-ttu-id="eb909-117">如果[PerformReminderAction](performreminderaction-operation.md)操作未成功完成或未在服务器上进行任何更改，则为空值返回**UpdatedItemIds**元素。</span><span class="sxs-lookup"><span data-stu-id="eb909-117">If the [PerformReminderAction](performreminderaction-operation.md) operation did not complete successfully, or no changes were made on the server, the **UpdatedItemIds** element is returned as an empty value.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="eb909-118">元素信息</span><span class="sxs-lookup"><span data-stu-id="eb909-118">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb909-119">命名空间</span><span class="sxs-lookup"><span data-stu-id="eb909-119">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="eb909-120">架构名称</span><span class="sxs-lookup"><span data-stu-id="eb909-120">Schema Name</span></span>  <br/> |<span data-ttu-id="eb909-121">消息架构</span><span class="sxs-lookup"><span data-stu-id="eb909-121">Messages schema</span></span>  <br/> |
|<span data-ttu-id="eb909-122">验证文件</span><span class="sxs-lookup"><span data-stu-id="eb909-122">Validation File</span></span>  <br/> |<span data-ttu-id="eb909-123">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="eb909-123">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="eb909-124">可以为空</span><span class="sxs-lookup"><span data-stu-id="eb909-124">Can be Empty</span></span>  <br/> |<span data-ttu-id="eb909-125">True</span><span class="sxs-lookup"><span data-stu-id="eb909-125">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb909-126">另请参阅</span><span class="sxs-lookup"><span data-stu-id="eb909-126">See also</span></span>



[<span data-ttu-id="eb909-127">PerformReminderActionResponse</span><span class="sxs-lookup"><span data-stu-id="eb909-127">PerformReminderActionResponse</span></span>](performreminderactionresponse.md)


- [<span data-ttu-id="eb909-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="eb909-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

