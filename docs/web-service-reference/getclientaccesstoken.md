---
title: GetClientAccessToken
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3704435b-9c84-4cff-a2a0-8288b4ca31ae
description: GetClientAccessToken元素中包含一个请求以获取客户端访问令牌。
ms.openlocfilehash: f0306f0d608300131ecbde500ed3b62eab0c7c66
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461091"
---
# <a name="getclientaccesstoken"></a><span data-ttu-id="08ef8-103">GetClientAccessToken</span><span class="sxs-lookup"><span data-stu-id="08ef8-103">GetClientAccessToken</span></span>

<span data-ttu-id="08ef8-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **GetClientAccessToken**元素中包含一个请求以获取客户端访问令牌。</span><span class="sxs-lookup"><span data-stu-id="08ef8-104">The **GetClientAccessToken** element contains a request to get a client access token.</span></span> 
  
```XML
<GetClientAccessToken>
   <TokenRequests/>
</GetClientAccessToken>
```

 <span data-ttu-id="08ef8-105">**GetClientAccessTokenType**</span><span class="sxs-lookup"><span data-stu-id="08ef8-105">**GetClientAccessTokenType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="08ef8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="08ef8-106">Attributes and elements</span></span>

<span data-ttu-id="08ef8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="08ef8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="08ef8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="08ef8-108">Attributes</span></span>

<span data-ttu-id="08ef8-109">无。</span><span class="sxs-lookup"><span data-stu-id="08ef8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="08ef8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="08ef8-110">Child elements</span></span>

[<span data-ttu-id="08ef8-111">TokenRequests</span><span class="sxs-lookup"><span data-stu-id="08ef8-111">TokenRequests</span></span>](tokenrequests.md)
  
### <a name="parent-elements"></a><span data-ttu-id="08ef8-112">父元素</span><span class="sxs-lookup"><span data-stu-id="08ef8-112">Parent elements</span></span>

<span data-ttu-id="08ef8-113">无。</span><span class="sxs-lookup"><span data-stu-id="08ef8-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="08ef8-114">说明</span><span class="sxs-lookup"><span data-stu-id="08ef8-114">Remarks</span></span>

<span data-ttu-id="08ef8-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="08ef8-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="08ef8-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="08ef8-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="08ef8-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="08ef8-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="08ef8-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="08ef8-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="08ef8-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="08ef8-119">Schema name</span></span>  <br/> |<span data-ttu-id="08ef8-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="08ef8-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="08ef8-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="08ef8-121">Validation file</span></span>  <br/> |<span data-ttu-id="08ef8-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="08ef8-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="08ef8-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="08ef8-123">Can be empty</span></span>  <br/> ||
   

