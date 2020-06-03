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
ms.openlocfilehash: 23d1c5b7a61a9161d7383ec8b38cd0ebbebfc8cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460972"
---
# <a name="getdiscoverysearchconfigurationresponsemessage"></a><span data-ttu-id="8deb3-103">GetDiscoverySearchConfigurationResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8deb3-103">GetDiscoverySearchConfigurationResponseMessage</span></span>

<span data-ttu-id="8deb3-104">**GetDiscoverySearchConfigurationResponseMessage**元素指定**GetDiscoverySearchConfiguration**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="8deb3-104">The **GetDiscoverySearchConfigurationResponseMessage** element specifies the response message for a **GetDiscoverySearchConfiguration** request.</span></span> 
  
```XML
<GetDiscoverySearchConfigurationResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DiscoverySearchConfigurations/>
</GetDiscoverySearchConfigurationResponseMessage>
```

 <span data-ttu-id="8deb3-105">**GetDiscoverySearchConfigurationResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="8deb3-105">**GetDiscoverySearchConfigurationResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8deb3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8deb3-106">Attributes and elements</span></span>

<span data-ttu-id="8deb3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8deb3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8deb3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8deb3-108">Attributes</span></span>

<span data-ttu-id="8deb3-109">无。</span><span class="sxs-lookup"><span data-stu-id="8deb3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8deb3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8deb3-110">Child elements</span></span>

<span data-ttu-id="8deb3-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span><span class="sxs-lookup"><span data-stu-id="8deb3-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [DiscoverySearchConfigurations](discoverysearchconfigurations.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8deb3-112">父元素</span><span class="sxs-lookup"><span data-stu-id="8deb3-112">Parent elements</span></span>

[<span data-ttu-id="8deb3-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="8deb3-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="8deb3-114">备注</span><span class="sxs-lookup"><span data-stu-id="8deb3-114">Remarks</span></span>

<span data-ttu-id="8deb3-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8deb3-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="8deb3-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8deb3-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8deb3-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="8deb3-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8deb3-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="8deb3-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8deb3-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="8deb3-119">Schema name</span></span>  <br/> |<span data-ttu-id="8deb3-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="8deb3-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8deb3-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="8deb3-121">Validation file</span></span>  <br/> |<span data-ttu-id="8deb3-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8deb3-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8deb3-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="8deb3-123">Can be empty</span></span>  <br/> |<span data-ttu-id="8deb3-124">false</span><span class="sxs-lookup"><span data-stu-id="8deb3-124">false</span></span>  <br/> |
   

