---
title: GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: 769df8eb-9c72-48b5-a49f-82c6b86bc5fc
description: GetItem 元素定义一个请求以获取从 Exchange 存储中的邮箱项目。
ms.openlocfilehash: 39db141bad62c34bec5ae6a937ba94c2d1288090
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754606"
---
# <a name="getitem"></a><span data-ttu-id="65e3d-103">GetItem</span><span class="sxs-lookup"><span data-stu-id="65e3d-103">GetItem</span></span>

<span data-ttu-id="65e3d-104">**GetItem**元素定义一个请求以获取从 Exchange 存储中的邮箱项目。</span><span class="sxs-lookup"><span data-stu-id="65e3d-104">The **GetItem** element defines a request to get an item from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 <span data-ttu-id="65e3d-105">**GetItemType**</span><span class="sxs-lookup"><span data-stu-id="65e3d-105">**GetItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="65e3d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="65e3d-106">Attributes and elements</span></span>

<span data-ttu-id="65e3d-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="65e3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="65e3d-108">属性</span><span class="sxs-lookup"><span data-stu-id="65e3d-108">Attributes</span></span>

<span data-ttu-id="65e3d-109">无。</span><span class="sxs-lookup"><span data-stu-id="65e3d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="65e3d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="65e3d-110">Child elements</span></span>

|<span data-ttu-id="65e3d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="65e3d-111">**Element**</span></span>|<span data-ttu-id="65e3d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="65e3d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="65e3d-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="65e3d-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="65e3d-114">标识项目属性和**GetItem**响应中包括的内容。</span><span class="sxs-lookup"><span data-stu-id="65e3d-114">Identifies the item properties and content to include in a **GetItem** response.</span></span>  <br/> |
|[<span data-ttu-id="65e3d-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="65e3d-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="65e3d-116">包含唯一标识的项目和匹配项，用于从 Exchange 存储中获取项的定期主项目。</span><span class="sxs-lookup"><span data-stu-id="65e3d-116">Contains the unique identities of items, occurrence items, and recurring master items that are used to get items from the Exchange store.</span></span> <span data-ttu-id="65e3d-117">这些项表示联系人、 任务、 邮件、 日历项、 会议请求和邮箱中的其他有效项。</span><span class="sxs-lookup"><span data-stu-id="65e3d-117">These items represent contacts, tasks, messages, calendar items, meeting requests, and other valid items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="65e3d-118">父元素</span><span class="sxs-lookup"><span data-stu-id="65e3d-118">Parent elements</span></span>

<span data-ttu-id="65e3d-119">无。</span><span class="sxs-lookup"><span data-stu-id="65e3d-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65e3d-120">备注</span><span class="sxs-lookup"><span data-stu-id="65e3d-120">Remarks</span></span>

<span data-ttu-id="65e3d-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="65e3d-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="65e3d-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="65e3d-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65e3d-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="65e3d-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="65e3d-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="65e3d-124">Schema Name</span></span>  <br/> |<span data-ttu-id="65e3d-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="65e3d-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="65e3d-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="65e3d-126">Validation File</span></span>  <br/> |<span data-ttu-id="65e3d-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="65e3d-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="65e3d-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="65e3d-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="65e3d-129">False</span><span class="sxs-lookup"><span data-stu-id="65e3d-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="65e3d-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="65e3d-130">See also</span></span>



[<span data-ttu-id="65e3d-131">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="65e3d-131">GetItem operation</span></span>](getitem-operation.md)

