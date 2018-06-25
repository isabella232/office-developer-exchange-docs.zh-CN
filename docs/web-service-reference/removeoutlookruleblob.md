---
title: RemoveOutlookRuleBlob
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveOutlookRuleBlob
api_type:
- schema
ms.assetid: 69614475-8bd3-4475-b988-614fe9cad8ef
description: RemoveOutlookRuleBlob 元素指示是否删除 Microsoft Outlook 规则 blob。
ms.openlocfilehash: 45336e296c39161704ce6e0d51fba1d2c61797b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827102"
---
# <a name="removeoutlookruleblob"></a><span data-ttu-id="c0b40-103">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="c0b40-103">RemoveOutlookRuleBlob</span></span>

<span data-ttu-id="c0b40-104">**RemoveOutlookRuleBlob**元素指示是否删除 Microsoft Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="c0b40-104">The **RemoveOutlookRuleBlob** element indicates whether to remove the Microsoft Outlook rule blob.</span></span> 
  
[<span data-ttu-id="c0b40-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0b40-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="c0b40-106">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="c0b40-106">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 <span data-ttu-id="c0b40-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="c0b40-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0b40-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c0b40-108">Attributes and elements</span></span>

<span data-ttu-id="c0b40-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c0b40-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0b40-110">属性</span><span class="sxs-lookup"><span data-stu-id="c0b40-110">Attributes</span></span>

<span data-ttu-id="c0b40-111">无。</span><span class="sxs-lookup"><span data-stu-id="c0b40-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0b40-112">子元素</span><span class="sxs-lookup"><span data-stu-id="c0b40-112">Child elements</span></span>

<span data-ttu-id="c0b40-113">无。</span><span class="sxs-lookup"><span data-stu-id="c0b40-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c0b40-114">父元素</span><span class="sxs-lookup"><span data-stu-id="c0b40-114">Parent elements</span></span>

|<span data-ttu-id="c0b40-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="c0b40-115">**Element**</span></span>|<span data-ttu-id="c0b40-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="c0b40-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0b40-117">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="c0b40-117">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="c0b40-118">定义更新中的邮箱服务器存储区中的收件箱规则的请求。</span><span class="sxs-lookup"><span data-stu-id="c0b40-118">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="c0b40-119">文本值</span><span class="sxs-lookup"><span data-stu-id="c0b40-119">Text value</span></span>

<span data-ttu-id="c0b40-120">文本值为**true**指示应删除 Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="c0b40-120">A text value of **true** indicates that the Outlook rule blob should be removed.</span></span> <span data-ttu-id="c0b40-121">文本值为**false**指示 Outlook 规则 blob 应不会删除。</span><span class="sxs-lookup"><span data-stu-id="c0b40-121">A text value of **false** indicates that the Outlook rule blob should not be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c0b40-122">注解</span><span class="sxs-lookup"><span data-stu-id="c0b40-122">Remarks</span></span>

<span data-ttu-id="c0b40-123">将此元素设置为**true**以允许收件箱规则更新。</span><span class="sxs-lookup"><span data-stu-id="c0b40-123">Set this element to **true** to allow for an Inbox rule update.</span></span> 
  
<span data-ttu-id="c0b40-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c0b40-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0b40-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="c0b40-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0b40-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="c0b40-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c0b40-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="c0b40-127">Schema Name</span></span>  <br/> |<span data-ttu-id="c0b40-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="c0b40-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="c0b40-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="c0b40-129">Validation File</span></span>  <br/> |<span data-ttu-id="c0b40-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c0b40-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c0b40-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="c0b40-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0b40-132">True</span><span class="sxs-lookup"><span data-stu-id="c0b40-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0b40-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0b40-133">See also</span></span>



[<span data-ttu-id="c0b40-134">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="c0b40-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="c0b40-135">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c0b40-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

