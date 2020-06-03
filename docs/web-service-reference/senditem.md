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
description: SendItem 元素是在 Exchange 存储中发送项目的请求中的根元素。
ms.openlocfilehash: 28f0d484dd079146c998cb7317bd2d80c6739e19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530563"
---
# <a name="senditem"></a><span data-ttu-id="f8cad-103">SendItem</span><span class="sxs-lookup"><span data-stu-id="f8cad-103">SendItem</span></span>

<span data-ttu-id="f8cad-104">**SendItem**元素是在 Exchange 存储中发送项目的请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="f8cad-104">The **SendItem** element is the root element in a request to send an item in the Exchange store.</span></span> 
  
```xml
<SendItem SaveItemToFolder="">
   <ItemIds/>
   <SavedItemFolderId/>
</SendItem>
```

 <span data-ttu-id="f8cad-105">**SendItemType**</span><span class="sxs-lookup"><span data-stu-id="f8cad-105">**SendItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8cad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f8cad-106">Attributes and elements</span></span>

<span data-ttu-id="f8cad-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f8cad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8cad-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f8cad-108">Attributes</span></span>

|<span data-ttu-id="f8cad-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="f8cad-109">**Attribute**</span></span>|<span data-ttu-id="f8cad-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8cad-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8cad-111">**SaveItemToFolder**</span><span class="sxs-lookup"><span data-stu-id="f8cad-111">**SaveItemToFolder**</span></span> <br/> |<span data-ttu-id="f8cad-112">标识是否保存已发送项目的副本。</span><span class="sxs-lookup"><span data-stu-id="f8cad-112">Identifies whether a copy of the sent item is saved.</span></span> <span data-ttu-id="f8cad-113">Save 操作取决于**SaveItemToFolder**的值，以及请求中是否存在[SavedItemFolderId](saveditemfolderid.md)元素。</span><span class="sxs-lookup"><span data-stu-id="f8cad-113">The save action depends on the value of **SaveItemToFolder** and whether a [SavedItemFolderId](saveditemfolderid.md) element is present in the request.</span></span> <span data-ttu-id="f8cad-114">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="f8cad-114">This element is required.</span></span>  <br/> |
   
#### <a name="saveitemtofolder-attribute"></a><span data-ttu-id="f8cad-115">SaveItemToFolder 属性</span><span class="sxs-lookup"><span data-stu-id="f8cad-115">SaveItemToFolder Attribute</span></span>

|<span data-ttu-id="f8cad-116">**值**</span><span class="sxs-lookup"><span data-stu-id="f8cad-116">**Value**</span></span>|<span data-ttu-id="f8cad-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8cad-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8cad-118">**true**</span><span class="sxs-lookup"><span data-stu-id="f8cad-118">**true**</span></span> <br/> |<span data-ttu-id="f8cad-119">如果[SavedItemFolderId](saveditemfolderid.md)元素不存在，则会将该项目保存在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="f8cad-119">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is saved in the Sent Items folder.</span></span> <span data-ttu-id="f8cad-120">如果存在[SavedItemFolderId](saveditemfolderid.md)元素，则会将该项目保存在由[SavedItemFolderId](saveditemfolderid.md)元素指定的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="f8cad-120">If the [SavedItemFolderId](saveditemfolderid.md) element is present, the item is saved in the folder that is specified by the [SavedItemFolderId](saveditemfolderid.md) element.</span></span>  <br/> |
|<span data-ttu-id="f8cad-121">**该值**</span><span class="sxs-lookup"><span data-stu-id="f8cad-121">**false**</span></span> <br/> |<span data-ttu-id="f8cad-122">如果不存在[SavedItemFolderId](saveditemfolderid.md)元素，则不会保存项目。</span><span class="sxs-lookup"><span data-stu-id="f8cad-122">If the [SavedItemFolderId](saveditemfolderid.md) element is not present, the item is not saved.</span></span> <span data-ttu-id="f8cad-123">如果存在[SavedItemFolderId](saveditemfolderid.md)元素，则将返回一个包含**ErrorInvalidSendItemSaveSettings**值的[ResponseCode](responsecode.md)元素的错误响应。</span><span class="sxs-lookup"><span data-stu-id="f8cad-123">If the [SavedItemFolderId](saveditemfolderid.md) element is present, an error response will be returned with a [ResponseCode](responsecode.md) element that contains the **ErrorInvalidSendItemSaveSettings** value.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f8cad-124">子元素</span><span class="sxs-lookup"><span data-stu-id="f8cad-124">Child elements</span></span>

|<span data-ttu-id="f8cad-125">**元素**</span><span class="sxs-lookup"><span data-stu-id="f8cad-125">**Element**</span></span>|<span data-ttu-id="f8cad-126">**描述**</span><span class="sxs-lookup"><span data-stu-id="f8cad-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8cad-127">ItemIds</span><span class="sxs-lookup"><span data-stu-id="f8cad-127">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="f8cad-128">包含项目、具体值项目和定期主项目的唯一标识，这些标识用于删除、发送、获取、移动或复制 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="f8cad-128">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="f8cad-129">SavedItemFolderId</span><span class="sxs-lookup"><span data-stu-id="f8cad-129">SavedItemFolderId</span></span>](saveditemfolderid.md) <br/> |<span data-ttu-id="f8cad-130">标识在 Exchange 存储中更新、发送和创建项目的操作的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="f8cad-130">Identifies the target folder for operations that update, send, and create items in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8cad-131">父元素</span><span class="sxs-lookup"><span data-stu-id="f8cad-131">Parent elements</span></span>

<span data-ttu-id="f8cad-132">无。</span><span class="sxs-lookup"><span data-stu-id="f8cad-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8cad-133">说明</span><span class="sxs-lookup"><span data-stu-id="f8cad-133">Remarks</span></span>

<span data-ttu-id="f8cad-134">如果发送了 "已发送邮件" 文件夹中的项目，则会删除已发送邮件，并将其副本放在 "已发送邮件" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="f8cad-134">If an item in the Sent Items folder is sent, the sent item is deleted and a copy of it is put in the Sent Items folder.</span></span>
  
<span data-ttu-id="f8cad-135">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f8cad-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8cad-136">元素信息</span><span class="sxs-lookup"><span data-stu-id="f8cad-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8cad-137">命名空间</span><span class="sxs-lookup"><span data-stu-id="f8cad-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f8cad-138">架构名称</span><span class="sxs-lookup"><span data-stu-id="f8cad-138">Schema Name</span></span>  <br/> |<span data-ttu-id="f8cad-139">消息架构</span><span class="sxs-lookup"><span data-stu-id="f8cad-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f8cad-140">验证文件</span><span class="sxs-lookup"><span data-stu-id="f8cad-140">Validation File</span></span>  <br/> |<span data-ttu-id="f8cad-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f8cad-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f8cad-142">可以为空</span><span class="sxs-lookup"><span data-stu-id="f8cad-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="f8cad-143">False</span><span class="sxs-lookup"><span data-stu-id="f8cad-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8cad-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8cad-144">See also</span></span>



[<span data-ttu-id="f8cad-145">SendItem 操作</span><span class="sxs-lookup"><span data-stu-id="f8cad-145">SendItem operation</span></span>](senditem-operation.md)

