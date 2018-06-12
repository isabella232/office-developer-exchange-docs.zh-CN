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
description: EmailAddresses 元素均表示一个联系人的电子邮件地址的集合。
ms.openlocfilehash: 2eddb68ecffd8f61a2fbb775d8013433d715db1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754061"
---
# <a name="emailaddresses"></a><span data-ttu-id="8910a-103">EmailAddresses</span><span class="sxs-lookup"><span data-stu-id="8910a-103">EmailAddresses</span></span>

<span data-ttu-id="8910a-104">**EmailAddresses**元素均表示一个联系人的电子邮件地址的集合。</span><span class="sxs-lookup"><span data-stu-id="8910a-104">The **EmailAddresses** element represents a collection of e-mail addresses for a contact.</span></span> 
  
```xml
<EmailAddresses>
   <Entry/>
</EmailAddresses>
```

 <span data-ttu-id="8910a-105">**EmailAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="8910a-105">**EmailAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8910a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8910a-106">Attributes and elements</span></span>

<span data-ttu-id="8910a-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8910a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8910a-108">属性</span><span class="sxs-lookup"><span data-stu-id="8910a-108">Attributes</span></span>

<span data-ttu-id="8910a-109">无。</span><span class="sxs-lookup"><span data-stu-id="8910a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8910a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8910a-110">Child elements</span></span>

|<span data-ttu-id="8910a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8910a-111">**Element**</span></span>|<span data-ttu-id="8910a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8910a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8910a-113">条目 （电子邮件地址）</span><span class="sxs-lookup"><span data-stu-id="8910a-113">Entry (EmailAddress)</span></span>](entry-emailaddress.md) <br/> |<span data-ttu-id="8910a-114">代表单个电子邮件地址的联系人。</span><span class="sxs-lookup"><span data-stu-id="8910a-114">Represents a single e-mail address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8910a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="8910a-115">Parent elements</span></span>

|<span data-ttu-id="8910a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="8910a-116">**Element**</span></span>|<span data-ttu-id="8910a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="8910a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8910a-118">联系人</span><span class="sxs-lookup"><span data-stu-id="8910a-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="8910a-119">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="8910a-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8910a-120">备注</span><span class="sxs-lookup"><span data-stu-id="8910a-120">Remarks</span></span>

<span data-ttu-id="8910a-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8910a-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8910a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="8910a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8910a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="8910a-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8910a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="8910a-124">Schema name</span></span>  <br/> |<span data-ttu-id="8910a-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="8910a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="8910a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="8910a-126">Validation file</span></span>  <br/> |<span data-ttu-id="8910a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8910a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8910a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="8910a-128">Can be empty</span></span>  <br/> |<span data-ttu-id="8910a-129">False</span><span class="sxs-lookup"><span data-stu-id="8910a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8910a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8910a-130">See also</span></span>

- [<span data-ttu-id="8910a-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8910a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8910a-132">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="8910a-132">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="8910a-133">更新联系人</span><span class="sxs-lookup"><span data-stu-id="8910a-133">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx) 
- [<span data-ttu-id="8910a-134">删除联系人</span><span class="sxs-lookup"><span data-stu-id="8910a-134">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

