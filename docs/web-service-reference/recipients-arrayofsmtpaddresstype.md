---
title: 收件人（ArrayOfSmtpAddressType）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recipients
api_type:
- schema
ms.assetid: cf68417d-85cf-49e0-857a-f987d3675344
description: 收件人元素指定邮件的收件人数组。
ms.openlocfilehash: 4c2478a81836c2e52baad9c928d112108679b837
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465504"
---
# <a name="recipients-arrayofsmtpaddresstype"></a><span data-ttu-id="344b5-103">收件人（ArrayOfSmtpAddressType）</span><span class="sxs-lookup"><span data-stu-id="344b5-103">Recipients (ArrayOfSmtpAddressType)</span></span>

<span data-ttu-id="344b5-104">**收件人**元素指定邮件的收件人数组。</span><span class="sxs-lookup"><span data-stu-id="344b5-104">The **Recipients** element specifies an array of recipients of a message.</span></span> 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 <span data-ttu-id="344b5-105">**ArrayOfSmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="344b5-105">**ArrayOfSmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="344b5-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="344b5-106">Attributes and elements</span></span>

<span data-ttu-id="344b5-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="344b5-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="344b5-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="344b5-108">Attributes</span></span>

<span data-ttu-id="344b5-109">无。</span><span class="sxs-lookup"><span data-stu-id="344b5-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="344b5-110">子元素</span><span class="sxs-lookup"><span data-stu-id="344b5-110">Child elements</span></span>

|<span data-ttu-id="344b5-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="344b5-111">**Element**</span></span>|<span data-ttu-id="344b5-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="344b5-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="344b5-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="344b5-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="344b5-114">表示日历或联系人共享请求的简单邮件传输协议（SMTP）收件人地址。</span><span class="sxs-lookup"><span data-stu-id="344b5-114">Represents the Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="344b5-115">父元素</span><span class="sxs-lookup"><span data-stu-id="344b5-115">Parent elements</span></span>

|<span data-ttu-id="344b5-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="344b5-116">**Element**</span></span>|<span data-ttu-id="344b5-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="344b5-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="344b5-118">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="344b5-118">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="344b5-119">定义一个请求，以获取标识共享邀请的不透明身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="344b5-119">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="344b5-120">说明</span><span class="sxs-lookup"><span data-stu-id="344b5-120">Remarks</span></span>

<span data-ttu-id="344b5-121">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="344b5-121">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="344b5-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="344b5-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="344b5-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="344b5-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="344b5-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="344b5-124">Schema Name</span></span>  <br/> |<span data-ttu-id="344b5-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="344b5-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="344b5-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="344b5-126">Validation File</span></span>  <br/> |<span data-ttu-id="344b5-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="344b5-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="344b5-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="344b5-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="344b5-129">False</span><span class="sxs-lookup"><span data-stu-id="344b5-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="344b5-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="344b5-130">See also</span></span>



[<span data-ttu-id="344b5-131">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="344b5-131">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="344b5-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="344b5-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

