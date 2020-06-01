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
ms.openlocfilehash: df70d8ecf78b4f9b99ceaa3c28d2b1831a1c6171
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465791"
---
# <a name="schemaversionsupported"></a><span data-ttu-id="bb5f4-103">SchemaVersionSupported</span><span class="sxs-lookup"><span data-stu-id="bb5f4-103">SchemaVersionSupported</span></span>

<span data-ttu-id="bb5f4-104">**SchemaVersionSupported**元素包含客户端支持的清单架构的版本。</span><span class="sxs-lookup"><span data-stu-id="bb5f4-104">The **SchemaVersionSupported** element contains the version of the manifest schema supported by the client.</span></span> 
  
```XML
<SchemaVersionSupported />
```

 <span data-ttu-id="bb5f4-105">**string**</span><span class="sxs-lookup"><span data-stu-id="bb5f4-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bb5f4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bb5f4-106">Attributes and elements</span></span>

<span data-ttu-id="bb5f4-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bb5f4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bb5f4-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bb5f4-108">Attributes</span></span>

<span data-ttu-id="bb5f4-109">无。</span><span class="sxs-lookup"><span data-stu-id="bb5f4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bb5f4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bb5f4-110">Child elements</span></span>

<span data-ttu-id="bb5f4-111">无。</span><span class="sxs-lookup"><span data-stu-id="bb5f4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bb5f4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bb5f4-112">Parent elements</span></span>

[<span data-ttu-id="bb5f4-113">Getappmanifests 已</span><span class="sxs-lookup"><span data-stu-id="bb5f4-113">GetAppManifests</span></span>](getappmanifests.md)
  
## <a name="text-value"></a><span data-ttu-id="bb5f4-114">文本值</span><span class="sxs-lookup"><span data-stu-id="bb5f4-114">Text value</span></span>

<span data-ttu-id="bb5f4-115">**SchemaVersionSupported**元素的文本值包含客户端支持的清单架构的版本。</span><span class="sxs-lookup"><span data-stu-id="bb5f4-115">The text value of the **SchemaVersionSupported** element contains the version of the manifest schema supported by the client.</span></span> <span data-ttu-id="bb5f4-116">此值指示应在响应中向客户端返回哪些应用程序清单。</span><span class="sxs-lookup"><span data-stu-id="bb5f4-116">This value indicates which app manifests should be returned to the client in the response.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bb5f4-117">说明</span><span class="sxs-lookup"><span data-stu-id="bb5f4-117">Remarks</span></span>

<span data-ttu-id="bb5f4-118">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bb5f4-118">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bb5f4-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="bb5f4-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb5f4-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="bb5f4-120">Namespace</span></span>  <br/> | https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bb5f4-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="bb5f4-121">Schema Name</span></span>  <br/> |<span data-ttu-id="bb5f4-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="bb5f4-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bb5f4-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="bb5f4-123">Validation File</span></span>  <br/> |<span data-ttu-id="bb5f4-124">不适用</span><span class="sxs-lookup"><span data-stu-id="bb5f4-124">Not applicable</span></span>  <br/> |
|<span data-ttu-id="bb5f4-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="bb5f4-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="bb5f4-126">False</span><span class="sxs-lookup"><span data-stu-id="bb5f4-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb5f4-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bb5f4-127">See also</span></span>



[<span data-ttu-id="bb5f4-128">Getappmanifests 已</span><span class="sxs-lookup"><span data-stu-id="bb5f4-128">GetAppManifests</span></span>](getappmanifests.md)


- [<span data-ttu-id="bb5f4-129">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="bb5f4-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

