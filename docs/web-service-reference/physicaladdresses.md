---
title: PhysicalAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PhysicalAddresses
api_type:
- schema
ms.assetid: 5276c5f2-9e08-43af-a0b2-da4ff1dcae2d
description: PhysicalAddresses 元素包含与联系人关联的物理地址的集合。
ms.openlocfilehash: b609abed481359fa6562f41a551645eb613ddfa0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468878"
---
# <a name="physicaladdresses"></a><span data-ttu-id="6565a-103">PhysicalAddresses</span><span class="sxs-lookup"><span data-stu-id="6565a-103">PhysicalAddresses</span></span>

<span data-ttu-id="6565a-104">**PhysicalAddresses**元素包含与联系人关联的物理地址的集合。</span><span class="sxs-lookup"><span data-stu-id="6565a-104">The **PhysicalAddresses** element contains a collection of physical addresses that are associated with a contact.</span></span> 
  
```xml
<PhysicalAddresses>
   <Entry/>
</PhysicalAddresses>
```

 <span data-ttu-id="6565a-105">**PhysicalAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="6565a-105">**PhysicalAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6565a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6565a-106">Attributes and elements</span></span>

<span data-ttu-id="6565a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6565a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6565a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6565a-108">Attributes</span></span>

<span data-ttu-id="6565a-109">无。</span><span class="sxs-lookup"><span data-stu-id="6565a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6565a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6565a-110">Child elements</span></span>

|<span data-ttu-id="6565a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6565a-111">**Element**</span></span>|<span data-ttu-id="6565a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6565a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6565a-113">条目（PhysicalAddress）</span><span class="sxs-lookup"><span data-stu-id="6565a-113">Entry (PhysicalAddress)</span></span>](entry-physicaladdress.md) <br/> |<span data-ttu-id="6565a-114">描述联系人项目的单个物理地址。</span><span class="sxs-lookup"><span data-stu-id="6565a-114">Describes a single physical address for a contact item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6565a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6565a-115">Parent elements</span></span>

|<span data-ttu-id="6565a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6565a-116">**Element**</span></span>|<span data-ttu-id="6565a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6565a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6565a-118">Contact</span><span class="sxs-lookup"><span data-stu-id="6565a-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6565a-119">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="6565a-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6565a-120">说明</span><span class="sxs-lookup"><span data-stu-id="6565a-120">Remarks</span></span>

<span data-ttu-id="6565a-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6565a-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6565a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="6565a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6565a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="6565a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6565a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="6565a-124">Schema name</span></span>  <br/> |<span data-ttu-id="6565a-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="6565a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="6565a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="6565a-126">Validation file</span></span>  <br/> |<span data-ttu-id="6565a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6565a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6565a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="6565a-128">Can be empty</span></span>  <br/> |<span data-ttu-id="6565a-129">False</span><span class="sxs-lookup"><span data-stu-id="6565a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6565a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6565a-130">See also</span></span>



- [<span data-ttu-id="6565a-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6565a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6565a-132">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="6565a-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="6565a-133">更新联系人</span><span class="sxs-lookup"><span data-stu-id="6565a-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="6565a-134">删除联系人</span><span class="sxs-lookup"><span data-stu-id="6565a-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

