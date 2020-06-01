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
description: GetUserOofSettingsResponse 元素包含响应消息和用户的外出（OOF）设置。
ms.openlocfilehash: f7f28c67fd36630ffb5294ab35c0fef2f467ba22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457814"
---
# <a name="getuseroofsettingsresponse"></a><span data-ttu-id="874df-103">GetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="874df-103">GetUserOofSettingsResponse</span></span>

<span data-ttu-id="874df-104">**GetUserOofSettingsResponse**元素包含响应消息和用户的外出（OOF）设置。</span><span class="sxs-lookup"><span data-stu-id="874df-104">The **GetUserOofSettingsResponse** element contains the response message and the Out of Office (OOF) settings for a user.</span></span> 
  
```xml
<GetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
   <OofSettings>...</OofSettings>
   <AllowExternalOof>...</AllowExternalOof>
</GetUserOofSettingsResponse>
```

 <span data-ttu-id="874df-105">**GetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="874df-105">**GetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="874df-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="874df-106">Attributes and elements</span></span>

<span data-ttu-id="874df-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="874df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="874df-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="874df-108">Attributes</span></span>

<span data-ttu-id="874df-109">无。</span><span class="sxs-lookup"><span data-stu-id="874df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="874df-110">子元素</span><span class="sxs-lookup"><span data-stu-id="874df-110">Child elements</span></span>

|<span data-ttu-id="874df-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="874df-111">**Element**</span></span>|<span data-ttu-id="874df-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="874df-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="874df-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="874df-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="874df-114">提供有关响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="874df-114">Provides descriptive information about the response status.</span></span>  <br/> |
|[<span data-ttu-id="874df-115">OofSettings</span><span class="sxs-lookup"><span data-stu-id="874df-115">OofSettings</span></span>](oofsettings.md) <br/> |<span data-ttu-id="874df-116">包含 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="874df-116">Contains the OOF settings.</span></span>  <br/> |
|[<span data-ttu-id="874df-117">AllowExternalOof</span><span class="sxs-lookup"><span data-stu-id="874df-117">AllowExternalOof</span></span>](allowexternaloof.md) <br/> |<span data-ttu-id="874df-118">包含一个标识要向其发送外部 OOF 邮件的值。</span><span class="sxs-lookup"><span data-stu-id="874df-118">Contains a value that identifies to whom external OOF messages are sent.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="874df-119">父元素</span><span class="sxs-lookup"><span data-stu-id="874df-119">Parent elements</span></span>

<span data-ttu-id="874df-120">无。</span><span class="sxs-lookup"><span data-stu-id="874df-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="874df-121">说明</span><span class="sxs-lookup"><span data-stu-id="874df-121">Remarks</span></span>

<span data-ttu-id="874df-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="874df-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="874df-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="874df-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="874df-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="874df-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="874df-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="874df-125">Schema Name</span></span>  <br/> |<span data-ttu-id="874df-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="874df-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="874df-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="874df-127">Validation File</span></span>  <br/> |<span data-ttu-id="874df-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="874df-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="874df-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="874df-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="874df-130">False</span><span class="sxs-lookup"><span data-stu-id="874df-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="874df-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="874df-131">See also</span></span>



[<span data-ttu-id="874df-132">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="874df-132">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)
  
[<span data-ttu-id="874df-133">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="874df-133">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

