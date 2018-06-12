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
ms.openlocfilehash: 6e271f2cf0e37f26b945332c94167b6a42354115
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19826535"
---
# <a name="nonindexableitemdetailsresult"></a><span data-ttu-id="a748e-103">NonIndexableItemDetailsResult</span><span class="sxs-lookup"><span data-stu-id="a748e-103">NonIndexableItemDetailsResult</span></span>

<span data-ttu-id="a748e-104">**NonIndexableItemDetailsResult**元素指定**GetNonIndexableItemDetails** WSDL 操作的结果。</span><span class="sxs-lookup"><span data-stu-id="a748e-104">The **NonIndexableItemDetailsResult** element specifies the results of the **GetNonIndexableItemDetails** WSDL operation.</span></span> 
  
```XML
<NonIndexableItemDetailsResult>
   <Items/>
   <FailedMailboxes/>
</NonIndexableItemDetailsResult>
```

 <span data-ttu-id="a748e-105">**NonIndexableItemDetailResultType**</span><span class="sxs-lookup"><span data-stu-id="a748e-105">**NonIndexableItemDetailResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a748e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a748e-106">Attributes and elements</span></span>

<span data-ttu-id="a748e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a748e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a748e-108">属性</span><span class="sxs-lookup"><span data-stu-id="a748e-108">Attributes</span></span>

<span data-ttu-id="a748e-109">无。</span><span class="sxs-lookup"><span data-stu-id="a748e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a748e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a748e-110">Child elements</span></span>

<span data-ttu-id="a748e-111">[项目 (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) [FailedMailboxes](failedmailboxes.md)</span><span class="sxs-lookup"><span data-stu-id="a748e-111">[Items (ArrayOfNonIndexableItemDetailsType)](items-arrayofnonindexableitemdetailstype.md) , [FailedMailboxes](failedmailboxes.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a748e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a748e-112">Parent elements</span></span>

<span data-ttu-id="a748e-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span><span class="sxs-lookup"><span data-stu-id="a748e-113">[GetNonIndexableItemDetailsResponse](getnonindexableitemdetailsresponse.md) , [GetNonIndexableItemDetailsResponseMessage](getnonindexableitemdetailsresponsemessage.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a748e-114">备注</span><span class="sxs-lookup"><span data-stu-id="a748e-114">Remarks</span></span>

<span data-ttu-id="a748e-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a748e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a748e-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a748e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a748e-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="a748e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a748e-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="a748e-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a748e-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="a748e-119">Schema name</span></span>  <br/> |<span data-ttu-id="a748e-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="a748e-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a748e-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="a748e-121">Validation file</span></span>  <br/> |<span data-ttu-id="a748e-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a748e-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a748e-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="a748e-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a748e-124">False</span><span class="sxs-lookup"><span data-stu-id="a748e-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a748e-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a748e-125">See also</span></span>



[<span data-ttu-id="a748e-126">GetNonIndexableItemDetails 操作</span><span class="sxs-lookup"><span data-stu-id="a748e-126">GetNonIndexableItemDetails operation</span></span>](getnonindexableitemdetails-operation.md)


- [<span data-ttu-id="a748e-127">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a748e-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

