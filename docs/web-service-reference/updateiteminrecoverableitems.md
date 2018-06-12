---
title: UpdateItemInRecoverableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c49816b1-dbb5-4716-86c7-30790e86f30e
description: UpdateItemInRecoverableItems 元素指定更新可恢复的项目中的项的请求。
ms.openlocfilehash: 768de4bb8abe4780ab520405bae3149b8f17637c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838397"
---
# <a name="updateiteminrecoverableitems"></a><span data-ttu-id="dd081-103">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="dd081-103">UpdateItemInRecoverableItems</span></span>

<span data-ttu-id="dd081-104">**UpdateItemInRecoverableItems**元素指定更新可恢复的项目中的项的请求。</span><span class="sxs-lookup"><span data-stu-id="dd081-104">The **UpdateItemInRecoverableItems** element specifies a request to update an item in recoverable items.</span></span> 
  
```XML
<UpdateItemInRecoverableItems>
   <ItemId/>
   <Updates/>
   <Attachments/>
   <MakeItemImmutable/>
</UpdateItemInRecoverableItems>
```

 <span data-ttu-id="dd081-105">**UpdateItemInRecoverableItemsType**</span><span class="sxs-lookup"><span data-stu-id="dd081-105">**UpdateItemInRecoverableItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dd081-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dd081-106">Attributes and elements</span></span>

<span data-ttu-id="dd081-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dd081-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dd081-108">属性</span><span class="sxs-lookup"><span data-stu-id="dd081-108">Attributes</span></span>

<span data-ttu-id="dd081-109">无。</span><span class="sxs-lookup"><span data-stu-id="dd081-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dd081-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dd081-110">Child elements</span></span>

<span data-ttu-id="dd081-111">[ItemId](itemid.md) | [更新 （项）](updates-item.md) | [附件](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span><span class="sxs-lookup"><span data-stu-id="dd081-111">[ItemId](itemid.md) | [Updates (Item)](updates-item.md) | [Attachments](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dd081-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dd081-112">Parent elements</span></span>

<span data-ttu-id="dd081-113">无。</span><span class="sxs-lookup"><span data-stu-id="dd081-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd081-114">备注</span><span class="sxs-lookup"><span data-stu-id="dd081-114">Remarks</span></span>

<span data-ttu-id="dd081-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="dd081-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dd081-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dd081-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dd081-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="dd081-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd081-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="dd081-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="dd081-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="dd081-119">Schema name</span></span>  <br/> |<span data-ttu-id="dd081-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="dd081-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="dd081-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="dd081-121">Validation file</span></span>  <br/> |<span data-ttu-id="dd081-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="dd081-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="dd081-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="dd081-123">Can be empty</span></span>  <br/> |<span data-ttu-id="dd081-124">false</span><span class="sxs-lookup"><span data-stu-id="dd081-124">false</span></span>  <br/> |
   

