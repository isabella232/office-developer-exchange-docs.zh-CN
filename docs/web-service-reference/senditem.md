---
title: SendItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SendItem
api_type:
- schema
ms.assetid: a966da19-b05a-4504-ac98-91acc1667b9a
description: SendItem 元素是请求发送 Exchange 存储中的项中的根元素。
ms.openlocfilehash: c5ce52ee4643219aa31ae59e8b7d40d7a904c8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827340"
---
# <a name="senditem"></a><span data-ttu-id="a427a-103">SendItem</span><span class="sxs-lookup"><span data-stu-id="a427a-103">SendItem</span></span>

<span data-ttu-id="a427a-104">**SendItem**元素是请求发送 Exchange 存储中的项中的根元素。</span><span class="sxs-lookup"><span data-stu-id="a427a-104">The **SendItem** element is the root element in a request to send an item in the Exchange store.</span></span> 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 <span data-ttu-id="a427a-105">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="a427a-105">**SendItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a427a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a427a-106">Attributes and elements</span></span>

<span data-ttu-id="a427a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a427a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a427a-108">属性</span><span class="sxs-lookup"><span data-stu-id="a427a-108">Attributes</span></span>

|<span data-ttu-id="a427a-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="a427a-109">**Attribute**</span></span>|<span data-ttu-id="a427a-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="a427a-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a427a-111">**SaveItemToFolder**</span><span class="sxs-lookup"><span data-stu-id="a427a-111">**SaveItemToFolder**</span></span> <br/> |<span data-ttu-id="a427a-112">标识是否保存一份发送项目。</span><span class="sxs-lookup"><span data-stu-id="a427a-112">Identifies whether a copy of the sent item is saved.</span></span> <span data-ttu-id="a427a-113">保存操作取决于**SaveItemToFolder**和[SavedItemFolderId](saveditemfolderid.md)元素是否存在于请求中的值。</span><span class="sxs-lookup"><span data-stu-id="a427a-113">The save action depends on the value of **SaveItemToFolder** and whether a [SavedItemFolderId](saveditemfolderid.md) element is present in the request.</span></span> <span data-ttu-id="a427a-114">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="a427a-114">This element is required.</span></span>  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a><span data-ttu-id="a427a-115">SaveItemToFolder 属性</span><span class="sxs-lookup"><span data-stu-id="a427a-115">SaveItemToFolder Attribute</span></span>

|<span data-ttu-id="a427a-116">**值**</span><span class="sxs-lookup"><span data-stu-id="a427a-116">**Value**</span></span>|<span data-ttu-id="a427a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="a427a-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a427a-118">**true**</span><span class="sxs-lookup"><span data-stu-id="a427a-118">**true**</span></span> <br/> |<span data-ttu-id="a427a-119">如果不存在的[SavedItemFolderId](saveditemfolderid.md)元素，则在已发送邮件文件夹中保存项目。</span><span class="sxs-lookup"><span data-stu-id="a427a-119">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is saved in the Sent Items folder.</span></span> <span data-ttu-id="a427a-120">如果[SavedItemFolderId](saveditemfolderid.md)元素存在，由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中保存项目。</span><span class="sxs-lookup"><span data-stu-id="a427a-120">If the [SavedItemFolderId](saveditemfolderid.md) element is present, the item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="a427a-121">**false**</span><span class="sxs-lookup"><span data-stu-id="a427a-121">**false**</span></span> <br/> |<span data-ttu-id="a427a-122">如果[SavedItemFolderId](saveditemfolderid.md)元素不存在，则不会保存项目。</span><span class="sxs-lookup"><span data-stu-id="a427a-122">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is not saved.</span></span> <span data-ttu-id="a427a-123">如果[SavedItemFolderId](saveditemfolderid.md)元素存在，将返回错误响应与[ResponseCode](responsecode.md)元素包含**ErrorInvalidSendItemSaveSettings**值。</span><span class="sxs-lookup"><span data-stu-id="a427a-123">If the [SavedItemFolderId](saveditemfolderid.md) element is present, an error response will be returned with a [ResponseCode](responsecode.md) element that contains the **ErrorInvalidSendItemSaveSettings** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a427a-124">子元素</span><span class="sxs-lookup"><span data-stu-id="a427a-124">Child elements</span></span>

|<span data-ttu-id="a427a-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="a427a-125">**Element**</span></span>|<span data-ttu-id="a427a-126">**说明**</span><span class="sxs-lookup"><span data-stu-id="a427a-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a427a-127">ItemIds</span><span class="sxs-lookup"><span data-stu-id="a427a-127">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="a427a-128">包含唯一标识的项目和匹配项，用于删除、 发送、 获取、 移动或在 Exchange 存储中复制项的定期主项目。</span><span class="sxs-lookup"><span data-stu-id="a427a-128">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a427a-129">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="a427a-129">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="a427a-130">标识用于更新、 发送和在 Exchange 存储中创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="a427a-130">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a427a-131">父元素</span><span class="sxs-lookup"><span data-stu-id="a427a-131">Parent elements</span></span>

<span data-ttu-id="a427a-132">无。</span><span class="sxs-lookup"><span data-stu-id="a427a-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a427a-133">注解</span><span class="sxs-lookup"><span data-stu-id="a427a-133">Remarks</span></span>

<span data-ttu-id="a427a-134">如果发送发送邮件文件夹中的项目，删除发送的项目并将它的一个副本置于发送邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="a427a-134">If an item in the Sent Items folder is sent, the sent item is deleted and a copy of it is put in the Sent Items folder.</span></span>
  
<span data-ttu-id="a427a-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a427a-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a427a-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="a427a-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a427a-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="a427a-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a427a-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="a427a-138">Schema Name</span></span>  <br/> |<span data-ttu-id="a427a-139">消息架构</span><span class="sxs-lookup"><span data-stu-id="a427a-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a427a-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="a427a-140">Validation File</span></span>  <br/> |<span data-ttu-id="a427a-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a427a-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a427a-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="a427a-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="a427a-143">False</span><span class="sxs-lookup"><span data-stu-id="a427a-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a427a-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a427a-144">See also</span></span>



[<span data-ttu-id="a427a-145">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="a427a-145">SendItem operation</span></span>](senditem-operation.md)

