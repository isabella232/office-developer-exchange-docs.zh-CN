---
title: GetFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolderResponse
api_type:
- schema
ms.assetid: 47abeec8-78dd-4297-8525-099174ec880d
description: GetFolderResponse 元素定义 GetFolder 请求的响应。
ms.openlocfilehash: 0831224f1f649f3febf20fac2d7e987de03edcb8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754569"
---
# <a name="getfolderresponse"></a><span data-ttu-id="94503-103">GetFolderResponse</span><span class="sxs-lookup"><span data-stu-id="94503-103">GetFolderResponse</span></span>

<span data-ttu-id="94503-104">**GetFolderResponse**元素定义 GetFolder 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="94503-104">The **GetFolderResponse** element defines a response to a GetFolder request.</span></span> 
  
```xml
<GetFolderResponse>
   <ResponseMessages/>
</GetFolderResponse>
```

 <span data-ttu-id="94503-105">**GetFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="94503-105">**GetFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="94503-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="94503-106">Attributes and elements</span></span>

<span data-ttu-id="94503-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="94503-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="94503-108">属性</span><span class="sxs-lookup"><span data-stu-id="94503-108">Attributes</span></span>

<span data-ttu-id="94503-109">无。</span><span class="sxs-lookup"><span data-stu-id="94503-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="94503-110">子元素</span><span class="sxs-lookup"><span data-stu-id="94503-110">Child elements</span></span>

|<span data-ttu-id="94503-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="94503-111">**Element**</span></span>|<span data-ttu-id="94503-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="94503-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="94503-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="94503-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="94503-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="94503-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="94503-115">父元素</span><span class="sxs-lookup"><span data-stu-id="94503-115">Parent elements</span></span>

<span data-ttu-id="94503-116">无。</span><span class="sxs-lookup"><span data-stu-id="94503-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="94503-117">备注</span><span class="sxs-lookup"><span data-stu-id="94503-117">Remarks</span></span>

<span data-ttu-id="94503-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="94503-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="94503-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="94503-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="94503-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="94503-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="94503-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="94503-121">Schema name</span></span>  <br/> |<span data-ttu-id="94503-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="94503-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="94503-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="94503-123">Validation file</span></span>  <br/> |<span data-ttu-id="94503-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="94503-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="94503-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="94503-125">Can be empty</span></span>  <br/> |<span data-ttu-id="94503-126">False</span><span class="sxs-lookup"><span data-stu-id="94503-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="94503-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="94503-127">See also</span></span>



[<span data-ttu-id="94503-128">GetFolder</span><span class="sxs-lookup"><span data-stu-id="94503-128">GetFolder</span></span>](getfolder.md)
  
[<span data-ttu-id="94503-129">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="94503-129">GetFolder operation</span></span>](getfolder-operation.md)
  
[<span data-ttu-id="94503-130">GetFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="94503-130">GetFolderResponseMessage</span></span>](getfolderresponsemessage.md)

