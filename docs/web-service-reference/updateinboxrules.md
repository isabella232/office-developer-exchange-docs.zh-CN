---
title: UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: d220064f-ff4d-4537-8077-adf94f2cbdbd
description: UpdateInboxRules元素定义的请求来更新服务器存储区中邮箱的收件箱规则。
ms.openlocfilehash: d604604d582d28c07eaa75d3239082d1b6735e65
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456358"
---
# <a name="updateinboxrules"></a><span data-ttu-id="e53c2-103">UpdateInboxRules</span><span class="sxs-lookup"><span data-stu-id="e53c2-103">UpdateInboxRules</span></span>

<span data-ttu-id="e53c2-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **UpdateInboxRules**元素定义的请求来更新服务器存储区中邮箱的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="e53c2-104">The **UpdateInboxRules** element defines a request to update the Inbox rules in a mailbox in the server store.</span></span> 
  
```XML
<UpdateInboxRules>
   <MailboxSmtpAddress/>
   <RemoveOutlookRuleBlob/>
   <Operations/>
</UpdateInboxRules>
```

 <span data-ttu-id="e53c2-105">**UpdateInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="e53c2-105">**UpdateInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e53c2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e53c2-106">Attributes and elements</span></span>

<span data-ttu-id="e53c2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e53c2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e53c2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e53c2-108">Attributes</span></span>

<span data-ttu-id="e53c2-109">无。</span><span class="sxs-lookup"><span data-stu-id="e53c2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e53c2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e53c2-110">Child elements</span></span>

|<span data-ttu-id="e53c2-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e53c2-111">**Element**</span></span>|<span data-ttu-id="e53c2-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e53c2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e53c2-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="e53c2-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="e53c2-114">表示其收件箱规则来创建、 修改或删除的用户的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="e53c2-114">Represents the SMTP address of the user whose Inbox rules are to be created, modified, or deleted.</span></span>  <br/> |
|[<span data-ttu-id="e53c2-115">RemoveOutlookRuleBlob</span><span class="sxs-lookup"><span data-stu-id="e53c2-115">RemoveOutlookRuleBlob</span></span>](removeoutlookruleblob.md) <br/> |<span data-ttu-id="e53c2-116">指示是否删除 Microsoft Outlook 规则 blob。</span><span class="sxs-lookup"><span data-stu-id="e53c2-116">Indicates whether to remove the Microsoft Outlook rule blob.</span></span>  <br/> |
|[<span data-ttu-id="e53c2-117">操作</span><span class="sxs-lookup"><span data-stu-id="e53c2-117">Operations</span></span>](operations.md) <br/> |<span data-ttu-id="e53c2-118">包含规则的操作，可以在收件箱的一个数组。</span><span class="sxs-lookup"><span data-stu-id="e53c2-118">Contains an array of rule operations that can be performed on an Inbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e53c2-119">父元素</span><span class="sxs-lookup"><span data-stu-id="e53c2-119">Parent elements</span></span>

<span data-ttu-id="e53c2-120">无。</span><span class="sxs-lookup"><span data-stu-id="e53c2-120">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="e53c2-121">文本值</span><span class="sxs-lookup"><span data-stu-id="e53c2-121">Text value</span></span>

<span data-ttu-id="e53c2-122">无。</span><span class="sxs-lookup"><span data-stu-id="e53c2-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e53c2-123">说明</span><span class="sxs-lookup"><span data-stu-id="e53c2-123">Remarks</span></span>

<span data-ttu-id="e53c2-124">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e53c2-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e53c2-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="e53c2-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e53c2-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="e53c2-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e53c2-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="e53c2-127">Schema Name</span></span>  <br/> |<span data-ttu-id="e53c2-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="e53c2-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e53c2-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="e53c2-129">Validation File</span></span>  <br/> |<span data-ttu-id="e53c2-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e53c2-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e53c2-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="e53c2-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="e53c2-132">True</span><span class="sxs-lookup"><span data-stu-id="e53c2-132">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e53c2-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e53c2-133">See also</span></span>



[<span data-ttu-id="e53c2-134">UpdateInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="e53c2-134">UpdateInboxRules operation</span></span>](updateinboxrules-operation.md)


- [<span data-ttu-id="e53c2-135">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e53c2-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

