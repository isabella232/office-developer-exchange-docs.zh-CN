---
title: GetClientExtensionResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ef4b1aba-a55d-4d64-ac80-5d4e6c4e72bd
description: GetClientExtensionResponse 元素包含响应获取应用程序的配置信息。
ms.openlocfilehash: 523a103ec9397b0dce08aa47b074303c9e6ac897
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754484"
---
# <a name="getclientextensionresponse"></a><span data-ttu-id="0ea00-103">GetClientExtensionResponse</span><span class="sxs-lookup"><span data-stu-id="0ea00-103">GetClientExtensionResponse</span></span>

<span data-ttu-id="0ea00-104">**GetClientExtensionResponse**元素包含响应获取应用程序的配置信息。</span><span class="sxs-lookup"><span data-stu-id="0ea00-104">The **GetClientExtensionResponse** element contains the response to get configuration information about an app.</span></span> 
  
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

 <span data-ttu-id="0ea00-105">**ClientExtensionResponseType**</span><span class="sxs-lookup"><span data-stu-id="0ea00-105">**ClientExtensionResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0ea00-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0ea00-106">Attributes and elements</span></span>

<span data-ttu-id="0ea00-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0ea00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ea00-108">属性</span><span class="sxs-lookup"><span data-stu-id="0ea00-108">Attributes</span></span>

<span data-ttu-id="0ea00-109">无。</span><span class="sxs-lookup"><span data-stu-id="0ea00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0ea00-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0ea00-110">Child elements</span></span>

<span data-ttu-id="0ea00-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [ClientExtensions](clientextensions.md) | [RawMasterTableXml](rawmastertablexml.md)</span><span class="sxs-lookup"><span data-stu-id="0ea00-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [ClientExtensions](clientextensions.md) | [RawMasterTableXml](rawmastertablexml.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0ea00-112">父元素</span><span class="sxs-lookup"><span data-stu-id="0ea00-112">Parent elements</span></span>

<span data-ttu-id="0ea00-113">无。</span><span class="sxs-lookup"><span data-stu-id="0ea00-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ea00-114">备注</span><span class="sxs-lookup"><span data-stu-id="0ea00-114">Remarks</span></span>

<span data-ttu-id="0ea00-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="0ea00-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="0ea00-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0ea00-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0ea00-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="0ea00-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ea00-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="0ea00-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0ea00-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="0ea00-119">Schema name</span></span>  <br/> |<span data-ttu-id="0ea00-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="0ea00-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0ea00-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="0ea00-121">Validation file</span></span>  <br/> |<span data-ttu-id="0ea00-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0ea00-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0ea00-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="0ea00-123">Can be empty</span></span>  <br/> |<span data-ttu-id="0ea00-124">false</span><span class="sxs-lookup"><span data-stu-id="0ea00-124">false</span></span>  <br/> |
   

