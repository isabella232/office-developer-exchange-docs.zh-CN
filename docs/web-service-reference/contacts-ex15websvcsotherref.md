---
title: Contacts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contacts
api_type:
- schema
ms.assetid: 0cc67cdf-9707-45e7-92c6-fa83a016cdbe
description: Contacts 元素包含与任务相关联的联系人列表。
ms.openlocfilehash: c2b7bbadd494081a3e47b7b6c489218fab31d574
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458388"
---
# <a name="contacts"></a><span data-ttu-id="b4b0a-103">联系人</span><span class="sxs-lookup"><span data-stu-id="b4b0a-103">Contacts</span></span>

<span data-ttu-id="b4b0a-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Contacts** 元素包含与任务相关联的联系人列表。</span><span class="sxs-lookup"><span data-stu-id="b4b0a-104">The **Contacts** element contains a list of contacts that are associated with a task.</span></span> 
  
```xml
<Contacts>
   <String/>
</Contacts>
```

 <span data-ttu-id="b4b0a-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="b4b0a-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4b0a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b4b0a-106">Attributes and elements</span></span>

<span data-ttu-id="b4b0a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b4b0a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4b0a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b4b0a-108">Attributes</span></span>

<span data-ttu-id="b4b0a-109">无。</span><span class="sxs-lookup"><span data-stu-id="b4b0a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4b0a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b4b0a-110">Child elements</span></span>

|<span data-ttu-id="b4b0a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b4b0a-111">**Element**</span></span>|<span data-ttu-id="b4b0a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b4b0a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4b0a-113">字符串</span><span class="sxs-lookup"><span data-stu-id="b4b0a-113">String</span></span>](string.md) <br/> |<span data-ttu-id="b4b0a-114">表示以逗号分隔的联系人姓名列表。</span><span class="sxs-lookup"><span data-stu-id="b4b0a-114">Represents a comma-separated list of contact names.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b4b0a-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b4b0a-115">Parent elements</span></span>

|<span data-ttu-id="b4b0a-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b4b0a-116">**Element**</span></span>|<span data-ttu-id="b4b0a-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b4b0a-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4b0a-118">任务</span><span class="sxs-lookup"><span data-stu-id="b4b0a-118">Task</span></span>](task.md) <br/> |<span data-ttu-id="b4b0a-119">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="b4b0a-119">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4b0a-120">说明</span><span class="sxs-lookup"><span data-stu-id="b4b0a-120">Remarks</span></span>

<span data-ttu-id="b4b0a-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b4b0a-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4b0a-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b4b0a-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4b0a-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b4b0a-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b4b0a-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b4b0a-124">Schema name</span></span>  <br/> |<span data-ttu-id="b4b0a-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="b4b0a-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b4b0a-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b4b0a-126">Validation file</span></span>  <br/> |<span data-ttu-id="b4b0a-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b4b0a-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b4b0a-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b4b0a-128">Can be empty</span></span>  <br/> |<span data-ttu-id="b4b0a-129">False</span><span class="sxs-lookup"><span data-stu-id="b4b0a-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4b0a-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b4b0a-130">See also</span></span>



- [<span data-ttu-id="b4b0a-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b4b0a-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

