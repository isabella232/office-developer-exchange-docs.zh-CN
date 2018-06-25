---
title: DeletedEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeletedEvent
api_type:
- schema
ms.assetid: c4565eb4-b537-466c-b1ff-11602533812b
description: DeletedEvent 元素表示删除项或文件夹的事件。
ms.openlocfilehash: f06ca0727916f415c648e876f88bf7eacef5a5ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753795"
---
# <a name="deletedevent"></a><span data-ttu-id="e81cf-103">DeletedEvent</span><span class="sxs-lookup"><span data-stu-id="e81cf-103">DeletedEvent</span></span>

<span data-ttu-id="e81cf-104">**DeletedEvent**元素表示删除项或文件夹的事件。</span><span class="sxs-lookup"><span data-stu-id="e81cf-104">The **DeletedEvent** element represents an event in which an item or folder is deleted.</span></span> 
  
```xml
<DeletedEvent>
   <Watermark/>
   <TimeStamp/>
   <ItemId/>
   <ParentFolderId/>
</DeletedEvent>
```

<span data-ttu-id="e81cf-105">**BaseObjectChangedEventType**</span><span class="sxs-lookup"><span data-stu-id="e81cf-105">**BaseObjectChangedEventType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e81cf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e81cf-106">Attributes and elements</span></span>

<span data-ttu-id="e81cf-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e81cf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e81cf-108">属性</span><span class="sxs-lookup"><span data-stu-id="e81cf-108">Attributes</span></span>

<span data-ttu-id="e81cf-109">无。</span><span class="sxs-lookup"><span data-stu-id="e81cf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e81cf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e81cf-110">Child elements</span></span>

|<span data-ttu-id="e81cf-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e81cf-111">**Element**</span></span>|<span data-ttu-id="e81cf-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e81cf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e81cf-113">水印</span><span class="sxs-lookup"><span data-stu-id="e81cf-113">Watermark</span></span>](watermark.md) <br/> |<span data-ttu-id="e81cf-114">代表邮箱事件表格中的事件书签。</span><span class="sxs-lookup"><span data-stu-id="e81cf-114">Represents an event bookmark in the mailbox events table.</span></span>  <br/> |
|[<span data-ttu-id="e81cf-115">时间戳</span><span class="sxs-lookup"><span data-stu-id="e81cf-115">TimeStamp</span></span>](timestamp.md) <br/> |<span data-ttu-id="e81cf-116">代表已删除的项目或文件夹邮箱事件的时间戳。</span><span class="sxs-lookup"><span data-stu-id="e81cf-116">Represents the timestamp of a deleted item or folder mailbox event.</span></span>  <br/> |
|[<span data-ttu-id="e81cf-117">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="e81cf-117">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="e81cf-118">代表已删除文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="e81cf-118">Represents the identifier of the deleted folder.</span></span>  <br/> |
|[<span data-ttu-id="e81cf-119">ItemId</span><span class="sxs-lookup"><span data-stu-id="e81cf-119">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e81cf-120">代表已删除的项目的标识符。</span><span class="sxs-lookup"><span data-stu-id="e81cf-120">Represents the identifier of the deleted item.</span></span>  <br/> |
|[<span data-ttu-id="e81cf-121">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="e81cf-121">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="e81cf-122">代表已删除项的父文件夹或删除之前的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="e81cf-122">Represents the identifier of the parent folder of the deleted item or folder before deletion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e81cf-123">父元素</span><span class="sxs-lookup"><span data-stu-id="e81cf-123">Parent elements</span></span>

|<span data-ttu-id="e81cf-124">**元素**</span><span class="sxs-lookup"><span data-stu-id="e81cf-124">**Element**</span></span>|<span data-ttu-id="e81cf-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="e81cf-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e81cf-126">通知</span><span class="sxs-lookup"><span data-stu-id="e81cf-126">Notification</span></span>](notification-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e81cf-127">包含有关订阅和自上次通知以来发生的事件的信息。</span><span class="sxs-lookup"><span data-stu-id="e81cf-127">Contains information about the subscription and the events that have occurred since the last notification.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e81cf-128">备注</span><span class="sxs-lookup"><span data-stu-id="e81cf-128">Remarks</span></span>

<span data-ttu-id="e81cf-129">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e81cf-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e81cf-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="e81cf-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e81cf-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="e81cf-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e81cf-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="e81cf-132">Schema name</span></span>  <br/> |<span data-ttu-id="e81cf-133">类型架构</span><span class="sxs-lookup"><span data-stu-id="e81cf-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="e81cf-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="e81cf-134">Validation file</span></span>  <br/> |<span data-ttu-id="e81cf-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e81cf-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e81cf-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="e81cf-136">Can be empty</span></span>  <br/> |<span data-ttu-id="e81cf-137">False</span><span class="sxs-lookup"><span data-stu-id="e81cf-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e81cf-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e81cf-138">See also</span></span>

- [<span data-ttu-id="e81cf-139">订阅操作</span><span class="sxs-lookup"><span data-stu-id="e81cf-139">Subscribe operation</span></span>](subscribe-operation.md)  
- [<span data-ttu-id="e81cf-140">GetEvents 操作</span><span class="sxs-lookup"><span data-stu-id="e81cf-140">GetEvents operation</span></span>](getevents-operation.md)  
- [<span data-ttu-id="e81cf-141">取消操作</span><span class="sxs-lookup"><span data-stu-id="e81cf-141">Unsubscribe operation</span></span>](unsubscribe-operation.md)

