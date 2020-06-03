---
title: 条目（PhysicalAddress）
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
ms.assetid: 9e5b6515-453e-4f4c-b55e-6ffefe23c31b
description: Entry 元素描述联系人项目的单个物理地址。
ms.openlocfilehash: 5e8343e9abebeeff8c2b81327b2e0f4ddcf45364
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459628"
---
# <a name="entry-physicaladdress"></a><span data-ttu-id="85890-103">条目（PhysicalAddress）</span><span class="sxs-lookup"><span data-stu-id="85890-103">Entry (PhysicalAddress)</span></span>

<span data-ttu-id="85890-104">**Entry**元素描述联系人项目的单个物理地址。</span><span class="sxs-lookup"><span data-stu-id="85890-104">The **Entry** element describes a single physical address for a contact item.</span></span> 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 <span data-ttu-id="85890-105">**PhysicalAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="85890-105">**PhysicalAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85890-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="85890-106">Attributes and elements</span></span>

<span data-ttu-id="85890-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="85890-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85890-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="85890-108">Attributes</span></span>

|<span data-ttu-id="85890-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="85890-109">**Attribute**</span></span>|<span data-ttu-id="85890-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="85890-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="85890-111">**Key**</span><span class="sxs-lookup"><span data-stu-id="85890-111">**Key**</span></span> <br/> | <span data-ttu-id="85890-112">标识物理地址。</span><span class="sxs-lookup"><span data-stu-id="85890-112">Identifies a physical address.</span></span><br/><br/> <span data-ttu-id="85890-113">以下是该属性可能的值：</span><span class="sxs-lookup"><span data-stu-id="85890-113">The following are the possible values for this attribute:</span></span><br/>  <br/><span data-ttu-id="85890-114">-业务</span><span class="sxs-lookup"><span data-stu-id="85890-114">-  Business</span></span>  <br/><span data-ttu-id="85890-115">-主页</span><span class="sxs-lookup"><span data-stu-id="85890-115">-  Home</span></span>  <br/><span data-ttu-id="85890-116">-其他</span><span class="sxs-lookup"><span data-stu-id="85890-116">-  Other</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="85890-117">子元素</span><span class="sxs-lookup"><span data-stu-id="85890-117">Child elements</span></span>

|<span data-ttu-id="85890-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="85890-118">**Element**</span></span>|<span data-ttu-id="85890-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="85890-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85890-120">地址</span><span class="sxs-lookup"><span data-stu-id="85890-120">Street</span></span>](street.md) <br/> |<span data-ttu-id="85890-121">表示联系人项目的街道地址。</span><span class="sxs-lookup"><span data-stu-id="85890-121">Represents a street address for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="85890-122">市/县</span><span class="sxs-lookup"><span data-stu-id="85890-122">City</span></span>](city.md) <br/> |<span data-ttu-id="85890-123">表示与联系人关联的城市名称。</span><span class="sxs-lookup"><span data-stu-id="85890-123">Represents the city name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="85890-124">State</span><span class="sxs-lookup"><span data-stu-id="85890-124">State</span></span>](state-ex15websvcsotherref.md) <br/> |<span data-ttu-id="85890-125">表示联系人项目的居住状态。</span><span class="sxs-lookup"><span data-stu-id="85890-125">Represents the state of residence for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="85890-126">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="85890-126">CountryOrRegion</span></span>](countryorregion.md) <br/> |<span data-ttu-id="85890-127">表示给定物理地址所在的国家或地区。</span><span class="sxs-lookup"><span data-stu-id="85890-127">Represents the country or region for a given physical address.</span></span>  <br/> |
|[<span data-ttu-id="85890-128">PostalCode</span><span class="sxs-lookup"><span data-stu-id="85890-128">PostalCode</span></span>](postalcode.md) <br/> |<span data-ttu-id="85890-129">表示联系人项目的邮政编码。</span><span class="sxs-lookup"><span data-stu-id="85890-129">Represents the postal code for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="85890-130">父元素</span><span class="sxs-lookup"><span data-stu-id="85890-130">Parent elements</span></span>

|<span data-ttu-id="85890-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="85890-131">**Element**</span></span>|<span data-ttu-id="85890-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="85890-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85890-133">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="85890-133">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="85890-134">包含与联系人关联的物理地址的集合。</span><span class="sxs-lookup"><span data-stu-id="85890-134">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="85890-135">说明</span><span class="sxs-lookup"><span data-stu-id="85890-135">Remarks</span></span>

<span data-ttu-id="85890-136">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="85890-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85890-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="85890-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85890-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="85890-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85890-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="85890-139">Schema Name</span></span>  <br/> |<span data-ttu-id="85890-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="85890-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="85890-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="85890-141">Validation File</span></span>  <br/> |<span data-ttu-id="85890-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85890-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85890-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="85890-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="85890-144">False</span><span class="sxs-lookup"><span data-stu-id="85890-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85890-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="85890-145">See also</span></span>

- [<span data-ttu-id="85890-146">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="85890-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="85890-147">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="85890-147">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="85890-148">更新联系人</span><span class="sxs-lookup"><span data-stu-id="85890-148">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="85890-149">删除联系人</span><span class="sxs-lookup"><span data-stu-id="85890-149">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

