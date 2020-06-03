---
title: TokenType （ClientAccessTokenType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96103f15-a3e0-497c-af21-90adbf9a4b14
description: TokenType 元素标识将在 GetClientAccessToken 响应中返回的客户端访问令牌的类型。
ms.openlocfilehash: 49ba2973967b12396e0c7f56129c89c40ccbcf97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466050"
---
# <a name="tokentype-clientaccesstokentype"></a><span data-ttu-id="07bf0-103">TokenType （ClientAccessTokenType）</span><span class="sxs-lookup"><span data-stu-id="07bf0-103">TokenType (ClientAccessTokenType)</span></span>

<span data-ttu-id="07bf0-104">**TokenType**元素标识将在**GetClientAccessToken**响应中返回的客户端访问令牌的类型。</span><span class="sxs-lookup"><span data-stu-id="07bf0-104">The **TokenType** element identifies the type of client access token that will be returned in the **GetClientAccessToken** response.</span></span> 
  
```XML
<TokenType>CallerIdentity | ExtensionCallback | ScopedToken</TokenType>
```

 <span data-ttu-id="07bf0-105">**ClientAccessTokenTypeType**</span><span class="sxs-lookup"><span data-stu-id="07bf0-105">**ClientAccessTokenTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07bf0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="07bf0-106">Attributes and elements</span></span>

<span data-ttu-id="07bf0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="07bf0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07bf0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="07bf0-108">Attributes</span></span>

<span data-ttu-id="07bf0-109">无。</span><span class="sxs-lookup"><span data-stu-id="07bf0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07bf0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="07bf0-110">Child elements</span></span>

<span data-ttu-id="07bf0-111">无。</span><span class="sxs-lookup"><span data-stu-id="07bf0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="07bf0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="07bf0-112">Parent elements</span></span>

<span data-ttu-id="07bf0-113">[TokenRequest](tokenrequest.md)  | [令牌（ClientAccessTokenType）](token-clientaccesstokentype.md)</span><span class="sxs-lookup"><span data-stu-id="07bf0-113">[TokenRequest](tokenrequest.md) | [Token (ClientAccessTokenType)](token-clientaccesstokentype.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="07bf0-114">文本值</span><span class="sxs-lookup"><span data-stu-id="07bf0-114">Text value</span></span>

<span data-ttu-id="07bf0-115">**CallerIdentity**的文本值表示返回调用方标识客户端访问令牌。</span><span class="sxs-lookup"><span data-stu-id="07bf0-115">A text value of **CallerIdentity** means a caller identity client access token is returned.</span></span> <span data-ttu-id="07bf0-116">**ExtensionCallback**的文本值表示返回一个扩展回调客户端访问令牌。</span><span class="sxs-lookup"><span data-stu-id="07bf0-116">A text value of **ExtensionCallback** indicates that an extension callback client access token is returned.</span></span> <span data-ttu-id="07bf0-117">**ScopedToken**的文本值指示客户端访问令牌是作用域内的令牌。</span><span class="sxs-lookup"><span data-stu-id="07bf0-117">A text value of **ScopedToken** indicates that the client access token is a scoped token.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="07bf0-118">备注</span><span class="sxs-lookup"><span data-stu-id="07bf0-118">Remarks</span></span>

<span data-ttu-id="07bf0-119">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="07bf0-119">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="07bf0-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="07bf0-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07bf0-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="07bf0-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07bf0-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="07bf0-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="07bf0-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="07bf0-123">Schema name</span></span>  <br/> |<span data-ttu-id="07bf0-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="07bf0-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="07bf0-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="07bf0-125">Validation file</span></span>  <br/> |<span data-ttu-id="07bf0-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="07bf0-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="07bf0-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="07bf0-127">Can be empty</span></span>  <br/> |<span data-ttu-id="07bf0-128">false</span><span class="sxs-lookup"><span data-stu-id="07bf0-128">false</span></span>  <br/> |
   

