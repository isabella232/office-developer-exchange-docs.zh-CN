---
title: ProtocolConnection （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6eef2188-6194-48f1-ad7e-46104aecdf56
description: ProtocolConnection 元素表示服务器 Web 客户端的协议连接。
ms.openlocfilehash: b9df3febe36db53d7c5bf0610ba857f13aa96abc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528858"
---
# <a name="protocolconnection-soap"></a><span data-ttu-id="61579-103">ProtocolConnection （SOAP）</span><span class="sxs-lookup"><span data-stu-id="61579-103">ProtocolConnection (SOAP)</span></span>

<span data-ttu-id="61579-104">**ProtocolConnection**元素表示服务器 Web 客户端的协议连接。</span><span class="sxs-lookup"><span data-stu-id="61579-104">The **ProtocolConnection** element represents the protocol connection of the server Web client.</span></span> 
  
```XML
<ProtocolConnection>
   <Hostname/>
   <Port/>
   <EncryptionMethod/>
</ProtocolConnection>
```

 <span data-ttu-id="61579-105">**ProtocolConnection**</span><span class="sxs-lookup"><span data-stu-id="61579-105">**ProtocolConnection**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61579-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="61579-106">Attributes and elements</span></span>

<span data-ttu-id="61579-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="61579-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61579-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="61579-108">Attributes</span></span>

<span data-ttu-id="61579-109">无。</span><span class="sxs-lookup"><span data-stu-id="61579-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61579-110">子元素</span><span class="sxs-lookup"><span data-stu-id="61579-110">Child elements</span></span>

|<span data-ttu-id="61579-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="61579-111">**Element**</span></span>|<span data-ttu-id="61579-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="61579-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61579-113">Hostname （SOAP）</span><span class="sxs-lookup"><span data-stu-id="61579-113">Hostname (SOAP)</span></span>](hostname-soap.md) <br/> |<span data-ttu-id="61579-114">表示计算机的完整计算机名称的主机名部分。</span><span class="sxs-lookup"><span data-stu-id="61579-114">Represents the host name portion of the full computer name of the computer.</span></span>  <br/> |
|[<span data-ttu-id="61579-115">端口（SOAP）</span><span class="sxs-lookup"><span data-stu-id="61579-115">Port (SOAP)</span></span>](port-soap.md) <br/> |<span data-ttu-id="61579-116">表示要用于协议的端口号。</span><span class="sxs-lookup"><span data-stu-id="61579-116">Represents the port number to use for the protocol.</span></span>  <br/> |
|[<span data-ttu-id="61579-117">EncryptionMethod （SOAP）</span><span class="sxs-lookup"><span data-stu-id="61579-117">EncryptionMethod (SOAP)</span></span>](encryptionmethod-soap.md) <br/> |<span data-ttu-id="61579-118">表示用于 POP、IMAP 和 SMTP 协议的加密方法。</span><span class="sxs-lookup"><span data-stu-id="61579-118">Represents the cryptographic method that is used for the POP, IMAP, and SMTP protocols.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61579-119">父元素</span><span class="sxs-lookup"><span data-stu-id="61579-119">Parent elements</span></span>

|<span data-ttu-id="61579-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="61579-120">**Element**</span></span>|<span data-ttu-id="61579-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="61579-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61579-122">ProtocolConnections （SOAP）</span><span class="sxs-lookup"><span data-stu-id="61579-122">ProtocolConnections (SOAP)</span></span>](protocolconnections-soap.md) <br/> |<span data-ttu-id="61579-123">包含零个或多个协议连接。</span><span class="sxs-lookup"><span data-stu-id="61579-123">Contains zero or more protocol connections.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="61579-124">文本值</span><span class="sxs-lookup"><span data-stu-id="61579-124">Text value</span></span>

<span data-ttu-id="61579-125">无。</span><span class="sxs-lookup"><span data-stu-id="61579-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61579-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="61579-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61579-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="61579-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="61579-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="61579-128">Schema Name</span></span>  <br/> |<span data-ttu-id="61579-129">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="61579-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="61579-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="61579-130">Validation File</span></span>  <br/> |<span data-ttu-id="61579-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="61579-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61579-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="61579-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="61579-133">True</span><span class="sxs-lookup"><span data-stu-id="61579-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61579-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61579-134">See also</span></span>



[<span data-ttu-id="61579-135">ProtocolConnectionCollectionSetting （SOAP）</span><span class="sxs-lookup"><span data-stu-id="61579-135">ProtocolConnectionCollectionSetting (SOAP)</span></span>](protocolconnectioncollectionsetting-soap.md)

