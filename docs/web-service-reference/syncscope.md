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
description: SyncScope 元素指定是否同步响应中返回项目或项目和文件夹的相关信息。
ms.openlocfilehash: 847c0244a8847364e29ea584b0c0b721f00d3064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838178"
---
# <a name="syncscope"></a><span data-ttu-id="466c9-103">SyncScope</span><span class="sxs-lookup"><span data-stu-id="466c9-103">SyncScope</span></span>

<span data-ttu-id="466c9-104">**SyncScope**元素指定是否同步响应中返回项目或项目和文件夹的相关信息。</span><span class="sxs-lookup"><span data-stu-id="466c9-104">The **SyncScope** element specifies whether just items or items and folder associated information are returned in a synchronization response.</span></span> 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 <span data-ttu-id="466c9-105">**SyncFolderItemsScopeType**</span><span class="sxs-lookup"><span data-stu-id="466c9-105">**SyncFolderItemsScopeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="466c9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="466c9-106">Attributes and elements</span></span>

<span data-ttu-id="466c9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="466c9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="466c9-108">属性</span><span class="sxs-lookup"><span data-stu-id="466c9-108">Attributes</span></span>

<span data-ttu-id="466c9-109">无。</span><span class="sxs-lookup"><span data-stu-id="466c9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="466c9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="466c9-110">Child elements</span></span>

<span data-ttu-id="466c9-111">无。</span><span class="sxs-lookup"><span data-stu-id="466c9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="466c9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="466c9-112">Parent elements</span></span>

|<span data-ttu-id="466c9-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="466c9-113">**Element**</span></span>|<span data-ttu-id="466c9-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="466c9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="466c9-115">SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="466c9-115">SyncFolderItems</span></span>](syncfolderitems.md) <br/> |<span data-ttu-id="466c9-116">定义同步 Exchange 存储区文件夹中的项目的请求的元素。</span><span class="sxs-lookup"><span data-stu-id="466c9-116">The element that defines a request to synchronize items in an Exchange store folder.</span></span>  <br/> <span data-ttu-id="466c9-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="466c9-117">The following is the XPath expression to this element:</span></span>  <br/> <span data-ttu-id="466c9-118">/ SyncFolderItems</span><span class="sxs-lookup"><span data-stu-id="466c9-118">/SyncFolderItems</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="466c9-119">文本值</span><span class="sxs-lookup"><span data-stu-id="466c9-119">Text value</span></span>

<span data-ttu-id="466c9-120">下表列出了**SyncScope**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="466c9-120">The following table lists the possible values for the **SyncScope** element.</span></span> 
  
<span data-ttu-id="466c9-121">**SyncScope 元素的值**</span><span class="sxs-lookup"><span data-stu-id="466c9-121">**SyncScope element values**</span></span>

|<span data-ttu-id="466c9-122">**值**</span><span class="sxs-lookup"><span data-stu-id="466c9-122">**Value**</span></span>|<span data-ttu-id="466c9-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="466c9-123">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="466c9-124">NormalItems</span><span class="sxs-lookup"><span data-stu-id="466c9-124">NormalItems</span></span>  <br/> |<span data-ttu-id="466c9-125">指定同步响应中返回的仅文件夹中的项目。</span><span class="sxs-lookup"><span data-stu-id="466c9-125">Specifies that only items in the folder are returned in a synchronization response.</span></span>  <br/> |
|<span data-ttu-id="466c9-126">NormalAndAssociatedItems</span><span class="sxs-lookup"><span data-stu-id="466c9-126">NormalAndAssociatedItems</span></span>  <br/> |<span data-ttu-id="466c9-127">指定同步响应中返回的两个项目中的文件夹和文件夹的相关信息。</span><span class="sxs-lookup"><span data-stu-id="466c9-127">Specifies that both items in the folder and folder associated information are returned in a synchronization response.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="466c9-128">注解</span><span class="sxs-lookup"><span data-stu-id="466c9-128">Remarks</span></span>

<span data-ttu-id="466c9-129">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="466c9-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="466c9-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="466c9-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="466c9-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="466c9-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="466c9-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="466c9-132">Schema Name</span></span>  <br/> |<span data-ttu-id="466c9-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="466c9-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="466c9-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="466c9-134">Validation File</span></span>  <br/> |<span data-ttu-id="466c9-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="466c9-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="466c9-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="466c9-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="466c9-137">False</span><span class="sxs-lookup"><span data-stu-id="466c9-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="466c9-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="466c9-138">See also</span></span>



[<span data-ttu-id="466c9-139">SyncFolderItems 操作</span><span class="sxs-lookup"><span data-stu-id="466c9-139">SyncFolderItems operation</span></span>](syncfolderitems-operation.md)


- [<span data-ttu-id="466c9-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="466c9-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

