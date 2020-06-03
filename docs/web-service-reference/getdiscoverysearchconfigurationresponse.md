---
title: GetDiscoverySearchConfigurationResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d963e6c-e94d-462b-8c44-95d55c848fb2
description: GetDiscoverySearchConfigurationResponse 元素指定对 GetDiscoverySearchConfiguration 请求的响应。
ms.openlocfilehash: 98393943434b5e3460485b7d75c2b5285983f597
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460979"
---
# <a name="getdiscoverysearchconfigurationresponse"></a><span data-ttu-id="7cfb1-103">GetDiscoverySearchConfigurationResponse</span><span class="sxs-lookup"><span data-stu-id="7cfb1-103">GetDiscoverySearchConfigurationResponse</span></span>

<span data-ttu-id="7cfb1-104">**GetDiscoverySearchConfigurationResponse**元素指定对**GetDiscoverySearchConfiguration**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="7cfb1-104">The **GetDiscoverySearchConfigurationResponse** element specifies the response to a **GetDiscoverySearchConfiguration** request.</span></span> 
  
```XML
<GetDiscoverySearchConfigurationResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DiscoverySearchConfigurations/>
</GetDiscoverySearchConfigurationResponse>
```

 <span data-ttu-id="7cfb1-105">**GetDiscoverySearchConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="7cfb1-105">**GetDiscoverySearchConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cfb1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7cfb1-106">Attributes and elements</span></span>

<span data-ttu-id="7cfb1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7cfb1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cfb1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7cfb1-108">Attributes</span></span>

<span data-ttu-id="7cfb1-109">无。</span><span class="sxs-lookup"><span data-stu-id="7cfb1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cfb1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7cfb1-110">Child elements</span></span>

<span data-ttu-id="7cfb1-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span><span class="sxs-lookup"><span data-stu-id="7cfb1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7cfb1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7cfb1-112">Parent elements</span></span>

[<span data-ttu-id="7cfb1-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="7cfb1-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="7cfb1-114">备注</span><span class="sxs-lookup"><span data-stu-id="7cfb1-114">Remarks</span></span>

<span data-ttu-id="7cfb1-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7cfb1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7cfb1-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7cfb1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cfb1-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="7cfb1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cfb1-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="7cfb1-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7cfb1-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="7cfb1-119">Schema name</span></span>  <br/> |<span data-ttu-id="7cfb1-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="7cfb1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7cfb1-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="7cfb1-121">Validation file</span></span>  <br/> |<span data-ttu-id="7cfb1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7cfb1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7cfb1-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="7cfb1-123">Can be empty</span></span>  <br/> |<span data-ttu-id="7cfb1-124">false</span><span class="sxs-lookup"><span data-stu-id="7cfb1-124">false</span></span>  <br/> |
   

