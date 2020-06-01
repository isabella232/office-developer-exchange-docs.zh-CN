---
title: IsSigned
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsSigned
api_type:
- schema
ms.assetid: a4f90fe5-2834-4621-9aa3-b561f74d4674
description: IsSigned 元素指示是否必须签署传入的邮件，以便条件或例外情况适用。
ms.openlocfilehash: fe8551d01e6f9e813da8936f15b0b7ba1d4ce56c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455525"
---
# <a name="issigned"></a><span data-ttu-id="36f44-103">IsSigned</span><span class="sxs-lookup"><span data-stu-id="36f44-103">IsSigned</span></span>

<span data-ttu-id="36f44-104">**IsSigned**元素指示是否必须签署传入的邮件，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="36f44-104">The **IsSigned** element indicates whether incoming messages must be signed in order for the condition or exception to apply.</span></span> 
  
```XML
<IsSigned>true | false</IsSigned>
```

 <span data-ttu-id="36f44-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="36f44-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="36f44-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="36f44-106">Attributes and elements</span></span>

<span data-ttu-id="36f44-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="36f44-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="36f44-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="36f44-108">Attributes</span></span>

<span data-ttu-id="36f44-109">无。</span><span class="sxs-lookup"><span data-stu-id="36f44-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="36f44-110">子元素</span><span class="sxs-lookup"><span data-stu-id="36f44-110">Child elements</span></span>

<span data-ttu-id="36f44-111">无。</span><span class="sxs-lookup"><span data-stu-id="36f44-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="36f44-112">父元素</span><span class="sxs-lookup"><span data-stu-id="36f44-112">Parent elements</span></span>

|<span data-ttu-id="36f44-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="36f44-113">**Element**</span></span>|<span data-ttu-id="36f44-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="36f44-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="36f44-115">条件</span><span class="sxs-lookup"><span data-stu-id="36f44-115">Conditions</span></span>](conditions.md) <br/> |<span data-ttu-id="36f44-116">表示履行时将触发规则的规则操作的条件。</span><span class="sxs-lookup"><span data-stu-id="36f44-116">Represents the conditions that, when fulfilled, will trigger the rule actions for a rule.</span></span>  <br/> |
|[<span data-ttu-id="36f44-117">异常</span><span class="sxs-lookup"><span data-stu-id="36f44-117">Exceptions</span></span>](exceptions.md) <br/> |<span data-ttu-id="36f44-118">表示表示收件箱规则的所有可用的规则例外条件的异常。</span><span class="sxs-lookup"><span data-stu-id="36f44-118">Represents the exceptions that represent all the available rule exception conditions for an Inbox rule.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="36f44-119">文本值</span><span class="sxs-lookup"><span data-stu-id="36f44-119">Text value</span></span>

<span data-ttu-id="36f44-120">如果文本值为**true** ，则表示必须对邮件进行签名，以便条件或例外情况适用。</span><span class="sxs-lookup"><span data-stu-id="36f44-120">A text value of **true** indicates that the message must be signed in order for the condition or exception to apply.</span></span> <span data-ttu-id="36f44-121">如果文本值为**false** ，则表示无需签署该邮件即可应用的条件或例外。</span><span class="sxs-lookup"><span data-stu-id="36f44-121">A text value of **false** indicates that the message does not have to be signed for the condition or exception to apply.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="36f44-122">说明</span><span class="sxs-lookup"><span data-stu-id="36f44-122">Remarks</span></span>

<span data-ttu-id="36f44-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="36f44-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="36f44-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="36f44-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="36f44-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="36f44-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="36f44-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="36f44-126">Schema Name</span></span>  <br/> |<span data-ttu-id="36f44-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="36f44-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="36f44-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="36f44-128">Validation File</span></span>  <br/> |<span data-ttu-id="36f44-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="36f44-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="36f44-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="36f44-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="36f44-131">True</span><span class="sxs-lookup"><span data-stu-id="36f44-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="36f44-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="36f44-132">See also</span></span>



- [<span data-ttu-id="36f44-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="36f44-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

