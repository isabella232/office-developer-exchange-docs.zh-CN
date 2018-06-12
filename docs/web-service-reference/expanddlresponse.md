---
title: ExpandDLResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDLResponse
api_type:
- schema
ms.assetid: 1c60dd64-a083-460a-9840-021d30f871d6
description: ExpandDLResponse 元素定义对展开通讯组列表的请求的响应。
ms.openlocfilehash: dbcb0ff8e5c11460c070b8a87da53cecca279b88
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754196"
---
# <a name="expanddlresponse"></a><span data-ttu-id="f8b14-103">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="f8b14-103">ExpandDLResponse</span></span>

<span data-ttu-id="f8b14-104">**ExpandDLResponse**元素定义对展开通讯组列表的请求的响应。</span><span class="sxs-lookup"><span data-stu-id="f8b14-104">The **ExpandDLResponse** element defines a response to a request to expand a distribution list.</span></span> 
  
[<span data-ttu-id="f8b14-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="f8b14-105">ExpandDLResponse</span></span>](expanddlresponse.md)
  
```xml
<ExpandDLResponse>
   <ResponseMessages/>
</ExpandDLResponse>
```

 <span data-ttu-id="f8b14-106">**ExpandDLResponseType**</span><span class="sxs-lookup"><span data-stu-id="f8b14-106">**ExpandDLResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f8b14-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f8b14-107">Attributes and elements</span></span>

<span data-ttu-id="f8b14-108">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f8b14-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8b14-109">属性</span><span class="sxs-lookup"><span data-stu-id="f8b14-109">Attributes</span></span>

<span data-ttu-id="f8b14-110">无。</span><span class="sxs-lookup"><span data-stu-id="f8b14-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f8b14-111">子元素</span><span class="sxs-lookup"><span data-stu-id="f8b14-111">Child elements</span></span>

|<span data-ttu-id="f8b14-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="f8b14-112">**Element**</span></span>|<span data-ttu-id="f8b14-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="f8b14-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f8b14-114">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f8b14-114">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="f8b14-115">包含为 Exchange Web 服务请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="f8b14-115">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f8b14-116">父元素</span><span class="sxs-lookup"><span data-stu-id="f8b14-116">Parent elements</span></span>

<span data-ttu-id="f8b14-117">无。</span><span class="sxs-lookup"><span data-stu-id="f8b14-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f8b14-118">备注</span><span class="sxs-lookup"><span data-stu-id="f8b14-118">Remarks</span></span>

<span data-ttu-id="f8b14-119">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f8b14-119">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f8b14-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="f8b14-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8b14-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="f8b14-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f8b14-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="f8b14-122">Schema name</span></span>  <br/> |<span data-ttu-id="f8b14-123">类型架构</span><span class="sxs-lookup"><span data-stu-id="f8b14-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="f8b14-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="f8b14-124">Validation file</span></span>  <br/> |<span data-ttu-id="f8b14-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f8b14-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f8b14-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="f8b14-126">Can be empty</span></span>  <br/> |<span data-ttu-id="f8b14-127">False</span><span class="sxs-lookup"><span data-stu-id="f8b14-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8b14-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f8b14-128">See also</span></span>



[<span data-ttu-id="f8b14-129">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="f8b14-129">ExpandDL</span></span>](expanddl.md)
  
[<span data-ttu-id="f8b14-130">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="f8b14-130">ExpandDL operation</span></span>](expanddl-operation.md)

