---
title: GetUserOofSettingsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetUserOofSettingsRequest
api_type:
- schema
ms.assetid: 15dea99c-7f5d-4af1-82ff-4255127fe567
description: GetUserOofSettingsRequest 元素是根元素，其中包含用于获取邮箱用户的外出（OOF）设置的参数。
ms.openlocfilehash: f515e8cf016d3aff6c652ae92a0da71a8f0a5f6b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457828"
---
# <a name="getuseroofsettingsrequest"></a><span data-ttu-id="780eb-103">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="780eb-103">GetUserOofSettingsRequest</span></span>

<span data-ttu-id="780eb-104">**GetUserOofSettingsRequest**元素是根元素，其中包含用于获取邮箱用户的外出（OOF）设置的参数。</span><span class="sxs-lookup"><span data-stu-id="780eb-104">The **GetUserOofSettingsRequest** element is the root element that contains the arguments used to get a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<GetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
</GetUserOofSettingsRequest>
```

 <span data-ttu-id="780eb-105">**GetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="780eb-105">**GetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="780eb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="780eb-106">Attributes and elements</span></span>

<span data-ttu-id="780eb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="780eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="780eb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="780eb-108">Attributes</span></span>

<span data-ttu-id="780eb-109">无。</span><span class="sxs-lookup"><span data-stu-id="780eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="780eb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="780eb-110">Child elements</span></span>

|<span data-ttu-id="780eb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="780eb-111">**Element**</span></span>|<span data-ttu-id="780eb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="780eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="780eb-113">邮箱（可用性）</span><span class="sxs-lookup"><span data-stu-id="780eb-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="780eb-114">标识 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="780eb-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="780eb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="780eb-115">Parent elements</span></span>

<span data-ttu-id="780eb-116">无。</span><span class="sxs-lookup"><span data-stu-id="780eb-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="780eb-117">说明</span><span class="sxs-lookup"><span data-stu-id="780eb-117">Remarks</span></span>

<span data-ttu-id="780eb-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="780eb-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="780eb-119">示例</span><span class="sxs-lookup"><span data-stu-id="780eb-119">Example</span></span>

<span data-ttu-id="780eb-120">下面是一个 GetUserOofSettings 请求的示例，该请求获取单个用户的 OOF 信息。</span><span class="sxs-lookup"><span data-stu-id="780eb-120">The following is an example of a GetUserOofSettings request that gets a single user's OOF information.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="780eb-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="780eb-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="780eb-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="780eb-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="780eb-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="780eb-123">Schema Name</span></span>  <br/> |<span data-ttu-id="780eb-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="780eb-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="780eb-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="780eb-125">Validation File</span></span>  <br/> |<span data-ttu-id="780eb-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="780eb-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="780eb-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="780eb-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="780eb-128">False</span><span class="sxs-lookup"><span data-stu-id="780eb-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="780eb-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="780eb-129">See also</span></span>



[<span data-ttu-id="780eb-130">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="780eb-130">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)

