---
title: MailboxCulture
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxCulture
api_type:
- schema
ms.assetid: 105cc061-3c35-455f-b102-8023e2055632
description: MailboxCulture 元素指示在打开邮箱时要使用的区域性。 此元素出现在 SOAP 标头中。
ms.openlocfilehash: 5760bac3b4589cdba599c5200db7d77b73855ca4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467807"
---
# <a name="mailboxculture"></a><span data-ttu-id="d66f9-104">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="d66f9-104">MailboxCulture</span></span>

<span data-ttu-id="d66f9-105">**MailboxCulture**元素指示在打开邮箱时要使用的区域性。</span><span class="sxs-lookup"><span data-stu-id="d66f9-105">The **MailboxCulture** element indicates the culture to use when opening a mailbox.</span></span> <span data-ttu-id="d66f9-106">此元素出现在 SOAP 标头中。</span><span class="sxs-lookup"><span data-stu-id="d66f9-106">This element occurs in the SOAP header.</span></span> 
  
```xml
<MailboxCulture/>
```

<span data-ttu-id="d66f9-107">**MailboxCultureType**</span><span class="sxs-lookup"><span data-stu-id="d66f9-107">**MailboxCultureType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d66f9-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d66f9-108">Attributes and elements</span></span>

<span data-ttu-id="d66f9-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d66f9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d66f9-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="d66f9-110">Attributes</span></span>

<span data-ttu-id="d66f9-111">无。</span><span class="sxs-lookup"><span data-stu-id="d66f9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d66f9-112">子元素</span><span class="sxs-lookup"><span data-stu-id="d66f9-112">Child elements</span></span>

<span data-ttu-id="d66f9-113">无。</span><span class="sxs-lookup"><span data-stu-id="d66f9-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d66f9-114">父元素</span><span class="sxs-lookup"><span data-stu-id="d66f9-114">Parent elements</span></span>

<span data-ttu-id="d66f9-115">无。</span><span class="sxs-lookup"><span data-stu-id="d66f9-115">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="d66f9-116">文本值</span><span class="sxs-lookup"><span data-stu-id="d66f9-116">Text value</span></span>

<span data-ttu-id="d66f9-117">该文本值指示在 Exchange Web 服务操作中使用的语言。</span><span class="sxs-lookup"><span data-stu-id="d66f9-117">The text value indicates the language that is used in the Exchange Web Service operations.</span></span> <span data-ttu-id="d66f9-118">RFC 3066 对此元素的可能值进行了描述。</span><span class="sxs-lookup"><span data-stu-id="d66f9-118">The possible values for this element are described by RFC 3066.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d66f9-119">备注</span><span class="sxs-lookup"><span data-stu-id="d66f9-119">Remarks</span></span>

<span data-ttu-id="d66f9-120">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d66f9-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d66f9-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="d66f9-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d66f9-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="d66f9-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d66f9-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="d66f9-123">Schema Name</span></span>  <br/> |<span data-ttu-id="d66f9-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="d66f9-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="d66f9-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="d66f9-125">Validation File</span></span>  <br/> |<span data-ttu-id="d66f9-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d66f9-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d66f9-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="d66f9-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="d66f9-128">False</span><span class="sxs-lookup"><span data-stu-id="d66f9-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d66f9-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d66f9-129">See also</span></span>

- [<span data-ttu-id="d66f9-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d66f9-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

