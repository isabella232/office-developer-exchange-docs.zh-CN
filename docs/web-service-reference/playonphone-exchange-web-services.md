---
title: PlayOnPhone （Exchange Web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 486612be-470c-4f99-929a-f2b283e055c1
description: PlayOnPhone 元素表示为 read item 电话上的请求。
ms.openlocfilehash: 75493a31940ea609fd6cf454e91ca5881fb7e678
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826816"
---
# <a name="playonphone-exchange-web-services"></a><span data-ttu-id="b5f14-103">PlayOnPhone （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="b5f14-103">PlayOnPhone (Exchange Web Services)</span></span>

<span data-ttu-id="b5f14-104">**PlayOnPhone**元素表示为 read item 电话上的请求。</span><span class="sxs-lookup"><span data-stu-id="b5f14-104">The **PlayOnPhone** element represents a request to read an item on a phone.</span></span> 
  
```xml
<PlayOnPhone>   <ItemId/>   <DialString/></PlayOnPhone>
```

 <span data-ttu-id="b5f14-105">**PlayOnPhoneType**</span><span class="sxs-lookup"><span data-stu-id="b5f14-105">**PlayOnPhoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5f14-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b5f14-106">Attributes and elements</span></span>

<span data-ttu-id="b5f14-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b5f14-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5f14-108">属性</span><span class="sxs-lookup"><span data-stu-id="b5f14-108">Attributes</span></span>

<span data-ttu-id="b5f14-109">无。</span><span class="sxs-lookup"><span data-stu-id="b5f14-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5f14-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b5f14-110">Child elements</span></span>

|<span data-ttu-id="b5f14-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b5f14-111">**Element**</span></span>|<span data-ttu-id="b5f14-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b5f14-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b5f14-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="b5f14-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="b5f14-114">表示一个项目以在电话上播放的标识符。</span><span class="sxs-lookup"><span data-stu-id="b5f14-114">Represents the identifier of an item to play on a phone.</span></span> <span data-ttu-id="b5f14-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b5f14-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="b5f14-116">DialString （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="b5f14-116">DialString (Exchange Web Services)</span></span>](dialstring-exchange-web-services.md) <br/> |<span data-ttu-id="b5f14-117">代表调用播放项目通过电话的电话号码的拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="b5f14-117">Represents the dial string of the phone number that is called to play an item by phone.</span></span> <span data-ttu-id="b5f14-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="b5f14-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b5f14-119">父元素</span><span class="sxs-lookup"><span data-stu-id="b5f14-119">Parent elements</span></span>

<span data-ttu-id="b5f14-120">无。</span><span class="sxs-lookup"><span data-stu-id="b5f14-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5f14-121">注解</span><span class="sxs-lookup"><span data-stu-id="b5f14-121">Remarks</span></span>

<span data-ttu-id="b5f14-122">描述此元素的架构位于运行 Microsoft Exchange Server 2010 的安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b5f14-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5f14-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="b5f14-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5f14-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="b5f14-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b5f14-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="b5f14-125">Schema Name</span></span>  <br/> |<span data-ttu-id="b5f14-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="b5f14-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b5f14-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="b5f14-127">Validation File</span></span>  <br/> |<span data-ttu-id="b5f14-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b5f14-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5f14-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="b5f14-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="b5f14-130">False</span><span class="sxs-lookup"><span data-stu-id="b5f14-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b5f14-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b5f14-131">See also</span></span>



- [<span data-ttu-id="b5f14-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b5f14-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

