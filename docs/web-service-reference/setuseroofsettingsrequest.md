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
description: SetUserOofSettingsRequest 元素包含用于设置邮箱用户的外出（OOF）设置的参数。
ms.openlocfilehash: 10edc9809fd72f80c316de1c6688eaedec4f93df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466148"
---
# <a name="setuseroofsettingsrequest"></a><span data-ttu-id="22ce8-103">SetUserOofSettingsRequest</span><span class="sxs-lookup"><span data-stu-id="22ce8-103">SetUserOofSettingsRequest</span></span>

<span data-ttu-id="22ce8-104">**SetUserOofSettingsRequest**元素包含用于设置邮箱用户的外出（OOF）设置的参数。</span><span class="sxs-lookup"><span data-stu-id="22ce8-104">The **SetUserOofSettingsRequest** element contains the arguments used to set a mailbox user's Out of Office (OOF) settings.</span></span> 
  
```xml
<SetUserOofSettingsRequest>
   <Mailbox>...</Mailbox>
   <UserOofSettings>...</UserOofSettings>
<SetUserOofSettingsRequest>
```

 <span data-ttu-id="22ce8-105">**SetUserOofSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="22ce8-105">**SetUserOofSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22ce8-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22ce8-106">Attributes and elements</span></span>

<span data-ttu-id="22ce8-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22ce8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22ce8-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="22ce8-108">Attributes</span></span>

<span data-ttu-id="22ce8-109">无。</span><span class="sxs-lookup"><span data-stu-id="22ce8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22ce8-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22ce8-110">Child elements</span></span>

|<span data-ttu-id="22ce8-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="22ce8-111">**Element**</span></span>|<span data-ttu-id="22ce8-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="22ce8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22ce8-113">邮箱（可用性）</span><span class="sxs-lookup"><span data-stu-id="22ce8-113">Mailbox (Availability)</span></span>](mailbox-availability.md) <br/> |<span data-ttu-id="22ce8-114">标识 SetUserOofSettings 或 GetUserOofSettings 请求的邮箱用户。</span><span class="sxs-lookup"><span data-stu-id="22ce8-114">Identifies the mailbox user for a SetUserOofSettings or GetUserOofSettings request.</span></span>  <br/> |
|[<span data-ttu-id="22ce8-115">UserOofSettings</span><span class="sxs-lookup"><span data-stu-id="22ce8-115">UserOofSettings</span></span>](useroofsettings.md) <br/> |<span data-ttu-id="22ce8-116">指定 OOF 设置。</span><span class="sxs-lookup"><span data-stu-id="22ce8-116">Specifies the OOF settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="22ce8-117">父元素</span><span class="sxs-lookup"><span data-stu-id="22ce8-117">Parent elements</span></span>

<span data-ttu-id="22ce8-118">无。</span><span class="sxs-lookup"><span data-stu-id="22ce8-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22ce8-119">说明</span><span class="sxs-lookup"><span data-stu-id="22ce8-119">Remarks</span></span>

<span data-ttu-id="22ce8-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22ce8-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="22ce8-121">示例</span><span class="sxs-lookup"><span data-stu-id="22ce8-121">Example</span></span>

<span data-ttu-id="22ce8-122">以下示例的 SetUserOofSettings 请求将 OOF 设置设置为10天。</span><span class="sxs-lookup"><span data-stu-id="22ce8-122">The following example of a SetUserOofSettings request sets an OOF setting for ten days.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetUserOofSettingsRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <Mailbox xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
        <Name>David Alexander</Name>
        <Address>someone@example.com</Address>
        <RoutingType>SMTP</RoutingType>
      </Mailbox>
      <UserOofSettings xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="22ce8-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="22ce8-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22ce8-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="22ce8-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="22ce8-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="22ce8-125">Schema Name</span></span>  <br/> |<span data-ttu-id="22ce8-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="22ce8-126">Messages schema</span></span>  <br/> |
|<span data-ttu-id="22ce8-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="22ce8-127">Validation File</span></span>  <br/> |<span data-ttu-id="22ce8-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="22ce8-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="22ce8-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="22ce8-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="22ce8-130">False</span><span class="sxs-lookup"><span data-stu-id="22ce8-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22ce8-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22ce8-131">See also</span></span>



[<span data-ttu-id="22ce8-132">SetUserOofSettings 操作</span><span class="sxs-lookup"><span data-stu-id="22ce8-132">SetUserOofSettings operation</span></span>](setuseroofsettings-operation.md)

