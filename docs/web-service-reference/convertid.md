---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: ConvertId 元素定义转换支持 Exchange 格式之间的项目和文件夹标识符的请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 956f6464fd9013f9e72d2915f21c3b011d0add5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753593"
---
# <a name="convertid"></a><span data-ttu-id="8a517-104">ConvertId</span><span class="sxs-lookup"><span data-stu-id="8a517-104">ConvertId</span></span>

<span data-ttu-id="8a517-105">**ConvertId**元素定义转换支持 Exchange 格式之间的项目和文件夹标识符的请求。</span><span class="sxs-lookup"><span data-stu-id="8a517-105">The **ConvertId** element defines a request to convert item and folder identifiers between supported Exchange formats.</span></span> <span data-ttu-id="8a517-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="8a517-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 <span data-ttu-id="8a517-107">**ConvertIdType**</span><span class="sxs-lookup"><span data-stu-id="8a517-107">**ConvertIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8a517-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8a517-108">Attributes and elements</span></span>

<span data-ttu-id="8a517-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8a517-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8a517-110">属性</span><span class="sxs-lookup"><span data-stu-id="8a517-110">Attributes</span></span>

|<span data-ttu-id="8a517-111">**属性**</span><span class="sxs-lookup"><span data-stu-id="8a517-111">**Attribute**</span></span>|<span data-ttu-id="8a517-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a517-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a517-113">**DestinationFormat**</span><span class="sxs-lookup"><span data-stu-id="8a517-113">**DestinationFormat**</span></span> <br/> |<span data-ttu-id="8a517-114">描述将返回所有已转换的标识符的标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8a517-114">Describes the identifier format that will be returned for all the converted identifiers.</span></span> <span data-ttu-id="8a517-115">DestinationFormat 由 IdFormatType 描述。</span><span class="sxs-lookup"><span data-stu-id="8a517-115">The DestinationFormat is described by the IdFormatType.</span></span>  <br/> |
   
#### <a name="destinationformat-attribute"></a><span data-ttu-id="8a517-116">DestinationFormat 属性</span><span class="sxs-lookup"><span data-stu-id="8a517-116">DestinationFormat Attribute</span></span>

|<span data-ttu-id="8a517-117">**值**</span><span class="sxs-lookup"><span data-stu-id="8a517-117">**Value**</span></span>|<span data-ttu-id="8a517-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a517-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a517-119">**EwsLegacyId**</span><span class="sxs-lookup"><span data-stu-id="8a517-119">**EwsLegacyId**</span></span> <br/> |<span data-ttu-id="8a517-120">表示用于初始发行版 Exchange 2007 中提供的 Exchange Web 服务标识符的标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8a517-120">Represents the identifier format that is used for Exchange Web Services identifiers that are provided in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="8a517-121">**EwsId**</span><span class="sxs-lookup"><span data-stu-id="8a517-121">**EwsId**</span></span> <br/> |<span data-ttu-id="8a517-122">表示用于启动与 Exchange Server 2007 SP1 的 Exchange Web 服务标识符的标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8a517-122">Represents the identifier format that is used for Exchange Web Services identifiers starting with Exchange Server 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="8a517-123">**EntryId**</span><span class="sxs-lookup"><span data-stu-id="8a517-123">**EntryId**</span></span> <br/> |<span data-ttu-id="8a517-124">表示的 MAPI 标识符，如 PR_ENTRYID 属性中所示。</span><span class="sxs-lookup"><span data-stu-id="8a517-124">Represents the MAPI identifier, as in the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="8a517-125">**HexEntryId**</span><span class="sxs-lookup"><span data-stu-id="8a517-125">**HexEntryId**</span></span> <br/> |<span data-ttu-id="8a517-126">代表可用性日历事件标识符。</span><span class="sxs-lookup"><span data-stu-id="8a517-126">Represents the availability calendar event identifier.</span></span> <span data-ttu-id="8a517-127">这是 PR_ENTRYID 属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="8a517-127">This is a hexadecimal-encoded representation of the PR_ENTRYID property.</span></span>  <br/> |
|<span data-ttu-id="8a517-128">**StoreId**</span><span class="sxs-lookup"><span data-stu-id="8a517-128">**StoreId**</span></span> <br/> |<span data-ttu-id="8a517-129">表示 Exchange 存储区标识符。</span><span class="sxs-lookup"><span data-stu-id="8a517-129">Represents the Exchange store identifier.</span></span>  <br/> |
|<span data-ttu-id="8a517-130">**OwaId**</span><span class="sxs-lookup"><span data-stu-id="8a517-130">**OwaId**</span></span> <br/> |<span data-ttu-id="8a517-131">代表 Outlook Web Access 标识符格式。</span><span class="sxs-lookup"><span data-stu-id="8a517-131">Represents the Outlook Web Access identifier format.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8a517-132">子元素</span><span class="sxs-lookup"><span data-stu-id="8a517-132">Child elements</span></span>

|<span data-ttu-id="8a517-133">**元素**</span><span class="sxs-lookup"><span data-stu-id="8a517-133">**Element**</span></span>|<span data-ttu-id="8a517-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="8a517-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8a517-135">SourceIds</span><span class="sxs-lookup"><span data-stu-id="8a517-135">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="8a517-136">包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="8a517-136">Contains the source identifiers to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8a517-137">父元素</span><span class="sxs-lookup"><span data-stu-id="8a517-137">Parent elements</span></span>

<span data-ttu-id="8a517-138">无。</span><span class="sxs-lookup"><span data-stu-id="8a517-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8a517-139">备注</span><span class="sxs-lookup"><span data-stu-id="8a517-139">Remarks</span></span>

<span data-ttu-id="8a517-140">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8a517-140">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a517-141">元素信息</span><span class="sxs-lookup"><span data-stu-id="8a517-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a517-142">命名空间</span><span class="sxs-lookup"><span data-stu-id="8a517-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8a517-143">架构名称</span><span class="sxs-lookup"><span data-stu-id="8a517-143">Schema Name</span></span>  <br/> |<span data-ttu-id="8a517-144">邮件架构</span><span class="sxs-lookup"><span data-stu-id="8a517-144">messages schema</span></span>  <br/> |
|<span data-ttu-id="8a517-145">验证文件</span><span class="sxs-lookup"><span data-stu-id="8a517-145">Validation File</span></span>  <br/> |<span data-ttu-id="8a517-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8a517-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8a517-147">可以为空</span><span class="sxs-lookup"><span data-stu-id="8a517-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="8a517-148">False</span><span class="sxs-lookup"><span data-stu-id="8a517-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8a517-149">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8a517-149">See also</span></span>



[<span data-ttu-id="8a517-150">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="8a517-150">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="8a517-151">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="8a517-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="8a517-152">转换标识符</span><span class="sxs-lookup"><span data-stu-id="8a517-152">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

