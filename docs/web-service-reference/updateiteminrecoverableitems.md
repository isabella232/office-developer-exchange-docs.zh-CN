---
title: UpdateItemInRecoverableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c49816b1-dbb5-4716-86c7-30790e86f30e
description: UpdateItemInRecoverableItems 元素指定用于更新可恢复项目中的项目的请求。
ms.openlocfilehash: f3dae55097c613b84a80795185baad559e312b90
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459782"
---
# <a name="updateiteminrecoverableitems"></a><span data-ttu-id="2cfe5-103">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="2cfe5-103">UpdateItemInRecoverableItems</span></span>

<span data-ttu-id="2cfe5-104">**UpdateItemInRecoverableItems**元素指定用于更新可恢复项目中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="2cfe5-104">The **UpdateItemInRecoverableItems** element specifies a request to update an item in recoverable items.</span></span> 
  
```XML
<UpdateItemInRecoverableItems>
   <ItemId/>
   <Updates/>
   <Attachments/>
   <MakeItemImmutable/>
</UpdateItemInRecoverableItems>
```

 <span data-ttu-id="2cfe5-105">**UpdateItemInRecoverableItemsType**</span><span class="sxs-lookup"><span data-stu-id="2cfe5-105">**UpdateItemInRecoverableItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2cfe5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2cfe5-106">Attributes and elements</span></span>

<span data-ttu-id="2cfe5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2cfe5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2cfe5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="2cfe5-108">Attributes</span></span>

<span data-ttu-id="2cfe5-109">无。</span><span class="sxs-lookup"><span data-stu-id="2cfe5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2cfe5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2cfe5-110">Child elements</span></span>

<span data-ttu-id="2cfe5-111">[ItemId](itemid.md)  | [更新（项目）](updates-item.md)  | [附件](attachments-ex15websvcsotherref.md)  | [MakeItemImmutable](makeitemimmutable.md)</span><span class="sxs-lookup"><span data-stu-id="2cfe5-111">[ItemId](itemid.md) | [Updates (Item)](updates-item.md) | [Attachments](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2cfe5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2cfe5-112">Parent elements</span></span>

<span data-ttu-id="2cfe5-113">无。</span><span class="sxs-lookup"><span data-stu-id="2cfe5-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2cfe5-114">说明</span><span class="sxs-lookup"><span data-stu-id="2cfe5-114">Remarks</span></span>

<span data-ttu-id="2cfe5-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2cfe5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2cfe5-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2cfe5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2cfe5-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2cfe5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2cfe5-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2cfe5-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2cfe5-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2cfe5-119">Schema name</span></span>  <br/> |<span data-ttu-id="2cfe5-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="2cfe5-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2cfe5-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2cfe5-121">Validation file</span></span>  <br/> |<span data-ttu-id="2cfe5-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2cfe5-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2cfe5-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2cfe5-123">Can be empty</span></span>  <br/> |<span data-ttu-id="2cfe5-124">false</span><span class="sxs-lookup"><span data-stu-id="2cfe5-124">false</span></span>  <br/> |
   

