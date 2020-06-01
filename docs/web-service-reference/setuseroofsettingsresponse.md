---
title: SetUserOofSettingsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettingsResponse
api_type:
- schema
ms.assetid: 8aa4025b-38df-4d63-a6a5-c3b932bec26e
description: SetUserOofSettingsResponse 元素包含 SetUserOofSettingsRequest 消息尝试的结果。
ms.openlocfilehash: 9b02d905f82488965f5ae0514a52eb6062aaff7d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466127"
---
# <a name="setuseroofsettingsresponse"></a><span data-ttu-id="abfbd-103">SetUserOofSettingsResponse</span><span class="sxs-lookup"><span data-stu-id="abfbd-103">SetUserOofSettingsResponse</span></span>

<span data-ttu-id="abfbd-104">**SetUserOofSettingsResponse**元素包含[SetUserOofSettingsRequest](setuseroofsettingsrequest.md)消息尝试的结果。</span><span class="sxs-lookup"><span data-stu-id="abfbd-104">The **SetUserOofSettingsResponse** element contains the result of a [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) message attempt.</span></span> 
  
```xml
<SetUserOofSettingsResponse>
   <ResponseMessage>...</ResponseMessage>
<SetUserOofSettingsResponse>
```

 <span data-ttu-id="abfbd-105">**SetUserOofSettingsResponse**</span><span class="sxs-lookup"><span data-stu-id="abfbd-105">**SetUserOofSettingsResponse**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="abfbd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="abfbd-106">Attributes and elements</span></span>

<span data-ttu-id="abfbd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="abfbd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="abfbd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="abfbd-108">Attributes</span></span>

<span data-ttu-id="abfbd-109">无。</span><span class="sxs-lookup"><span data-stu-id="abfbd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="abfbd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="abfbd-110">Child elements</span></span>

|<span data-ttu-id="abfbd-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="abfbd-111">**Element**</span></span>|<span data-ttu-id="abfbd-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="abfbd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="abfbd-113">ResponseMessage</span><span class="sxs-lookup"><span data-stu-id="abfbd-113">ResponseMessage</span></span>](responsemessage.md) <br/> |<span data-ttu-id="abfbd-114">提供有关响应状态的描述性信息。</span><span class="sxs-lookup"><span data-stu-id="abfbd-114">Provides descriptive information about the response status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="abfbd-115">父元素</span><span class="sxs-lookup"><span data-stu-id="abfbd-115">Parent elements</span></span>

<span data-ttu-id="abfbd-116">无。</span><span class="sxs-lookup"><span data-stu-id="abfbd-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="abfbd-117">说明</span><span class="sxs-lookup"><span data-stu-id="abfbd-117">Remarks</span></span>

<span data-ttu-id="abfbd-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="abfbd-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="abfbd-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="abfbd-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="abfbd-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="abfbd-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="abfbd-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="abfbd-121">Schema Name</span></span>  <br/> |<span data-ttu-id="abfbd-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="abfbd-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="abfbd-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="abfbd-123">Validation File</span></span>  <br/> |<span data-ttu-id="abfbd-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="abfbd-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="abfbd-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="abfbd-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="abfbd-126">False</span><span class="sxs-lookup"><span data-stu-id="abfbd-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="abfbd-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="abfbd-127">See also</span></span>



[<span data-ttu-id="abfbd-128">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="abfbd-128">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

