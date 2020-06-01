---
title: 条目（PhoneNumber）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: Entry 元素表示联系人的电话号码。
ms.openlocfilehash: 62f7091bb750dc7ca74b1e5637a437e2cdad4f1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459635"
---
# <a name="entry-phonenumber"></a><span data-ttu-id="70fad-103">条目（PhoneNumber）</span><span class="sxs-lookup"><span data-stu-id="70fad-103">Entry (PhoneNumber)</span></span>

<span data-ttu-id="70fad-104">**Entry**元素表示联系人的电话号码。</span><span class="sxs-lookup"><span data-stu-id="70fad-104">The **Entry** element represents a telephone number for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="70fad-105">**PhoneNumberDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="70fad-105">**PhoneNumberDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70fad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="70fad-106">Attributes and elements</span></span>

<span data-ttu-id="70fad-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="70fad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70fad-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="70fad-108">Attributes</span></span>

|<span data-ttu-id="70fad-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="70fad-109">**Attribute**</span></span>|<span data-ttu-id="70fad-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="70fad-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70fad-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="70fad-111">**Key**</span></span> <br/> | <span data-ttu-id="70fad-112">标识电话号码。</span><span class="sxs-lookup"><span data-stu-id="70fad-112">Identifies the telephone number.</span></span> <span data-ttu-id="70fad-113">Key 属性的类型为**PhoneNumberKeyType**。</span><span class="sxs-lookup"><span data-stu-id="70fad-113">The Key attribute is of type **PhoneNumberKeyType**.</span></span><br/><br/> <span data-ttu-id="70fad-114">以下是该属性可能的值：</span><span class="sxs-lookup"><span data-stu-id="70fad-114">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="70fad-115">- AssistantPhone</span><span class="sxs-lookup"><span data-stu-id="70fad-115">-  AssistantPhone</span></span>  <br/><span data-ttu-id="70fad-116">- BusinessFax</span><span class="sxs-lookup"><span data-stu-id="70fad-116">-  BusinessFax</span></span>  <br/><span data-ttu-id="70fad-117">- BusinessPhone</span><span class="sxs-lookup"><span data-stu-id="70fad-117">-  BusinessPhone</span></span>  <br/><span data-ttu-id="70fad-118">- BusinessPhone2</span><span class="sxs-lookup"><span data-stu-id="70fad-118">-  BusinessPhone2</span></span>  <br/><span data-ttu-id="70fad-119">-回调</span><span class="sxs-lookup"><span data-stu-id="70fad-119">-  Callback</span></span>  <br/><span data-ttu-id="70fad-120">- CarPhone</span><span class="sxs-lookup"><span data-stu-id="70fad-120">-  CarPhone</span></span>  <br/><span data-ttu-id="70fad-121">- CompanyMainPhone</span><span class="sxs-lookup"><span data-stu-id="70fad-121">-  CompanyMainPhone</span></span>  <br/><span data-ttu-id="70fad-122">- HomeFax</span><span class="sxs-lookup"><span data-stu-id="70fad-122">-  HomeFax</span></span>  <br/><span data-ttu-id="70fad-123">-HomePhone</span><span class="sxs-lookup"><span data-stu-id="70fad-123">-  HomePhone</span></span>  <br/><span data-ttu-id="70fad-124">- HomePhone2</span><span class="sxs-lookup"><span data-stu-id="70fad-124">-  HomePhone2</span></span>  <br/><span data-ttu-id="70fad-125">-Isdn</span><span class="sxs-lookup"><span data-stu-id="70fad-125">-  Isdn</span></span>  <br/><span data-ttu-id="70fad-126">-MobilePhone</span><span class="sxs-lookup"><span data-stu-id="70fad-126">-  MobilePhone</span></span>  <br/><span data-ttu-id="70fad-127">-OtherFax</span><span class="sxs-lookup"><span data-stu-id="70fad-127">-  OtherFax</span></span>  <br/><span data-ttu-id="70fad-128">-OtherTelephone</span><span class="sxs-lookup"><span data-stu-id="70fad-128">-  OtherTelephone</span></span>  <br/><span data-ttu-id="70fad-129">-寻呼机</span><span class="sxs-lookup"><span data-stu-id="70fad-129">-  Pager</span></span>  <br/><span data-ttu-id="70fad-130">- PrimaryPhone</span><span class="sxs-lookup"><span data-stu-id="70fad-130">-  PrimaryPhone</span></span>  <br/><span data-ttu-id="70fad-131">- RadioPhone</span><span class="sxs-lookup"><span data-stu-id="70fad-131">-  RadioPhone</span></span>  <br/><span data-ttu-id="70fad-132">-电报</span><span class="sxs-lookup"><span data-stu-id="70fad-132">-  Telex</span></span>  <br/><span data-ttu-id="70fad-133">- TtyTddPhone</span><span class="sxs-lookup"><span data-stu-id="70fad-133">-  TtyTddPhone</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="70fad-134">子元素</span><span class="sxs-lookup"><span data-stu-id="70fad-134">Child elements</span></span>

<span data-ttu-id="70fad-135">无。</span><span class="sxs-lookup"><span data-stu-id="70fad-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="70fad-136">父元素</span><span class="sxs-lookup"><span data-stu-id="70fad-136">Parent elements</span></span>

|<span data-ttu-id="70fad-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="70fad-137">**Element**</span></span>|<span data-ttu-id="70fad-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="70fad-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70fad-139">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="70fad-139">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="70fad-140">表示联系人的电话号码的集合。</span><span class="sxs-lookup"><span data-stu-id="70fad-140">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="70fad-141">文本值</span><span class="sxs-lookup"><span data-stu-id="70fad-141">Text value</span></span>

<span data-ttu-id="70fad-142">如果使用此元素，则表示电话号码的文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="70fad-142">A text value that represents a telephone number is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70fad-143">说明</span><span class="sxs-lookup"><span data-stu-id="70fad-143">Remarks</span></span>

<span data-ttu-id="70fad-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="70fad-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70fad-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="70fad-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70fad-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="70fad-146">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="70fad-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="70fad-147">Schema name</span></span>  <br/> |<span data-ttu-id="70fad-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="70fad-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="70fad-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="70fad-149">Validation file</span></span>  <br/> |<span data-ttu-id="70fad-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="70fad-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="70fad-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="70fad-151">Can be empty</span></span>  <br/> |<span data-ttu-id="70fad-152">False</span><span class="sxs-lookup"><span data-stu-id="70fad-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70fad-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70fad-153">See also</span></span>

- [<span data-ttu-id="70fad-154">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="70fad-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="70fad-155">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="70fad-155">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="70fad-156">更新联系人</span><span class="sxs-lookup"><span data-stu-id="70fad-156">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="70fad-157">删除联系人</span><span class="sxs-lookup"><span data-stu-id="70fad-157">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

