---
title: DisableApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 42d2a888-fa62-4970-8306-9ddde4eeb1f0
description: DisableApp 元素指定要禁用应用程序的请求。
ms.openlocfilehash: e99464677dc34e011e45548083fb830b819649fa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457821"
---
# <a name="disableapp"></a><span data-ttu-id="1be05-103">DisableApp</span><span class="sxs-lookup"><span data-stu-id="1be05-103">DisableApp</span></span>

<span data-ttu-id="1be05-104">**DisableApp**元素指定要禁用应用程序的请求。</span><span class="sxs-lookup"><span data-stu-id="1be05-104">The **DisableApp** element specifies a request to disable an app.</span></span> 
  
```XML
<DisableApp>
    <ID></ID>
    <DisableReason></DisableReason>
</DisableApp>
```

 <span data-ttu-id="1be05-105">**DisableAppType**</span><span class="sxs-lookup"><span data-stu-id="1be05-105">**DisableAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1be05-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1be05-106">Attributes and elements</span></span>

<span data-ttu-id="1be05-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1be05-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1be05-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1be05-108">Attributes</span></span>

<span data-ttu-id="1be05-109">无。</span><span class="sxs-lookup"><span data-stu-id="1be05-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1be05-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1be05-110">Child elements</span></span>

|<span data-ttu-id="1be05-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1be05-111">**Element**</span></span>|<span data-ttu-id="1be05-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1be05-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1be05-113">ID （字符串）</span><span class="sxs-lookup"><span data-stu-id="1be05-113">ID (String)</span></span>](id-string.md) <br/> |<span data-ttu-id="1be05-114">指定项的标识符。</span><span class="sxs-lookup"><span data-stu-id="1be05-114">Specifies the identifier of an item.</span></span>  <br/> |
|[<span data-ttu-id="1be05-115">DisableReason</span><span class="sxs-lookup"><span data-stu-id="1be05-115">DisableReason</span></span>](disablereason.md) <br/> |<span data-ttu-id="1be05-116">指定禁用应用程序的原因。</span><span class="sxs-lookup"><span data-stu-id="1be05-116">Specifies the reason for disabling an app.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1be05-117">父元素</span><span class="sxs-lookup"><span data-stu-id="1be05-117">Parent elements</span></span>

<span data-ttu-id="1be05-118">无。</span><span class="sxs-lookup"><span data-stu-id="1be05-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1be05-119">说明</span><span class="sxs-lookup"><span data-stu-id="1be05-119">Remarks</span></span>

<span data-ttu-id="1be05-120">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1be05-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1be05-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1be05-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1be05-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="1be05-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1be05-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="1be05-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1be05-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="1be05-124">Schema Name</span></span>  <br/> |<span data-ttu-id="1be05-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="1be05-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="1be05-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="1be05-126">Validation File</span></span>  <br/> |<span data-ttu-id="1be05-127">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="1be05-127">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1be05-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="1be05-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="1be05-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1be05-129">See also</span></span>

- [<span data-ttu-id="1be05-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1be05-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

