---
title: TokenType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: TokenType 元素指定标记的类型。
ms.openlocfilehash: 5c8e880f035ed74776a7c77e4b4e60ca46d66d4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838255"
---
# <a name="tokentype"></a><span data-ttu-id="5a5f6-103">TokenType</span><span class="sxs-lookup"><span data-stu-id="5a5f6-103">TokenType</span></span>

<span data-ttu-id="5a5f6-104">**TokenType**元素指定标记的类型。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-104">The **TokenType** element specifies the type of token.</span></span> 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 <span data-ttu-id="5a5f6-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="5a5f6-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5a5f6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5a5f6-106">Attributes and elements</span></span>

<span data-ttu-id="5a5f6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a5f6-108">属性</span><span class="sxs-lookup"><span data-stu-id="5a5f6-108">Attributes</span></span>

<span data-ttu-id="5a5f6-109">无。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5a5f6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5a5f6-110">Child elements</span></span>

<span data-ttu-id="5a5f6-111">无。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5a5f6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5a5f6-112">Parent elements</span></span>

<span data-ttu-id="5a5f6-113">[TokenRequest](tokenrequest.md) | [令牌](token.md)</span><span class="sxs-lookup"><span data-stu-id="5a5f6-113">[TokenRequest](tokenrequest.md) | [Token](token.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5a5f6-114">文本值</span><span class="sxs-lookup"><span data-stu-id="5a5f6-114">Text value</span></span>

<span data-ttu-id="5a5f6-115">标记类型**TokenType**元素的文本值。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-115">The text value of the **TokenType** element is the token type.</span></span> <span data-ttu-id="5a5f6-116">**CallerIdentity**的文本值指示令牌是呼叫者标识令牌。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-116">The text value of **CallerIdentity** indicates that the token is a caller identity token.</span></span> <span data-ttu-id="5a5f6-117">**ExtensionCallback**的文本值指示标记为扩展回调。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-117">The text value of **ExtensionCallback** indicates that the token is for an extension callback.</span></span> <span data-ttu-id="5a5f6-118">**ScopedToken**的文本值指示客户端访问令牌的作用域的令牌。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-118">The text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5a5f6-119">备注</span><span class="sxs-lookup"><span data-stu-id="5a5f6-119">Remarks</span></span>

<span data-ttu-id="5a5f6-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="5a5f6-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5a5f6-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a5f6-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="5a5f6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a5f6-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="5a5f6-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a5f6-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="5a5f6-124">Schema name</span></span>  <br/> |<span data-ttu-id="5a5f6-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="5a5f6-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a5f6-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="5a5f6-126">Validation file</span></span>  <br/> |<span data-ttu-id="5a5f6-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5a5f6-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a5f6-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="5a5f6-128">Can be empty</span></span>  <br/> |<span data-ttu-id="5a5f6-129">false</span><span class="sxs-lookup"><span data-stu-id="5a5f6-129">false</span></span>  <br/> |
   

