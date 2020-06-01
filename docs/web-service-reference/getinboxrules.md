---
title: GetInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetInboxRules
api_type:
- schema
ms.assetid: 7a54992d-03a6-4afc-a2e4-dcdc9ce54194
description: GetInboxRules元素定义一个请求，以获取有关服务器存储中的邮箱的收件箱规则。
ms.openlocfilehash: 890592fd3f87fc5592a618a2febf28e4daf0dbe4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457926"
---
# <a name="getinboxrules"></a><span data-ttu-id="c5fc6-103">GetInboxRules</span><span class="sxs-lookup"><span data-stu-id="c5fc6-103">GetInboxRules</span></span>

<span data-ttu-id="c5fc6-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **GetInboxRules**元素定义一个请求，以获取有关服务器存储中的邮箱的收件箱规则。</span><span class="sxs-lookup"><span data-stu-id="c5fc6-104">The **GetInboxRules** element defines a request to get the Inbox rules on a mailbox in the server store.</span></span> 
  
```XML
<GetInboxRules>
   <MailboxSmtpAddress/>
</GetInboxRules>
```

 <span data-ttu-id="c5fc6-105">**GetInboxRulesRequestType**</span><span class="sxs-lookup"><span data-stu-id="c5fc6-105">**GetInboxRulesRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c5fc6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c5fc6-106">Attributes and elements</span></span>

<span data-ttu-id="c5fc6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c5fc6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5fc6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c5fc6-108">Attributes</span></span>

<span data-ttu-id="c5fc6-109">无。</span><span class="sxs-lookup"><span data-stu-id="c5fc6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c5fc6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c5fc6-110">Child elements</span></span>

|<span data-ttu-id="c5fc6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c5fc6-111">**Element**</span></span>|<span data-ttu-id="c5fc6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c5fc6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c5fc6-113">MailboxSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="c5fc6-113">MailboxSmtpAddress</span></span>](mailboxsmtpaddress.md) <br/> |<span data-ttu-id="c5fc6-114">表示要检索其收件箱规则的用户的 SMTP 地址。</span><span class="sxs-lookup"><span data-stu-id="c5fc6-114">Represents the SMTP address of the user whose Inbox rules are to be retrieved.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c5fc6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c5fc6-115">Parent elements</span></span>

<span data-ttu-id="c5fc6-116">无。</span><span class="sxs-lookup"><span data-stu-id="c5fc6-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5fc6-117">说明</span><span class="sxs-lookup"><span data-stu-id="c5fc6-117">Remarks</span></span>

<span data-ttu-id="c5fc6-118">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c5fc6-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5fc6-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="c5fc6-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5fc6-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="c5fc6-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c5fc6-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="c5fc6-121">Schema Name</span></span>  <br/> |<span data-ttu-id="c5fc6-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="c5fc6-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c5fc6-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="c5fc6-123">Validation File</span></span>  <br/> |<span data-ttu-id="c5fc6-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c5fc6-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c5fc6-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="c5fc6-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="c5fc6-126">True</span><span class="sxs-lookup"><span data-stu-id="c5fc6-126">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c5fc6-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c5fc6-127">See also</span></span>



[<span data-ttu-id="c5fc6-128">GetInboxRules 操作</span><span class="sxs-lookup"><span data-stu-id="c5fc6-128">GetInboxRules operation</span></span>](getinboxrules-operation.md)

