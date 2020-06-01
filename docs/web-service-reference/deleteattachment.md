---
title: DeleteAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 43d0c1cb-92ca-4399-9b3a-acb2b5c22624
description: DeleteAttachment 元素是从 Exchange 存储中删除附件的请求中的根元素。
ms.openlocfilehash: ae8dd5abc1dced2645e579a62f1f57a66cbc9877
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457345"
---
# <a name="deleteattachment"></a><span data-ttu-id="86a04-103">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="86a04-103">DeleteAttachment</span></span>

<span data-ttu-id="86a04-104">**DeleteAttachment**元素是从 Exchange 存储中删除附件的请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="86a04-104">The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store.</span></span> 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

<span data-ttu-id="86a04-105">**DeleteAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="86a04-105">**DeleteAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="86a04-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="86a04-106">Attributes and elements</span></span>

<span data-ttu-id="86a04-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="86a04-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86a04-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="86a04-108">Attributes</span></span>

<span data-ttu-id="86a04-109">无。</span><span class="sxs-lookup"><span data-stu-id="86a04-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="86a04-110">子元素</span><span class="sxs-lookup"><span data-stu-id="86a04-110">Child elements</span></span>

|<span data-ttu-id="86a04-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="86a04-111">**Element**</span></span>|<span data-ttu-id="86a04-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="86a04-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86a04-113">会话</span><span class="sxs-lookup"><span data-stu-id="86a04-113">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="86a04-114">包含用于删除附件的附件标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="86a04-114">Contains an array of attachment identifiers that are used to delete the attachments.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="86a04-115">父元素</span><span class="sxs-lookup"><span data-stu-id="86a04-115">Parent elements</span></span>

<span data-ttu-id="86a04-116">无。</span><span class="sxs-lookup"><span data-stu-id="86a04-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86a04-117">说明</span><span class="sxs-lookup"><span data-stu-id="86a04-117">Remarks</span></span>

<span data-ttu-id="86a04-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="86a04-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="86a04-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="86a04-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86a04-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="86a04-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="86a04-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="86a04-121">Schema Name</span></span>  <br/> |<span data-ttu-id="86a04-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="86a04-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="86a04-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="86a04-123">Validation File</span></span>  <br/> |<span data-ttu-id="86a04-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="86a04-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="86a04-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="86a04-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="86a04-126">False</span><span class="sxs-lookup"><span data-stu-id="86a04-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="86a04-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="86a04-127">See also</span></span>

- [<span data-ttu-id="86a04-128">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="86a04-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

