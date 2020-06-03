---
title: 生成
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Generation
api_type:
- schema
ms.assetid: a4812843-8aec-4fc4-945f-3aeb17a6593a
description: 世代元素代表联系人的全名后面的一种代缩写。
ms.openlocfilehash: 75246153d19632c1a0ad245a460584731275565e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463018"
---
# <a name="generation"></a><span data-ttu-id="5f992-103">生成</span><span class="sxs-lookup"><span data-stu-id="5f992-103">Generation</span></span>

<span data-ttu-id="5f992-104">**世代**元素代表联系人的全名后面的一种代缩写。</span><span class="sxs-lookup"><span data-stu-id="5f992-104">The **Generation** element represents a generational abbreviation that follows the full name of a contact.</span></span> 
  
```xml
<Generation/>
```

 <span data-ttu-id="5f992-105">**String**</span><span class="sxs-lookup"><span data-stu-id="5f992-105">**String**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5f992-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5f992-106">Attributes and elements</span></span>

<span data-ttu-id="5f992-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5f992-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5f992-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="5f992-108">Attributes</span></span>

<span data-ttu-id="5f992-109">无。</span><span class="sxs-lookup"><span data-stu-id="5f992-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5f992-110">子元素</span><span class="sxs-lookup"><span data-stu-id="5f992-110">Child elements</span></span>

<span data-ttu-id="5f992-111">无。</span><span class="sxs-lookup"><span data-stu-id="5f992-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5f992-112">父元素</span><span class="sxs-lookup"><span data-stu-id="5f992-112">Parent elements</span></span>

|<span data-ttu-id="5f992-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="5f992-113">**Element**</span></span>|<span data-ttu-id="5f992-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5f992-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5f992-115">Contact</span><span class="sxs-lookup"><span data-stu-id="5f992-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="5f992-116">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="5f992-116">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5f992-117">文本值</span><span class="sxs-lookup"><span data-stu-id="5f992-117">Text value</span></span>

<span data-ttu-id="5f992-118">如果使用此元素，则需要一个 text 值。</span><span class="sxs-lookup"><span data-stu-id="5f992-118">A text value is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f992-119">备注</span><span class="sxs-lookup"><span data-stu-id="5f992-119">Remarks</span></span>

<span data-ttu-id="5f992-120">此元素表示 PR_Generation MAPI 属性所表示的相同信息。</span><span class="sxs-lookup"><span data-stu-id="5f992-120">This element represents the same information that is represented by the PR_Generation MAPI property.</span></span>
  
<span data-ttu-id="5f992-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="5f992-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5f992-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="5f992-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5f992-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="5f992-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5f992-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="5f992-124">Schema name</span></span>  <br/> |<span data-ttu-id="5f992-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="5f992-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="5f992-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="5f992-126">Validation file</span></span>  <br/> |<span data-ttu-id="5f992-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5f992-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5f992-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="5f992-128">Can be empty</span></span>  <br/> |<span data-ttu-id="5f992-129">False</span><span class="sxs-lookup"><span data-stu-id="5f992-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5f992-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5f992-130">See also</span></span>



- [<span data-ttu-id="5f992-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="5f992-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="5f992-132">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="5f992-132">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="5f992-133">更新联系人</span><span class="sxs-lookup"><span data-stu-id="5f992-133">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="5f992-134">删除联系人</span><span class="sxs-lookup"><span data-stu-id="5f992-134">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

