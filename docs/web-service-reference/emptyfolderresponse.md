---
title: EmptyFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c900be49-3c90-41aa-aba5-bcf1116ec2aa
description: EmptyFolderResponse 元素定义 EmptyFolder 操作请求的响应。
ms.openlocfilehash: ab753351a1eb7deba83823875989816ba75b9809
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754093"
---
# <a name="emptyfolderresponse"></a><span data-ttu-id="7326e-103">EmptyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="7326e-103">EmptyFolderResponse</span></span>

<span data-ttu-id="7326e-104">**EmptyFolderResponse**元素定义[EmptyFolder 操作](emptyfolder-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7326e-104">The **EmptyFolderResponse** element defines a response to an [EmptyFolder operation](emptyfolder-operation.md) request.</span></span> 
  
```XML
<EmptyFolderResponse>
   <ResponseMessages/>
</EmptyFolderResponse>
```

 <span data-ttu-id="7326e-105">**EmptyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="7326e-105">**EmptyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7326e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7326e-106">Attributes and elements</span></span>

<span data-ttu-id="7326e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7326e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7326e-108">属性</span><span class="sxs-lookup"><span data-stu-id="7326e-108">Attributes</span></span>

<span data-ttu-id="7326e-109">无。</span><span class="sxs-lookup"><span data-stu-id="7326e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7326e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7326e-110">Child elements</span></span>

|<span data-ttu-id="7326e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7326e-111">**Element**</span></span>|<span data-ttu-id="7326e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7326e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7326e-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7326e-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7326e-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="7326e-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7326e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7326e-115">Parent elements</span></span>

<span data-ttu-id="7326e-116">无。</span><span class="sxs-lookup"><span data-stu-id="7326e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7326e-117">备注</span><span class="sxs-lookup"><span data-stu-id="7326e-117">Remarks</span></span>

<span data-ttu-id="7326e-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7326e-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7326e-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="7326e-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7326e-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="7326e-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7326e-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="7326e-121">Schema name</span></span>  <br/> |<span data-ttu-id="7326e-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="7326e-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7326e-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="7326e-123">Validation file</span></span>  <br/> |<span data-ttu-id="7326e-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7326e-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7326e-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="7326e-125">Can be empty</span></span>  <br/> |<span data-ttu-id="7326e-126">False</span><span class="sxs-lookup"><span data-stu-id="7326e-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7326e-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7326e-127">See also</span></span>



[<span data-ttu-id="7326e-128">EmptyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="7326e-128">EmptyFolder operation</span></span>](emptyfolder-operation.md)
  
[<span data-ttu-id="7326e-129">EmptyFolder</span><span class="sxs-lookup"><span data-stu-id="7326e-129">EmptyFolder</span></span>](emptyfolder.md)


- [<span data-ttu-id="7326e-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7326e-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

