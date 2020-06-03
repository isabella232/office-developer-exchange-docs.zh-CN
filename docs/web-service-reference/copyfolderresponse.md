---
title: CopyFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolderResponse
api_type:
- schema
ms.assetid: 5bfbb4d3-e2ed-4b84-96f7-2175f1947aed
description: CopyFolderResponse 元素定义对 CopyFolder 请求的响应。
ms.openlocfilehash: aaf5d2bde8c9ba6b0c8aa6345af39dd9a6006ae5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458514"
---
# <a name="copyfolderresponse"></a><span data-ttu-id="5b441-103">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="5b441-103">CopyFolderResponse</span></span>

<span data-ttu-id="5b441-104">**CopyFolderResponse**元素定义对 CopyFolder 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="5b441-104">The **CopyFolderResponse** element defines a response to a CopyFolder request.</span></span> 
  
```xml
<CopyFolderResponse>
   <ResponseMessages/>
</CopyFolderResponse>
```

 <span data-ttu-id="5b441-105">**CopyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="5b441-105">**CopyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5b441-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5b441-106">Attributes and elements</span></span>

<span data-ttu-id="5b441-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5b441-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5b441-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5b441-108">Attributes</span></span>

<span data-ttu-id="5b441-109">无。</span><span class="sxs-lookup"><span data-stu-id="5b441-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5b441-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5b441-110">Child elements</span></span>

|<span data-ttu-id="5b441-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="5b441-111">**Element**</span></span>|<span data-ttu-id="5b441-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="5b441-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5b441-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5b441-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="5b441-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="5b441-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5b441-115">父元素</span><span class="sxs-lookup"><span data-stu-id="5b441-115">Parent elements</span></span>

<span data-ttu-id="5b441-116">无。</span><span class="sxs-lookup"><span data-stu-id="5b441-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b441-117">说明</span><span class="sxs-lookup"><span data-stu-id="5b441-117">Remarks</span></span>

<span data-ttu-id="5b441-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5b441-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5b441-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="5b441-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b441-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="5b441-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5b441-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="5b441-121">Schema name</span></span>  <br/> |<span data-ttu-id="5b441-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="5b441-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5b441-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="5b441-123">Validation file</span></span>  <br/> |<span data-ttu-id="5b441-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5b441-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5b441-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="5b441-125">Can be empty</span></span>  <br/> |<span data-ttu-id="5b441-126">False</span><span class="sxs-lookup"><span data-stu-id="5b441-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b441-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5b441-127">See also</span></span>



[<span data-ttu-id="5b441-128">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="5b441-128">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="5b441-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="5b441-129">CopyFolder</span></span>](copyfolder.md)


- [<span data-ttu-id="5b441-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5b441-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

