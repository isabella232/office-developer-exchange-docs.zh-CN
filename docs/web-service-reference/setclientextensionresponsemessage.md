---
title: SetClientExtensionResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3365e58c-adb3-4d92-92cc-acc95ce36cca
description: SetClientExtensionResponseMessage 元素指定 SetClientExtension 请求的响应消息。
ms.openlocfilehash: 29d126c84f2db6f9c674a5840547451847442e15
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827405"
---
# <a name="setclientextensionresponsemessage"></a><span data-ttu-id="1b197-103">SetClientExtensionResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1b197-103">SetClientExtensionResponseMessage</span></span>

<span data-ttu-id="1b197-104">**SetClientExtensionResponseMessage**元素指定**SetClientExtension**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="1b197-104">The **SetClientExtensionResponseMessage** element specifies the response message for a **SetClientExtension** request.</span></span> 
  
```XML
<SetClientExtensionResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</SetClientExtensionResponseMessage>
```

 <span data-ttu-id="1b197-105">**ResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1b197-105">**ResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b197-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1b197-106">Attributes and elements</span></span>

<span data-ttu-id="1b197-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1b197-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b197-108">属性</span><span class="sxs-lookup"><span data-stu-id="1b197-108">Attributes</span></span>

<span data-ttu-id="1b197-109">无。</span><span class="sxs-lookup"><span data-stu-id="1b197-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b197-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1b197-110">Child elements</span></span>

<span data-ttu-id="1b197-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md)</span><span class="sxs-lookup"><span data-stu-id="1b197-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b197-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1b197-112">Parent elements</span></span>

[<span data-ttu-id="1b197-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="1b197-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="1b197-114">备注</span><span class="sxs-lookup"><span data-stu-id="1b197-114">Remarks</span></span>

<span data-ttu-id="1b197-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1b197-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1b197-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1b197-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b197-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1b197-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b197-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1b197-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1b197-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1b197-119">Schema name</span></span>  <br/> |<span data-ttu-id="1b197-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="1b197-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1b197-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1b197-121">Validation file</span></span>  <br/> |<span data-ttu-id="1b197-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1b197-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1b197-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1b197-123">Can be empty</span></span>  <br/> ||
   
