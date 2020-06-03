---
title: GetAppManifestsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 86cf88f4-09c4-436a-a100-ac5cba0c4388
description: GetAppManifestsResponse 元素定义 Getappmanifests 已操作请求的响应。
ms.openlocfilehash: a01f6265d6d534e2f7868b17acf19f0f5d52a01f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462962"
---
# <a name="getappmanifestsresponse"></a><span data-ttu-id="67ef5-103">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="67ef5-103">GetAppManifestsResponse</span></span>

<span data-ttu-id="67ef5-104">**GetAppManifestsResponse**元素定义**getappmanifests 已**操作请求的响应。</span><span class="sxs-lookup"><span data-stu-id="67ef5-104">The **GetAppManifestsResponse** element defines the response for a **GetAppManifests** operation request.</span></span> 
  
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

<span data-ttu-id="67ef5-105">**GetAppManifestsResponseType**</span><span class="sxs-lookup"><span data-stu-id="67ef5-105">**GetAppManifestsResponseType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="67ef5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="67ef5-106">Attributes and elements</span></span>

<span data-ttu-id="67ef5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="67ef5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67ef5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="67ef5-108">Attributes</span></span>

<span data-ttu-id="67ef5-109">无。</span><span class="sxs-lookup"><span data-stu-id="67ef5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67ef5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="67ef5-110">Child elements</span></span>

<span data-ttu-id="67ef5-111">[ResponseCode](responsecode.md)  | [清单](manifests.md)  | [应用](apps.md)</span><span class="sxs-lookup"><span data-stu-id="67ef5-111">[ResponseCode](responsecode.md) | [Manifests](manifests.md) | [Apps](apps.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="67ef5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="67ef5-112">Parent elements</span></span>

<span data-ttu-id="67ef5-113">无。</span><span class="sxs-lookup"><span data-stu-id="67ef5-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67ef5-114">说明</span><span class="sxs-lookup"><span data-stu-id="67ef5-114">Remarks</span></span>

<span data-ttu-id="67ef5-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="67ef5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="67ef5-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="67ef5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67ef5-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="67ef5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67ef5-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="67ef5-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="67ef5-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="67ef5-119">Schema Name</span></span>  <br/> |<span data-ttu-id="67ef5-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="67ef5-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="67ef5-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="67ef5-121">Validation File</span></span>  <br/> |<span data-ttu-id="67ef5-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="67ef5-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="67ef5-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="67ef5-123">Can Be Empty</span></span>  <br/> |<span data-ttu-id="67ef5-124">False</span><span class="sxs-lookup"><span data-stu-id="67ef5-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="67ef5-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="67ef5-125">See also</span></span>

- [<span data-ttu-id="67ef5-126">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="67ef5-126">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

