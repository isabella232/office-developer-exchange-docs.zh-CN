---
title: 消息 （可用性）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Message
api_type:
- schema
ms.assetid: 1eec24dd-c981-41f4-a2f0-c51d43f1d7c0
description: 消息元素包含外出 (OOF) 响应的。
ms.openlocfilehash: 9facd04767fdcc0fd9dfd84fc6badb1a7633d2b5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826452"
---
# <a name="message-availability"></a><span data-ttu-id="84c7e-103">消息 （可用性）</span><span class="sxs-lookup"><span data-stu-id="84c7e-103">Message (Availability)</span></span>

<span data-ttu-id="84c7e-104">**消息**元素包含外出 (OOF) 响应的。</span><span class="sxs-lookup"><span data-stu-id="84c7e-104">The **Message** element contains the out of Office (OOF) response.</span></span> 
  
```xml
<Message/> 
```

 <span data-ttu-id="84c7e-105">**string**</span><span class="sxs-lookup"><span data-stu-id="84c7e-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="84c7e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="84c7e-106">Attributes and elements</span></span>

<span data-ttu-id="84c7e-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="84c7e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="84c7e-108">属性</span><span class="sxs-lookup"><span data-stu-id="84c7e-108">Attributes</span></span>

<span data-ttu-id="84c7e-109">无。</span><span class="sxs-lookup"><span data-stu-id="84c7e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="84c7e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="84c7e-110">Child elements</span></span>

<span data-ttu-id="84c7e-111">无。</span><span class="sxs-lookup"><span data-stu-id="84c7e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="84c7e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="84c7e-112">Parent elements</span></span>

|<span data-ttu-id="84c7e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="84c7e-113">**Element**</span></span>|<span data-ttu-id="84c7e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="84c7e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="84c7e-115">InternalReply</span><span class="sxs-lookup"><span data-stu-id="84c7e-115">InternalReply</span></span>](internalreply.md) <br/> | <span data-ttu-id="84c7e-116">包含 OOF 邮件发送给发件人的域中其他用户。</span><span class="sxs-lookup"><span data-stu-id="84c7e-116">Contains the OOF message sent to other users in the sender's domain.</span></span> <br/> <br/>  <span data-ttu-id="84c7e-117">以下是此元素可能 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="84c7e-117">The following are the possible XPath expressions to this element:</span></span> <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/InternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/InternalReply` <br/> |
|[<span data-ttu-id="84c7e-118">ExternalReply</span><span class="sxs-lookup"><span data-stu-id="84c7e-118">ExternalReply</span></span>](externalreply.md) <br/> | <span data-ttu-id="84c7e-119">包含 OOF 邮件发送到外部发件人的域地址。</span><span class="sxs-lookup"><span data-stu-id="84c7e-119">Contains the OOF message that is sent to addresses outside the sender's domain.</span></span>  <br/> <br/> <span data-ttu-id="84c7e-120">以下是此元素可能 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="84c7e-120">The following are the possible XPath expressions to this element:</span></span>  <br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/ExternalReply` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/ExternalReply` <br/> |
|[<span data-ttu-id="84c7e-121">ReplyBody</span><span class="sxs-lookup"><span data-stu-id="84c7e-121">ReplyBody</span></span>](replybody.md) <br/> |<span data-ttu-id="84c7e-122">包含 OOF 邮件和消息所使用的语言。</span><span class="sxs-lookup"><span data-stu-id="84c7e-122">Contains an OOF message and the language used for the message.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="84c7e-123">文本值</span><span class="sxs-lookup"><span data-stu-id="84c7e-123">Text value</span></span>

<span data-ttu-id="84c7e-124">设置 OOF 邮件需要的文本值。</span><span class="sxs-lookup"><span data-stu-id="84c7e-124">A text value is required to set the OOF message.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84c7e-125">备注</span><span class="sxs-lookup"><span data-stu-id="84c7e-125">Remarks</span></span>

<span data-ttu-id="84c7e-126">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="84c7e-126">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="84c7e-127">示例</span><span class="sxs-lookup"><span data-stu-id="84c7e-127">Example</span></span>

<span data-ttu-id="84c7e-128">下面的示例的[SetUserOofSettings 操作](setuseroofsettings-operation.md)请求将[OofState](oofstate.md)设置为**已启用**，将 OOF 的持续时间设置为 10 天，并设置内部和外部 OOF 邮件。</span><span class="sxs-lookup"><span data-stu-id="84c7e-128">The following example of a [SetUserOofSettings operation](setuseroofsettings-operation.md) request sets the [OofState](oofstate.md) to **Enabled**, sets the duration of OOF to 10 days, and sets the internal and external OOF messages.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
        <OofState>Enabled</OofState>
        <ExternalAudience>All</ExternalAudience>
        <Duration>
          <StartTime>2005-10-05T00:00:00</StartTime>
          <EndTime>2005-10-25T00:00:00</EndTime>
        </Duration>
        <InternalReply>
          <Message>I am out of office.  This is my internal reply.</Message>
        </InternalReply>
        <ExternalReply>
          <Message>I am out of office. This is my external reply.</Message>
        </ExternalReply>
      </UserOofSettings>
    </SetUserOofSettingsRequest>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a><span data-ttu-id="84c7e-129">元素信息</span><span class="sxs-lookup"><span data-stu-id="84c7e-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="84c7e-130">命名空间</span><span class="sxs-lookup"><span data-stu-id="84c7e-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="84c7e-131">架构名称</span><span class="sxs-lookup"><span data-stu-id="84c7e-131">Schema Name</span></span>  <br/> |<span data-ttu-id="84c7e-132">类型架构</span><span class="sxs-lookup"><span data-stu-id="84c7e-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="84c7e-133">验证文件</span><span class="sxs-lookup"><span data-stu-id="84c7e-133">Validation File</span></span>  <br/> |<span data-ttu-id="84c7e-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="84c7e-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="84c7e-135">可以为空</span><span class="sxs-lookup"><span data-stu-id="84c7e-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="84c7e-136">False</span><span class="sxs-lookup"><span data-stu-id="84c7e-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84c7e-137">另请参阅</span><span class="sxs-lookup"><span data-stu-id="84c7e-137">See also</span></span>

- [<span data-ttu-id="84c7e-138">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="84c7e-138">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)
- [<span data-ttu-id="84c7e-139">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="84c7e-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

