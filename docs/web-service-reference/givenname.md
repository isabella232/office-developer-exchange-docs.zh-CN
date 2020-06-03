---
title: GivenName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GivenName
api_type:
- schema
ms.assetid: 8efc46fd-6056-4439-9af3-fc9e13ee6d9a
description: GivenName 元素包含联系人的名字。
ms.openlocfilehash: a22c5ef99844b55fa75f60acb8667ee423420336
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530132"
---
# <a name="givenname"></a><span data-ttu-id="6199e-103">GivenName</span><span class="sxs-lookup"><span data-stu-id="6199e-103">GivenName</span></span>

<span data-ttu-id="6199e-104">**GivenName**元素包含联系人的名字。</span><span class="sxs-lookup"><span data-stu-id="6199e-104">The **GivenName** element contains a contact's given name.</span></span> 
  
```xml
<GivenName/>
```

 <span data-ttu-id="6199e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="6199e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6199e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6199e-106">Attributes and elements</span></span>

<span data-ttu-id="6199e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6199e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6199e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6199e-108">Attributes</span></span>

<span data-ttu-id="6199e-109">无。</span><span class="sxs-lookup"><span data-stu-id="6199e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6199e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6199e-110">Child elements</span></span>

<span data-ttu-id="6199e-111">无。</span><span class="sxs-lookup"><span data-stu-id="6199e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6199e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6199e-112">Parent elements</span></span>

|<span data-ttu-id="6199e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6199e-113">**Element**</span></span>|<span data-ttu-id="6199e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6199e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6199e-115">Contact</span><span class="sxs-lookup"><span data-stu-id="6199e-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6199e-116">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="6199e-116">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6199e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6199e-117">Text value</span></span>

<span data-ttu-id="6199e-118">如果使用此元素，则需要一个表示联系人的名字的文本值。</span><span class="sxs-lookup"><span data-stu-id="6199e-118">A text value that represents a contact's given name is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6199e-119">备注</span><span class="sxs-lookup"><span data-stu-id="6199e-119">Remarks</span></span>

<span data-ttu-id="6199e-120">给定名称通常是个人的名字。</span><span class="sxs-lookup"><span data-stu-id="6199e-120">A given name is usually a person's first name.</span></span>
  
<span data-ttu-id="6199e-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6199e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6199e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="6199e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6199e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="6199e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6199e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="6199e-124">Schema name</span></span>  <br/> |<span data-ttu-id="6199e-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="6199e-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="6199e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="6199e-126">Validation file</span></span>  <br/> |<span data-ttu-id="6199e-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6199e-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6199e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="6199e-128">Can be empty</span></span>  <br/> |<span data-ttu-id="6199e-129">False</span><span class="sxs-lookup"><span data-stu-id="6199e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6199e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6199e-130">See also</span></span>



- [<span data-ttu-id="6199e-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6199e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6199e-132">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="6199e-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="6199e-133">更新联系人</span><span class="sxs-lookup"><span data-stu-id="6199e-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="6199e-134">删除联系人</span><span class="sxs-lookup"><span data-stu-id="6199e-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

