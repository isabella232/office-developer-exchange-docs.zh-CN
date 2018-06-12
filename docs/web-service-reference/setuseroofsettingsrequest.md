---
title: SetUserOofSettingsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SetUserOofSettingsRequest
api_type:
- schema
ms.assetid: 628acf0b-3ebc-42f1-8ce2-7a02b4c8141f
description: SetUserOofSettingsRequest 元素包含用于设置用户的外出 (OOF) 设置的邮箱的参数。
ms.openlocfilehash: ed54bb1d066da7b15605fb81931a6ef75dfc61bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827474"
---
# <a name="setuseroofsettingsrequest"></a><span data-ttu-id="557e1-103">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="557e1-103">SetUserOofSettingsRequest</span></span>

<span data-ttu-id="557e1-104">**SetUserOofSettingsRequest**元素包含用于设置用户的外出 (OOF) 设置的邮箱的参数。</span><span class="sxs-lookup"><span data-stu-id="557e1-104">The **SetUserOofSettingsRequest** element contains the arguments used to set a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<SetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
   <UserOofSettings>...</UserOofSettings>
<SetUserOofSettingsRequest>
```

 <span data-ttu-id="557e1-105">**SetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="557e1-105">**SetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="557e1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="557e1-106">Attributes and elements</span></span>

<span data-ttu-id="557e1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="557e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="557e1-108">属性</span><span class="sxs-lookup"><span data-stu-id="557e1-108">Attributes</span></span>

<span data-ttu-id="557e1-109">无。</span><span class="sxs-lookup"><span data-stu-id="557e1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="557e1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="557e1-110">Child elements</span></span>

|<span data-ttu-id="557e1-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="557e1-111">**Element**</span></span>|<span data-ttu-id="557e1-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="557e1-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="557e1-113">邮箱 （可用性）</span><span class="sxs-lookup"><span data-stu-id="557e1-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="557e1-114">标识 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="557e1-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
|[<span data-ttu-id="557e1-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="557e1-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="557e1-116">指定 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="557e1-116">Specifies the OOF settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="557e1-117">父元素</span><span class="sxs-lookup"><span data-stu-id="557e1-117">Parent elements</span></span>

<span data-ttu-id="557e1-118">无。</span><span class="sxs-lookup"><span data-stu-id="557e1-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="557e1-119">备注</span><span class="sxs-lookup"><span data-stu-id="557e1-119">Remarks</span></span>

<span data-ttu-id="557e1-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="557e1-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="557e1-121">示例</span><span class="sxs-lookup"><span data-stu-id="557e1-121">Example</span></span>

<span data-ttu-id="557e1-122">下面的示例 SetUserOofSettings 请求的设置十天 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="557e1-122">The following example of a SetUserOofSettings request sets an OOF setting for ten days.</span></span>
  
```xml
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

## <a name="element-information"></a><span data-ttu-id="557e1-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="557e1-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="557e1-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="557e1-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="557e1-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="557e1-125">Schema Name</span></span>  <br/> |<span data-ttu-id="557e1-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="557e1-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="557e1-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="557e1-127">Validation File</span></span>  <br/> |<span data-ttu-id="557e1-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="557e1-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="557e1-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="557e1-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="557e1-130">False</span><span class="sxs-lookup"><span data-stu-id="557e1-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="557e1-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="557e1-131">See also</span></span>



[<span data-ttu-id="557e1-132">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="557e1-132">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

