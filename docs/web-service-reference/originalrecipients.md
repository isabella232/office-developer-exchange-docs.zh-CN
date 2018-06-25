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
ms.openlocfilehash: 8f99368409dbfb5ac798b691be65c7fd64f32660
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826665"
---
# <a name="originalrecipients"></a><span data-ttu-id="4c9ab-103">OriginalRecipients</span><span class="sxs-lookup"><span data-stu-id="4c9ab-103">OriginalRecipients</span></span>

<span data-ttu-id="4c9ab-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **OriginalRecipients**元素表示的第一个邮件收件人的电子邮件地址的列表。</span><span class="sxs-lookup"><span data-stu-id="4c9ab-104">The **OriginalRecipients** element represents a list of e-mail addresses of the first message recipients.</span></span> 
  
```XML
<OriginalRecipients>
   <Address/>
</OriginalRecipients>
```

 <span data-ttu-id="4c9ab-105">**ArrayOfEmailAddressesType**</span><span class="sxs-lookup"><span data-stu-id="4c9ab-105">**ArrayOfEmailAddressesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4c9ab-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4c9ab-106">Attributes and elements</span></span>

<span data-ttu-id="4c9ab-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4c9ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4c9ab-108">属性</span><span class="sxs-lookup"><span data-stu-id="4c9ab-108">Attributes</span></span>

<span data-ttu-id="4c9ab-109">无。</span><span class="sxs-lookup"><span data-stu-id="4c9ab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c9ab-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4c9ab-110">Child elements</span></span>

|<span data-ttu-id="4c9ab-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4c9ab-111">**Element**</span></span>|<span data-ttu-id="4c9ab-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4c9ab-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c9ab-113">地址 (EmailAddressType)</span><span class="sxs-lookup"><span data-stu-id="4c9ab-113">Address (EmailAddressType)</span></span>](address-emailaddresstype.md) <br/> |<span data-ttu-id="4c9ab-114">包含完全解析电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="4c9ab-114">Contains a fully resolved e-mail address.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4c9ab-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4c9ab-115">Parent elements</span></span>

|<span data-ttu-id="4c9ab-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4c9ab-116">**Element**</span></span>|<span data-ttu-id="4c9ab-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4c9ab-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c9ab-118">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="4c9ab-118">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="4c9ab-119">包含在[GetMessageTrackingReport 操作](getmessagetrackingreport-operation.md)中返回一条消息。</span><span class="sxs-lookup"><span data-stu-id="4c9ab-119">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c9ab-120">备注</span><span class="sxs-lookup"><span data-stu-id="4c9ab-120">Remarks</span></span>

<span data-ttu-id="4c9ab-121">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4c9ab-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c9ab-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="4c9ab-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c9ab-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="4c9ab-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4c9ab-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="4c9ab-124">Schema Name</span></span>  <br/> |<span data-ttu-id="4c9ab-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="4c9ab-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="4c9ab-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="4c9ab-126">Validation File</span></span>  <br/> |<span data-ttu-id="4c9ab-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4c9ab-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4c9ab-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="4c9ab-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="4c9ab-129">False</span><span class="sxs-lookup"><span data-stu-id="4c9ab-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c9ab-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4c9ab-130">See also</span></span>



[<span data-ttu-id="4c9ab-131">GetMessageTrackingReport 操作</span><span class="sxs-lookup"><span data-stu-id="4c9ab-131">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)


- [<span data-ttu-id="4c9ab-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4c9ab-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

