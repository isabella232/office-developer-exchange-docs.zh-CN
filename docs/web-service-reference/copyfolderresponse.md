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
description: CopyFolderResponse 元素定义 CopyFolder 请求的响应。
ms.openlocfilehash: 2f95089b9cb61e9e0047d02968d59d483fd7cdba
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753608"
---
# <a name="copyfolderresponse"></a><span data-ttu-id="d063c-103">CopyFolderResponse</span><span class="sxs-lookup"><span data-stu-id="d063c-103">CopyFolderResponse</span></span>

<span data-ttu-id="d063c-104">**CopyFolderResponse**元素定义 CopyFolder 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="d063c-104">The **CopyFolderResponse** element defines a response to a CopyFolder request.</span></span> 
  
```xml
<CopyFolderResponse>
   <ResponseMessages/>
</CopyFolderResponse>
```

 <span data-ttu-id="d063c-105">**CopyFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="d063c-105">**CopyFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d063c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d063c-106">Attributes and elements</span></span>

<span data-ttu-id="d063c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d063c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d063c-108">属性</span><span class="sxs-lookup"><span data-stu-id="d063c-108">Attributes</span></span>

<span data-ttu-id="d063c-109">无。</span><span class="sxs-lookup"><span data-stu-id="d063c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d063c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d063c-110">Child elements</span></span>

|<span data-ttu-id="d063c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d063c-111">**Element**</span></span>|<span data-ttu-id="d063c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d063c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d063c-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d063c-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="d063c-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="d063c-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d063c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d063c-115">Parent elements</span></span>

<span data-ttu-id="d063c-116">无。</span><span class="sxs-lookup"><span data-stu-id="d063c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d063c-117">备注</span><span class="sxs-lookup"><span data-stu-id="d063c-117">Remarks</span></span>

<span data-ttu-id="d063c-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d063c-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d063c-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="d063c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d063c-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="d063c-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d063c-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="d063c-121">Schema name</span></span>  <br/> |<span data-ttu-id="d063c-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="d063c-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d063c-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="d063c-123">Validation file</span></span>  <br/> |<span data-ttu-id="d063c-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d063c-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d063c-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="d063c-125">Can be empty</span></span>  <br/> |<span data-ttu-id="d063c-126">False</span><span class="sxs-lookup"><span data-stu-id="d063c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d063c-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d063c-127">See also</span></span>



[<span data-ttu-id="d063c-128">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="d063c-128">CopyFolder operation</span></span>](copyfolder-operation.md)
  
[<span data-ttu-id="d063c-129">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d063c-129">CopyFolder</span></span>](copyfolder.md)


- [<span data-ttu-id="d063c-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d063c-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

