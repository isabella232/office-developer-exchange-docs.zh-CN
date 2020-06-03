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
description: GetItem 元素定义一个请求，以从 Exchange 存储中的邮箱获取项目。
ms.openlocfilehash: a02403ee84195a41387d5dbe1785ae6d12b47da5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458696"
---
# <a name="getitem"></a><span data-ttu-id="aa253-103">GetItem</span><span class="sxs-lookup"><span data-stu-id="aa253-103">GetItem</span></span>

<span data-ttu-id="aa253-104">**GetItem**元素定义一个请求，以从 Exchange 存储中的邮箱获取项目。</span><span class="sxs-lookup"><span data-stu-id="aa253-104">The **GetItem** element defines a request to get an item from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetItem>
   <ItemShape/>
   <ItemIds/>
</GetItem>
```

 <span data-ttu-id="aa253-105">**GetItemType**</span><span class="sxs-lookup"><span data-stu-id="aa253-105">**GetItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa253-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa253-106">Attributes and elements</span></span>

<span data-ttu-id="aa253-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa253-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa253-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="aa253-108">Attributes</span></span>

<span data-ttu-id="aa253-109">无。</span><span class="sxs-lookup"><span data-stu-id="aa253-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa253-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aa253-110">Child elements</span></span>

|<span data-ttu-id="aa253-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa253-111">**Element**</span></span>|<span data-ttu-id="aa253-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa253-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa253-113">ItemShape</span><span class="sxs-lookup"><span data-stu-id="aa253-113">ItemShape</span></span>](itemshape.md) <br/> |<span data-ttu-id="aa253-114">标识要包含在**GetItem**响应中的项目属性和内容。</span><span class="sxs-lookup"><span data-stu-id="aa253-114">Identifies the item properties and content to include in a **GetItem** response.</span></span>  <br/> |
|[<span data-ttu-id="aa253-115">ItemIds</span><span class="sxs-lookup"><span data-stu-id="aa253-115">ItemIds</span></span>](itemids.md) <br/> |<span data-ttu-id="aa253-116">包含项目、具体值项目和用于从 Exchange 存储中获取项目的定期主项目的唯一标识。</span><span class="sxs-lookup"><span data-stu-id="aa253-116">Contains the unique identities of items, occurrence items, and recurring master items that are used to get items from the Exchange store.</span></span> <span data-ttu-id="aa253-117">这些项表示邮箱中的联系人、任务、邮件、日历项目、会议请求和其他有效项目。</span><span class="sxs-lookup"><span data-stu-id="aa253-117">These items represent contacts, tasks, messages, calendar items, meeting requests, and other valid items in a mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa253-118">父元素</span><span class="sxs-lookup"><span data-stu-id="aa253-118">Parent elements</span></span>

<span data-ttu-id="aa253-119">无。</span><span class="sxs-lookup"><span data-stu-id="aa253-119">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aa253-120">说明</span><span class="sxs-lookup"><span data-stu-id="aa253-120">Remarks</span></span>

<span data-ttu-id="aa253-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="aa253-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa253-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa253-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa253-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa253-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa253-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa253-124">Schema Name</span></span>  <br/> |<span data-ttu-id="aa253-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="aa253-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="aa253-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa253-126">Validation File</span></span>  <br/> |<span data-ttu-id="aa253-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aa253-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa253-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa253-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa253-129">False</span><span class="sxs-lookup"><span data-stu-id="aa253-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa253-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa253-130">See also</span></span>



[<span data-ttu-id="aa253-131">GetItem 操作</span><span class="sxs-lookup"><span data-stu-id="aa253-131">GetItem operation</span></span>](getitem-operation.md)

