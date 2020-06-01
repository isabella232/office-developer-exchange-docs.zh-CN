---
title: PhoneNumbers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhoneNumbers
api_type:
- schema
ms.assetid: 6cb71be1-c4fe-4ce7-9604-11fc01956ee9
description: PhoneNumbers 元素表示联系人的电话号码的集合。
ms.openlocfilehash: b64d811618176377048d9ba80d8d7573f2df034a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44440230"
---
# <a name="phonenumbers"></a><span data-ttu-id="e6df5-103">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="e6df5-103">PhoneNumbers</span></span>

<span data-ttu-id="e6df5-104">**PhoneNumbers**元素表示联系人的电话号码的集合。</span><span class="sxs-lookup"><span data-stu-id="e6df5-104">The **PhoneNumbers** element represents a collection of telephone numbers for a contact.</span></span> 
  
```xml
<PhoneNumbers>
   <Entry/>
</PhoneNumbers>
```

 <span data-ttu-id="e6df5-105">**PhoneNumberDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="e6df5-105">**PhoneNumberDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e6df5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e6df5-106">Attributes and elements</span></span>

<span data-ttu-id="e6df5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e6df5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e6df5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="e6df5-108">Attributes</span></span>

<span data-ttu-id="e6df5-109">无。</span><span class="sxs-lookup"><span data-stu-id="e6df5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e6df5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e6df5-110">Child elements</span></span>

|<span data-ttu-id="e6df5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6df5-111">**Element**</span></span>|<span data-ttu-id="e6df5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6df5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6df5-113">条目（PhoneNumber）</span><span class="sxs-lookup"><span data-stu-id="e6df5-113">Entry (PhoneNumber)</span></span>](entry-phonenumber.md) <br/> |<span data-ttu-id="e6df5-114">表示联系人的电话号码。</span><span class="sxs-lookup"><span data-stu-id="e6df5-114">Represents a telephone number for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e6df5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="e6df5-115">Parent elements</span></span>

|<span data-ttu-id="e6df5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="e6df5-116">**Element**</span></span>|<span data-ttu-id="e6df5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="e6df5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e6df5-118">Contact</span><span class="sxs-lookup"><span data-stu-id="e6df5-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e6df5-119">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="e6df5-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6df5-120">说明</span><span class="sxs-lookup"><span data-stu-id="e6df5-120">Remarks</span></span>

<span data-ttu-id="e6df5-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e6df5-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e6df5-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="e6df5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e6df5-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="e6df5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e6df5-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="e6df5-124">Schema name</span></span>  <br/> |<span data-ttu-id="e6df5-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="e6df5-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="e6df5-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="e6df5-126">Validation file</span></span>  <br/> |<span data-ttu-id="e6df5-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e6df5-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e6df5-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="e6df5-128">Can be empty</span></span>  <br/> |<span data-ttu-id="e6df5-129">False</span><span class="sxs-lookup"><span data-stu-id="e6df5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e6df5-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e6df5-130">See also</span></span>



- [<span data-ttu-id="e6df5-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e6df5-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e6df5-132">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="e6df5-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="e6df5-133">更新联系人</span><span class="sxs-lookup"><span data-stu-id="e6df5-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="e6df5-134">删除联系人</span><span class="sxs-lookup"><span data-stu-id="e6df5-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

