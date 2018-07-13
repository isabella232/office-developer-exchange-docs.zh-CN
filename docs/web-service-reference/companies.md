---
title: Companies
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Companies
api_type:
- schema
ms.assetid: 5d9ea76f-e14d-4424-8842-0c3cc3305119
description: Companies 元素表示与某个联系人或任务相关联的公司集合。
ms.openlocfilehash: 5b8ac20d4a02017881f941d12380fe29078f51cc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753458"
---
# <a name="companies"></a><span data-ttu-id="6526e-103">Companies</span><span class="sxs-lookup"><span data-stu-id="6526e-103">Companies</span></span>

<span data-ttu-id="6526e-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Companies** 元素表示与某个联系人或任务相关联的公司集合。</span><span class="sxs-lookup"><span data-stu-id="6526e-104">The **Companies** element represents the collection of companies that are associated with a contact or task.</span></span> 
  
```xml
<Companies>
   <String/>
</Companies>
```

 <span data-ttu-id="6526e-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="6526e-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6526e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6526e-106">Attributes and elements</span></span>

<span data-ttu-id="6526e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6526e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6526e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6526e-108">Attributes</span></span>

<span data-ttu-id="6526e-109">无。</span><span class="sxs-lookup"><span data-stu-id="6526e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6526e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6526e-110">Child elements</span></span>

|<span data-ttu-id="6526e-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6526e-111">**Element**</span></span>|<span data-ttu-id="6526e-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6526e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6526e-113">字符串</span><span class="sxs-lookup"><span data-stu-id="6526e-113">String</span></span>](string.md) <br/> |<span data-ttu-id="6526e-114">表示公司名称。</span><span class="sxs-lookup"><span data-stu-id="6526e-114">Represents the name of a company.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6526e-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6526e-115">Parent elements</span></span>

|<span data-ttu-id="6526e-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6526e-116">**Element**</span></span>|<span data-ttu-id="6526e-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6526e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6526e-118">Contact</span><span class="sxs-lookup"><span data-stu-id="6526e-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6526e-119">表示 Exchange 存储中的联系人。</span><span class="sxs-lookup"><span data-stu-id="6526e-119">Represents a contact in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="6526e-120">任务</span><span class="sxs-lookup"><span data-stu-id="6526e-120">Task</span></span>](task.md) <br/> |<span data-ttu-id="6526e-121">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="6526e-121">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6526e-122">说明</span><span class="sxs-lookup"><span data-stu-id="6526e-122">Remarks</span></span>

<span data-ttu-id="6526e-123">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6526e-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6526e-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="6526e-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6526e-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="6526e-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6526e-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="6526e-126">Schema name</span></span>  <br/> |<span data-ttu-id="6526e-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="6526e-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="6526e-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="6526e-128">Validation file</span></span>  <br/> |<span data-ttu-id="6526e-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6526e-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6526e-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="6526e-130">Can be empty</span></span>  <br/> |<span data-ttu-id="6526e-131">False</span><span class="sxs-lookup"><span data-stu-id="6526e-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6526e-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6526e-132">See also</span></span>



- [<span data-ttu-id="6526e-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6526e-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

