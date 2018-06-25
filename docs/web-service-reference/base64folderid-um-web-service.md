---
title: base64FolderId （UM web 服务）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- base64FolderId
api_type:
- schema
ms.assetid: 662f8f2f-49a7-4c7a-9065-98a02a49cfcd
description: Base64FolderId 元素包含指定为默认电子邮件文件夹从其统一消息读取消息通过电话 SetTelephoneAccessFolderEmail 操作 （UM web 服务） 请求中的文件夹的标识符。
ms.openlocfilehash: 7d710542418a717c6fcad243a22682e5840ebbd2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753314"
---
# <a name="base64folderid-um-web-service"></a><span data-ttu-id="5d99d-103">base64FolderId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d99d-103">base64FolderId (UM web service)</span></span>

<span data-ttu-id="5d99d-104">**Base64FolderId**元素包含指定为默认电子邮件文件夹从其统一消息读取消息通过电话[SetTelephoneAccessFolderEmail 操作 （UM web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)请求中的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="5d99d-104">The **base64FolderId** element contains the identifier of the folder to specify as the default e-mail folder from which Unified Messaging reads messages over the telephone in a [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md) request.</span></span> 
  
[<span data-ttu-id="5d99d-105">SetTelephoneAccessFolderEmail （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d99d-105">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="5d99d-106">base64FolderId （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d99d-106">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)
  
```xml
<base64FolderId/>
```

 <span data-ttu-id="5d99d-107">**string**</span><span class="sxs-lookup"><span data-stu-id="5d99d-107">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d99d-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="5d99d-108">Attributes and elements</span></span>

<span data-ttu-id="5d99d-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="5d99d-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d99d-110">属性</span><span class="sxs-lookup"><span data-stu-id="5d99d-110">Attributes</span></span>

<span data-ttu-id="5d99d-111">无</span><span class="sxs-lookup"><span data-stu-id="5d99d-111">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d99d-112">子元素</span><span class="sxs-lookup"><span data-stu-id="5d99d-112">Child elements</span></span>

<span data-ttu-id="5d99d-113">无。</span><span class="sxs-lookup"><span data-stu-id="5d99d-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5d99d-114">父元素</span><span class="sxs-lookup"><span data-stu-id="5d99d-114">Parent elements</span></span>

|<span data-ttu-id="5d99d-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="5d99d-115">**Element**</span></span>|<span data-ttu-id="5d99d-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="5d99d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d99d-117">SetTelephoneAccessFolderEmail （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d99d-117">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md) <br/> |<span data-ttu-id="5d99d-118">定义请求设置电话访问电子邮件文件夹。</span><span class="sxs-lookup"><span data-stu-id="5d99d-118">Defines request to set the telephone access e-mail folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5d99d-119">文本值</span><span class="sxs-lookup"><span data-stu-id="5d99d-119">Text value</span></span>

<span data-ttu-id="5d99d-120">文本值是必需的。</span><span class="sxs-lookup"><span data-stu-id="5d99d-120">A text value is required.</span></span> <span data-ttu-id="5d99d-121">文本值表示的文件夹的 MAPI ID。</span><span class="sxs-lookup"><span data-stu-id="5d99d-121">The text value represents the MAPI ID of the folder.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d99d-122">注解</span><span class="sxs-lookup"><span data-stu-id="5d99d-122">Remarks</span></span>

<span data-ttu-id="5d99d-123">若要设置电话访问电子邮件文件夹，使用[SetTelephoneAccessFolderEmail 操作 （UM web 服务）](settelephoneaccessfolderemail-operation-um-web-service.md)。</span><span class="sxs-lookup"><span data-stu-id="5d99d-123">To set the telephone access e-mail folder, use the [SetTelephoneAccessFolderEmail operation (UM web service)](settelephoneaccessfolderemail-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d99d-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="5d99d-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d99d-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="5d99d-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5d99d-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="5d99d-126">Schema Name</span></span>  <br/> |<span data-ttu-id="5d99d-127">邮件</span><span class="sxs-lookup"><span data-stu-id="5d99d-127">Messages</span></span>  <br/> |
|<span data-ttu-id="5d99d-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="5d99d-128">Validation File</span></span>  <br/> |<span data-ttu-id="5d99d-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5d99d-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5d99d-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="5d99d-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d99d-131">False</span><span class="sxs-lookup"><span data-stu-id="5d99d-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d99d-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5d99d-132">See also</span></span>



[<span data-ttu-id="5d99d-133">SetTelephoneAccessFolderEmail （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d99d-133">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="5d99d-134">SetTelephoneAccessFolderEmail 操作 （UM web 服务）</span><span class="sxs-lookup"><span data-stu-id="5d99d-134">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>](settelephoneaccessfolderemail-operation-um-web-service.md)
  
[<span data-ttu-id="5d99d-135">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="5d99d-135">FindFolder operation</span></span>](findfolder-operation.md)
  
[<span data-ttu-id="5d99d-136">FindItem 操作</span><span class="sxs-lookup"><span data-stu-id="5d99d-136">FindItem operation</span></span>](finditem-operation.md)

