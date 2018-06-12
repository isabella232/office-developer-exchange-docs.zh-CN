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
description: ShowExternalRecipientCount 元素指示是否 GetMailTips 操作的使用者具有显示邮件提示指示邮件要发送到外部收件人的数量。
ms.openlocfilehash: 1fd3ceb629689c560dc60afe01f0413602f79a0d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827491"
---
# <a name="showexternalrecipientcount"></a><span data-ttu-id="be1e9-103">ShowExternalRecipientCount</span><span class="sxs-lookup"><span data-stu-id="be1e9-103">ShowExternalRecipientCount</span></span>

<span data-ttu-id="be1e9-104">**ShowExternalRecipientCount**元素指示是否[GetMailTips 操作](getmailtips-operation.md)的使用者具有显示邮件提示指示邮件要发送到外部收件人的数量。</span><span class="sxs-lookup"><span data-stu-id="be1e9-104">The **ShowExternalRecipientCount** element indicates whether consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 <span data-ttu-id="be1e9-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="be1e9-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be1e9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="be1e9-106">Attributes and elements</span></span>

<span data-ttu-id="be1e9-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be1e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be1e9-108">属性</span><span class="sxs-lookup"><span data-stu-id="be1e9-108">Attributes</span></span>

<span data-ttu-id="be1e9-109">无。</span><span class="sxs-lookup"><span data-stu-id="be1e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be1e9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="be1e9-110">Child elements</span></span>

<span data-ttu-id="be1e9-111">无。</span><span class="sxs-lookup"><span data-stu-id="be1e9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="be1e9-112">父元素</span><span class="sxs-lookup"><span data-stu-id="be1e9-112">Parent elements</span></span>

|<span data-ttu-id="be1e9-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="be1e9-113">**Element**</span></span>|<span data-ttu-id="be1e9-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="be1e9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="be1e9-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span><span class="sxs-lookup"><span data-stu-id="be1e9-115">MailTipsConfiguration (MailTipsServiceConfiguration)</span></span>](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |<span data-ttu-id="be1e9-116">包含邮件提示服务的服务配置信息。</span><span class="sxs-lookup"><span data-stu-id="be1e9-116">Contains service configuration information for the mail tips service.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="be1e9-117">文本值</span><span class="sxs-lookup"><span data-stu-id="be1e9-117">Text value</span></span>

<span data-ttu-id="be1e9-118">此元素的文本值为**true** ，如果[GetMailTips 操作](getmailtips-operation.md)的使用者必须显示邮件提示指示邮件要发送到外部收件人的数量。</span><span class="sxs-lookup"><span data-stu-id="be1e9-118">The text value of this element is **true** if consumers of the [GetMailTips operation](getmailtips-operation.md) have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> <span data-ttu-id="be1e9-119">如果[GetMailTips 操作](getmailtips-operation.md)的使用者没有显示指示邮件要发送到外部收件人数的邮件提示，则值为**false** 。</span><span class="sxs-lookup"><span data-stu-id="be1e9-119">The value is **false** if consumers of the [GetMailTips operation](getmailtips-operation.md) do not have to show mail tips that indicate the number of external recipients to which a message is addressed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="be1e9-120">备注</span><span class="sxs-lookup"><span data-stu-id="be1e9-120">Remarks</span></span>

<span data-ttu-id="be1e9-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="be1e9-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be1e9-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="be1e9-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be1e9-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="be1e9-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="be1e9-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="be1e9-124">Schema Name</span></span>  <br/> |<span data-ttu-id="be1e9-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="be1e9-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="be1e9-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="be1e9-126">Validation File</span></span>  <br/> |<span data-ttu-id="be1e9-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="be1e9-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="be1e9-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="be1e9-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="be1e9-129">False</span><span class="sxs-lookup"><span data-stu-id="be1e9-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="be1e9-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="be1e9-130">See also</span></span>



[<span data-ttu-id="be1e9-131">GetMailTips 操作</span><span class="sxs-lookup"><span data-stu-id="be1e9-131">GetMailTips operation</span></span>](getmailtips-operation.md)


- [<span data-ttu-id="be1e9-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="be1e9-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

