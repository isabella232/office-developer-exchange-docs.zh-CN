---
title: IsModerated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsModerated
api_type:
- schema
ms.assetid: a7562256-feb9-41a1-857e-b5d41cbed680
description: IsModerated 元素指示是否正在仲裁收件人的邮箱。
ms.openlocfilehash: 8db234f9706bb8187978a76f745323749d7a640a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826055"
---
# <a name="ismoderated"></a><span data-ttu-id="c79fd-103">IsModerated</span><span class="sxs-lookup"><span data-stu-id="c79fd-103">IsModerated</span></span>

<span data-ttu-id="c79fd-104">**IsModerated**元素指示是否正在仲裁收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="c79fd-104">The **IsModerated** element indicates whether the recipient's mailbox is being moderated.</span></span> 
  
```XML
<IsModerated>true | false</IsModerated>
```

 <span data-ttu-id="c79fd-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c79fd-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c79fd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c79fd-106">Attributes and elements</span></span>

<span data-ttu-id="c79fd-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c79fd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c79fd-108">属性</span><span class="sxs-lookup"><span data-stu-id="c79fd-108">Attributes</span></span>

<span data-ttu-id="c79fd-109">无。</span><span class="sxs-lookup"><span data-stu-id="c79fd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c79fd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c79fd-110">Child elements</span></span>

<span data-ttu-id="c79fd-111">无。</span><span class="sxs-lookup"><span data-stu-id="c79fd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c79fd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c79fd-112">Parent elements</span></span>

|<span data-ttu-id="c79fd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c79fd-113">**Element**</span></span>|<span data-ttu-id="c79fd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c79fd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c79fd-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="c79fd-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="c79fd-116">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="c79fd-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c79fd-117">文本值</span><span class="sxs-lookup"><span data-stu-id="c79fd-117">Text value</span></span>

<span data-ttu-id="c79fd-118">此元素的文本值为**true** ，如果正在仲裁收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="c79fd-118">The text value for this element is **true** if the recipient's mailbox is being moderated.</span></span> <span data-ttu-id="c79fd-119">如果不被仲裁收件人的邮箱，则值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="c79fd-119">The value is **false** if the recipient's mailbox is not being moderated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c79fd-120">备注</span><span class="sxs-lookup"><span data-stu-id="c79fd-120">Remarks</span></span>

<span data-ttu-id="c79fd-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c79fd-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c79fd-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="c79fd-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c79fd-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="c79fd-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c79fd-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="c79fd-124">Schema Name</span></span>  <br/> |<span data-ttu-id="c79fd-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="c79fd-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c79fd-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="c79fd-126">Validation File</span></span>  <br/> |<span data-ttu-id="c79fd-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c79fd-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c79fd-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="c79fd-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="c79fd-129">False</span><span class="sxs-lookup"><span data-stu-id="c79fd-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c79fd-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c79fd-130">See also</span></span>



- [<span data-ttu-id="c79fd-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c79fd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

