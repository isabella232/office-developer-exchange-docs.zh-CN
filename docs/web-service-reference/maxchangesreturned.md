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
description: MaxChangesReturned 元素介绍可以同步响应中返回的更改的最大数量。
ms.openlocfilehash: c3719b12b7e3e2f83a9454c7b68432b375d78614
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826395"
---
# <a name="maxchangesreturned"></a><span data-ttu-id="c2bf0-103">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="c2bf0-103">MaxChangesReturned</span></span>

<span data-ttu-id="c2bf0-104">**MaxChangesReturned**元素介绍可以同步响应中返回的更改的最大数量。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-104">The **MaxChangesReturned** element describes the maximum number of changes that can be returned in a synchronization response.</span></span> 
  
[<span data-ttu-id="c2bf0-105">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="c2bf0-105">SyncFolderItems</span></span>](syncfolderitems.md)
  
[<span data-ttu-id="c2bf0-106">MaxChangesReturned</span><span class="sxs-lookup"><span data-stu-id="c2bf0-106">MaxChangesReturned</span></span>](maxchangesreturned.md)
  
```xml
<MaxChangesReturned/>
```

 <span data-ttu-id="c2bf0-107">**int**</span><span class="sxs-lookup"><span data-stu-id="c2bf0-107">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c2bf0-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c2bf0-108">Attributes and elements</span></span>

<span data-ttu-id="c2bf0-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c2bf0-110">属性</span><span class="sxs-lookup"><span data-stu-id="c2bf0-110">Attributes</span></span>

<span data-ttu-id="c2bf0-111">无。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c2bf0-112">子元素</span><span class="sxs-lookup"><span data-stu-id="c2bf0-112">Child elements</span></span>

<span data-ttu-id="c2bf0-113">无。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c2bf0-114">父元素</span><span class="sxs-lookup"><span data-stu-id="c2bf0-114">Parent elements</span></span>

|<span data-ttu-id="c2bf0-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="c2bf0-115">**Element**</span></span>|<span data-ttu-id="c2bf0-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="c2bf0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c2bf0-117">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="c2bf0-117">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="c2bf0-118">定义同步 Exchange 存储区文件夹中的项目的请求。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-118">Defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c2bf0-119">文本值</span><span class="sxs-lookup"><span data-stu-id="c2bf0-119">Text value</span></span>

<span data-ttu-id="c2bf0-120">文本值表示一个整数，描述单个同步呼叫中返回的项的最大数目。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-120">The text value represents an integer that describes the maximum number of items that are returned in a single synchronization call.</span></span> <span data-ttu-id="c2bf0-121">值必须是介于 1 和 512，非独占之间。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-121">The value must be between 1 and 512, inclusive.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c2bf0-122">备注</span><span class="sxs-lookup"><span data-stu-id="c2bf0-122">Remarks</span></span>

<span data-ttu-id="c2bf0-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c2bf0-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c2bf0-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="c2bf0-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c2bf0-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="c2bf0-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c2bf0-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="c2bf0-126">Schema name</span></span>  <br/> |<span data-ttu-id="c2bf0-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="c2bf0-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="c2bf0-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="c2bf0-128">Validation file</span></span>  <br/> |<span data-ttu-id="c2bf0-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c2bf0-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c2bf0-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="c2bf0-130">Can be empty</span></span>  <br/> |<span data-ttu-id="c2bf0-131">False</span><span class="sxs-lookup"><span data-stu-id="c2bf0-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c2bf0-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c2bf0-132">See also</span></span>



[<span data-ttu-id="c2bf0-133">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="c2bf0-133">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="c2bf0-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c2bf0-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

