---
title: 条目 (PhoneNumber)
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
ms.openlocfilehash: 3953488fb0b57fcf01c2fb99039478bbe03c7f5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754143"
---
# <a name="entry-phonenumber"></a><span data-ttu-id="850ae-103">条目 (PhoneNumber)</span><span class="sxs-lookup"><span data-stu-id="850ae-103">Entry (PhoneNumber)</span></span>

<span data-ttu-id="850ae-104">**Entry**元素表示联系人的电话号码。</span><span class="sxs-lookup"><span data-stu-id="850ae-104">The **Entry** element represents a telephone number for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="850ae-105">**PhoneNumberDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="850ae-105">**PhoneNumberDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="850ae-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="850ae-106">Attributes and elements</span></span>

<span data-ttu-id="850ae-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="850ae-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="850ae-108">属性</span><span class="sxs-lookup"><span data-stu-id="850ae-108">Attributes</span></span>

|<span data-ttu-id="850ae-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="850ae-109">**Attribute**</span></span>|<span data-ttu-id="850ae-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="850ae-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="850ae-111">**注册表项**</span><span class="sxs-lookup"><span data-stu-id="850ae-111">**Key**</span></span> <br/> | <span data-ttu-id="850ae-112">标识电话号码。</span><span class="sxs-lookup"><span data-stu-id="850ae-112">Identifies the telephone number.</span></span> <span data-ttu-id="850ae-113">Key 属性是类型**PhoneNumberKeyType**。</span><span class="sxs-lookup"><span data-stu-id="850ae-113">The Key attribute is of type **PhoneNumberKeyType**.</span></span><br/><br/> <span data-ttu-id="850ae-114">以下是该属性可能的值：</span><span class="sxs-lookup"><span data-stu-id="850ae-114">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="850ae-115">-AssistantPhone</span><span class="sxs-lookup"><span data-stu-id="850ae-115">-  AssistantPhone</span></span>  <br/><span data-ttu-id="850ae-116">-商务传真</span><span class="sxs-lookup"><span data-stu-id="850ae-116">-  BusinessFax</span></span>  <br/><span data-ttu-id="850ae-117">-BusinessPhone</span><span class="sxs-lookup"><span data-stu-id="850ae-117">-  BusinessPhone</span></span>  <br/><span data-ttu-id="850ae-118">-BusinessPhone2</span><span class="sxs-lookup"><span data-stu-id="850ae-118">-  BusinessPhone2</span></span>  <br/><span data-ttu-id="850ae-119">-回调</span><span class="sxs-lookup"><span data-stu-id="850ae-119">-  Callback</span></span>  <br/><span data-ttu-id="850ae-120">-CarPhone</span><span class="sxs-lookup"><span data-stu-id="850ae-120">-  CarPhone</span></span>  <br/><span data-ttu-id="850ae-121">-CompanyMainPhone</span><span class="sxs-lookup"><span data-stu-id="850ae-121">-  CompanyMainPhone</span></span>  <br/><span data-ttu-id="850ae-122">-HomeFax</span><span class="sxs-lookup"><span data-stu-id="850ae-122">-  HomeFax</span></span>  <br/><span data-ttu-id="850ae-123">-住宅电话</span><span class="sxs-lookup"><span data-stu-id="850ae-123">-  HomePhone</span></span>  <br/><span data-ttu-id="850ae-124">-HomePhone2</span><span class="sxs-lookup"><span data-stu-id="850ae-124">-  HomePhone2</span></span>  <br/><span data-ttu-id="850ae-125">Isdn</span><span class="sxs-lookup"><span data-stu-id="850ae-125">-  Isdn</span></span>  <br/><span data-ttu-id="850ae-126">-MobilePhone</span><span class="sxs-lookup"><span data-stu-id="850ae-126">-  MobilePhone</span></span>  <br/><span data-ttu-id="850ae-127">-OtherFax</span><span class="sxs-lookup"><span data-stu-id="850ae-127">-  OtherFax</span></span>  <br/><span data-ttu-id="850ae-128">-OtherTelephone</span><span class="sxs-lookup"><span data-stu-id="850ae-128">-  OtherTelephone</span></span>  <br/><span data-ttu-id="850ae-129">-寻呼机</span><span class="sxs-lookup"><span data-stu-id="850ae-129">-  Pager</span></span>  <br/><span data-ttu-id="850ae-130">-PrimaryPhone</span><span class="sxs-lookup"><span data-stu-id="850ae-130">-  PrimaryPhone</span></span>  <br/><span data-ttu-id="850ae-131">-RadioPhone</span><span class="sxs-lookup"><span data-stu-id="850ae-131">-  RadioPhone</span></span>  <br/><span data-ttu-id="850ae-132">-电报</span><span class="sxs-lookup"><span data-stu-id="850ae-132">-  Telex</span></span>  <br/><span data-ttu-id="850ae-133">-TtyTddPhone</span><span class="sxs-lookup"><span data-stu-id="850ae-133">-  TtyTddPhone</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="850ae-134">子元素</span><span class="sxs-lookup"><span data-stu-id="850ae-134">Child elements</span></span>

<span data-ttu-id="850ae-135">无。</span><span class="sxs-lookup"><span data-stu-id="850ae-135">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="850ae-136">父元素</span><span class="sxs-lookup"><span data-stu-id="850ae-136">Parent elements</span></span>

|<span data-ttu-id="850ae-137">**元素**</span><span class="sxs-lookup"><span data-stu-id="850ae-137">**Element**</span></span>|<span data-ttu-id="850ae-138">**说明**</span><span class="sxs-lookup"><span data-stu-id="850ae-138">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="850ae-139">PhoneNumbers</span><span class="sxs-lookup"><span data-stu-id="850ae-139">PhoneNumbers</span></span>](phonenumbers.md) <br/> |<span data-ttu-id="850ae-140">表示联系人的电话号码的集合。</span><span class="sxs-lookup"><span data-stu-id="850ae-140">Represents a collection of telephone numbers for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="850ae-141">文本值</span><span class="sxs-lookup"><span data-stu-id="850ae-141">Text value</span></span>

<span data-ttu-id="850ae-142">如果使用此元素，则需要一个表示电话号码的文本值。</span><span class="sxs-lookup"><span data-stu-id="850ae-142">A text value that represents a telephone number is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="850ae-143">备注</span><span class="sxs-lookup"><span data-stu-id="850ae-143">Remarks</span></span>

<span data-ttu-id="850ae-144">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="850ae-144">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="850ae-145">元素信息</span><span class="sxs-lookup"><span data-stu-id="850ae-145">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="850ae-146">命名空间</span><span class="sxs-lookup"><span data-stu-id="850ae-146">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="850ae-147">架构名称</span><span class="sxs-lookup"><span data-stu-id="850ae-147">Schema name</span></span>  <br/> |<span data-ttu-id="850ae-148">类型架构</span><span class="sxs-lookup"><span data-stu-id="850ae-148">Types schema</span></span>  <br/> |
|<span data-ttu-id="850ae-149">验证文件</span><span class="sxs-lookup"><span data-stu-id="850ae-149">Validation file</span></span>  <br/> |<span data-ttu-id="850ae-150">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="850ae-150">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="850ae-151">可以为空</span><span class="sxs-lookup"><span data-stu-id="850ae-151">Can be empty</span></span>  <br/> |<span data-ttu-id="850ae-152">False</span><span class="sxs-lookup"><span data-stu-id="850ae-152">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="850ae-153">另请参阅</span><span class="sxs-lookup"><span data-stu-id="850ae-153">See also</span></span>

- [<span data-ttu-id="850ae-154">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="850ae-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="850ae-155">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="850ae-155">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [<span data-ttu-id="850ae-156">更新联系人</span><span class="sxs-lookup"><span data-stu-id="850ae-156">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="850ae-157">删除联系人</span><span class="sxs-lookup"><span data-stu-id="850ae-157">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

