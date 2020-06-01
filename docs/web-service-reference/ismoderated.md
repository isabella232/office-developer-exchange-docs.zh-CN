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
ms.openlocfilehash: 930d5a7e09712f35d22850a93462d051a34785a1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44435483"
---
# <a name="ismoderated"></a><span data-ttu-id="f661f-103">IsModerated</span><span class="sxs-lookup"><span data-stu-id="f661f-103">IsModerated</span></span>

<span data-ttu-id="f661f-104">**IsModerated**元素指示是否正在仲裁收件人的邮箱。</span><span class="sxs-lookup"><span data-stu-id="f661f-104">The **IsModerated** element indicates whether the recipient's mailbox is being moderated.</span></span> 
  
```XML
<IsModerated>true | false</IsModerated>
```

 <span data-ttu-id="f661f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="f661f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f661f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f661f-106">Attributes and elements</span></span>

<span data-ttu-id="f661f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f661f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f661f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f661f-108">Attributes</span></span>

<span data-ttu-id="f661f-109">无。</span><span class="sxs-lookup"><span data-stu-id="f661f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f661f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f661f-110">Child elements</span></span>

<span data-ttu-id="f661f-111">无。</span><span class="sxs-lookup"><span data-stu-id="f661f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f661f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f661f-112">Parent elements</span></span>

|<span data-ttu-id="f661f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f661f-113">**Element**</span></span>|<span data-ttu-id="f661f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f661f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f661f-115">邮件提示</span><span class="sxs-lookup"><span data-stu-id="f661f-115">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="f661f-116">表示各种邮件提示类型的值。</span><span class="sxs-lookup"><span data-stu-id="f661f-116">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f661f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f661f-117">Text value</span></span>

<span data-ttu-id="f661f-118">如果收件人的邮箱正在被仲裁，则此元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="f661f-118">The text value for this element is **true** if the recipient's mailbox is being moderated.</span></span> <span data-ttu-id="f661f-119">如果未对收件人的邮箱进行仲裁，则该值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="f661f-119">The value is **false** if the recipient's mailbox is not being moderated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f661f-120">说明</span><span class="sxs-lookup"><span data-stu-id="f661f-120">Remarks</span></span>

<span data-ttu-id="f661f-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f661f-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f661f-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="f661f-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f661f-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="f661f-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f661f-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="f661f-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f661f-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="f661f-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f661f-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="f661f-126">Validation File</span></span>  <br/> |<span data-ttu-id="f661f-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f661f-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f661f-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="f661f-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f661f-129">False</span><span class="sxs-lookup"><span data-stu-id="f661f-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f661f-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f661f-130">See also</span></span>



- [<span data-ttu-id="f661f-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f661f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

