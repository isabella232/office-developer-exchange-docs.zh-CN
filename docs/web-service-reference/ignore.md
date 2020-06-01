---
title: 忽略
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Ignore
api_type:
- schema
ms.assetid: 7789eec5-ceec-43f2-84d5-d0d15b734076
description: Ignore 元素标识在同步过程中要跳过的项。
ms.openlocfilehash: b65d11d8c7655279dac0e7d3cbd13f8a9317540c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458570"
---
# <a name="ignore"></a><span data-ttu-id="3fc92-103">忽略</span><span class="sxs-lookup"><span data-stu-id="3fc92-103">Ignore</span></span>

<span data-ttu-id="3fc92-104">**Ignore**元素标识在同步过程中要跳过的项。</span><span class="sxs-lookup"><span data-stu-id="3fc92-104">The **Ignore** element identifies items to skip during synchronization.</span></span> 
  
[<span data-ttu-id="3fc92-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="3fc92-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="3fc92-106">忽略</span><span class="sxs-lookup"><span data-stu-id="3fc92-106">Ignore</span></span>](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 <span data-ttu-id="3fc92-107">**ArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="3fc92-107">**ArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3fc92-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3fc92-108">Attributes and elements</span></span>

<span data-ttu-id="3fc92-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3fc92-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3fc92-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="3fc92-110">Attributes</span></span>

<span data-ttu-id="3fc92-111">无。</span><span class="sxs-lookup"><span data-stu-id="3fc92-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3fc92-112">子元素</span><span class="sxs-lookup"><span data-stu-id="3fc92-112">Child elements</span></span>

|<span data-ttu-id="3fc92-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="3fc92-113">**Element**</span></span>|<span data-ttu-id="3fc92-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="3fc92-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fc92-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="3fc92-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="3fc92-116">包含 Exchange 存储中某项的唯一标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="3fc92-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3fc92-117">父元素</span><span class="sxs-lookup"><span data-stu-id="3fc92-117">Parent elements</span></span>

|<span data-ttu-id="3fc92-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="3fc92-118">**Element**</span></span>|<span data-ttu-id="3fc92-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="3fc92-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3fc92-120">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="3fc92-120">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="3fc92-121">定义对 Exchange 存储文件夹中的项目进行同步的请求。</span><span class="sxs-lookup"><span data-stu-id="3fc92-121">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3fc92-122">说明</span><span class="sxs-lookup"><span data-stu-id="3fc92-122">Remarks</span></span>

<span data-ttu-id="3fc92-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3fc92-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3fc92-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="3fc92-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fc92-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="3fc92-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3fc92-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="3fc92-126">Schema name</span></span>  <br/> |<span data-ttu-id="3fc92-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="3fc92-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3fc92-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="3fc92-128">Validation file</span></span>  <br/> |<span data-ttu-id="3fc92-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3fc92-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3fc92-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="3fc92-130">Can be empty</span></span>  <br/> |<span data-ttu-id="3fc92-131">False</span><span class="sxs-lookup"><span data-stu-id="3fc92-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fc92-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3fc92-132">See also</span></span>



[<span data-ttu-id="3fc92-133">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="3fc92-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="3fc92-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3fc92-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

