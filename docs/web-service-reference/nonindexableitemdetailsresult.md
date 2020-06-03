---
title: NonIndexableItemDetailsResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7cbdbc21-5405-4cbc-8ca0-d7b0257927aa
description: NonIndexableItemDetailsResult 元素指定 GetNonIndexableItemDetails WSDL 操作的结果。
ms.openlocfilehash: 647f58b5e7285af70bbfb3a203ba71c9a3ccebcc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465441"
---
# <a name="nonindexableitemdetailsresult"></a><span data-ttu-id="30fe2-103">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="30fe2-103">NonIndexableItemDetailsResult</span></span>

<span data-ttu-id="30fe2-104">**NonIndexableItemDetailsResult**元素指定**GetNonIndexableItemDetails** WSDL 操作的结果。</span><span class="sxs-lookup"><span data-stu-id="30fe2-104">The **NonIndexableItemDetailsResult** element specifies the results of the **GetNonIndexableItemDetails** WSDL operation.</span></span> 
  
```XML
<NonIndexableItemDetailsResult>
   <Items/>
   <FailedMailboxes/>
</NonIndexableItemDetailsResult>
```

 <span data-ttu-id="30fe2-105">**NonIndexableItemDetailResultType**</span><span class="sxs-lookup"><span data-stu-id="30fe2-105">**NonIndexableItemDetailResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="30fe2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="30fe2-106">Attributes and elements</span></span>

<span data-ttu-id="30fe2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="30fe2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30fe2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="30fe2-108">Attributes</span></span>

<span data-ttu-id="30fe2-109">无。</span><span class="sxs-lookup"><span data-stu-id="30fe2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30fe2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="30fe2-110">Child elements</span></span>

<span data-ttu-id="30fe2-111">[Items （ArrayOfNonIndexableItemDetailsType）](items-arrayofnonindexableitemdetailstype.md) 、 [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="30fe2-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="30fe2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="30fe2-112">Parent elements</span></span>

<span data-ttu-id="30fe2-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) 、 [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="30fe2-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="30fe2-114">备注</span><span class="sxs-lookup"><span data-stu-id="30fe2-114">Remarks</span></span>

<span data-ttu-id="30fe2-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="30fe2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="30fe2-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="30fe2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30fe2-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="30fe2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30fe2-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="30fe2-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="30fe2-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="30fe2-119">Schema name</span></span>  <br/> |<span data-ttu-id="30fe2-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="30fe2-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="30fe2-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="30fe2-121">Validation file</span></span>  <br/> |<span data-ttu-id="30fe2-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="30fe2-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="30fe2-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="30fe2-123">Can be empty</span></span>  <br/> |<span data-ttu-id="30fe2-124">False</span><span class="sxs-lookup"><span data-stu-id="30fe2-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30fe2-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30fe2-125">See also</span></span>



[<span data-ttu-id="30fe2-126">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="30fe2-126">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)


- [<span data-ttu-id="30fe2-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="30fe2-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

