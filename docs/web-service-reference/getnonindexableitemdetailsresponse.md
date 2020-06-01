---
title: GetNonIndexableItemDetailsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6cf2aea3-c6f7-4cad-a45d-2daffeece4b6
description: GetNonIndexableItemDetailsResponse 元素指定对 GetNonIndexableItemDetails 请求的响应。
ms.openlocfilehash: 7563a772e04f72c50ddfea0a69fa511d2a538b8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455616"
---
# <a name="getnonindexableitemdetailsresponse"></a><span data-ttu-id="6c778-103">GetNonIndexableItemDetailsResponse</span><span class="sxs-lookup"><span data-stu-id="6c778-103">GetNonIndexableItemDetailsResponse</span></span>

<span data-ttu-id="6c778-104">**GetNonIndexableItemDetailsResponse**元素指定对**GetNonIndexableItemDetails**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="6c778-104">The **GetNonIndexableItemDetailsResponse** element specifies the response to a **GetNonIndexableItemDetails** request.</span></span> 
  
```XML
<GetNonIndexableItemDetailsResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <NonIndexableItemDetailsResult/>
</GetNonIndexableItemDetailsResponse>
```

 <span data-ttu-id="6c778-105">**GetNonIndexableItemDetailsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6c778-105">**GetNonIndexableItemDetailsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c778-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c778-106">Attributes and elements</span></span>

<span data-ttu-id="6c778-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c778-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c778-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6c778-108">Attributes</span></span>

<span data-ttu-id="6c778-109">无。</span><span class="sxs-lookup"><span data-stu-id="6c778-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c778-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6c778-110">Child elements</span></span>

<span data-ttu-id="6c778-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [NonIndexableItemDetailsResult](nonindexableitemdetailsresult.md)</span><span class="sxs-lookup"><span data-stu-id="6c778-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [NonIndexableItemDetailsResult](nonindexableitemdetailsresult.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6c778-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6c778-112">Parent elements</span></span>

[<span data-ttu-id="6c778-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6c778-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="6c778-114">备注</span><span class="sxs-lookup"><span data-stu-id="6c778-114">Remarks</span></span>

<span data-ttu-id="6c778-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6c778-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6c778-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6c778-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c778-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c778-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c778-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c778-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6c778-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c778-119">Schema name</span></span>  <br/> |<span data-ttu-id="6c778-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="6c778-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6c778-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c778-121">Validation file</span></span>  <br/> |<span data-ttu-id="6c778-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6c778-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c778-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c778-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6c778-124">false</span><span class="sxs-lookup"><span data-stu-id="6c778-124">false</span></span>  <br/> |
   

