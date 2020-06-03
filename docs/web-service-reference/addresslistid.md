---
title: AddressListId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a3334bb2-90dc-4fe1-96d9-890b13d9ff30
description: AddressListId 元素指定地址列表的标识符。
ms.openlocfilehash: c33944bf6e41903a5de596628e1ce7ba9f7421e1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463606"
---
# <a name="addresslistid"></a><span data-ttu-id="8a481-103">AddressListId</span><span class="sxs-lookup"><span data-stu-id="8a481-103">AddressListId</span></span>

<span data-ttu-id="8a481-104">**AddressListId**元素指定地址列表的标识符。</span><span class="sxs-lookup"><span data-stu-id="8a481-104">The **AddressListId** element specifies the identifier of an address list.</span></span> 
  
```XML
<AddressListId Id="">
</AddressListId>
```

 <span data-ttu-id="8a481-105">**AddressListIdType**</span><span class="sxs-lookup"><span data-stu-id="8a481-105">**AddressListIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a481-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a481-106">Attributes and elements</span></span>

<span data-ttu-id="8a481-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a481-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a481-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8a481-108">Attributes</span></span>

|<span data-ttu-id="8a481-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="8a481-109">**Attribute**</span></span>|<span data-ttu-id="8a481-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a481-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a481-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="8a481-111">**Id**</span></span> <br/> |<span data-ttu-id="8a481-112">字符串地址列表标识符。</span><span class="sxs-lookup"><span data-stu-id="8a481-112">A string address list identifier.</span></span> <span data-ttu-id="8a481-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="8a481-113">This attribute is required.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8a481-114">子元素</span><span class="sxs-lookup"><span data-stu-id="8a481-114">Child elements</span></span>

<span data-ttu-id="8a481-115">无。</span><span class="sxs-lookup"><span data-stu-id="8a481-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8a481-116">父元素</span><span class="sxs-lookup"><span data-stu-id="8a481-116">Parent elements</span></span>

|<span data-ttu-id="8a481-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="8a481-117">**Element**</span></span>|<span data-ttu-id="8a481-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a481-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a481-119">ContextFolderId</span><span class="sxs-lookup"><span data-stu-id="8a481-119">ContextFolderId</span></span>](contextfolderid.md) <br/> |<span data-ttu-id="8a481-120">指示针对使用文件夹的操作的文件夹。</span><span class="sxs-lookup"><span data-stu-id="8a481-120">Indicates the folder that is targeted for actions that use folders.</span></span> <span data-ttu-id="8a481-121">在复制、删除、移动和设置目标文件夹中会话项的读取状态时，必须存在此元素。</span><span class="sxs-lookup"><span data-stu-id="8a481-121">This element must be present when copying, deleting, moving, and setting read state on conversation items in a target folder.</span></span>  <br/> |
|[<span data-ttu-id="8a481-122">CopyToFolder</span><span class="sxs-lookup"><span data-stu-id="8a481-122">CopyToFolder</span></span>](copytofolder.md) <br/> |<span data-ttu-id="8a481-123">指定要将电子邮件项目复制到其中的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="8a481-123">Specifies the identifier of the folder to which email items are copied.</span></span>  <br/> |
|[<span data-ttu-id="8a481-124">DestinationFolderId</span><span class="sxs-lookup"><span data-stu-id="8a481-124">DestinationFolderId</span></span>](destinationfolderid.md) <br/> |<span data-ttu-id="8a481-125">指示复制和移动操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="8a481-125">Indicates the destination folder for copy and move actions.</span></span>  <br/> |
|[<span data-ttu-id="8a481-126">MoveToFolder</span><span class="sxs-lookup"><span data-stu-id="8a481-126">MoveToFolder</span></span>](movetofolder.md) <br/> |<span data-ttu-id="8a481-127">指定将电子邮件项目移至其中的文件夹的标识符</span><span class="sxs-lookup"><span data-stu-id="8a481-127">Specifies the identifier of the folder to which email items are moved</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a481-128">备注</span><span class="sxs-lookup"><span data-stu-id="8a481-128">Remarks</span></span>

<span data-ttu-id="8a481-129">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8a481-129">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8a481-130">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a481-130">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a481-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a481-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a481-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a481-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8a481-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a481-133">Schema Name</span></span>  <br/> |<span data-ttu-id="8a481-134">类型架构</span><span class="sxs-lookup"><span data-stu-id="8a481-134">Type schema</span></span>  <br/> |
|<span data-ttu-id="8a481-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a481-135">Validation File</span></span>  <br/> |<span data-ttu-id="8a481-136">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="8a481-136">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8a481-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a481-137">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="8a481-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a481-138">See also</span></span>

- [<span data-ttu-id="8a481-139">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8a481-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

