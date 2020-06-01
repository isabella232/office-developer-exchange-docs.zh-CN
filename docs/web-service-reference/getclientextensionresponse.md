---
title: GetClientExtensionResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ef4b1aba-a55d-4d64-ac80-5d4e6c4e72bd
description: GetClientExtensionResponse 元素包含获取有关应用程序的配置信息的响应。
ms.openlocfilehash: 65c1995fe75b3894607d27ed65548fbbdce0664a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459516"
---
# <a name="getclientextensionresponse"></a><span data-ttu-id="d79dc-103">GetClientExtensionResponse</span><span class="sxs-lookup"><span data-stu-id="d79dc-103">GetClientExtensionResponse</span></span>

<span data-ttu-id="d79dc-104">**GetClientExtensionResponse**元素包含获取有关应用程序的配置信息的响应。</span><span class="sxs-lookup"><span data-stu-id="d79dc-104">The **GetClientExtensionResponse** element contains the response to get configuration information about an app.</span></span> 
  
```XML
<GetClientExtensionResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <ClientExtensions/>
   <RawMasterTableXml/>
</GetClientExtensionResponse>
```

 <span data-ttu-id="d79dc-105">**ClientExtensionResponseType**</span><span class="sxs-lookup"><span data-stu-id="d79dc-105">**ClientExtensionResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d79dc-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d79dc-106">Attributes and elements</span></span>

<span data-ttu-id="d79dc-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d79dc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d79dc-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="d79dc-108">Attributes</span></span>

<span data-ttu-id="d79dc-109">无。</span><span class="sxs-lookup"><span data-stu-id="d79dc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d79dc-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d79dc-110">Child elements</span></span>

<span data-ttu-id="d79dc-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [ClientExtensions](clientextensions.md)  | [RawMasterTableXml](rawmastertablexml.md)</span><span class="sxs-lookup"><span data-stu-id="d79dc-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [ClientExtensions](clientextensions.md) | [RawMasterTableXml](rawmastertablexml.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d79dc-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d79dc-112">Parent elements</span></span>

<span data-ttu-id="d79dc-113">无。</span><span class="sxs-lookup"><span data-stu-id="d79dc-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d79dc-114">说明</span><span class="sxs-lookup"><span data-stu-id="d79dc-114">Remarks</span></span>

<span data-ttu-id="d79dc-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d79dc-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d79dc-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d79dc-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d79dc-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="d79dc-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d79dc-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="d79dc-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d79dc-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="d79dc-119">Schema name</span></span>  <br/> |<span data-ttu-id="d79dc-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="d79dc-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d79dc-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="d79dc-121">Validation file</span></span>  <br/> |<span data-ttu-id="d79dc-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d79dc-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d79dc-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="d79dc-123">Can be empty</span></span>  <br/> |<span data-ttu-id="d79dc-124">false</span><span class="sxs-lookup"><span data-stu-id="d79dc-124">false</span></span>  <br/> |
   

