---
title: SyncFolderHierarchyResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchyResponse
api_type:
- schema
ms.assetid: 7e6061d2-bbce-4864-a7bb-a6457628cb7c
description: SyncFolderHierarchyResponse 元素定义对 SyncFolderHierarchy 请求的响应。
ms.openlocfilehash: bf17ee9080405d308328197f7cbeb92e9b1e02d3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456421"
---
# <a name="syncfolderhierarchyresponse"></a><span data-ttu-id="8a499-103">SyncFolderHierarchyResponse</span><span class="sxs-lookup"><span data-stu-id="8a499-103">SyncFolderHierarchyResponse</span></span>

<span data-ttu-id="8a499-104">**SyncFolderHierarchyResponse**元素定义对 SyncFolderHierarchy 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="8a499-104">The **SyncFolderHierarchyResponse** element defines a response to a SyncFolderHierarchy request.</span></span> 
  
```xml
<SyncFolderHierarchyResponse>
   <ResponseMessages/>
</SyncFolderHierarchyResponse>
```

 <span data-ttu-id="8a499-105">**SyncFolderHierarchyResponseType**</span><span class="sxs-lookup"><span data-stu-id="8a499-105">**SyncFolderHierarchyResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a499-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a499-106">Attributes and elements</span></span>

<span data-ttu-id="8a499-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a499-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a499-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8a499-108">Attributes</span></span>

<span data-ttu-id="8a499-109">无。</span><span class="sxs-lookup"><span data-stu-id="8a499-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8a499-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8a499-110">Child elements</span></span>

|<span data-ttu-id="8a499-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8a499-111">**Element**</span></span>|<span data-ttu-id="8a499-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a499-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a499-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8a499-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="8a499-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="8a499-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8a499-115">父元素</span><span class="sxs-lookup"><span data-stu-id="8a499-115">Parent elements</span></span>

<span data-ttu-id="8a499-116">无。</span><span class="sxs-lookup"><span data-stu-id="8a499-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a499-117">说明</span><span class="sxs-lookup"><span data-stu-id="8a499-117">Remarks</span></span>

<span data-ttu-id="8a499-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a499-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a499-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a499-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a499-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a499-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a499-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a499-121">Schema name</span></span>  <br/> |<span data-ttu-id="8a499-122">邮件架构</span><span class="sxs-lookup"><span data-stu-id="8a499-122">messages schema</span></span>  <br/> |
|<span data-ttu-id="8a499-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a499-123">Validation file</span></span>  <br/> |<span data-ttu-id="8a499-124">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="8a499-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a499-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a499-125">Can be empty</span></span>  <br/> |<span data-ttu-id="8a499-126">False</span><span class="sxs-lookup"><span data-stu-id="8a499-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a499-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a499-127">See also</span></span>



[<span data-ttu-id="8a499-128">SyncFolderHierarchy 操作</span><span class="sxs-lookup"><span data-stu-id="8a499-128">SyncFolderHierarchy operation</span></span>](syncfolderhierarchy-operation.md)


- [<span data-ttu-id="8a499-129">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8a499-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

