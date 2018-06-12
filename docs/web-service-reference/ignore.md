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
description: 忽略元素标识同步过程中跳过的项目。
ms.openlocfilehash: 0ecff9bfeb1257552b7e52c0115e9e814edecd4b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825858"
---
# <a name="ignore"></a><span data-ttu-id="e0779-103">忽略</span><span class="sxs-lookup"><span data-stu-id="e0779-103">Ignore</span></span>

<span data-ttu-id="e0779-104">**忽略**元素标识同步过程中跳过的项目。</span><span class="sxs-lookup"><span data-stu-id="e0779-104">The **Ignore** element identifies items to skip during synchronization.</span></span> 
  
[<span data-ttu-id="e0779-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e0779-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="e0779-106">忽略</span><span class="sxs-lookup"><span data-stu-id="e0779-106">Ignore</span></span>](ignore.md)
  
```xml
<Ignore>
   <ItemId/>
</Ignore>
```

 <span data-ttu-id="e0779-107">**ArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="e0779-107">**ArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0779-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e0779-108">Attributes and elements</span></span>

<span data-ttu-id="e0779-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e0779-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0779-110">属性</span><span class="sxs-lookup"><span data-stu-id="e0779-110">Attributes</span></span>

<span data-ttu-id="e0779-111">无。</span><span class="sxs-lookup"><span data-stu-id="e0779-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0779-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e0779-112">Child elements</span></span>

|<span data-ttu-id="e0779-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e0779-113">**Element**</span></span>|<span data-ttu-id="e0779-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e0779-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0779-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="e0779-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="e0779-116">包含在 Exchange 存储中的项目的唯一标识符和更改的键。</span><span class="sxs-lookup"><span data-stu-id="e0779-116">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0779-117">父元素</span><span class="sxs-lookup"><span data-stu-id="e0779-117">Parent elements</span></span>

|<span data-ttu-id="e0779-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="e0779-118">**Element**</span></span>|<span data-ttu-id="e0779-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="e0779-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0779-120">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="e0779-120">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="e0779-121">定义同步 Exchange 存储区文件夹中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="e0779-121">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0779-122">备注</span><span class="sxs-lookup"><span data-stu-id="e0779-122">Remarks</span></span>

<span data-ttu-id="e0779-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e0779-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e0779-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="e0779-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0779-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="e0779-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e0779-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="e0779-126">Schema name</span></span>  <br/> |<span data-ttu-id="e0779-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="e0779-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e0779-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="e0779-128">Validation file</span></span>  <br/> |<span data-ttu-id="e0779-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e0779-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e0779-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="e0779-130">Can be empty</span></span>  <br/> |<span data-ttu-id="e0779-131">False</span><span class="sxs-lookup"><span data-stu-id="e0779-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0779-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e0779-132">See also</span></span>



[<span data-ttu-id="e0779-133">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="e0779-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="e0779-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e0779-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

