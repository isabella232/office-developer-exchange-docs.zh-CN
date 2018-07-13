---
title: 联系人
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
ms.openlocfilehash: da7963d30f58f7da52e76e3f7f1d0f7fd68abf74
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753498"
---
# <a name="contacts"></a><span data-ttu-id="6b8c6-103">联系人</span><span class="sxs-lookup"><span data-stu-id="6b8c6-103">Contacts</span></span>

<span data-ttu-id="6b8c6-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Contacts** 元素包含与任务相关联的联系人列表。</span><span class="sxs-lookup"><span data-stu-id="6b8c6-104">The **Contacts** element contains a list of contacts that are associated with a task.</span></span> 
  
```xml
<Contacts>
   <String/>
</Contacts>
```

 <span data-ttu-id="6b8c6-105">**ArrayOfStringsType**</span><span class="sxs-lookup"><span data-stu-id="6b8c6-105">**ArrayOfStringsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b8c6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6b8c6-106">Attributes and elements</span></span>

<span data-ttu-id="6b8c6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6b8c6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b8c6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6b8c6-108">Attributes</span></span>

<span data-ttu-id="6b8c6-109">无。</span><span class="sxs-lookup"><span data-stu-id="6b8c6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b8c6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6b8c6-110">Child elements</span></span>

|<span data-ttu-id="6b8c6-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6b8c6-111">**Element**</span></span>|<span data-ttu-id="6b8c6-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6b8c6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b8c6-113">字符串</span><span class="sxs-lookup"><span data-stu-id="6b8c6-113">String</span></span>](string.md) <br/> |<span data-ttu-id="6b8c6-114">表示以逗号分隔的联系人姓名列表。</span><span class="sxs-lookup"><span data-stu-id="6b8c6-114">Represents a comma-separated list of contact names.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6b8c6-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6b8c6-115">Parent elements</span></span>

|<span data-ttu-id="6b8c6-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="6b8c6-116">**Element**</span></span>|<span data-ttu-id="6b8c6-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="6b8c6-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6b8c6-118">任务</span><span class="sxs-lookup"><span data-stu-id="6b8c6-118">Task</span></span>](task.md) <br/> |<span data-ttu-id="6b8c6-119">表示 Exchange 存储中的任务。</span><span class="sxs-lookup"><span data-stu-id="6b8c6-119">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b8c6-120">说明</span><span class="sxs-lookup"><span data-stu-id="6b8c6-120">Remarks</span></span>

<span data-ttu-id="6b8c6-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6b8c6-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b8c6-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="6b8c6-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b8c6-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="6b8c6-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6b8c6-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="6b8c6-124">Schema name</span></span>  <br/> |<span data-ttu-id="6b8c6-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="6b8c6-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="6b8c6-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="6b8c6-126">Validation file</span></span>  <br/> |<span data-ttu-id="6b8c6-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6b8c6-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6b8c6-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="6b8c6-128">Can be empty</span></span>  <br/> |<span data-ttu-id="6b8c6-129">False</span><span class="sxs-lookup"><span data-stu-id="6b8c6-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b8c6-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6b8c6-130">See also</span></span>



- [<span data-ttu-id="6b8c6-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6b8c6-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

