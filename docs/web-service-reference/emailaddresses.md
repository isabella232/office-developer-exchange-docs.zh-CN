---
title: EmailAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EmailAddresses
api_type:
- schema
ms.assetid: fd4d773c-f7dc-4a04-9025-e772d7a45fdf
description: EmailAddresses 元素表示联系人的电子邮件地址的集合。
ms.openlocfilehash: 9d247f6159d621124ecdd9968ee468ed2b4fe84b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456176"
---
# <a name="emailaddresses"></a><span data-ttu-id="c97b3-103">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="c97b3-103">EmailAddresses</span></span>

<span data-ttu-id="c97b3-104">**EmailAddresses**元素表示联系人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="c97b3-104">The **EmailAddresses** element represents a collection of e-mail addresses for a contact.</span></span> 
  
```xml
<EmailAddresses>
   <Entry/>
</EmailAddresses>
```

 <span data-ttu-id="c97b3-105">**EmailAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="c97b3-105">**EmailAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c97b3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c97b3-106">Attributes and elements</span></span>

<span data-ttu-id="c97b3-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c97b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c97b3-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c97b3-108">Attributes</span></span>

<span data-ttu-id="c97b3-109">无。</span><span class="sxs-lookup"><span data-stu-id="c97b3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c97b3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c97b3-110">Child elements</span></span>

|<span data-ttu-id="c97b3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c97b3-111">**Element**</span></span>|<span data-ttu-id="c97b3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c97b3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c97b3-113">条目（EmailAddress）</span><span class="sxs-lookup"><span data-stu-id="c97b3-113">Entry (EmailAddress)</span></span>](entry-emailaddress.md) <br/> |<span data-ttu-id="c97b3-114">表示联系人的单个电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="c97b3-114">Represents a single e-mail address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c97b3-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c97b3-115">Parent elements</span></span>

|<span data-ttu-id="c97b3-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="c97b3-116">**Element**</span></span>|<span data-ttu-id="c97b3-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="c97b3-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c97b3-118">Contact</span><span class="sxs-lookup"><span data-stu-id="c97b3-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="c97b3-119">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="c97b3-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c97b3-120">说明</span><span class="sxs-lookup"><span data-stu-id="c97b3-120">Remarks</span></span>

<span data-ttu-id="c97b3-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c97b3-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c97b3-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="c97b3-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c97b3-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="c97b3-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c97b3-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="c97b3-124">Schema name</span></span>  <br/> |<span data-ttu-id="c97b3-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="c97b3-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="c97b3-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="c97b3-126">Validation file</span></span>  <br/> |<span data-ttu-id="c97b3-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c97b3-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c97b3-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="c97b3-128">Can be empty</span></span>  <br/> |<span data-ttu-id="c97b3-129">False</span><span class="sxs-lookup"><span data-stu-id="c97b3-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c97b3-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c97b3-130">See also</span></span>

- [<span data-ttu-id="c97b3-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c97b3-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="c97b3-132">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="c97b3-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="c97b3-133">更新联系人</span><span class="sxs-lookup"><span data-stu-id="c97b3-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx) 
- [<span data-ttu-id="c97b3-134">删除联系人</span><span class="sxs-lookup"><span data-stu-id="c97b3-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

