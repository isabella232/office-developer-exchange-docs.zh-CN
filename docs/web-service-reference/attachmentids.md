---
title: 会话
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttachmentIds
api_type:
- schema
ms.assetid: 46ce3ad7-4b20-43ae-8c63-39f1e3c2666b
description: 会话元素包含附件标识符的数组。
ms.openlocfilehash: cff1cb5658690fd6dd2c6a7812e1f600a4c80e29
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464250"
---
# <a name="attachmentids"></a><span data-ttu-id="fedda-103">会话</span><span class="sxs-lookup"><span data-stu-id="fedda-103">AttachmentIds</span></span>

<span data-ttu-id="fedda-104">**会话**元素包含附件标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="fedda-104">The **AttachmentIds** element contains an array of attachment identifiers.</span></span> 
  
```xml
<AttachmentIds>
   <AttachmentId Id=""/>
</AttachmentIds>
```

 <span data-ttu-id="fedda-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span><span class="sxs-lookup"><span data-stu-id="fedda-105">**NonEmptyArrayOfRequestAttachmentIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fedda-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fedda-106">Attributes and elements</span></span>

<span data-ttu-id="fedda-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fedda-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fedda-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fedda-108">Attributes</span></span>

<span data-ttu-id="fedda-109">无。</span><span class="sxs-lookup"><span data-stu-id="fedda-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fedda-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fedda-110">Child elements</span></span>

|<span data-ttu-id="fedda-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="fedda-111">**Element**</span></span>|<span data-ttu-id="fedda-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="fedda-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fedda-113">AttachmentId （GetAttachment 和 DeleteAttachment）</span><span class="sxs-lookup"><span data-stu-id="fedda-113">AttachmentId (GetAttachment and DeleteAttachment)</span></span>](attachmentid-getattachment-and-deleteattachment.md) <br/> |<span data-ttu-id="fedda-114">标识单个附件的元素。</span><span class="sxs-lookup"><span data-stu-id="fedda-114">The element that identifies a single attachment.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fedda-115">父元素</span><span class="sxs-lookup"><span data-stu-id="fedda-115">Parent elements</span></span>

|<span data-ttu-id="fedda-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="fedda-116">**Element**</span></span>|<span data-ttu-id="fedda-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="fedda-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fedda-118">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="fedda-118">DeleteAttachment</span></span>](deleteattachment.md) <br/> |<span data-ttu-id="fedda-119">定义从 Exchange 存储中删除附件的请求的元素。</span><span class="sxs-lookup"><span data-stu-id="fedda-119">The element that defines a request to delete an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="fedda-120">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="fedda-120">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteAttachment` <br/> |
|[<span data-ttu-id="fedda-121">GetAttachment</span><span class="sxs-lookup"><span data-stu-id="fedda-121">GetAttachment</span></span>](getattachment.md) <br/> |<span data-ttu-id="fedda-122">定义从 Exchange 存储中获取附件的请求的元素。</span><span class="sxs-lookup"><span data-stu-id="fedda-122">The element that defines a request to get an attachment from the Exchange store.</span></span>  <br/> <span data-ttu-id="fedda-123">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="fedda-123">The following is the XPath expression to this element:</span></span>  <br/>  `/GetAttachment` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fedda-124">说明</span><span class="sxs-lookup"><span data-stu-id="fedda-124">Remarks</span></span>

<span data-ttu-id="fedda-125">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fedda-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fedda-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="fedda-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fedda-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="fedda-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fedda-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="fedda-128">Schema Name</span></span>  <br/> |<span data-ttu-id="fedda-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="fedda-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fedda-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="fedda-130">Validation File</span></span>  <br/> |<span data-ttu-id="fedda-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fedda-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fedda-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="fedda-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="fedda-133">False</span><span class="sxs-lookup"><span data-stu-id="fedda-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fedda-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fedda-134">See also</span></span>

- [<span data-ttu-id="fedda-135">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="fedda-135">DeleteAttachment operation</span></span>](deleteattachment-operation.md)
- [<span data-ttu-id="fedda-136">GetAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="fedda-136">GetAttachment operation</span></span>](getattachment-operation.md)

