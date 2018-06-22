---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: AddressListId 元素指定的地址列表的标识符。
ms.openlocfilehash: d8a513559b7d127559537b43d7c6c0a4db121702
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753127"
---
# <a name="addresslistid"></a><span data-ttu-id="e7106-103">AddressListId</span><span class="sxs-lookup"><span data-stu-id="e7106-103">AddressListId</span></span>

<span data-ttu-id="e7106-104">**AddressListId**元素指定的地址列表的标识符。</span><span class="sxs-lookup"><span data-stu-id="e7106-104">The **AddressListId** element specifies the identifier of an address list.</span></span> 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 <span data-ttu-id="e7106-105">**AddressListIdType**</span><span class="sxs-lookup"><span data-stu-id="e7106-105">**AddressListIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7106-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e7106-106">Attributes and elements</span></span>

<span data-ttu-id="e7106-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e7106-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7106-108">属性</span><span class="sxs-lookup"><span data-stu-id="e7106-108">Attributes</span></span>

|<span data-ttu-id="e7106-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="e7106-109">**Attribute**</span></span>|<span data-ttu-id="e7106-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7106-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e7106-111">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="e7106-111">**Id**</span></span> <br/> |<span data-ttu-id="e7106-112">一个 string 地址列表标识符。</span><span class="sxs-lookup"><span data-stu-id="e7106-112">A string address list identifier.</span></span> <span data-ttu-id="e7106-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="e7106-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e7106-114">子元素</span><span class="sxs-lookup"><span data-stu-id="e7106-114">Child elements</span></span>

<span data-ttu-id="e7106-115">无。</span><span class="sxs-lookup"><span data-stu-id="e7106-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7106-116">父元素</span><span class="sxs-lookup"><span data-stu-id="e7106-116">Parent elements</span></span>

|<span data-ttu-id="e7106-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7106-117">**Element**</span></span>|<span data-ttu-id="e7106-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7106-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7106-119">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="e7106-119">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="e7106-120">指示使用文件夹的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="e7106-120">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="e7106-121">此元素必须存在时复制、 删除、 移动和目标文件夹中的对话项目上设置只读的状态。</span><span class="sxs-lookup"><span data-stu-id="e7106-121">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="e7106-122">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="e7106-122">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="e7106-123">指定电子邮件项目复制到其中的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="e7106-123">Specifies the identifier of the folder to which email items are copied.</span></span>  <br/> |
|[<span data-ttu-id="e7106-124">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="e7106-124">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="e7106-125">指示副本的目标文件夹，并移动操作。</span><span class="sxs-lookup"><span data-stu-id="e7106-125">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="e7106-126">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="e7106-126">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="e7106-127">指定电子邮件项目移至其中的文件夹的标识符</span><span class="sxs-lookup"><span data-stu-id="e7106-127">Specifies the identifier of the folder to which email items are moved</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7106-128">备注</span><span class="sxs-lookup"><span data-stu-id="e7106-128">Remarks</span></span>

<span data-ttu-id="e7106-129">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e7106-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e7106-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e7106-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7106-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="e7106-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7106-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="e7106-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7106-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="e7106-133">Schema Name</span></span>  <br/> |<span data-ttu-id="e7106-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="e7106-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="e7106-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="e7106-135">Validation File</span></span>  <br/> |<span data-ttu-id="e7106-136">types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7106-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7106-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="e7106-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e7106-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7106-138">See also</span></span>

- [<span data-ttu-id="e7106-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7106-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

