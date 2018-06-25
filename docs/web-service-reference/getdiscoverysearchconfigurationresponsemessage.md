---
title: GetDiscoverySearchConfigurationResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1b84a4c6-cb0a-4bca-85b2-fec32227930b
description: GetDiscoverySearchConfigurationResponseMessage 元素指定 GetDiscoverySearchConfiguration 请求的响应消息。
ms.openlocfilehash: a6cf09753031a7fd2eb46132e8bfb0729140d6c3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754519"
---
# <a name="getdiscoverysearchconfigurationresponsemessage"></a><span data-ttu-id="f7e49-103">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f7e49-103">GetDiscoverySearchConfigurationResponseMessage</span></span>

<span data-ttu-id="f7e49-104">**GetDiscoverySearchConfigurationResponseMessage**元素指定**GetDiscoverySearchConfiguration**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="f7e49-104">The **GetDiscoverySearchConfigurationResponseMessage** element specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span> 
  
```XML
<GetDiscoverySearchConfigurationResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DiscoverySearchConfigurations/>
</GetDiscoverySearchConfigurationResponseMessage>
```

 <span data-ttu-id="f7e49-105">**GetDiscoverySearchConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="f7e49-105">**GetDiscoverySearchConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7e49-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7e49-106">Attributes and elements</span></span>

<span data-ttu-id="f7e49-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7e49-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7e49-108">属性</span><span class="sxs-lookup"><span data-stu-id="f7e49-108">Attributes</span></span>

<span data-ttu-id="f7e49-109">无。</span><span class="sxs-lookup"><span data-stu-id="f7e49-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7e49-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f7e49-110">Child elements</span></span>

<span data-ttu-id="f7e49-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span><span class="sxs-lookup"><span data-stu-id="f7e49-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7e49-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f7e49-112">Parent elements</span></span>

[<span data-ttu-id="f7e49-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="f7e49-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="f7e49-114">备注</span><span class="sxs-lookup"><span data-stu-id="f7e49-114">Remarks</span></span>

<span data-ttu-id="f7e49-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="f7e49-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f7e49-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f7e49-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7e49-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7e49-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7e49-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7e49-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f7e49-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7e49-119">Schema name</span></span>  <br/> |<span data-ttu-id="f7e49-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="f7e49-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f7e49-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7e49-121">Validation file</span></span>  <br/> |<span data-ttu-id="f7e49-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f7e49-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7e49-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7e49-123">Can be empty</span></span>  <br/> |<span data-ttu-id="f7e49-124">false</span><span class="sxs-lookup"><span data-stu-id="f7e49-124">false</span></span>  <br/> |
   

