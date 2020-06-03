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
ms.openlocfilehash: be03fc964b56c463320f09e68d143a0377300f5c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460097"
---
# <a name="markasjunkresponsemessage"></a><span data-ttu-id="e8fac-103">MarkAsJunkResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e8fac-103">MarkAsJunkResponseMessage</span></span>

<span data-ttu-id="e8fac-104">**MarkAsJunkResponseMessage**元素指定**MarkAsJunk**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="e8fac-104">The **MarkAsJunkResponseMessage** element specifies the response message for a **MarkAsJunk** request.</span></span> 
  
```XML
<MarkAsJunkResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MovedItemId/>
</MarkAsJunkResponseMessage>
```

 <span data-ttu-id="e8fac-105">**MarkAsJunkResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="e8fac-105">**MarkAsJunkResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8fac-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e8fac-106">Attributes and elements</span></span>

<span data-ttu-id="e8fac-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e8fac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8fac-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e8fac-108">Attributes</span></span>

<span data-ttu-id="e8fac-109">无。</span><span class="sxs-lookup"><span data-stu-id="e8fac-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8fac-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e8fac-110">Child elements</span></span>

<span data-ttu-id="e8fac-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [MovedItemId](moveditemid.md)</span><span class="sxs-lookup"><span data-stu-id="e8fac-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [MovedItemId](moveditemid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8fac-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e8fac-112">Parent elements</span></span>

[<span data-ttu-id="e8fac-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e8fac-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="e8fac-114">备注</span><span class="sxs-lookup"><span data-stu-id="e8fac-114">Remarks</span></span>

<span data-ttu-id="e8fac-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e8fac-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e8fac-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e8fac-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8fac-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="e8fac-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8fac-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="e8fac-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e8fac-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="e8fac-119">Schema name</span></span>  <br/> |<span data-ttu-id="e8fac-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="e8fac-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e8fac-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="e8fac-121">Validation file</span></span>  <br/> |<span data-ttu-id="e8fac-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="e8fac-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8fac-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="e8fac-123">Can be empty</span></span>  <br/> ||
   

