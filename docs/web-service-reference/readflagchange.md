---
title: ReadFlagChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ReadFlagChange
api_type:
- schema
ms.assetid: 527bfe90-63d0-4b2f-97f7-7875b3a516b2
description: ReadFlagChange 元素中 SyncFolderItems 操作响应时返回的项目具有读取。 此属性是只读的。
ms.openlocfilehash: 28ef0267e8308ba58057bec01ab2672a19ee94a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826953"
---
# <a name="readflagchange"></a><span data-ttu-id="0bef2-104">ReadFlagChange</span><span class="sxs-lookup"><span data-stu-id="0bef2-104">ReadFlagChange</span></span>

<span data-ttu-id="0bef2-105">读取项目后，将在[SyncFolderItems 操作](syncfolderitems-operation.md)响应中返回**ReadFlagChange**元素。</span><span class="sxs-lookup"><span data-stu-id="0bef2-105">The **ReadFlagChange** element is returned in [SyncFolderItems operation](syncfolderitems-operation.md) responses when an item has been read.</span></span> <span data-ttu-id="0bef2-106">此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="0bef2-106">This property is read-only.</span></span> 
  
```xml
<ReadFlagChange>
   <ItemId/>
   <IsRead/>
</ReadFlagChange>
```

 <span data-ttu-id="0bef2-107">**SyncFolderItemsReadFlagType**</span><span class="sxs-lookup"><span data-stu-id="0bef2-107">**SyncFolderItemsReadFlagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0bef2-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0bef2-108">Attributes and elements</span></span>

<span data-ttu-id="0bef2-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0bef2-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0bef2-110">属性</span><span class="sxs-lookup"><span data-stu-id="0bef2-110">Attributes</span></span>

<span data-ttu-id="0bef2-111">无。</span><span class="sxs-lookup"><span data-stu-id="0bef2-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0bef2-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0bef2-112">Child elements</span></span>

|<span data-ttu-id="0bef2-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0bef2-113">**Element**</span></span>|<span data-ttu-id="0bef2-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0bef2-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0bef2-115">ItemId</span><span class="sxs-lookup"><span data-stu-id="0bef2-115">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="0bef2-116">标识已为其更改读取标志的项。</span><span class="sxs-lookup"><span data-stu-id="0bef2-116">Identifies the item for which the read-flag has been changed.</span></span>  <br/> |
|[<span data-ttu-id="0bef2-117">IsRead</span><span class="sxs-lookup"><span data-stu-id="0bef2-117">IsRead</span></span>](isread.md) <br/> |<span data-ttu-id="0bef2-118">指示是否已将读取标志设置为**true**。</span><span class="sxs-lookup"><span data-stu-id="0bef2-118">Indicates whether the read-flag has been set to **true**.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0bef2-119">父元素</span><span class="sxs-lookup"><span data-stu-id="0bef2-119">Parent elements</span></span>

|<span data-ttu-id="0bef2-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="0bef2-120">**Element**</span></span>|<span data-ttu-id="0bef2-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="0bef2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0bef2-122">更改 （项）</span><span class="sxs-lookup"><span data-stu-id="0bef2-122">Changes (Items)</span></span>](changes-items.md) <br/> |<span data-ttu-id="0bef2-123">包含表示客户端上的项目和 Exchange 服务器上的项目之间的差异的类型的更改类型序列数组。</span><span class="sxs-lookup"><span data-stu-id="0bef2-123">Contains a sequence array of change types that represent the types of differences between the items on the client and the items on the Exchange server.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bef2-124">注解</span><span class="sxs-lookup"><span data-stu-id="0bef2-124">Remarks</span></span>

<span data-ttu-id="0bef2-125">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0bef2-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0bef2-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="0bef2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0bef2-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="0bef2-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0bef2-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="0bef2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0bef2-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="0bef2-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="0bef2-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="0bef2-130">Validation File</span></span>  <br/> |<span data-ttu-id="0bef2-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0bef2-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0bef2-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="0bef2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0bef2-133">False</span><span class="sxs-lookup"><span data-stu-id="0bef2-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0bef2-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0bef2-134">See also</span></span>



- [<span data-ttu-id="0bef2-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0bef2-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

