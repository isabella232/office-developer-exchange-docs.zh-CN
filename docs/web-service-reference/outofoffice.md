---
title: OutOfOffice
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutOfOffice
api_type:
- schema
ms.assetid: fe1256ab-5c0f-467d-abb3-b38a2dc312ae
description: 外出元素表示响应消息和发送响应消息持续时间。
ms.openlocfilehash: f35b84d7a8a37c7a57b58c97fd0d37318bb50a33
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354265"
---
# <a name="outofoffice"></a><span data-ttu-id="34734-103">OutOfOffice</span><span class="sxs-lookup"><span data-stu-id="34734-103">OutOfOffice</span></span>

<span data-ttu-id="34734-104">**外出**元素表示响应消息和发送响应消息持续时间。</span><span class="sxs-lookup"><span data-stu-id="34734-104">The **OutOfOffice** element represents the response message and a duration time for sending the response message.</span></span> 
  
```XML
<OutOfOffice>
   <ReplyBody/>
   <Duration/>
</OutOfOffice>
```

```XML
<OutOfOffice>
   <ReplyBody/>
</OutOfOffice>
```

<span data-ttu-id="34734-105">**OutOfOfficeMailTip**</span><span class="sxs-lookup"><span data-stu-id="34734-105">**OutOfOfficeMailTip**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="34734-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="34734-106">Attributes and elements</span></span>

<span data-ttu-id="34734-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="34734-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="34734-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="34734-108">Attributes</span></span>

<span data-ttu-id="34734-109">无。</span><span class="sxs-lookup"><span data-stu-id="34734-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="34734-110">子元素</span><span class="sxs-lookup"><span data-stu-id="34734-110">Child elements</span></span>

|<span data-ttu-id="34734-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="34734-111">**Element**</span></span>|<span data-ttu-id="34734-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="34734-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34734-113">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="34734-113">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="34734-114">包含 Office 外出 (OOF) 邮件和消息所使用的语言。</span><span class="sxs-lookup"><span data-stu-id="34734-114">Contains an Out of Office (OOF) message and the language used for the message.</span></span>  <br/> |
|[<span data-ttu-id="34734-115">Duration (UserOofSettings)</span><span class="sxs-lookup"><span data-stu-id="34734-115">Duration (UserOofSettings)</span></span>](duration-useroofsettings.md) <br/> |<span data-ttu-id="34734-116">包含如果[OofState](oofstate.md)元素设置为计划，则启用 OOF 状态的工期。</span><span class="sxs-lookup"><span data-stu-id="34734-116">Contains the duration that the OOF status is enabled if the [OofState](oofstate.md) element is set to Scheduled.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="34734-117">父元素</span><span class="sxs-lookup"><span data-stu-id="34734-117">Parent elements</span></span>

|<span data-ttu-id="34734-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="34734-118">**Element**</span></span>|<span data-ttu-id="34734-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="34734-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="34734-120">MailTips</span><span class="sxs-lookup"><span data-stu-id="34734-120">MailTips</span></span>](mailtips.md) <br/> |<span data-ttu-id="34734-121">表示的邮件提示的各种类型的值。</span><span class="sxs-lookup"><span data-stu-id="34734-121">Represents values for various types of mail tips.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="34734-122">文本值</span><span class="sxs-lookup"><span data-stu-id="34734-122">Text value</span></span>

<span data-ttu-id="34734-123">无。</span><span class="sxs-lookup"><span data-stu-id="34734-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34734-124">说明</span><span class="sxs-lookup"><span data-stu-id="34734-124">Remarks</span></span>

<span data-ttu-id="34734-125">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="34734-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="34734-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="34734-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="34734-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="34734-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="34734-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="34734-128">Schema Name</span></span>  <br/> |<span data-ttu-id="34734-129">类型架构</span><span class="sxs-lookup"><span data-stu-id="34734-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="34734-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="34734-130">Validation File</span></span>  <br/> |<span data-ttu-id="34734-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="34734-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="34734-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="34734-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="34734-133">False</span><span class="sxs-lookup"><span data-stu-id="34734-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34734-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="34734-134">See also</span></span>

- [<span data-ttu-id="34734-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="34734-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

