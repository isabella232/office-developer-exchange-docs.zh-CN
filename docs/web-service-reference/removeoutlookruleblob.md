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
ms.openlocfilehash: b4202ab52bf16d1ad1546ec963cd8b9dacd2bd63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467667"
---
# <a name="removeoutlookruleblob"></a><span data-ttu-id="78db0-103">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="78db0-103">RemoveOutlookRuleBlob</span></span>

<span data-ttu-id="78db0-104">**RemoveOutlookRuleBlob**元素指示是否删除 Microsoft Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="78db0-104">The **RemoveOutlookRuleBlob** element indicates whether to remove the Microsoft Outlook rule blob.</span></span> 
  
[<span data-ttu-id="78db0-105">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="78db0-105">UpdateInboxRules</span></span>](updateinboxrules.md)
  
[<span data-ttu-id="78db0-106">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="78db0-106">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md)
  
```XML
<RemoveOutlookRuleBlob>true | false</RemoveOutlookRuleBlob>
```

 <span data-ttu-id="78db0-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="78db0-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78db0-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="78db0-108">Attributes and elements</span></span>

<span data-ttu-id="78db0-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="78db0-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78db0-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="78db0-110">Attributes</span></span>

<span data-ttu-id="78db0-111">无。</span><span class="sxs-lookup"><span data-stu-id="78db0-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78db0-112">子元素</span><span class="sxs-lookup"><span data-stu-id="78db0-112">Child elements</span></span>

<span data-ttu-id="78db0-113">无。</span><span class="sxs-lookup"><span data-stu-id="78db0-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="78db0-114">父元素</span><span class="sxs-lookup"><span data-stu-id="78db0-114">Parent elements</span></span>

|<span data-ttu-id="78db0-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="78db0-115">**Element**</span></span>|<span data-ttu-id="78db0-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="78db0-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78db0-117">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="78db0-117">UpdateInboxRules</span></span>](updateinboxrules.md) <br/> |<span data-ttu-id="78db0-118">定义更新服务器存储中的邮箱的收件箱规则的请求。</span><span class="sxs-lookup"><span data-stu-id="78db0-118">Defines a request to update the Inbox rules in a mailbox in the server store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="78db0-119">文本值</span><span class="sxs-lookup"><span data-stu-id="78db0-119">Text value</span></span>

<span data-ttu-id="78db0-120">如果文本值为**true** ，则表示应删除 Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="78db0-120">A text value of **true** indicates that the Outlook rule blob should be removed.</span></span> <span data-ttu-id="78db0-121">如果文本值为**false** ，则表示不应删除 Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="78db0-121">A text value of **false** indicates that the Outlook rule blob should not be removed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="78db0-122">备注</span><span class="sxs-lookup"><span data-stu-id="78db0-122">Remarks</span></span>

<span data-ttu-id="78db0-123">将此元素设置为**true**以允许使用收件箱规则更新。</span><span class="sxs-lookup"><span data-stu-id="78db0-123">Set this element to **true** to allow for an Inbox rule update.</span></span> 
  
<span data-ttu-id="78db0-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="78db0-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78db0-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="78db0-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78db0-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="78db0-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78db0-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="78db0-127">Schema Name</span></span>  <br/> |<span data-ttu-id="78db0-128">类型架构</span><span class="sxs-lookup"><span data-stu-id="78db0-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="78db0-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="78db0-129">Validation File</span></span>  <br/> |<span data-ttu-id="78db0-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78db0-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78db0-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="78db0-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="78db0-132">True</span><span class="sxs-lookup"><span data-stu-id="78db0-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78db0-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="78db0-133">See also</span></span>



[<span data-ttu-id="78db0-134">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="78db0-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="78db0-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="78db0-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

