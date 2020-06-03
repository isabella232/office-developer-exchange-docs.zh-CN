---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: AlternateId 元素描述要在请求中转换的标识符和响应中转换后的标识符的结果。
ms.openlocfilehash: 26df68bd814c2d323630c6bb40b4c31745017c71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527451"
---
# <a name="alternateid"></a><span data-ttu-id="7d61d-103">AlternateId</span><span class="sxs-lookup"><span data-stu-id="7d61d-103">AlternateId</span></span>

<span data-ttu-id="7d61d-104">**AlternateId**元素描述要在请求中转换的标识符和响应中转换后的标识符的结果。</span><span class="sxs-lookup"><span data-stu-id="7d61d-104">The **AlternateId** element describes an identifier to convert in a request and the results of a converted identifier in the response.</span></span> 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 <span data-ttu-id="7d61d-105">**AlternateIdType**</span><span class="sxs-lookup"><span data-stu-id="7d61d-105">**AlternateIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7d61d-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7d61d-106">Attributes and elements</span></span>

<span data-ttu-id="7d61d-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7d61d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7d61d-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7d61d-108">Attributes</span></span>

|<span data-ttu-id="7d61d-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="7d61d-109">**Attribute**</span></span>|<span data-ttu-id="7d61d-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="7d61d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d61d-111">Id</span><span class="sxs-lookup"><span data-stu-id="7d61d-111">Id</span></span>  <br/> |<span data-ttu-id="7d61d-112">描述[ConvertId 操作](convertid-operation.md)请求中的源标识符，并描述[ConvertId 操作](convertid-operation.md)响应中的目标标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-112">Describes the source identifier in a [ConvertId operation](convertid-operation.md) request and describes the destination identifier in a [ConvertId operation](convertid-operation.md) response.</span></span>  <br/> |
|<span data-ttu-id="7d61d-113">Format</span><span class="sxs-lookup"><span data-stu-id="7d61d-113">Format</span></span>  <br/> |<span data-ttu-id="7d61d-114">描述[ConvertId 操作](convertid-operation.md)请求中的源格式，并描述[ConvertId 操作](convertid-operation.md)响应中的目标格式。</span><span class="sxs-lookup"><span data-stu-id="7d61d-114">Describes the source format in a [ConvertId operation](convertid-operation.md) request and describes the destination format in a [ConvertId operation](convertid-operation.md) response.</span></span> <span data-ttu-id="7d61d-115">目标格式由请求中的[ConvertId](convertid.md)元素的**DestinationFormat**属性描述。</span><span class="sxs-lookup"><span data-stu-id="7d61d-115">The destination format is described by the **DestinationFormat** attribute of the [ConvertId](convertid.md) element in the request.</span></span> <span data-ttu-id="7d61d-116">此属性的类型为**IdFormatType**。</span><span class="sxs-lookup"><span data-stu-id="7d61d-116">This attribute is of type **IdFormatType**.</span></span>  <br/> |
|<span data-ttu-id="7d61d-117">邮箱</span><span class="sxs-lookup"><span data-stu-id="7d61d-117">Mailbox</span></span>  <br/> |<span data-ttu-id="7d61d-118">描述邮箱主要简单邮件传输协议（SMTP）地址，该地址包含要翻译的标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-118">Describes the mailbox primary Simple Mail Transfer Protocol (SMTP) address that contains the identifiers to translate.</span></span>  <br/> |
|<span data-ttu-id="7d61d-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="7d61d-119">IsArchive</span></span>  <br/> |<span data-ttu-id="7d61d-120">指示标识符是否表示存档的项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="7d61d-120">Indicates whether the identifier represents an archived item or folder.</span></span> <span data-ttu-id="7d61d-121">**如果值为 true** ，则表示标识符表示存档项或文件夹。</span><span class="sxs-lookup"><span data-stu-id="7d61d-121">A value of **true** indicates that the identifier represents an archived item or folder.</span></span> <span data-ttu-id="7d61d-122">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="7d61d-122">This attribute is optional.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="7d61d-123">格式属性值</span><span class="sxs-lookup"><span data-stu-id="7d61d-123">Format attribute values</span></span>

|<span data-ttu-id="7d61d-124">**值**</span><span class="sxs-lookup"><span data-stu-id="7d61d-124">**Value**</span></span>|<span data-ttu-id="7d61d-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="7d61d-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d61d-126">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="7d61d-126">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="7d61d-127">介绍 exchange 2007 的初始发布版本中的 Exchange Web 服务生成的标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-127">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="7d61d-128">EwsId</span><span class="sxs-lookup"><span data-stu-id="7d61d-128">EwsId</span></span>  <br/> |<span data-ttu-id="7d61d-129">介绍了 Exchange Web 服务从 Exchange 2007 SP1 开始生成的标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-129">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="7d61d-130">EntryId</span><span class="sxs-lookup"><span data-stu-id="7d61d-130">EntryId</span></span>  <br/> |<span data-ttu-id="7d61d-131">描述 MAPI 标识符，如**PR_ENTRYID**属性中所示。</span><span class="sxs-lookup"><span data-stu-id="7d61d-131">Describes MAPI identifiers, as in the **PR_ENTRYID** property.</span></span>  <br/> |
|<span data-ttu-id="7d61d-132">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="7d61d-132">HexEntryId</span></span>  <br/> |<span data-ttu-id="7d61d-133">描述了**PR_ENTRYID**属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="7d61d-133">Describes a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="7d61d-134">这是可用性日历事件标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="7d61d-134">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="7d61d-135">StoreId</span><span class="sxs-lookup"><span data-stu-id="7d61d-135">StoreId</span></span>  <br/> |<span data-ttu-id="7d61d-136">描述 Exchange 存储标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-136">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="7d61d-137">OwaId</span><span class="sxs-lookup"><span data-stu-id="7d61d-137">OwaId</span></span>  <br/> |<span data-ttu-id="7d61d-138">介绍 Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-138">Describes an Outlook Web App identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7d61d-139">子元素</span><span class="sxs-lookup"><span data-stu-id="7d61d-139">Child elements</span></span>

<span data-ttu-id="7d61d-140">无。</span><span class="sxs-lookup"><span data-stu-id="7d61d-140">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7d61d-141">父元素</span><span class="sxs-lookup"><span data-stu-id="7d61d-141">Parent elements</span></span>

|<span data-ttu-id="7d61d-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="7d61d-142">**Element**</span></span>|<span data-ttu-id="7d61d-143">**描述**</span><span class="sxs-lookup"><span data-stu-id="7d61d-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7d61d-144">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7d61d-144">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md) <br/> |<span data-ttu-id="7d61d-145">包含[ConvertId 操作](convertid-operation.md)请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="7d61d-145">Contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="7d61d-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="7d61d-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="7d61d-147">包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-147">Contains the source identifiers to convert.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7d61d-148">文本值</span><span class="sxs-lookup"><span data-stu-id="7d61d-148">Text value</span></span>

<span data-ttu-id="7d61d-149">无。</span><span class="sxs-lookup"><span data-stu-id="7d61d-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d61d-150">说明</span><span class="sxs-lookup"><span data-stu-id="7d61d-150">Remarks</span></span>

<span data-ttu-id="7d61d-151">**AlternateId**元素描述两个标识符：要在[ConvertId 操作](convertid-operation.md)请求中转换的源标识符，以及[ConvertIdResponse](convertidresponse.md)元素中的已转换标识符。</span><span class="sxs-lookup"><span data-stu-id="7d61d-151">The **AlternateId** element describes two identifiers, the source identifier that is to be converted in the [ConvertId operation](convertid-operation.md) request, and the converted identifier in the [ConvertIdResponse](convertidresponse.md) element.</span></span> 
  
<span data-ttu-id="7d61d-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7d61d-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7d61d-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="7d61d-153">Element information</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="7d61d-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="7d61d-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7d61d-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="7d61d-155">Schema Name</span></span>  <br/> |<span data-ttu-id="7d61d-156">消息架构</span><span class="sxs-lookup"><span data-stu-id="7d61d-156">Messages schema</span></span>  <br/> |<span data-ttu-id="7d61d-157">类型架构</span><span class="sxs-lookup"><span data-stu-id="7d61d-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="7d61d-158">验证文件</span><span class="sxs-lookup"><span data-stu-id="7d61d-158">Validation File</span></span>  <br/> |<span data-ttu-id="7d61d-159">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7d61d-159">Messages.xsd</span></span>  <br/> |<span data-ttu-id="7d61d-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7d61d-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7d61d-161">可以为空</span><span class="sxs-lookup"><span data-stu-id="7d61d-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="7d61d-162">False</span><span class="sxs-lookup"><span data-stu-id="7d61d-162">False</span></span>  <br/> |<span data-ttu-id="7d61d-163">False</span><span class="sxs-lookup"><span data-stu-id="7d61d-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d61d-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7d61d-164">See also</span></span>

- [<span data-ttu-id="7d61d-165">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="7d61d-165">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="7d61d-166">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7d61d-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="7d61d-167">转换标识符</span><span class="sxs-lookup"><span data-stu-id="7d61d-167">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

