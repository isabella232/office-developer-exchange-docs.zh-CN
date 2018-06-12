---
title: GetUserOofSettingsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 011cb38b-da3c-4b1b-8836-a6b212b511f6
description: GetUserOofSettingsResponse 元素包含响应消息和用户的外出 (OOF) 设置。
ms.openlocfilehash: dc63b6d54471973ce5961a5a5ad6a23f6521fc0e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825693"
---
# <a name="getuseroofsettingsresponse"></a><span data-ttu-id="7cce3-103">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="7cce3-103">GetUserOofSettingsResponse</span></span>

<span data-ttu-id="7cce3-104">**GetUserOofSettingsResponse**元素包含响应消息和用户的外出 (OOF) 设置。</span><span class="sxs-lookup"><span data-stu-id="7cce3-104">The **GetUserOofSettingsResponse** element contains the response message and the Out of Office (OOF) settings for a user.</span></span> 
  
```xml
<GetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
   <OofSettings>...</OofSettings>
   <AllowExternalOof>...</AllowExternalOof>
</GetUserOofSettingsResponse>
```

 <span data-ttu-id="7cce3-105">**GetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="7cce3-105">**GetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7cce3-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7cce3-106">Attributes and elements</span></span>

<span data-ttu-id="7cce3-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7cce3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cce3-108">属性</span><span class="sxs-lookup"><span data-stu-id="7cce3-108">Attributes</span></span>

<span data-ttu-id="7cce3-109">无。</span><span class="sxs-lookup"><span data-stu-id="7cce3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cce3-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7cce3-110">Child elements</span></span>

|<span data-ttu-id="7cce3-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="7cce3-111">**Element**</span></span>|<span data-ttu-id="7cce3-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="7cce3-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cce3-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7cce3-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="7cce3-114">提供有关的响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="7cce3-114">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="7cce3-115">OofSettings</span><span class="sxs-lookup"><span data-stu-id="7cce3-115">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="7cce3-116">包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="7cce3-116">Contains the OOF settings.</span></span>  <br/> |
|[<span data-ttu-id="7cce3-117">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="7cce3-117">AllowExternalOof</span></span>](allowexternaloof.md) <br/> |<span data-ttu-id="7cce3-118">包含向其发送外部 OOF 邮件标识值。</span><span class="sxs-lookup"><span data-stu-id="7cce3-118">Contains a value that identifies to whom external OOF messages are sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7cce3-119">父元素</span><span class="sxs-lookup"><span data-stu-id="7cce3-119">Parent elements</span></span>

<span data-ttu-id="7cce3-120">无。</span><span class="sxs-lookup"><span data-stu-id="7cce3-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7cce3-121">备注</span><span class="sxs-lookup"><span data-stu-id="7cce3-121">Remarks</span></span>

<span data-ttu-id="7cce3-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7cce3-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cce3-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="7cce3-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cce3-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="7cce3-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7cce3-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="7cce3-125">Schema Name</span></span>  <br/> |<span data-ttu-id="7cce3-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="7cce3-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7cce3-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="7cce3-127">Validation File</span></span>  <br/> |<span data-ttu-id="7cce3-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7cce3-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7cce3-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="7cce3-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="7cce3-130">False</span><span class="sxs-lookup"><span data-stu-id="7cce3-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7cce3-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7cce3-131">See also</span></span>



[<span data-ttu-id="7cce3-132">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="7cce3-132">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="7cce3-133">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="7cce3-133">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

