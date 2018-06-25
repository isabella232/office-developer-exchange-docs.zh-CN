---
title: IncludesLastItemInRange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludesLastItemInRange
api_type:
- schema
ms.assetid: e7d6c7d3-548e-48b0-a313-bfef81e4832a
description: IncludesLastItemInRange 元素指示响应中是否包括要同步的最后一项。
ms.openlocfilehash: b4786c5aa81e9b4fee98e7ed4238215ff327443e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825906"
---
# <a name="includeslastiteminrange"></a><span data-ttu-id="5ba02-103">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="5ba02-103">IncludesLastItemInRange</span></span>

<span data-ttu-id="5ba02-104">**IncludesLastItemInRange**元素指示响应中是否包括要同步的最后一项。</span><span class="sxs-lookup"><span data-stu-id="5ba02-104">The **IncludesLastItemInRange** element indicates whether the last item to synchronize has been included in the response.</span></span> 
  
[<span data-ttu-id="5ba02-105">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="5ba02-105">SyncFolderItemsResponse</span></span>](syncfolderitemsresponse.md)
  
[<span data-ttu-id="5ba02-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5ba02-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="5ba02-107">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5ba02-107">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md)
  
[<span data-ttu-id="5ba02-108">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="5ba02-108">IncludesLastItemInRange</span></span>](includeslastiteminrange.md)
  
```xml
<IncludesLastItemInRange/>
```

 <span data-ttu-id="5ba02-109">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ba02-109">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5ba02-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5ba02-110">Attributes and elements</span></span>

<span data-ttu-id="5ba02-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5ba02-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ba02-112">属性</span><span class="sxs-lookup"><span data-stu-id="5ba02-112">Attributes</span></span>

<span data-ttu-id="5ba02-113">无。</span><span class="sxs-lookup"><span data-stu-id="5ba02-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5ba02-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5ba02-114">Child elements</span></span>

<span data-ttu-id="5ba02-115">无。</span><span class="sxs-lookup"><span data-stu-id="5ba02-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5ba02-116">父元素</span><span class="sxs-lookup"><span data-stu-id="5ba02-116">Parent elements</span></span>

|<span data-ttu-id="5ba02-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="5ba02-117">**Element**</span></span>|<span data-ttu-id="5ba02-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="5ba02-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ba02-119">SyncFolderItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5ba02-119">SyncFolderItemsResponseMessage</span></span>](syncfolderitemsresponsemessage.md) <br/> |<span data-ttu-id="5ba02-120">包含状态和 SyncFolderItems 请求的结果。</span><span class="sxs-lookup"><span data-stu-id="5ba02-120">Contains the status and result of a SyncFolderItems request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5ba02-121">文本值</span><span class="sxs-lookup"><span data-stu-id="5ba02-121">Text value</span></span>

<span data-ttu-id="5ba02-122">表示一个布尔值的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="5ba02-122">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ba02-123">备注</span><span class="sxs-lookup"><span data-stu-id="5ba02-123">Remarks</span></span>

<span data-ttu-id="5ba02-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5ba02-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ba02-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="5ba02-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ba02-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="5ba02-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5ba02-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="5ba02-127">Schema name</span></span>  <br/> |<span data-ttu-id="5ba02-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="5ba02-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5ba02-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="5ba02-129">Validation file</span></span>  <br/> |<span data-ttu-id="5ba02-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5ba02-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5ba02-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="5ba02-131">Can be empty</span></span>  <br/> |<span data-ttu-id="5ba02-132">False</span><span class="sxs-lookup"><span data-stu-id="5ba02-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ba02-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5ba02-133">See also</span></span>



[<span data-ttu-id="5ba02-134">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="5ba02-134">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="5ba02-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5ba02-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

