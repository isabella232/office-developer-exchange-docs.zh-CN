---
title: 请求（GetFederationInformation）（SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: Request 元素表示 GetFederationInformationRequest （SOAP）请求。
ms.openlocfilehash: dbd88537d03f6325cf0025d08c63ae486544d705
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459579"
---
# <a name="request-getfederationinformation-soap"></a><span data-ttu-id="f141d-103">请求（GetFederationInformation）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="f141d-103">Request (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="f141d-104">**Request**元素表示[GetFederationInformationRequest （SOAP）](getfederationinformationrequest-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="f141d-104">The **Request** element represents a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) request.</span></span> 
  
```XML
<Request>
   <Domain/>
</Request>
```

 <span data-ttu-id="f141d-105">**GetFederationInformationRequest**</span><span class="sxs-lookup"><span data-stu-id="f141d-105">**GetFederationInformationRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f141d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f141d-106">Attributes and elements</span></span>

<span data-ttu-id="f141d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f141d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f141d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f141d-108">Attributes</span></span>

<span data-ttu-id="f141d-109">无。</span><span class="sxs-lookup"><span data-stu-id="f141d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f141d-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f141d-110">Child elements</span></span>

|<span data-ttu-id="f141d-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f141d-111">**Element**</span></span>|<span data-ttu-id="f141d-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f141d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f141d-113">Domain （GetFederationInformation）（SOAP）</span><span class="sxs-lookup"><span data-stu-id="f141d-113">Domain (GetFederationInformation) (SOAP)</span></span>](domain-getfederationinformationsoap.md) <br/> |<span data-ttu-id="f141d-114">标识具有联合身份验证信任的域。</span><span class="sxs-lookup"><span data-stu-id="f141d-114">Identifies the domain that has a federation trust.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f141d-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f141d-115">Parent elements</span></span>

|<span data-ttu-id="f141d-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f141d-116">**Element**</span></span>|<span data-ttu-id="f141d-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f141d-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f141d-118">GetFederationInformationRequestMessage （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f141d-118">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md) <br/> |<span data-ttu-id="f141d-119">准备对服务器的调用，以请求安全令牌服务（STS）的配置数据。</span><span class="sxs-lookup"><span data-stu-id="f141d-119">Prepares a call to the server to request configuration data for the security token service (STS).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="f141d-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="f141d-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f141d-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="f141d-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f141d-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="f141d-122">Schema Name</span></span>  <br/> |<span data-ttu-id="f141d-123">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f141d-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f141d-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="f141d-124">Validation File</span></span>  <br/> |<span data-ttu-id="f141d-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f141d-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f141d-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="f141d-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="f141d-127">True</span><span class="sxs-lookup"><span data-stu-id="f141d-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f141d-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f141d-128">See also</span></span>



[<span data-ttu-id="f141d-129">使用自动发现</span><span class="sxs-lookup"><span data-stu-id="f141d-129">Working with Autodiscover</span></span>](https://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

