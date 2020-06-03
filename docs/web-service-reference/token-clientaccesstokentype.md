---
title: 令牌（ClientAccessTokenType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cddd6075-06b6-4858-9ffa-9db4d9d9b030
description: Token 元素指定客户端访问令牌。
ms.openlocfilehash: d195e81d8d20eb2288e921c640c7b2898a5341ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467863"
---
# <a name="token-clientaccesstokentype"></a><span data-ttu-id="121b5-103">令牌（ClientAccessTokenType）</span><span class="sxs-lookup"><span data-stu-id="121b5-103">Token (ClientAccessTokenType)</span></span>

<span data-ttu-id="121b5-104">**Token**元素指定客户端访问令牌。</span><span class="sxs-lookup"><span data-stu-id="121b5-104">The **Token** element specifies a client access token.</span></span> 
  
```XML
<Token>
   <Id/>
   <TokenType/>
   <TokenValue/>
   <TTL/>
</Token>
```

 <span data-ttu-id="121b5-105">**ClientAccessTokenType**</span><span class="sxs-lookup"><span data-stu-id="121b5-105">**ClientAccessTokenType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="121b5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="121b5-106">Attributes and elements</span></span>

<span data-ttu-id="121b5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="121b5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="121b5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="121b5-108">Attributes</span></span>

<span data-ttu-id="121b5-109">无。</span><span class="sxs-lookup"><span data-stu-id="121b5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="121b5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="121b5-110">Child elements</span></span>

<span data-ttu-id="121b5-111">[ID （字符串）](id-string.md)  | [TokenType](tokentype.md)  | [TokenValue](tokenvalue.md)  | [TTL](ttl.md)</span><span class="sxs-lookup"><span data-stu-id="121b5-111">[ID (String)](id-string.md) | [TokenType](tokentype.md) | [TokenValue](tokenvalue.md) | [TTL](ttl.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="121b5-112">父元素</span><span class="sxs-lookup"><span data-stu-id="121b5-112">Parent elements</span></span>

[<span data-ttu-id="121b5-113">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="121b5-113">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="121b5-114">备注</span><span class="sxs-lookup"><span data-stu-id="121b5-114">Remarks</span></span>

<span data-ttu-id="121b5-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="121b5-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="121b5-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="121b5-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="121b5-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="121b5-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="121b5-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="121b5-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="121b5-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="121b5-119">Schema name</span></span>  <br/> |<span data-ttu-id="121b5-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="121b5-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="121b5-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="121b5-121">Validation file</span></span>  <br/> |<span data-ttu-id="121b5-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="121b5-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="121b5-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="121b5-123">Can be empty</span></span>  <br/> ||
   

