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
description: SyncFolderItemsResponse 元素定义对 SyncFolderItems 请求的响应。
ms.openlocfilehash: 694730a5ead8b875da9b3544099d0b20a478a627
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530230"
---
# <a name="syncfolderitemsresponse"></a><span data-ttu-id="c7c6c-103">SyncFolderItemsResponse</span><span class="sxs-lookup"><span data-stu-id="c7c6c-103">SyncFolderItemsResponse</span></span>

<span data-ttu-id="c7c6c-104">**SyncFolderItemsResponse**元素定义对 SyncFolderItems 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="c7c6c-104">The **SyncFolderItemsResponse** element defines a response to a SyncFolderItems request.</span></span> 
  
```xml
<SyncFolderItemsResponse>
   <ResponseMessages/>
</SyncFolderItemsResponse>
```

 <span data-ttu-id="c7c6c-105">**SyncFolderItemsResponseType**</span><span class="sxs-lookup"><span data-stu-id="c7c6c-105">**SyncFolderItemsResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c7c6c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c7c6c-106">Attributes and elements</span></span>

<span data-ttu-id="c7c6c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c7c6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c7c6c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c7c6c-108">Attributes</span></span>

<span data-ttu-id="c7c6c-109">无。</span><span class="sxs-lookup"><span data-stu-id="c7c6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c7c6c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c7c6c-110">Child elements</span></span>

|<span data-ttu-id="c7c6c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c7c6c-111">**Element**</span></span>|<span data-ttu-id="c7c6c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c7c6c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c7c6c-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="c7c6c-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="c7c6c-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="c7c6c-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c7c6c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c7c6c-115">Parent elements</span></span>

<span data-ttu-id="c7c6c-116">无。</span><span class="sxs-lookup"><span data-stu-id="c7c6c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7c6c-117">说明</span><span class="sxs-lookup"><span data-stu-id="c7c6c-117">Remarks</span></span>

<span data-ttu-id="c7c6c-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c7c6c-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c7c6c-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="c7c6c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c7c6c-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="c7c6c-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c7c6c-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="c7c6c-121">Schema name</span></span>  <br/> |<span data-ttu-id="c7c6c-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="c7c6c-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c7c6c-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="c7c6c-123">Validation file</span></span>  <br/> |<span data-ttu-id="c7c6c-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c7c6c-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c7c6c-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="c7c6c-125">Can be empty</span></span>  <br/> |<span data-ttu-id="c7c6c-126">False</span><span class="sxs-lookup"><span data-stu-id="c7c6c-126">False</span></span>  <br/> |
   

