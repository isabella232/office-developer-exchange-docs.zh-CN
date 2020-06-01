---
title: MaxChangesReturned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxChangesReturned
api_type:
- schema
ms.assetid: f471db84-a666-4dfa-9993-8ca9113a0384
description: MaxChangesReturned 元素描述同步响应中可返回的最大更改数。
ms.openlocfilehash: caf96b6e95f2e63d0e544ead26fbea18cd637861
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460083"
---
# <a name="maxchangesreturned"></a><span data-ttu-id="18f42-103">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="18f42-103">MaxChangesReturned</span></span>

<span data-ttu-id="18f42-104">**MaxChangesReturned**元素描述同步响应中可返回的最大更改数。</span><span class="sxs-lookup"><span data-stu-id="18f42-104">The **MaxChangesReturned** element describes the maximum number of changes that can be returned in a synchronization response.</span></span> 
  
[<span data-ttu-id="18f42-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="18f42-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="18f42-106">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="18f42-106">MaxChangesReturned</span></span>](maxchangesreturned.md)
  
```xml
<MaxChangesReturned/>
```

 <span data-ttu-id="18f42-107">**int**</span><span class="sxs-lookup"><span data-stu-id="18f42-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="18f42-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="18f42-108">Attributes and elements</span></span>

<span data-ttu-id="18f42-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="18f42-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18f42-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="18f42-110">Attributes</span></span>

<span data-ttu-id="18f42-111">无。</span><span class="sxs-lookup"><span data-stu-id="18f42-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="18f42-112">子元素</span><span class="sxs-lookup"><span data-stu-id="18f42-112">Child elements</span></span>

<span data-ttu-id="18f42-113">无。</span><span class="sxs-lookup"><span data-stu-id="18f42-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="18f42-114">父元素</span><span class="sxs-lookup"><span data-stu-id="18f42-114">Parent elements</span></span>

|<span data-ttu-id="18f42-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="18f42-115">**Element**</span></span>|<span data-ttu-id="18f42-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="18f42-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="18f42-117">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="18f42-117">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="18f42-118">定义对 Exchange 存储文件夹中的项目进行同步的请求。</span><span class="sxs-lookup"><span data-stu-id="18f42-118">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="18f42-119">文本值</span><span class="sxs-lookup"><span data-stu-id="18f42-119">Text value</span></span>

<span data-ttu-id="18f42-120">该文本值表示一个整数，该整数描述在单个同步调用中返回的最大项目数。</span><span class="sxs-lookup"><span data-stu-id="18f42-120">The text value represents an integer that describes the maximum number of items that are returned in a single synchronization call.</span></span> <span data-ttu-id="18f42-121">该值必须介于1和512之间（含这两个值）。</span><span class="sxs-lookup"><span data-stu-id="18f42-121">The value must be between 1 and 512, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18f42-122">说明</span><span class="sxs-lookup"><span data-stu-id="18f42-122">Remarks</span></span>

<span data-ttu-id="18f42-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="18f42-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18f42-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="18f42-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18f42-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="18f42-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="18f42-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="18f42-126">Schema name</span></span>  <br/> |<span data-ttu-id="18f42-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="18f42-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="18f42-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="18f42-128">Validation file</span></span>  <br/> |<span data-ttu-id="18f42-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="18f42-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="18f42-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="18f42-130">Can be empty</span></span>  <br/> |<span data-ttu-id="18f42-131">False</span><span class="sxs-lookup"><span data-stu-id="18f42-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18f42-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="18f42-132">See also</span></span>



[<span data-ttu-id="18f42-133">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="18f42-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="18f42-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="18f42-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

