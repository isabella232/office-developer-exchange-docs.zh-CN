---
title: DeleteFolderResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolderResponse
api_type:
- schema
ms.assetid: 27578bda-ef0a-4a33-bccc-2c1bc1735424
description: DeleteFolderResponse 元素定义对 DeleteFolder 请求的响应。
ms.openlocfilehash: 58b814662c769784c5fd682a9e039863a9787d8d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458486"
---
# <a name="deletefolderresponse"></a><span data-ttu-id="4f73a-103">DeleteFolderResponse</span><span class="sxs-lookup"><span data-stu-id="4f73a-103">DeleteFolderResponse</span></span>

<span data-ttu-id="4f73a-104">**DeleteFolderResponse**元素定义对 DeleteFolder 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="4f73a-104">The **DeleteFolderResponse** element defines a response to a DeleteFolder request.</span></span> 
  
```xml
<DeleteFolderResponse>
   <ResponseMessages/>
</DeleteFolderResponse>
```

 <span data-ttu-id="4f73a-105">**DeleteFolderResponseType**</span><span class="sxs-lookup"><span data-stu-id="4f73a-105">**DeleteFolderResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4f73a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4f73a-106">Attributes and elements</span></span>

<span data-ttu-id="4f73a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4f73a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4f73a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4f73a-108">Attributes</span></span>

<span data-ttu-id="4f73a-109">无。</span><span class="sxs-lookup"><span data-stu-id="4f73a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4f73a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4f73a-110">Child elements</span></span>

|<span data-ttu-id="4f73a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4f73a-111">**Element**</span></span>|<span data-ttu-id="4f73a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4f73a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4f73a-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4f73a-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4f73a-114">包含 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="4f73a-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4f73a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4f73a-115">Parent elements</span></span>

<span data-ttu-id="4f73a-116">无。</span><span class="sxs-lookup"><span data-stu-id="4f73a-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4f73a-117">说明</span><span class="sxs-lookup"><span data-stu-id="4f73a-117">Remarks</span></span>

<span data-ttu-id="4f73a-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4f73a-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f73a-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="4f73a-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f73a-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="4f73a-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4f73a-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="4f73a-121">Schema name</span></span>  <br/> |<span data-ttu-id="4f73a-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="4f73a-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4f73a-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="4f73a-123">Validation file</span></span>  <br/> |<span data-ttu-id="4f73a-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4f73a-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4f73a-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="4f73a-125">Can be empty</span></span>  <br/> |<span data-ttu-id="4f73a-126">False</span><span class="sxs-lookup"><span data-stu-id="4f73a-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f73a-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4f73a-127">See also</span></span>

- [<span data-ttu-id="4f73a-128">DeleteFolder 操作</span><span class="sxs-lookup"><span data-stu-id="4f73a-128">DeleteFolder operation</span></span>](deletefolder-operation.md) 
- [<span data-ttu-id="4f73a-129">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="4f73a-129">DeleteFolder</span></span>](deletefolder.md)
- [<span data-ttu-id="4f73a-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4f73a-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

