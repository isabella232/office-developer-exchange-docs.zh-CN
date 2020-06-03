---
title: OldFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldFolderId
api_type:
- schema
ms.assetid: da554a97-ab87-4950-9fc4-26b1972381bb
description: OldFolderId 元素包含移动或复制的文件夹的原始标识符。
ms.openlocfilehash: a6713b9e0c47d68480724c3902086da6a8647dd7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458059"
---
# <a name="oldfolderid"></a><span data-ttu-id="7bc51-103">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="7bc51-103">OldFolderId</span></span>

<span data-ttu-id="7bc51-104">**OldFolderId**元素包含移动或复制的文件夹的原始标识符。</span><span class="sxs-lookup"><span data-stu-id="7bc51-104">The **OldFolderId** element contains the original identifier of a folder that was moved or copied.</span></span> 
  
```xml
<OldFolderId Id="" ChangeKey=""/>
```

 <span data-ttu-id="7bc51-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="7bc51-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7bc51-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7bc51-106">Attributes and elements</span></span>

<span data-ttu-id="7bc51-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7bc51-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7bc51-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7bc51-108">Attributes</span></span>

|<span data-ttu-id="7bc51-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="7bc51-109">**Attribute**</span></span>|<span data-ttu-id="7bc51-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="7bc51-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7bc51-111">**Id**</span><span class="sxs-lookup"><span data-stu-id="7bc51-111">**Id**</span></span> <br/> |<span data-ttu-id="7bc51-112">包含标识 Exchange 存储中的文件夹的字符串。</span><span class="sxs-lookup"><span data-stu-id="7bc51-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="7bc51-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="7bc51-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="7bc51-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="7bc51-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="7bc51-115">包含标识由 Id 属性标识的文件夹版本的字符串。</span><span class="sxs-lookup"><span data-stu-id="7bc51-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="7bc51-116">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="7bc51-116">This attribute is optional.</span></span> <span data-ttu-id="7bc51-117">使用此属性可确保使用的是正确的文件夹版本。</span><span class="sxs-lookup"><span data-stu-id="7bc51-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7bc51-118">子元素</span><span class="sxs-lookup"><span data-stu-id="7bc51-118">Child elements</span></span>

<span data-ttu-id="7bc51-119">无。</span><span class="sxs-lookup"><span data-stu-id="7bc51-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7bc51-120">父元素</span><span class="sxs-lookup"><span data-stu-id="7bc51-120">Parent elements</span></span>

|<span data-ttu-id="7bc51-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="7bc51-121">**Element**</span></span>|<span data-ttu-id="7bc51-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="7bc51-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7bc51-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="7bc51-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="7bc51-124">表示在其中复制项目或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7bc51-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="7bc51-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="7bc51-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="7bc51-126">代表将项目或文件夹从一个父文件夹移动到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="7bc51-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7bc51-127">说明</span><span class="sxs-lookup"><span data-stu-id="7bc51-127">Remarks</span></span>

<span data-ttu-id="7bc51-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7bc51-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7bc51-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="7bc51-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bc51-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="7bc51-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7bc51-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="7bc51-131">Schema Name</span></span>  <br/> |<span data-ttu-id="7bc51-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="7bc51-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="7bc51-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="7bc51-133">Validation File</span></span>  <br/> |<span data-ttu-id="7bc51-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7bc51-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7bc51-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="7bc51-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="7bc51-136">False</span><span class="sxs-lookup"><span data-stu-id="7bc51-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7bc51-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7bc51-137">See also</span></span>



[<span data-ttu-id="7bc51-138">订阅操作</span><span class="sxs-lookup"><span data-stu-id="7bc51-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="7bc51-139">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="7bc51-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="7bc51-140">取消订阅操作</span><span class="sxs-lookup"><span data-stu-id="7bc51-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="7bc51-141">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7bc51-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

