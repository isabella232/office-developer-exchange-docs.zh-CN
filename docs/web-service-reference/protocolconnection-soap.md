---
title: ProtocolConnection (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: ProtocolConnection 元素均表示服务器 Web 客户端的协议连接。
ms.openlocfilehash: 8b5396821cd959e41d24fcf7a94c519f9c634a1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826915"
---
# <a name="protocolconnection-soap"></a><span data-ttu-id="405ef-103">ProtocolConnection (SOAP)</span><span class="sxs-lookup"><span data-stu-id="405ef-103">ProtocolConnection (SOAP)</span></span>

<span data-ttu-id="405ef-104">**ProtocolConnection**元素均表示服务器 Web 客户端的协议连接。</span><span class="sxs-lookup"><span data-stu-id="405ef-104">The **ProtocolConnection** element represents the protocol connection of the server Web client.</span></span> 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 <span data-ttu-id="405ef-105">**ProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="405ef-105">**ProtocolConnection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="405ef-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="405ef-106">Attributes and elements</span></span>

<span data-ttu-id="405ef-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="405ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="405ef-108">属性</span><span class="sxs-lookup"><span data-stu-id="405ef-108">Attributes</span></span>

<span data-ttu-id="405ef-109">无。</span><span class="sxs-lookup"><span data-stu-id="405ef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="405ef-110">子元素</span><span class="sxs-lookup"><span data-stu-id="405ef-110">Child elements</span></span>

|<span data-ttu-id="405ef-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="405ef-111">**Element**</span></span>|<span data-ttu-id="405ef-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="405ef-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="405ef-113">主机名 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="405ef-113">Hostname (SOAP)</span></span>](hostname-soap.md) <br/> |<span data-ttu-id="405ef-114">表示完整的计算机的计算机名称的主机名部分。</span><span class="sxs-lookup"><span data-stu-id="405ef-114">Represents the host name portion of the full computer name of the computer.</span></span>  <br/> |
|[<span data-ttu-id="405ef-115">端口 (SOAP)</span><span class="sxs-lookup"><span data-stu-id="405ef-115">Port (SOAP)</span></span>](port-soap.md) <br/> |<span data-ttu-id="405ef-116">代表要使用的协议的端口号。</span><span class="sxs-lookup"><span data-stu-id="405ef-116">Represents the port number to use for the protocol.</span></span>  <br/> |
|[<span data-ttu-id="405ef-117">EncryptionMethod (SOAP)</span><span class="sxs-lookup"><span data-stu-id="405ef-117">EncryptionMethod (SOAP)</span></span>](encryptionmethod-soap.md) <br/> |<span data-ttu-id="405ef-118">表示用于 POP、 IMAP 和 SMTP 协议的加密方法。</span><span class="sxs-lookup"><span data-stu-id="405ef-118">Represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="405ef-119">父元素</span><span class="sxs-lookup"><span data-stu-id="405ef-119">Parent elements</span></span>

|<span data-ttu-id="405ef-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="405ef-120">**Element**</span></span>|<span data-ttu-id="405ef-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="405ef-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="405ef-122">ProtocolConnections (SOAP)</span><span class="sxs-lookup"><span data-stu-id="405ef-122">ProtocolConnections (SOAP)</span></span>](protocolconnections-soap.md) <br/> |<span data-ttu-id="405ef-123">包含零个或多个协议连接。</span><span class="sxs-lookup"><span data-stu-id="405ef-123">Contains zero or more protocol connections.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="405ef-124">文本值</span><span class="sxs-lookup"><span data-stu-id="405ef-124">Text value</span></span>

<span data-ttu-id="405ef-125">无。</span><span class="sxs-lookup"><span data-stu-id="405ef-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="405ef-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="405ef-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="405ef-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="405ef-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="405ef-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="405ef-128">Schema Name</span></span>  <br/> |<span data-ttu-id="405ef-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="405ef-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="405ef-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="405ef-130">Validation File</span></span>  <br/> |<span data-ttu-id="405ef-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="405ef-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="405ef-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="405ef-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="405ef-133">True</span><span class="sxs-lookup"><span data-stu-id="405ef-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="405ef-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="405ef-134">See also</span></span>



[<span data-ttu-id="405ef-135">ProtocolConnectionCollectionSetting (SOAP)</span><span class="sxs-lookup"><span data-stu-id="405ef-135">ProtocolConnectionCollectionSetting (SOAP)</span></span>](protocolconnectioncollectionsetting-soap.md)

