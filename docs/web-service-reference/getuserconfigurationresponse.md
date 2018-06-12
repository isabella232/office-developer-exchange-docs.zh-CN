---
title: GetUserConfigurationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserConfigurationResponse
api_type:
- schema
ms.assetid: 5e418c91-c836-4de0-a80d-f0dad0c684d7
description: GetUserConfigurationResponse 元素定义对单个 GetUserConfiguration 请求的响应。
ms.openlocfilehash: b720809a66c75dbf75f6e597a0064992b9f741e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825689"
---
# <a name="getuserconfigurationresponse"></a><span data-ttu-id="7caab-103">GetUserConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="7caab-103">GetUserConfigurationResponse</span></span>

<span data-ttu-id="7caab-104">**GetUserConfigurationResponse**元素定义对单个 GetUserConfiguration 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7caab-104">The **GetUserConfigurationResponse** element defines a response to a single GetUserConfiguration request.</span></span> 
  
```xml
<GetUserConfigurationResponse>   <ResponseMessages/></GetUserConfigurationResponse>
```

 <span data-ttu-id="7caab-105">**GetUserConfigurationResponseType**</span><span class="sxs-lookup"><span data-stu-id="7caab-105">**GetUserConfigurationResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7caab-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7caab-106">Attributes and elements</span></span>

<span data-ttu-id="7caab-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7caab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7caab-108">属性</span><span class="sxs-lookup"><span data-stu-id="7caab-108">Attributes</span></span>

<span data-ttu-id="7caab-109">无。</span><span class="sxs-lookup"><span data-stu-id="7caab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7caab-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7caab-110">Child elements</span></span>

|<span data-ttu-id="7caab-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7caab-111">**Element**</span></span>|<span data-ttu-id="7caab-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7caab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7caab-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7caab-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="7caab-114">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="7caab-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7caab-115">父元素</span><span class="sxs-lookup"><span data-stu-id="7caab-115">Parent elements</span></span>

<span data-ttu-id="7caab-116">无。</span><span class="sxs-lookup"><span data-stu-id="7caab-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7caab-117">备注</span><span class="sxs-lookup"><span data-stu-id="7caab-117">Remarks</span></span>

<span data-ttu-id="7caab-118">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7caab-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7caab-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="7caab-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7caab-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="7caab-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7caab-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="7caab-121">Schema Name</span></span>  <br/> |<span data-ttu-id="7caab-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="7caab-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7caab-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="7caab-123">Validation File</span></span>  <br/> |<span data-ttu-id="7caab-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7caab-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7caab-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="7caab-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="7caab-126">False</span><span class="sxs-lookup"><span data-stu-id="7caab-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7caab-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7caab-127">See also</span></span>



- [<span data-ttu-id="7caab-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7caab-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

