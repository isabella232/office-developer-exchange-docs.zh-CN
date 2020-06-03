---
title: OutlookRuleBlobExists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutlookRuleBlobExists
api_type:
- schema
ms.assetid: ae1bc448-deb9-4b5b-ab38-4b276abcb650
description: OutlookRuleBlobExists元素指示在该用户的邮箱中是否存在 Microsoft Outlook 规则 blob。
ms.openlocfilehash: 6a5c2a2ec0246d38b22279b86772972ea81922c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529026"
---
# <a name="outlookruleblobexists"></a><span data-ttu-id="10501-103">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="10501-103">OutlookRuleBlobExists</span></span>

<span data-ttu-id="10501-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **OutlookRuleBlobExists**元素指示在该用户的邮箱中是否存在 Microsoft Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="10501-104">The **OutlookRuleBlobExists** element indicates whether a Microsoft Outlook rule blob exists in the user's mailbox.</span></span> 
  
[<span data-ttu-id="10501-105">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="10501-105">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md)
  
[<span data-ttu-id="10501-106">OutlookRuleBlobExists</span><span class="sxs-lookup"><span data-stu-id="10501-106">OutlookRuleBlobExists</span></span>](outlookruleblobexists.md)
  
```XML
<OutlookRuleBlobExists>true | false</OutlookRuleBlobExists>
```

 <span data-ttu-id="10501-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="10501-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="10501-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="10501-108">Attributes and elements</span></span>

<span data-ttu-id="10501-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="10501-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10501-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="10501-110">Attributes</span></span>

<span data-ttu-id="10501-111">无。</span><span class="sxs-lookup"><span data-stu-id="10501-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="10501-112">子元素</span><span class="sxs-lookup"><span data-stu-id="10501-112">Child elements</span></span>

<span data-ttu-id="10501-113">无。</span><span class="sxs-lookup"><span data-stu-id="10501-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="10501-114">父元素</span><span class="sxs-lookup"><span data-stu-id="10501-114">Parent elements</span></span>

|<span data-ttu-id="10501-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="10501-115">**Element**</span></span>|<span data-ttu-id="10501-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="10501-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="10501-117">GetInboxRulesResponse</span><span class="sxs-lookup"><span data-stu-id="10501-117">GetInboxRulesResponse</span></span>](getinboxrulesresponse.md) <br/> |<span data-ttu-id="10501-118">代表[GetInboxRules 操作](getinboxrules-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="10501-118">Represents a response to a [GetInboxRules operation](getinboxrules-operation.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="10501-119">文本值</span><span class="sxs-lookup"><span data-stu-id="10501-119">Text value</span></span>

<span data-ttu-id="10501-p101">**true**的一个文字值表示 Outlook 规则 blob 存在。文本值为 **false**表示 Outlook 规则 blob 不存在。</span><span class="sxs-lookup"><span data-stu-id="10501-p101">A text value of **true** indicates that an Outlook rule blob exists. A text value of **false** indicates that an Outlook rule blob does not exist.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="10501-122">说明</span><span class="sxs-lookup"><span data-stu-id="10501-122">Remarks</span></span>

<span data-ttu-id="10501-123">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="10501-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10501-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="10501-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10501-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="10501-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="10501-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="10501-126">Schema Name</span></span>  <br/> |<span data-ttu-id="10501-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="10501-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="10501-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="10501-128">Validation File</span></span>  <br/> |<span data-ttu-id="10501-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="10501-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="10501-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="10501-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="10501-131">True</span><span class="sxs-lookup"><span data-stu-id="10501-131">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="10501-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="10501-132">See also</span></span>



- [<span data-ttu-id="10501-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="10501-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

