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
description: GetUserOofSettingsRequest 元素是包含用于获取用户的外出 (OOF) 设置的邮箱的参数的根元素。
ms.openlocfilehash: e64818961283f90e447e2044cf7f918eccd21f06
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825692"
---
# <a name="getuseroofsettingsrequest"></a><span data-ttu-id="9d6ec-103">GetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="9d6ec-103">GetUserOofSettingsRequest</span></span>

<span data-ttu-id="9d6ec-104">**GetUserOofSettingsRequest**元素是包含用于获取用户的外出 (OOF) 设置的邮箱的参数的根元素。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-104">The **GetUserOofSettingsRequest** element is the root element that contains the arguments used to get a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<GetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
</GetUserOofSettingsRequest>
```

 <span data-ttu-id="9d6ec-105">**GetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="9d6ec-105">**GetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d6ec-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9d6ec-106">Attributes and elements</span></span>

<span data-ttu-id="9d6ec-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d6ec-108">属性</span><span class="sxs-lookup"><span data-stu-id="9d6ec-108">Attributes</span></span>

<span data-ttu-id="9d6ec-109">无。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d6ec-110">子元素</span><span class="sxs-lookup"><span data-stu-id="9d6ec-110">Child elements</span></span>

|<span data-ttu-id="9d6ec-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="9d6ec-111">**Element**</span></span>|<span data-ttu-id="9d6ec-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="9d6ec-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d6ec-113">邮箱 （可用性）</span><span class="sxs-lookup"><span data-stu-id="9d6ec-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="9d6ec-114">标识 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d6ec-115">父元素</span><span class="sxs-lookup"><span data-stu-id="9d6ec-115">Parent elements</span></span>

<span data-ttu-id="9d6ec-116">无。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9d6ec-117">备注</span><span class="sxs-lookup"><span data-stu-id="9d6ec-117">Remarks</span></span>

<span data-ttu-id="9d6ec-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="9d6ec-119">示例</span><span class="sxs-lookup"><span data-stu-id="9d6ec-119">Example</span></span>

<span data-ttu-id="9d6ec-120">下面是一个获取对单个用户的 OOF 信息 GetUserOofSettings 请求示例。</span><span class="sxs-lookup"><span data-stu-id="9d6ec-120">The following is an example of a GetUserOofSettings request that gets a single user's OOF information.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
    </GetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="9d6ec-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="9d6ec-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d6ec-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="9d6ec-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9d6ec-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="9d6ec-123">Schema Name</span></span>  <br/> |<span data-ttu-id="9d6ec-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="9d6ec-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9d6ec-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="9d6ec-125">Validation File</span></span>  <br/> |<span data-ttu-id="9d6ec-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9d6ec-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9d6ec-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="9d6ec-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d6ec-128">False</span><span class="sxs-lookup"><span data-stu-id="9d6ec-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d6ec-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9d6ec-129">See also</span></span>



[<span data-ttu-id="9d6ec-130">GetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="9d6ec-130">GetUserOofSettings operation</span></span>](getuseroofsettings-operation.md)

