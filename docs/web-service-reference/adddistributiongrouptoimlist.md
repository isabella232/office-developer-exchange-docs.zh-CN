---
title: AddDistributionGroupToImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: adbffbfc-e436-4620-acfc-5dfd41a88cb8
description: AddDistributionGroupToImList 元素定义将通讯组列表添加到即时消息列表的请求。
ms.openlocfilehash: 90a84b23678fb0740158f601967905a8847286fd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460377"
---
# <a name="adddistributiongrouptoimlist"></a><span data-ttu-id="487c1-103">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="487c1-103">AddDistributionGroupToImList</span></span>

<span data-ttu-id="487c1-104">**AddDistributionGroupToImList**元素定义将通讯组列表添加到即时消息列表的请求。</span><span class="sxs-lookup"><span data-stu-id="487c1-104">The **AddDistributionGroupToImList** element defines a request to add a distribution list to an instant message list.</span></span> 
  
```XML
<AddDistributionGroupToImList>
   <SmtpAddress/>
   <DisplayName/>
</AddDistributionGroupToImList>
```

 <span data-ttu-id="487c1-105">**AddDistributionGroupToImListType**</span><span class="sxs-lookup"><span data-stu-id="487c1-105">**AddDistributionGroupToImListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="487c1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="487c1-106">Attributes and elements</span></span>

<span data-ttu-id="487c1-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="487c1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="487c1-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="487c1-108">Attributes</span></span>

<span data-ttu-id="487c1-109">无。</span><span class="sxs-lookup"><span data-stu-id="487c1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="487c1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="487c1-110">Child elements</span></span>

<span data-ttu-id="487c1-111">[SmtpAddress](smtpaddress.md)  | [DisplayName （NonEmptyStringType）](displayname-nonemptystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="487c1-111">[SmtpAddress](smtpaddress.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="487c1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="487c1-112">Parent elements</span></span>

<span data-ttu-id="487c1-113">无。</span><span class="sxs-lookup"><span data-stu-id="487c1-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="487c1-114">说明</span><span class="sxs-lookup"><span data-stu-id="487c1-114">Remarks</span></span>

<span data-ttu-id="487c1-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="487c1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="487c1-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="487c1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="487c1-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="487c1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="487c1-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="487c1-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="487c1-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="487c1-119">Schema name</span></span>  <br/> |<span data-ttu-id="487c1-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="487c1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="487c1-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="487c1-121">Validation file</span></span>  <br/> |<span data-ttu-id="487c1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="487c1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="487c1-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="487c1-123">Can be empty</span></span>  <br/> |<span data-ttu-id="487c1-124">false</span><span class="sxs-lookup"><span data-stu-id="487c1-124">false</span></span>  <br/> |
   

