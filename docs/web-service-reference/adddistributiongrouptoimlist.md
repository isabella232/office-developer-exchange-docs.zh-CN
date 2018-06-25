---
title: AddDistributionGroupToImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: adbffbfc-e436-4620-acfc-5dfd41a88cb8
description: AddDistributionGroupToImList 元素定义向即时消息列表添加通讯组列表的请求。
ms.openlocfilehash: b63daeb8b1d60123215bfcdec307f2f948d2ec39
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753106"
---
# <a name="adddistributiongrouptoimlist"></a><span data-ttu-id="a0446-103">AddDistributionGroupToImList</span><span class="sxs-lookup"><span data-stu-id="a0446-103">AddDistributionGroupToImList</span></span>

<span data-ttu-id="a0446-104">**AddDistributionGroupToImList**元素定义向即时消息列表添加通讯组列表的请求。</span><span class="sxs-lookup"><span data-stu-id="a0446-104">The **AddDistributionGroupToImList** element defines a request to add a distribution list to an instant message list.</span></span> 
  
```XML
<AddDistributionGroupToImList>
   <SmtpAddress/>
   <DisplayName/>
</AddDistributionGroupToImList>
```

 <span data-ttu-id="a0446-105">**AddDistributionGroupToImListType**</span><span class="sxs-lookup"><span data-stu-id="a0446-105">**AddDistributionGroupToImListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0446-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a0446-106">Attributes and elements</span></span>

<span data-ttu-id="a0446-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a0446-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0446-108">属性</span><span class="sxs-lookup"><span data-stu-id="a0446-108">Attributes</span></span>

<span data-ttu-id="a0446-109">无。</span><span class="sxs-lookup"><span data-stu-id="a0446-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a0446-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a0446-110">Child elements</span></span>

<span data-ttu-id="a0446-111">[SmtpAddress](smtpaddress.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="a0446-111">[SmtpAddress](smtpaddress.md) | [DisplayName (NonEmptyStringType)](displayname-nonemptystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a0446-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a0446-112">Parent elements</span></span>

<span data-ttu-id="a0446-113">无。</span><span class="sxs-lookup"><span data-stu-id="a0446-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0446-114">备注</span><span class="sxs-lookup"><span data-stu-id="a0446-114">Remarks</span></span>

<span data-ttu-id="a0446-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a0446-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="a0446-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a0446-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0446-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="a0446-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0446-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="a0446-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a0446-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="a0446-119">Schema name</span></span>  <br/> |<span data-ttu-id="a0446-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="a0446-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a0446-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="a0446-121">Validation file</span></span>  <br/> |<span data-ttu-id="a0446-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a0446-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a0446-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="a0446-123">Can be empty</span></span>  <br/> |<span data-ttu-id="a0446-124">false</span><span class="sxs-lookup"><span data-stu-id="a0446-124">false</span></span>  <br/> |
   

