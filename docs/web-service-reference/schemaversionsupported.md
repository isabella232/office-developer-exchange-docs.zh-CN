---
title: SchemaVersionSupported
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 578b1682-f3e1-4ccc-aa24-d2ca1a9de596
description: SchemaVersionSupported 元素包含客户端支持的清单架构的版本。
ms.openlocfilehash: 0b27a6f16f310ffe10ab819fc1046d4b0b6ecaa2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827272"
---
# <a name="schemaversionsupported"></a><span data-ttu-id="a1489-103">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="a1489-103">SchemaVersionSupported</span></span>

<span data-ttu-id="a1489-104">**SchemaVersionSupported**元素包含客户端支持的清单架构的版本。</span><span class="sxs-lookup"><span data-stu-id="a1489-104">The **SchemaVersionSupported** element contains the version of the manifest schema supported by the client.</span></span> 
  
```XML
<SchemaVersionSupported />
```

 <span data-ttu-id="a1489-105">**string**</span><span class="sxs-lookup"><span data-stu-id="a1489-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a1489-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a1489-106">Attributes and elements</span></span>

<span data-ttu-id="a1489-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a1489-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a1489-108">属性</span><span class="sxs-lookup"><span data-stu-id="a1489-108">Attributes</span></span>

<span data-ttu-id="a1489-109">无。</span><span class="sxs-lookup"><span data-stu-id="a1489-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1489-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a1489-110">Child elements</span></span>

<span data-ttu-id="a1489-111">无。</span><span class="sxs-lookup"><span data-stu-id="a1489-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a1489-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a1489-112">Parent elements</span></span>

[<span data-ttu-id="a1489-113">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="a1489-113">GetAppManifests</span></span>](getappmanifests.md)
  
## <a name="text-value"></a><span data-ttu-id="a1489-114">文本值</span><span class="sxs-lookup"><span data-stu-id="a1489-114">Text value</span></span>

<span data-ttu-id="a1489-115">**SchemaVersionSupported**元素的文本值包含客户端支持的清单架构的版本。</span><span class="sxs-lookup"><span data-stu-id="a1489-115">The text value of the **SchemaVersionSupported** element contains the version of the manifest schema supported by the client.</span></span> <span data-ttu-id="a1489-116">此值指示清单应返回到客户端的响应中的应用程序。</span><span class="sxs-lookup"><span data-stu-id="a1489-116">This value indicates which app manifests should be returned to the client in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1489-117">备注</span><span class="sxs-lookup"><span data-stu-id="a1489-117">Remarks</span></span>

<span data-ttu-id="a1489-118">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a1489-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1489-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="a1489-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1489-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="a1489-120">Namespace</span></span>  <br/> | http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a1489-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="a1489-121">Schema Name</span></span>  <br/> |<span data-ttu-id="a1489-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="a1489-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a1489-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="a1489-123">Validation File</span></span>  <br/> |<span data-ttu-id="a1489-124">不适用</span><span class="sxs-lookup"><span data-stu-id="a1489-124">Not applicable</span></span>  <br/> |
|<span data-ttu-id="a1489-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="a1489-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="a1489-126">False</span><span class="sxs-lookup"><span data-stu-id="a1489-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1489-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a1489-127">See also</span></span>



[<span data-ttu-id="a1489-128">GetAppManifests</span><span class="sxs-lookup"><span data-stu-id="a1489-128">GetAppManifests</span></span>](getappmanifests.md)


- [<span data-ttu-id="a1489-129">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a1489-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

