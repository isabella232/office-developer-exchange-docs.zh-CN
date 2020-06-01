---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: ShowExternalRecipientCount 元素指示 GetMailTips 操作的使用者是否必须显示指示向其发送邮件的外部收件人数的邮件提示。
ms.openlocfilehash: fc32e5c4a95f0e33b5532af9c77d31bd6446e641
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460468"
---
# <a name="showexternalrecipientcount"></a><span data-ttu-id="aeddf-103">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="aeddf-103">ShowExternalRecipientCount</span></span>

<span data-ttu-id="aeddf-104">**ShowExternalRecipientCount**元素指示[GetMailTips 操作](getmailtips-operation.md)的使用者是否必须显示指示向其发送邮件的外部收件人数的邮件提示。</span><span class="sxs-lookup"><span data-stu-id="aeddf-104">The **ShowExternalRecipientCount** element indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 <span data-ttu-id="aeddf-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="aeddf-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aeddf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aeddf-106">Attributes and elements</span></span>

<span data-ttu-id="aeddf-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aeddf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aeddf-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="aeddf-108">Attributes</span></span>

<span data-ttu-id="aeddf-109">无。</span><span class="sxs-lookup"><span data-stu-id="aeddf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aeddf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aeddf-110">Child elements</span></span>

<span data-ttu-id="aeddf-111">无。</span><span class="sxs-lookup"><span data-stu-id="aeddf-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aeddf-112">父元素</span><span class="sxs-lookup"><span data-stu-id="aeddf-112">Parent elements</span></span>

|<span data-ttu-id="aeddf-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="aeddf-113">**Element**</span></span>|<span data-ttu-id="aeddf-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="aeddf-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aeddf-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="aeddf-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="aeddf-116">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="aeddf-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aeddf-117">文本值</span><span class="sxs-lookup"><span data-stu-id="aeddf-117">Text value</span></span>

<span data-ttu-id="aeddf-118">如果[GetMailTips 操作](getmailtips-operation.md)的使用者必须显示指示邮件的目标外部收件人数的邮件提示，则此元素的文本值为**true** 。</span><span class="sxs-lookup"><span data-stu-id="aeddf-118">The text value of this element is **true** if consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="aeddf-119">如果[GetMailTips 操作](getmailtips-operation.md)的使用者不一定要显示指示邮件地址为的外部收件人数的邮件提示，则值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="aeddf-119">The value is **false** if consumers of the [GetMailTips operation](getmailtips-operation.md) do not have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aeddf-120">说明</span><span class="sxs-lookup"><span data-stu-id="aeddf-120">Remarks</span></span>

<span data-ttu-id="aeddf-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="aeddf-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aeddf-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="aeddf-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aeddf-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="aeddf-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aeddf-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="aeddf-124">Schema Name</span></span>  <br/> |<span data-ttu-id="aeddf-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="aeddf-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="aeddf-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="aeddf-126">Validation File</span></span>  <br/> |<span data-ttu-id="aeddf-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aeddf-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aeddf-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="aeddf-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="aeddf-129">False</span><span class="sxs-lookup"><span data-stu-id="aeddf-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aeddf-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aeddf-130">See also</span></span>



[<span data-ttu-id="aeddf-131">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="aeddf-131">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="aeddf-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="aeddf-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

