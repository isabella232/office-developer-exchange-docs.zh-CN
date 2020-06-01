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
description: PlayOnPhone 元素表示在电话上读取项目的请求。
ms.openlocfilehash: e2c09a67255106ad9afddb86fa19b7a4a5762ee5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466246"
---
# <a name="playonphone-exchange-web-services"></a><span data-ttu-id="95b07-103">PlayOnPhone （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="95b07-103">PlayOnPhone (Exchange Web Services)</span></span>

<span data-ttu-id="95b07-104">**PlayOnPhone**元素表示在电话上读取项目的请求。</span><span class="sxs-lookup"><span data-stu-id="95b07-104">The **PlayOnPhone** element represents a request to read an item on a phone.</span></span> 
  
```xml
<PlayOnPhone>   <ItemId/>   <DialString/></PlayOnPhone>
```

 <span data-ttu-id="95b07-105">**PlayOnPhoneType**</span><span class="sxs-lookup"><span data-stu-id="95b07-105">**PlayOnPhoneType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95b07-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95b07-106">Attributes and elements</span></span>

<span data-ttu-id="95b07-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95b07-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95b07-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="95b07-108">Attributes</span></span>

<span data-ttu-id="95b07-109">无。</span><span class="sxs-lookup"><span data-stu-id="95b07-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95b07-110">子元素</span><span class="sxs-lookup"><span data-stu-id="95b07-110">Child elements</span></span>

|<span data-ttu-id="95b07-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="95b07-111">**Element**</span></span>|<span data-ttu-id="95b07-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="95b07-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95b07-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="95b07-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="95b07-114">表示要在电话上播放的项的标识符。</span><span class="sxs-lookup"><span data-stu-id="95b07-114">Represents the identifier of an item to play on a phone.</span></span> <span data-ttu-id="95b07-115">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="95b07-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="95b07-116">DialString （Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="95b07-116">DialString (Exchange Web Services)</span></span>](dialstring-exchange-web-services.md) <br/> |<span data-ttu-id="95b07-117">表示呼叫通过电话播放某个项目的电话号码的拨号字符串。</span><span class="sxs-lookup"><span data-stu-id="95b07-117">Represents the dial string of the phone number that is called to play an item by phone.</span></span> <span data-ttu-id="95b07-118">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="95b07-118">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95b07-119">父元素</span><span class="sxs-lookup"><span data-stu-id="95b07-119">Parent elements</span></span>

<span data-ttu-id="95b07-120">无。</span><span class="sxs-lookup"><span data-stu-id="95b07-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95b07-121">说明</span><span class="sxs-lookup"><span data-stu-id="95b07-121">Remarks</span></span>

<span data-ttu-id="95b07-122">描述此元素的架构位于运行 Microsoft Exchange Server 2010 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="95b07-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95b07-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="95b07-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95b07-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="95b07-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="95b07-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="95b07-125">Schema Name</span></span>  <br/> |<span data-ttu-id="95b07-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="95b07-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="95b07-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="95b07-127">Validation File</span></span>  <br/> |<span data-ttu-id="95b07-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="95b07-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="95b07-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="95b07-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="95b07-130">False</span><span class="sxs-lookup"><span data-stu-id="95b07-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95b07-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95b07-131">See also</span></span>



- [<span data-ttu-id="95b07-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="95b07-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

