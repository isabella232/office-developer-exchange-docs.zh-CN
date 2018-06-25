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
description: AlternateId 元素描述要转换请求和响应中的转换标识符的结果中的标识符。
ms.openlocfilehash: e4d29087b63b52638dd93e4e3b643cdee39a5b97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753138"
---
# <a name="alternateid"></a><span data-ttu-id="d949b-103">AlternateId</span><span class="sxs-lookup"><span data-stu-id="d949b-103">AlternateId</span></span>

<span data-ttu-id="d949b-104">**AlternateId**元素描述要转换请求和响应中的转换标识符的结果中的标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-104">The **AlternateId** element describes an identifier to convert in a request and the results of a converted identifier in the response.</span></span> 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 <span data-ttu-id="d949b-105">**AlternateIdType**</span><span class="sxs-lookup"><span data-stu-id="d949b-105">**AlternateIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d949b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d949b-106">Attributes and elements</span></span>

<span data-ttu-id="d949b-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d949b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d949b-108">属性</span><span class="sxs-lookup"><span data-stu-id="d949b-108">Attributes</span></span>

|<span data-ttu-id="d949b-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="d949b-109">**Attribute**</span></span>|<span data-ttu-id="d949b-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="d949b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d949b-111">Id</span><span class="sxs-lookup"><span data-stu-id="d949b-111">Id</span></span>  <br/> |<span data-ttu-id="d949b-112">介绍[ConvertId 操作](convertid-operation.md)请求中的源标识符以及[ConvertId 操作](convertid-operation.md)响应中的目标标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-112">Describes the source identifier in a [ConvertId operation](convertid-operation.md) request and describes the destination identifier in a [ConvertId operation](convertid-operation.md) response.</span></span>  <br/> |
|<span data-ttu-id="d949b-113">格式</span><span class="sxs-lookup"><span data-stu-id="d949b-113">Format</span></span>  <br/> |<span data-ttu-id="d949b-114">介绍[ConvertId 操作](convertid-operation.md)请求中的源格式以及[ConvertId 操作](convertid-operation.md)响应中的目标格式。</span><span class="sxs-lookup"><span data-stu-id="d949b-114">Describes the source format in a [ConvertId operation](convertid-operation.md) request and describes the destination format in a [ConvertId operation](convertid-operation.md) response.</span></span> <span data-ttu-id="d949b-115">请求中的[ConvertId](convertid.md)元素的**DestinationFormat**属性描述了目标格式。</span><span class="sxs-lookup"><span data-stu-id="d949b-115">The destination format is described by the **DestinationFormat** attribute of the [ConvertId](convertid.md) element in the request.</span></span> <span data-ttu-id="d949b-116">此属性是类型**IdFormatType**。</span><span class="sxs-lookup"><span data-stu-id="d949b-116">This attribute is of type **IdFormatType**.</span></span>  <br/> |
|<span data-ttu-id="d949b-117">Mailbox</span><span class="sxs-lookup"><span data-stu-id="d949b-117">Mailbox</span></span>  <br/> |<span data-ttu-id="d949b-118">介绍邮箱主要简单邮件传输协议 (SMTP) 地址包含翻译的标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-118">Describes the mailbox primary Simple Mail Transfer Protocol (SMTP) address that contains the identifiers to translate.</span></span>  <br/> |
|<span data-ttu-id="d949b-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="d949b-119">IsArchive</span></span>  <br/> |<span data-ttu-id="d949b-120">指示标识符是否表示存档的项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="d949b-120">Indicates whether the identifier represents an archived item or folder.</span></span> <span data-ttu-id="d949b-121">值为**true**指示标识符表示存档的项目或文件夹。</span><span class="sxs-lookup"><span data-stu-id="d949b-121">A value of **true** indicates that the identifier represents an archived item or folder.</span></span> <span data-ttu-id="d949b-122">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="d949b-122">This attribute is optional.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="d949b-123">Format 属性值</span><span class="sxs-lookup"><span data-stu-id="d949b-123">Format attribute values</span></span>

|<span data-ttu-id="d949b-124">**值**</span><span class="sxs-lookup"><span data-stu-id="d949b-124">**Value**</span></span>|<span data-ttu-id="d949b-125">**说明**</span><span class="sxs-lookup"><span data-stu-id="d949b-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d949b-126">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="d949b-126">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="d949b-127">描述所产生的 Exchange Web 服务的初始发行版本的 Exchange 2007 中的标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-127">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="d949b-128">EwsId</span><span class="sxs-lookup"><span data-stu-id="d949b-128">EwsId</span></span>  <br/> |<span data-ttu-id="d949b-129">描述所产生的开头 Exchange 2007 SP1 的 Exchange Web 服务的标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-129">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="d949b-130">EntryId</span><span class="sxs-lookup"><span data-stu-id="d949b-130">EntryId</span></span>  <br/> |<span data-ttu-id="d949b-131">描述 MAPI 标识符，如**PR_ENTRYID**属性中所示。</span><span class="sxs-lookup"><span data-stu-id="d949b-131">Describes MAPI identifiers, as in the **PR_ENTRYID** property.</span></span>  <br/> |
|<span data-ttu-id="d949b-132">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="d949b-132">HexEntryId</span></span>  <br/> |<span data-ttu-id="d949b-133">介绍**PR_ENTRYID**属性的十六进制编码表示形式。</span><span class="sxs-lookup"><span data-stu-id="d949b-133">Describes a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="d949b-134">这是可用性日历事件标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="d949b-134">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="d949b-135">StoreId</span><span class="sxs-lookup"><span data-stu-id="d949b-135">StoreId</span></span>  <br/> |<span data-ttu-id="d949b-136">描述 Exchange 存储区标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-136">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="d949b-137">OwaId</span><span class="sxs-lookup"><span data-stu-id="d949b-137">OwaId</span></span>  <br/> |<span data-ttu-id="d949b-138">介绍 Outlook Web App 标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-138">Describes an Outlook Web App identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d949b-139">子元素</span><span class="sxs-lookup"><span data-stu-id="d949b-139">Child elements</span></span>

<span data-ttu-id="d949b-140">无。</span><span class="sxs-lookup"><span data-stu-id="d949b-140">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d949b-141">父元素</span><span class="sxs-lookup"><span data-stu-id="d949b-141">Parent elements</span></span>

|<span data-ttu-id="d949b-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="d949b-142">**Element**</span></span>|<span data-ttu-id="d949b-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="d949b-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d949b-144">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="d949b-144">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md) <br/> |<span data-ttu-id="d949b-145">包含状态和[ConvertId 操作](convertid-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="d949b-145">Contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="d949b-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="d949b-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="d949b-147">包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-147">Contains the source identifiers to convert.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d949b-148">文本值</span><span class="sxs-lookup"><span data-stu-id="d949b-148">Text value</span></span>

<span data-ttu-id="d949b-149">无。</span><span class="sxs-lookup"><span data-stu-id="d949b-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d949b-150">注解</span><span class="sxs-lookup"><span data-stu-id="d949b-150">Remarks</span></span>

<span data-ttu-id="d949b-151">**AlternateId**元素介绍两个标识符、 在[ConvertId 操作](convertid-operation.md)要求中，要转换的源标识符和[ConvertIdResponse](convertidresponse.md)元素中转换后的标识符。</span><span class="sxs-lookup"><span data-stu-id="d949b-151">The **AlternateId** element describes two identifiers, the source identifier that is to be converted in the [ConvertId operation](convertid-operation.md) request, and the converted identifier in the [ConvertIdResponse](convertidresponse.md) element.</span></span> 
  
<span data-ttu-id="d949b-152">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d949b-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d949b-153">元素信息</span><span class="sxs-lookup"><span data-stu-id="d949b-153">Element information</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="d949b-154">命名空间</span><span class="sxs-lookup"><span data-stu-id="d949b-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d949b-155">架构名称</span><span class="sxs-lookup"><span data-stu-id="d949b-155">Schema Name</span></span>  <br/> |<span data-ttu-id="d949b-156">消息架构</span><span class="sxs-lookup"><span data-stu-id="d949b-156">Messages schema</span></span>  <br/> |<span data-ttu-id="d949b-157">类型架构</span><span class="sxs-lookup"><span data-stu-id="d949b-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="d949b-158">验证文件</span><span class="sxs-lookup"><span data-stu-id="d949b-158">Validation File</span></span>  <br/> |<span data-ttu-id="d949b-159">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d949b-159">Messages.xsd</span></span>  <br/> |<span data-ttu-id="d949b-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d949b-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d949b-161">可以为空</span><span class="sxs-lookup"><span data-stu-id="d949b-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="d949b-162">False</span><span class="sxs-lookup"><span data-stu-id="d949b-162">False</span></span>  <br/> |<span data-ttu-id="d949b-163">False</span><span class="sxs-lookup"><span data-stu-id="d949b-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d949b-164">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d949b-164">See also</span></span>

- [<span data-ttu-id="d949b-165">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="d949b-165">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="d949b-166">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="d949b-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="d949b-167">转换标识符</span><span class="sxs-lookup"><span data-stu-id="d949b-167">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

