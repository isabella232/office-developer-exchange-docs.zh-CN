---
title: MarkAsJunkResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e2b7b53-ef3c-438e-93df-b08409dbab46
description: MarkAsJunkResponseMessage 元素指定 MarkAsJunk 请求的响应消息。
ms.openlocfilehash: 146ece430436c60fced53d4dfbfd7d92c0e42e98
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826352"
---
# <a name="markasjunkresponsemessage"></a><span data-ttu-id="d4abf-103">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d4abf-103">MarkAsJunkResponseMessage</span></span>

<span data-ttu-id="d4abf-104">**MarkAsJunkResponseMessage**元素指定**MarkAsJunk**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="d4abf-104">The **MarkAsJunkResponseMessage** element specifies the response message for a **MarkAsJunk** request.</span></span> 
  
```XML
<MarkAsJunkResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MovedItemId/>
</MarkAsJunkResponseMessage>
```

 <span data-ttu-id="d4abf-105">**MarkAsJunkResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="d4abf-105">**MarkAsJunkResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4abf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d4abf-106">Attributes and elements</span></span>

<span data-ttu-id="d4abf-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d4abf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4abf-108">属性</span><span class="sxs-lookup"><span data-stu-id="d4abf-108">Attributes</span></span>

<span data-ttu-id="d4abf-109">无。</span><span class="sxs-lookup"><span data-stu-id="d4abf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4abf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d4abf-110">Child elements</span></span>

<span data-ttu-id="d4abf-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MovedItemId](moveditemid.md)</span><span class="sxs-lookup"><span data-stu-id="d4abf-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MovedItemId](moveditemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d4abf-112">父元素</span><span class="sxs-lookup"><span data-stu-id="d4abf-112">Parent elements</span></span>

[<span data-ttu-id="d4abf-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="d4abf-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="d4abf-114">备注</span><span class="sxs-lookup"><span data-stu-id="d4abf-114">Remarks</span></span>

<span data-ttu-id="d4abf-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="d4abf-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d4abf-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d4abf-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4abf-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="d4abf-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4abf-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="d4abf-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d4abf-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="d4abf-119">Schema name</span></span>  <br/> |<span data-ttu-id="d4abf-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="d4abf-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="d4abf-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="d4abf-121">Validation file</span></span>  <br/> |<span data-ttu-id="d4abf-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d4abf-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d4abf-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="d4abf-123">Can be empty</span></span>  <br/> ||
   

