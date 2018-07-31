---
title: GetAppManifestsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86cf88f4-09c4-436a-a100-ac5cba0c4388
description: GetAppManifestsResponse 元素定义 GetAppManifests 操作请求的响应。
ms.openlocfilehash: ae9d1d853023a5b42db2e8fee2ed57f585433f69
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354146"
---
# <a name="getappmanifestsresponse"></a><span data-ttu-id="80b7a-103">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="80b7a-103">GetAppManifestsResponse</span></span>

<span data-ttu-id="80b7a-104">**GetAppManifestsResponse**元素定义**GetAppManifests**操作请求的响应。</span><span class="sxs-lookup"><span data-stu-id="80b7a-104">The **GetAppManifestsResponse** element defines the response for a **GetAppManifests** operation request.</span></span> 
  
```xml
<GetAppManifestsResponse>
    <ResponseCode/>
    <Manifests/>
</GetAppManifestsResponse>
```

```xml
<GetAppManifestsResponse>
    <ResponseCode/>
    <Apps/>
</GetAppManifestsResponse>
```

<span data-ttu-id="80b7a-105">**GetAppManifestsResponseType**</span><span class="sxs-lookup"><span data-stu-id="80b7a-105">**GetAppManifestsResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="80b7a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="80b7a-106">Attributes and elements</span></span>

<span data-ttu-id="80b7a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="80b7a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="80b7a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="80b7a-108">Attributes</span></span>

<span data-ttu-id="80b7a-109">无。</span><span class="sxs-lookup"><span data-stu-id="80b7a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="80b7a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="80b7a-110">Child elements</span></span>

<span data-ttu-id="80b7a-111">[ResponseCode](responsecode.md) | [清单](manifests.md) | [应用程序](apps.md)</span><span class="sxs-lookup"><span data-stu-id="80b7a-111">[ResponseCode](responsecode.md) | [Manifests](manifests.md) | [Apps](apps.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="80b7a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="80b7a-112">Parent elements</span></span>

<span data-ttu-id="80b7a-113">无。</span><span class="sxs-lookup"><span data-stu-id="80b7a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="80b7a-114">备注</span><span class="sxs-lookup"><span data-stu-id="80b7a-114">Remarks</span></span>

<span data-ttu-id="80b7a-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="80b7a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="80b7a-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="80b7a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="80b7a-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="80b7a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="80b7a-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="80b7a-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="80b7a-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="80b7a-119">Schema Name</span></span>  <br/> |<span data-ttu-id="80b7a-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="80b7a-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="80b7a-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="80b7a-121">Validation File</span></span>  <br/> |<span data-ttu-id="80b7a-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="80b7a-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="80b7a-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="80b7a-123">Can Be Empty</span></span>  <br/> |<span data-ttu-id="80b7a-124">False</span><span class="sxs-lookup"><span data-stu-id="80b7a-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80b7a-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="80b7a-125">See also</span></span>

- [<span data-ttu-id="80b7a-126">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="80b7a-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

