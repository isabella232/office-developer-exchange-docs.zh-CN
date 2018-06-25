---
title: 条目 (PhysicalAddress)
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
description: Entry 元素描述联系人项目的单一物理地址。
ms.openlocfilehash: 4551e6117e5f91d901fe160f37e8f67cb1bc5ac7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754137"
---
# <a name="entry-physicaladdress"></a><span data-ttu-id="0f5a7-103">条目 (PhysicalAddress)</span><span class="sxs-lookup"><span data-stu-id="0f5a7-103">Entry (PhysicalAddress)</span></span>

<span data-ttu-id="0f5a7-104">**Entry**元素描述联系人项目的单一物理地址。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-104">The **Entry** element describes a single physical address for a contact item.</span></span> 
  
```xml
<Entry Key="">
   <Street/>
   <City/>
   <State/>
   <Country/>
   <PostalCode/>
</Entry>
```

 <span data-ttu-id="0f5a7-105">**PhysicalAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-105">**PhysicalAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0f5a7-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0f5a7-106">Attributes and elements</span></span>

<span data-ttu-id="0f5a7-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0f5a7-108">属性</span><span class="sxs-lookup"><span data-stu-id="0f5a7-108">Attributes</span></span>

|<span data-ttu-id="0f5a7-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-109">**Attribute**</span></span>|<span data-ttu-id="0f5a7-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0f5a7-111">**注册表项**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-111">**Key**</span></span> <br/> | <span data-ttu-id="0f5a7-112">标识物理地址。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-112">Identifies a physical address.</span></span><br/><br/> <span data-ttu-id="0f5a7-113">以下是该属性可能的值：</span><span class="sxs-lookup"><span data-stu-id="0f5a7-113">The following are the possible values for this attribute:</span></span><br/>  <br/><span data-ttu-id="0f5a7-114">线业务</span><span class="sxs-lookup"><span data-stu-id="0f5a7-114">-  Business</span></span>  <br/><span data-ttu-id="0f5a7-115">-主页</span><span class="sxs-lookup"><span data-stu-id="0f5a7-115">-  Home</span></span>  <br/><span data-ttu-id="0f5a7-116">-其他</span><span class="sxs-lookup"><span data-stu-id="0f5a7-116">-  Other</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0f5a7-117">子元素</span><span class="sxs-lookup"><span data-stu-id="0f5a7-117">Child elements</span></span>

|<span data-ttu-id="0f5a7-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-118">**Element**</span></span>|<span data-ttu-id="0f5a7-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f5a7-120">街道</span><span class="sxs-lookup"><span data-stu-id="0f5a7-120">Street</span></span>](street.md) <br/> |<span data-ttu-id="0f5a7-121">表示一个联系人项目的街道地址。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-121">Represents a street address for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="0f5a7-122">市/县</span><span class="sxs-lookup"><span data-stu-id="0f5a7-122">City</span></span>](city.md) <br/> |<span data-ttu-id="0f5a7-123">表示与联系人相关联的城市名称。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-123">Represents the city name that is associated with a contact.</span></span>  <br/> |
|[<span data-ttu-id="0f5a7-124">State</span><span class="sxs-lookup"><span data-stu-id="0f5a7-124">State</span></span>](state-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0f5a7-125">表示为联系人项居住地所在的状态。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-125">Represents the state of residence for a contact item.</span></span>  <br/> |
|[<span data-ttu-id="0f5a7-126">CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="0f5a7-126">CountryOrRegion</span></span>](countryorregion.md) <br/> |<span data-ttu-id="0f5a7-127">表示的国家或地区给定的物理地址。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-127">Represents the country or region for a given physical address.</span></span>  <br/> |
|[<span data-ttu-id="0f5a7-128">PostalCode</span><span class="sxs-lookup"><span data-stu-id="0f5a7-128">PostalCode</span></span>](postalcode.md) <br/> |<span data-ttu-id="0f5a7-129">表示一个联系人项目的邮政编码。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-129">Represents the postal code for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0f5a7-130">父元素</span><span class="sxs-lookup"><span data-stu-id="0f5a7-130">Parent elements</span></span>

|<span data-ttu-id="0f5a7-131">**元素**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-131">**Element**</span></span>|<span data-ttu-id="0f5a7-132">**说明**</span><span class="sxs-lookup"><span data-stu-id="0f5a7-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f5a7-133">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="0f5a7-133">PhysicalAddresses</span></span>](physicaladdresses.md) <br/> |<span data-ttu-id="0f5a7-134">包含与联系人关联的物理地址的集合。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-134">Contains a collection of physical addresses that are associated with a contact.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f5a7-135">备注</span><span class="sxs-lookup"><span data-stu-id="0f5a7-135">Remarks</span></span>

<span data-ttu-id="0f5a7-136">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0f5a7-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0f5a7-137">元素信息</span><span class="sxs-lookup"><span data-stu-id="0f5a7-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f5a7-138">命名空间</span><span class="sxs-lookup"><span data-stu-id="0f5a7-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0f5a7-139">架构名称</span><span class="sxs-lookup"><span data-stu-id="0f5a7-139">Schema Name</span></span>  <br/> |<span data-ttu-id="0f5a7-140">类型架构</span><span class="sxs-lookup"><span data-stu-id="0f5a7-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="0f5a7-141">验证文件</span><span class="sxs-lookup"><span data-stu-id="0f5a7-141">Validation File</span></span>  <br/> |<span data-ttu-id="0f5a7-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0f5a7-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0f5a7-143">可以为空</span><span class="sxs-lookup"><span data-stu-id="0f5a7-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="0f5a7-144">False</span><span class="sxs-lookup"><span data-stu-id="0f5a7-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0f5a7-145">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0f5a7-145">See also</span></span>

- [<span data-ttu-id="0f5a7-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0f5a7-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="0f5a7-147">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="0f5a7-147">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="0f5a7-148">更新联系人</span><span class="sxs-lookup"><span data-stu-id="0f5a7-148">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="0f5a7-149">删除联系人</span><span class="sxs-lookup"><span data-stu-id="0f5a7-149">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

