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
description: OldFolderId 元素包含已移动或复制的文件夹的原始标识符。
ms.openlocfilehash: ef73cad73213a1e8b5341907cd22177d8e1ba628
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826645"
---
# <a name="oldfolderid"></a><span data-ttu-id="02a1c-103">OldFolderId</span><span class="sxs-lookup"><span data-stu-id="02a1c-103">OldFolderId</span></span>

<span data-ttu-id="02a1c-104">**OldFolderId**元素包含已移动或复制的文件夹的原始标识符。</span><span class="sxs-lookup"><span data-stu-id="02a1c-104">The **OldFolderId** element contains the original identifier of a folder that was moved or copied.</span></span> 
  
```xml
<OldFolderId Id="" ChangeKey=""/>
```

 <span data-ttu-id="02a1c-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="02a1c-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="02a1c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="02a1c-106">Attributes and elements</span></span>

<span data-ttu-id="02a1c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="02a1c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02a1c-108">属性</span><span class="sxs-lookup"><span data-stu-id="02a1c-108">Attributes</span></span>

|<span data-ttu-id="02a1c-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="02a1c-109">**Attribute**</span></span>|<span data-ttu-id="02a1c-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="02a1c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="02a1c-111">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="02a1c-111">**Id**</span></span> <br/> |<span data-ttu-id="02a1c-112">包含一个字符串，标识 Exchange 存储中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="02a1c-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="02a1c-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="02a1c-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="02a1c-114">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="02a1c-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="02a1c-115">包含一个字符串，标识的文件夹的 Id 属性标识的版本。</span><span class="sxs-lookup"><span data-stu-id="02a1c-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="02a1c-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="02a1c-116">This attribute is optional.</span></span> <span data-ttu-id="02a1c-117">使用此属性以确保正确版本的文件夹使用。</span><span class="sxs-lookup"><span data-stu-id="02a1c-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02a1c-118">子元素</span><span class="sxs-lookup"><span data-stu-id="02a1c-118">Child elements</span></span>

<span data-ttu-id="02a1c-119">无。</span><span class="sxs-lookup"><span data-stu-id="02a1c-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="02a1c-120">父元素</span><span class="sxs-lookup"><span data-stu-id="02a1c-120">Parent elements</span></span>

|<span data-ttu-id="02a1c-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="02a1c-121">**Element**</span></span>|<span data-ttu-id="02a1c-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="02a1c-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="02a1c-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="02a1c-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="02a1c-124">表示复制的项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="02a1c-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="02a1c-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="02a1c-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="02a1c-126">表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="02a1c-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02a1c-127">备注</span><span class="sxs-lookup"><span data-stu-id="02a1c-127">Remarks</span></span>

<span data-ttu-id="02a1c-128">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="02a1c-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02a1c-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="02a1c-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02a1c-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="02a1c-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="02a1c-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="02a1c-131">Schema Name</span></span>  <br/> |<span data-ttu-id="02a1c-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="02a1c-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="02a1c-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="02a1c-133">Validation File</span></span>  <br/> |<span data-ttu-id="02a1c-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="02a1c-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="02a1c-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="02a1c-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="02a1c-136">False</span><span class="sxs-lookup"><span data-stu-id="02a1c-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02a1c-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="02a1c-137">See also</span></span>



[<span data-ttu-id="02a1c-138">订阅操作</span><span class="sxs-lookup"><span data-stu-id="02a1c-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="02a1c-139">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="02a1c-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="02a1c-140">取消操作</span><span class="sxs-lookup"><span data-stu-id="02a1c-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="02a1c-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="02a1c-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

