---
title: TokenType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83c650eb-7ab8-480c-a7c9-df60072ee042
description: TokenType 元素指定令牌的类型。
ms.openlocfilehash: a42849dce9ed0253c3c5d4d4e899367b8e105594
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459880"
---
# <a name="tokentype"></a><span data-ttu-id="9b819-103">TokenType</span><span class="sxs-lookup"><span data-stu-id="9b819-103">TokenType</span></span>

<span data-ttu-id="9b819-104">**TokenType**元素指定令牌的类型。</span><span class="sxs-lookup"><span data-stu-id="9b819-104">The **TokenType** element specifies the type of token.</span></span> 
  
```XML
<TokenType> CallerIdentity | ExtensionCallback | ScopedToken </TokenType>
```

 <span data-ttu-id="9b819-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="9b819-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9b819-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9b819-106">Attributes and elements</span></span>

<span data-ttu-id="9b819-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9b819-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9b819-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="9b819-108">Attributes</span></span>

<span data-ttu-id="9b819-109">无。</span><span class="sxs-lookup"><span data-stu-id="9b819-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9b819-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9b819-110">Child elements</span></span>

<span data-ttu-id="9b819-111">无。</span><span class="sxs-lookup"><span data-stu-id="9b819-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9b819-112">父元素</span><span class="sxs-lookup"><span data-stu-id="9b819-112">Parent elements</span></span>

<span data-ttu-id="9b819-113">[TokenRequest](tokenrequest.md)  | [令牌](token.md)</span><span class="sxs-lookup"><span data-stu-id="9b819-113">[TokenRequest](tokenrequest.md) | [Token](token.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="9b819-114">文本值</span><span class="sxs-lookup"><span data-stu-id="9b819-114">Text value</span></span>

<span data-ttu-id="9b819-115">**TokenType**元素的文本值为令牌类型。</span><span class="sxs-lookup"><span data-stu-id="9b819-115">The text value of the **TokenType** element is the token type.</span></span> <span data-ttu-id="9b819-116">**CallerIdentity**的文本值指示令牌是调用方标识令牌。</span><span class="sxs-lookup"><span data-stu-id="9b819-116">The text value of **CallerIdentity** indicates that the token is a caller identity token.</span></span> <span data-ttu-id="9b819-117">**ExtensionCallback**的文本值指示令牌适用于扩展回调。</span><span class="sxs-lookup"><span data-stu-id="9b819-117">The text value of **ExtensionCallback** indicates that the token is for an extension callback.</span></span> <span data-ttu-id="9b819-118">**ScopedToken**的文本值指示客户端访问令牌是作用域内的令牌。</span><span class="sxs-lookup"><span data-stu-id="9b819-118">The text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9b819-119">备注</span><span class="sxs-lookup"><span data-stu-id="9b819-119">Remarks</span></span>

<span data-ttu-id="9b819-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9b819-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9b819-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9b819-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9b819-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="9b819-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9b819-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="9b819-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9b819-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="9b819-124">Schema name</span></span>  <br/> |<span data-ttu-id="9b819-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="9b819-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="9b819-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="9b819-126">Validation file</span></span>  <br/> |<span data-ttu-id="9b819-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9b819-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9b819-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="9b819-128">Can be empty</span></span>  <br/> |<span data-ttu-id="9b819-129">false</span><span class="sxs-lookup"><span data-stu-id="9b819-129">false</span></span>  <br/> |
   

