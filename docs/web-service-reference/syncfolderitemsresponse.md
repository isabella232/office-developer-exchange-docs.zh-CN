---
title: SyncFolderItemsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItemsResponse
api_type:
- schema
ms.assetid: 82fe0644-1756-40b2-955c-20c01110660c
description: SyncFolderItemsResponse 元素定义 SyncFolderItems 请求的响应。
ms.openlocfilehash: e6145a1757d67c1d4a2e50b74204e4a79bdb6df9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838175"
---
# <a name="syncfolderitemsresponse"></a><span data-ttu-id="913cf-103">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="913cf-103">SyncFolderItemsResponse</span></span>

<span data-ttu-id="913cf-104">**SyncFolderItemsResponse**元素定义 SyncFolderItems 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="913cf-104">The **SyncFolderItemsResponse** element defines a response to a SyncFolderItems request.</span></span> 
  
```xml
<SyncFolderItemsResponse>
   <ResponseMessages/>
</SyncFolderItemsResponse>
```

 <span data-ttu-id="913cf-105">**SyncFolderItemsResponseType**</span><span class="sxs-lookup"><span data-stu-id="913cf-105">**SyncFolderItemsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="913cf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="913cf-106">Attributes and elements</span></span>

<span data-ttu-id="913cf-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="913cf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="913cf-108">属性</span><span class="sxs-lookup"><span data-stu-id="913cf-108">Attributes</span></span>

<span data-ttu-id="913cf-109">无。</span><span class="sxs-lookup"><span data-stu-id="913cf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="913cf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="913cf-110">Child elements</span></span>

|<span data-ttu-id="913cf-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="913cf-111">**Element**</span></span>|<span data-ttu-id="913cf-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="913cf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="913cf-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="913cf-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="913cf-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="913cf-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="913cf-115">父元素</span><span class="sxs-lookup"><span data-stu-id="913cf-115">Parent elements</span></span>

<span data-ttu-id="913cf-116">无。</span><span class="sxs-lookup"><span data-stu-id="913cf-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="913cf-117">备注</span><span class="sxs-lookup"><span data-stu-id="913cf-117">Remarks</span></span>

<span data-ttu-id="913cf-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="913cf-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="913cf-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="913cf-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="913cf-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="913cf-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="913cf-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="913cf-121">Schema name</span></span>  <br/> |<span data-ttu-id="913cf-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="913cf-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="913cf-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="913cf-123">Validation file</span></span>  <br/> |<span data-ttu-id="913cf-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="913cf-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="913cf-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="913cf-125">Can be empty</span></span>  <br/> |<span data-ttu-id="913cf-126">False</span><span class="sxs-lookup"><span data-stu-id="913cf-126">False</span></span>  <br/> |
   

