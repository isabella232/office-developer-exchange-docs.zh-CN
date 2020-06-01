---
title: OriginalRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OriginalRecipients
api_type:
- schema
ms.assetid: e4af86a5-85af-4239-8055-e29f0acf77c1
description: OriginalRecipients元素表示的第一个邮件收件人的电子邮件地址的列表。
ms.openlocfilehash: 7385b1fd62313ee09c94cd04f3f669215e6cd497
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467177"
---
# <a name="originalrecipients"></a><span data-ttu-id="f0545-103">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="f0545-103">OriginalRecipients</span></span>

<span data-ttu-id="f0545-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **OriginalRecipients**元素表示的第一个邮件收件人的电子邮件地址的列表。</span><span class="sxs-lookup"><span data-stu-id="f0545-104">The **OriginalRecipients** element represents a list of e-mail addresses of the first message recipients.</span></span> 
  
```XML
<OriginalRecipients>
   <Address/>
</OriginalRecipients>
```

 <span data-ttu-id="f0545-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="f0545-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f0545-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f0545-106">Attributes and elements</span></span>

<span data-ttu-id="f0545-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f0545-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f0545-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f0545-108">Attributes</span></span>

<span data-ttu-id="f0545-109">无。</span><span class="sxs-lookup"><span data-stu-id="f0545-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f0545-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f0545-110">Child elements</span></span>

|<span data-ttu-id="f0545-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f0545-111">**Element**</span></span>|<span data-ttu-id="f0545-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f0545-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0545-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="f0545-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="f0545-114">包含完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f0545-114">Contains a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f0545-115">父元素</span><span class="sxs-lookup"><span data-stu-id="f0545-115">Parent elements</span></span>

|<span data-ttu-id="f0545-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="f0545-116">**Element**</span></span>|<span data-ttu-id="f0545-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="f0545-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f0545-118">Search-messagetrackingreport</span><span class="sxs-lookup"><span data-stu-id="f0545-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="f0545-119">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="f0545-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0545-120">说明</span><span class="sxs-lookup"><span data-stu-id="f0545-120">Remarks</span></span>

<span data-ttu-id="f0545-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f0545-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f0545-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="f0545-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0545-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="f0545-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f0545-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="f0545-124">Schema Name</span></span>  <br/> |<span data-ttu-id="f0545-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="f0545-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="f0545-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="f0545-126">Validation File</span></span>  <br/> |<span data-ttu-id="f0545-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f0545-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f0545-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="f0545-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="f0545-129">False</span><span class="sxs-lookup"><span data-stu-id="f0545-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f0545-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f0545-130">See also</span></span>



[<span data-ttu-id="f0545-131">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="f0545-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="f0545-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f0545-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

