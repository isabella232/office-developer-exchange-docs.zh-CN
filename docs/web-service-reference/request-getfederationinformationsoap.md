---
title: 请求 (GetFederationInformation) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: beeb5371-f57b-4346-9753-035dd42c6bee
description: 请求元素均表示一个 GetFederationInformationRequest (SOAP) 请求。
ms.openlocfilehash: 0fb9301c2f318aa2c27155675dd3c43b41aabecd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827119"
---
# <a name="request-getfederationinformation-soap"></a><span data-ttu-id="d0ff3-103">请求 (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d0ff3-103">Request (GetFederationInformation) (SOAP)</span></span>

<span data-ttu-id="d0ff3-104">**请求**元素均表示一个[GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md)请求。</span><span class="sxs-lookup"><span data-stu-id="d0ff3-104">The **Request** element represents a [GetFederationInformationRequest (SOAP)](getfederationinformationrequest-soap.md) request.</span></span> 
  
```XML
<Request>
   <Domain/>
</Request>
```

 <span data-ttu-id="d0ff3-105">**GetFederationInformationRequest**</span><span class="sxs-lookup"><span data-stu-id="d0ff3-105">**GetFederationInformationRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0ff3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d0ff3-106">Attributes and elements</span></span>

<span data-ttu-id="d0ff3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d0ff3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0ff3-108">属性</span><span class="sxs-lookup"><span data-stu-id="d0ff3-108">Attributes</span></span>

<span data-ttu-id="d0ff3-109">无。</span><span class="sxs-lookup"><span data-stu-id="d0ff3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0ff3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d0ff3-110">Child elements</span></span>

|<span data-ttu-id="d0ff3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d0ff3-111">**Element**</span></span>|<span data-ttu-id="d0ff3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d0ff3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0ff3-113">域 (GetFederationInformation) (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d0ff3-113">Domain (GetFederationInformation) (SOAP)</span></span>](domain-getfederationinformationsoap.md) <br/> |<span data-ttu-id="d0ff3-114">标识了联合身份验证信任的域。</span><span class="sxs-lookup"><span data-stu-id="d0ff3-114">Identifies the domain that has a federation trust.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0ff3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="d0ff3-115">Parent elements</span></span>

|<span data-ttu-id="d0ff3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="d0ff3-116">**Element**</span></span>|<span data-ttu-id="d0ff3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="d0ff3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0ff3-118">GetFederationInformationRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="d0ff3-118">GetFederationInformationRequestMessage (SOAP)</span></span>](getfederationinformationrequestmessage-soap.md) <br/> |<span data-ttu-id="d0ff3-119">为安全令牌服务 (STS) 准备调用请求配置数据的服务器。</span><span class="sxs-lookup"><span data-stu-id="d0ff3-119">Prepares a call to the server to request configuration data for the security token service (STS).</span></span>  <br/> |
   
## <a name="element-information"></a><span data-ttu-id="d0ff3-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="d0ff3-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0ff3-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="d0ff3-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="d0ff3-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="d0ff3-122">Schema Name</span></span>  <br/> |<span data-ttu-id="d0ff3-123">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="d0ff3-123">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="d0ff3-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="d0ff3-124">Validation File</span></span>  <br/> |<span data-ttu-id="d0ff3-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d0ff3-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d0ff3-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="d0ff3-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0ff3-127">True</span><span class="sxs-lookup"><span data-stu-id="d0ff3-127">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0ff3-128">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d0ff3-128">See also</span></span>



[<span data-ttu-id="d0ff3-129">使用自动发现</span><span class="sxs-lookup"><span data-stu-id="d0ff3-129">Working with Autodiscover</span></span>](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx)

