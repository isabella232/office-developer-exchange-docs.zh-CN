---
title: PlayOnPhone （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 206a2ad1-a01d-4e71-99a1-90c2530423da
description: PlayOnPhone 元素定义一个请求，以在电话上播放某个项目。
ms.openlocfilehash: 9acbf9edbf4a889506558b24f5736a44d5015d3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44434076"
---
# <a name="playonphone-um-web-service"></a><span data-ttu-id="263d6-103">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="263d6-103">PlayOnPhone (UM web service)</span></span>

<span data-ttu-id="263d6-104">**PlayOnPhone**元素定义一个请求，以在电话上播放某个项目。</span><span class="sxs-lookup"><span data-stu-id="263d6-104">The **PlayOnPhone** element defines a request to play an item on a telephone.</span></span> 
  
[<span data-ttu-id="263d6-105">PlayOnPhone （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="263d6-105">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md)
  
```xml
<PlayOnPhone>
  <entryId>   </entryId>
  <DialString>   </DialString>
</PlayOnPhone>
```

 <span data-ttu-id="263d6-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="263d6-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="263d6-107">属性和元素</span><span class="sxs-lookup"><span data-stu-id="263d6-107">Attributes and elements</span></span>

<span data-ttu-id="263d6-108">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="263d6-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="263d6-109">Attributes</span><span class="sxs-lookup"><span data-stu-id="263d6-109">Attributes</span></span>

<span data-ttu-id="263d6-110">无。</span><span class="sxs-lookup"><span data-stu-id="263d6-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="263d6-111">子元素</span><span class="sxs-lookup"><span data-stu-id="263d6-111">Child elements</span></span>

|<span data-ttu-id="263d6-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="263d6-112">**Element**</span></span>|<span data-ttu-id="263d6-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="263d6-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="263d6-114">entryId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="263d6-114">entryId (UM web service)</span></span>](entryid-um-web-service.md) <br/> |<span data-ttu-id="263d6-115">包含表示要在[PlayOnPhone 操作（UM web 服务）](playonphone-operation-um-web-service.md)请求中的电话上播放的项的标识符的值。</span><span class="sxs-lookup"><span data-stu-id="263d6-115">Contains the value that represents the identifier of the item to play on the telephone in a [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) request.</span></span>  <br/> |
|[<span data-ttu-id="263d6-116">dialString （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="263d6-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="263d6-117">包含要拨打的电话号码的值。</span><span class="sxs-lookup"><span data-stu-id="263d6-117">Contains the value for the telephone number to dial.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="263d6-118">父元素</span><span class="sxs-lookup"><span data-stu-id="263d6-118">Parent elements</span></span>

<span data-ttu-id="263d6-119">无。</span><span class="sxs-lookup"><span data-stu-id="263d6-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="263d6-120">文本值</span><span class="sxs-lookup"><span data-stu-id="263d6-120">Text value</span></span>

<span data-ttu-id="263d6-121">无。</span><span class="sxs-lookup"><span data-stu-id="263d6-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="263d6-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="263d6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="263d6-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="263d6-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="263d6-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="263d6-124">Schema Name</span></span>  <br/> |<span data-ttu-id="263d6-125">邮件</span><span class="sxs-lookup"><span data-stu-id="263d6-125">Messages</span></span>  <br/> |
|<span data-ttu-id="263d6-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="263d6-126">Validation File</span></span>  <br/> |<span data-ttu-id="263d6-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="263d6-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="263d6-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="263d6-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="263d6-129">False</span><span class="sxs-lookup"><span data-stu-id="263d6-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="263d6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="263d6-130">See also</span></span>



[<span data-ttu-id="263d6-131">PlayOnPhone 操作（UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="263d6-131">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)

