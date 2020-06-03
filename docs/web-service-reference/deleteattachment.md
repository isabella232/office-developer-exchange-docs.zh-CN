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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457345"
---
# <a name="deleteattachment"></a><span data-ttu-id="c83d0-103">DeleteAttachment</span><span class="sxs-lookup"><span data-stu-id="c83d0-103">DeleteAttachment</span></span>

<span data-ttu-id="c83d0-104">**DeleteAttachment**元素是从 Exchange 存储中删除附件的请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="c83d0-104">The **DeleteAttachment** element is the root element in a request to delete an attachment from the Exchange store.</span></span> 
  
```xml
<DeleteAttachment>
   <AttachmentIds/>
</DeleteAttachment>
```

<span data-ttu-id="c83d0-105">**DeleteAttachmentType**</span><span class="sxs-lookup"><span data-stu-id="c83d0-105">**DeleteAttachmentType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="c83d0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c83d0-106">Attributes and elements</span></span>

<span data-ttu-id="c83d0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c83d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c83d0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c83d0-108">Attributes</span></span>

<span data-ttu-id="c83d0-109">无。</span><span class="sxs-lookup"><span data-stu-id="c83d0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c83d0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c83d0-110">Child elements</span></span>

|<span data-ttu-id="c83d0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="c83d0-111">**Element**</span></span>|<span data-ttu-id="c83d0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="c83d0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c83d0-113">会话</span><span class="sxs-lookup"><span data-stu-id="c83d0-113">AttachmentIds</span></span>](attachmentids.md) <br/> |<span data-ttu-id="c83d0-114">包含用于删除附件的附件标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="c83d0-114">Contains an array of attachment identifiers that are used to delete the attachments.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c83d0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="c83d0-115">Parent elements</span></span>

<span data-ttu-id="c83d0-116">无。</span><span class="sxs-lookup"><span data-stu-id="c83d0-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c83d0-117">说明</span><span class="sxs-lookup"><span data-stu-id="c83d0-117">Remarks</span></span>

<span data-ttu-id="c83d0-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c83d0-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c83d0-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="c83d0-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c83d0-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="c83d0-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c83d0-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="c83d0-121">Schema Name</span></span>  <br/> |<span data-ttu-id="c83d0-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="c83d0-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c83d0-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="c83d0-123">Validation File</span></span>  <br/> |<span data-ttu-id="c83d0-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c83d0-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c83d0-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="c83d0-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="c83d0-126">False</span><span class="sxs-lookup"><span data-stu-id="c83d0-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c83d0-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c83d0-127">See also</span></span>

- [<span data-ttu-id="c83d0-128">DeleteAttachment 操作</span><span class="sxs-lookup"><span data-stu-id="c83d0-128">DeleteAttachment operation</span></span>](deleteattachment-operation.md)

