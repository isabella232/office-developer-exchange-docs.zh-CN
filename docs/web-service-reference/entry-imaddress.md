---
title: 条目 (IMAddress)
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
ms.assetid: ee444170-7353-4e86-86c6-d7300a2f1777
description: Entry 元素表示的即时消息 (IM) 的联系人的地址。
ms.openlocfilehash: 77de059cef470dde90ab0b929845cb260b4b867c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754151"
---
# <a name="entry-imaddress"></a><span data-ttu-id="768b3-103">条目 (IMAddress)</span><span class="sxs-lookup"><span data-stu-id="768b3-103">Entry (IMAddress)</span></span>

<span data-ttu-id="768b3-104">**Entry**元素表示的即时消息 (IM) 的联系人的地址。</span><span class="sxs-lookup"><span data-stu-id="768b3-104">The **Entry** element represents an instant messaging (IM) address for a contact.</span></span> 
  
```xml
<Entry Key=""/>
```

 <span data-ttu-id="768b3-105">**ImAddressDictionaryEntryType**</span><span class="sxs-lookup"><span data-stu-id="768b3-105">**ImAddressDictionaryEntryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="768b3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="768b3-106">Attributes and elements</span></span>

<span data-ttu-id="768b3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="768b3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="768b3-108">属性</span><span class="sxs-lookup"><span data-stu-id="768b3-108">Attributes</span></span>

|<span data-ttu-id="768b3-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="768b3-109">**Attribute**</span></span>|<span data-ttu-id="768b3-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="768b3-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="768b3-111">**注册表项**</span><span class="sxs-lookup"><span data-stu-id="768b3-111">**Key**</span></span> <br/> | <span data-ttu-id="768b3-112">标识的 IM 地址。</span><span class="sxs-lookup"><span data-stu-id="768b3-112">Identifies the IM address.</span></span><br/><br/><span data-ttu-id="768b3-113">以下是该属性可能的值：</span><span class="sxs-lookup"><span data-stu-id="768b3-113">The following are the possible values for this attribute:</span></span><br/><br/><span data-ttu-id="768b3-114">-ImAddress1</span><span class="sxs-lookup"><span data-stu-id="768b3-114">-  ImAddress1</span></span>  <br/><span data-ttu-id="768b3-115">-ImAddress2</span><span class="sxs-lookup"><span data-stu-id="768b3-115">-  ImAddress2</span></span>  <br/><span data-ttu-id="768b3-116">-ImAddress3</span><span class="sxs-lookup"><span data-stu-id="768b3-116">-  ImAddress3</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="768b3-117">子元素</span><span class="sxs-lookup"><span data-stu-id="768b3-117">Child elements</span></span>

<span data-ttu-id="768b3-118">无。</span><span class="sxs-lookup"><span data-stu-id="768b3-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="768b3-119">父元素</span><span class="sxs-lookup"><span data-stu-id="768b3-119">Parent elements</span></span>

|<span data-ttu-id="768b3-120">**元素**</span><span class="sxs-lookup"><span data-stu-id="768b3-120">**Element**</span></span>|<span data-ttu-id="768b3-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="768b3-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="768b3-122">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="768b3-122">ImAddresses</span></span>](imaddresses.md) <br/> |<span data-ttu-id="768b3-123">表示一个联系人的 IM 地址的集合。</span><span class="sxs-lookup"><span data-stu-id="768b3-123">Represents a collection of IM addresses for a contact.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="768b3-124">文本值</span><span class="sxs-lookup"><span data-stu-id="768b3-124">Text value</span></span>

<span data-ttu-id="768b3-125">如果使用此元素，则需要一个表示的 IM 地址的文本值。</span><span class="sxs-lookup"><span data-stu-id="768b3-125">A text value that represents the IM address is required if this element is used.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="768b3-126">备注</span><span class="sxs-lookup"><span data-stu-id="768b3-126">Remarks</span></span>

<span data-ttu-id="768b3-127">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="768b3-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="768b3-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="768b3-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="768b3-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="768b3-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="768b3-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="768b3-130">Schema name</span></span>  <br/> |<span data-ttu-id="768b3-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="768b3-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="768b3-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="768b3-132">Validation file</span></span>  <br/> |<span data-ttu-id="768b3-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="768b3-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="768b3-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="768b3-134">Can be empty</span></span>  <br/> |<span data-ttu-id="768b3-135">False</span><span class="sxs-lookup"><span data-stu-id="768b3-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="768b3-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="768b3-136">See also</span></span>

- [<span data-ttu-id="768b3-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="768b3-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="768b3-138">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="768b3-138">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)  
- [<span data-ttu-id="768b3-139">更新联系人</span><span class="sxs-lookup"><span data-stu-id="768b3-139">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [<span data-ttu-id="768b3-140">删除联系人</span><span class="sxs-lookup"><span data-stu-id="768b3-140">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

