---
title: OldItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OldItemId
api_type:
- schema
ms.assetid: fb57deee-9cc3-4730-9805-ff34f39e3ab7
description: OldItemId 元素包含已复制或移动的项的唯一标识符。
ms.openlocfilehash: ced7fc6891e0d1fde42a8cb9cad4f4e55493b5d1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826648"
---
# <a name="olditemid"></a><span data-ttu-id="2e8a5-103">OldItemId</span><span class="sxs-lookup"><span data-stu-id="2e8a5-103">OldItemId</span></span>

<span data-ttu-id="2e8a5-104">**OldItemId**元素包含已复制或移动的项的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-104">The **OldItemId** element contains the unique identifier of the item that was copied or moved.</span></span> 
  
```xml
<OldItemId Id="" ChangeKey=""/>
```

 <span data-ttu-id="2e8a5-105">**ItemIdType**</span><span class="sxs-lookup"><span data-stu-id="2e8a5-105">**ItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2e8a5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2e8a5-106">Attributes and elements</span></span>

<span data-ttu-id="2e8a5-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e8a5-108">属性</span><span class="sxs-lookup"><span data-stu-id="2e8a5-108">Attributes</span></span>

|<span data-ttu-id="2e8a5-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="2e8a5-109">**Attribute**</span></span>|<span data-ttu-id="2e8a5-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e8a5-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2e8a5-111">
  **Id**</span><span class="sxs-lookup"><span data-stu-id="2e8a5-111">**Id**</span></span> <br/> |<span data-ttu-id="2e8a5-112">包含一个字符串，标识 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-112">Contains a string that identifies an item in the Exchange store.</span></span> <span data-ttu-id="2e8a5-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="2e8a5-114">**更改密钥**</span><span class="sxs-lookup"><span data-stu-id="2e8a5-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="2e8a5-115">包含一个字符串，标识项目的 Id 属性标识的版本。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-115">Contains a string that identifies a version of an item that is identified by the Id attribute.</span></span> <span data-ttu-id="2e8a5-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-116">This attribute is optional.</span></span> <span data-ttu-id="2e8a5-117">使用此属性以确保正确版本的项目使用。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-117">Use this attribute to make sure that the correct version of an item is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2e8a5-118">子元素</span><span class="sxs-lookup"><span data-stu-id="2e8a5-118">Child elements</span></span>

<span data-ttu-id="2e8a5-119">无。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2e8a5-120">父元素</span><span class="sxs-lookup"><span data-stu-id="2e8a5-120">Parent elements</span></span>

|<span data-ttu-id="2e8a5-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="2e8a5-121">**Element**</span></span>|<span data-ttu-id="2e8a5-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="2e8a5-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2e8a5-123">CopiedEvent</span><span class="sxs-lookup"><span data-stu-id="2e8a5-123">CopiedEvent</span></span>](copiedevent.md) <br/> |<span data-ttu-id="2e8a5-124">表示复制的项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-124">Represents an event in which an item or folder is copied.</span></span>  <br/> |
|[<span data-ttu-id="2e8a5-125">MovedEvent</span><span class="sxs-lookup"><span data-stu-id="2e8a5-125">MovedEvent</span></span>](movedevent.md) <br/> |<span data-ttu-id="2e8a5-126">表示在其中项目或文件夹从一个父文件夹移到另一个父文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-126">Represents an event in which an item or folder is moved from one parent folder to another parent folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e8a5-127">备注</span><span class="sxs-lookup"><span data-stu-id="2e8a5-127">Remarks</span></span>

<span data-ttu-id="2e8a5-128">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2e8a5-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2e8a5-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="2e8a5-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e8a5-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="2e8a5-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="2e8a5-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="2e8a5-131">Schema Name</span></span>  <br/> |<span data-ttu-id="2e8a5-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="2e8a5-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="2e8a5-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="2e8a5-133">Validation File</span></span>  <br/> |<span data-ttu-id="2e8a5-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="2e8a5-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="2e8a5-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="2e8a5-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="2e8a5-136">False</span><span class="sxs-lookup"><span data-stu-id="2e8a5-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2e8a5-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2e8a5-137">See also</span></span>



[<span data-ttu-id="2e8a5-138">订阅操作</span><span class="sxs-lookup"><span data-stu-id="2e8a5-138">Subscribe operation</span></span>](subscribe-operation.md)
  
[<span data-ttu-id="2e8a5-139">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="2e8a5-139">GetEvents operation</span></span>](getevents-operation.md)
  
[<span data-ttu-id="2e8a5-140">取消操作</span><span class="sxs-lookup"><span data-stu-id="2e8a5-140">Unsubscribe operation</span></span>](unsubscribe-operation.md)


- [<span data-ttu-id="2e8a5-141">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="2e8a5-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

