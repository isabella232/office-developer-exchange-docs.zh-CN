---
title: SyncScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: SyncScope 元素指定是否仅在同步响应中返回项目或项目和文件夹相关信息。
ms.openlocfilehash: 5ede26204c823a452189222075c784f24e98d188
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463032"
---
# <a name="syncscope"></a><span data-ttu-id="76347-103">SyncScope</span><span class="sxs-lookup"><span data-stu-id="76347-103">SyncScope</span></span>

<span data-ttu-id="76347-104">**SyncScope**元素指定是否仅在同步响应中返回项目或项目和文件夹相关信息。</span><span class="sxs-lookup"><span data-stu-id="76347-104">The **SyncScope** element specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 <span data-ttu-id="76347-105">**SyncFolderItemsScopeType**</span><span class="sxs-lookup"><span data-stu-id="76347-105">**SyncFolderItemsScopeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76347-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="76347-106">Attributes and elements</span></span>

<span data-ttu-id="76347-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="76347-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76347-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="76347-108">Attributes</span></span>

<span data-ttu-id="76347-109">无。</span><span class="sxs-lookup"><span data-stu-id="76347-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76347-110">子元素</span><span class="sxs-lookup"><span data-stu-id="76347-110">Child elements</span></span>

<span data-ttu-id="76347-111">无。</span><span class="sxs-lookup"><span data-stu-id="76347-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="76347-112">父元素</span><span class="sxs-lookup"><span data-stu-id="76347-112">Parent elements</span></span>

|<span data-ttu-id="76347-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="76347-113">**Element**</span></span>|<span data-ttu-id="76347-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="76347-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76347-115">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="76347-115">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="76347-116">定义对 Exchange 存储文件夹中的项目的同步的请求的元素。</span><span class="sxs-lookup"><span data-stu-id="76347-116">The element that defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="76347-117">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="76347-117">The following is the XPath expression to this element:</span></span>  <br/> <span data-ttu-id="76347-118">/SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="76347-118">/SyncFolderItems</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="76347-119">文本值</span><span class="sxs-lookup"><span data-stu-id="76347-119">Text value</span></span>

<span data-ttu-id="76347-120">下表列出了**SyncScope**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="76347-120">The following table lists the possible values for the **SyncScope** element.</span></span> 
  
<span data-ttu-id="76347-121">**SyncScope 元素值**</span><span class="sxs-lookup"><span data-stu-id="76347-121">**SyncScope element values**</span></span>

|<span data-ttu-id="76347-122">**值**</span><span class="sxs-lookup"><span data-stu-id="76347-122">**Value**</span></span>|<span data-ttu-id="76347-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="76347-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="76347-124">NormalItems</span><span class="sxs-lookup"><span data-stu-id="76347-124">NormalItems</span></span>  <br/> |<span data-ttu-id="76347-125">指定在同步响应中仅返回文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="76347-125">Specifies that only items in the folder are returned in a synchronization response.</span></span>  <br/> |
|<span data-ttu-id="76347-126">NormalAndAssociatedItems</span><span class="sxs-lookup"><span data-stu-id="76347-126">NormalAndAssociatedItems</span></span>  <br/> |<span data-ttu-id="76347-127">指定在同步响应中返回与文件夹和文件夹相关联的信息中的两个项目。</span><span class="sxs-lookup"><span data-stu-id="76347-127">Specifies that both items in the folder and folder associated information are returned in a synchronization response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76347-128">备注</span><span class="sxs-lookup"><span data-stu-id="76347-128">Remarks</span></span>

<span data-ttu-id="76347-129">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="76347-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76347-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="76347-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76347-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="76347-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="76347-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="76347-132">Schema Name</span></span>  <br/> |<span data-ttu-id="76347-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="76347-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="76347-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="76347-134">Validation File</span></span>  <br/> |<span data-ttu-id="76347-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="76347-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="76347-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="76347-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="76347-137">False</span><span class="sxs-lookup"><span data-stu-id="76347-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76347-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="76347-138">See also</span></span>



[<span data-ttu-id="76347-139">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="76347-139">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="76347-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="76347-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

