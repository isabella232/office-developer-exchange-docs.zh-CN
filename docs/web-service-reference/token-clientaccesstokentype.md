---
title: 令牌 (ClientAccessTokenType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cddd6075-06b6-4858-9ffa-9db4d9d9b030
description: 令牌元素指定的客户端访问令牌。
ms.openlocfilehash: 2e1f401141aef07a57a214968f6a6bafdf71f0dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838251"
---
# <a name="token-clientaccesstokentype"></a><span data-ttu-id="ca99f-103">令牌 (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="ca99f-103">Token (ClientAccessTokenType)</span></span>

<span data-ttu-id="ca99f-104">**令牌**元素指定的客户端访问令牌。</span><span class="sxs-lookup"><span data-stu-id="ca99f-104">The **Token** element specifies a client access token.</span></span> 
  
```XML
<Token>
   <Id/>
   <TokenType/>
   <TokenValue/>
   <TTL/>
</Token>
```

 <span data-ttu-id="ca99f-105">**ClientAccessTokenType**</span><span class="sxs-lookup"><span data-stu-id="ca99f-105">**ClientAccessTokenType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ca99f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ca99f-106">Attributes and elements</span></span>

<span data-ttu-id="ca99f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ca99f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca99f-108">属性</span><span class="sxs-lookup"><span data-stu-id="ca99f-108">Attributes</span></span>

<span data-ttu-id="ca99f-109">无。</span><span class="sxs-lookup"><span data-stu-id="ca99f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ca99f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ca99f-110">Child elements</span></span>

<span data-ttu-id="ca99f-111">[ID （字符串）](id-string.md) | [TokenType](tokentype.md) | [TokenValue](tokenvalue.md) | [TTL](ttl.md)</span><span class="sxs-lookup"><span data-stu-id="ca99f-111">[ID (String)](id-string.md) | [TokenType](tokentype.md) | [TokenValue](tokenvalue.md) | [TTL](ttl.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ca99f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ca99f-112">Parent elements</span></span>

[<span data-ttu-id="ca99f-113">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ca99f-113">GetClientAccessTokenResponseMessage</span></span>](getclientaccesstokenresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="ca99f-114">备注</span><span class="sxs-lookup"><span data-stu-id="ca99f-114">Remarks</span></span>

<span data-ttu-id="ca99f-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ca99f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ca99f-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ca99f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca99f-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="ca99f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca99f-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="ca99f-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ca99f-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="ca99f-119">Schema name</span></span>  <br/> |<span data-ttu-id="ca99f-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="ca99f-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="ca99f-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="ca99f-121">Validation file</span></span>  <br/> |<span data-ttu-id="ca99f-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ca99f-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ca99f-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="ca99f-123">Can be empty</span></span>  <br/> ||
   

