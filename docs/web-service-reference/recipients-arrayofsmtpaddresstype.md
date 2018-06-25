---
title: 收件人 (ArrayOfSmtpAddressType)
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
description: 收件人元素指定的邮件收件人的数组。
ms.openlocfilehash: 8490988043b1e06fd3a8f553fcefaeb2e90e9d31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826988"
---
# <a name="recipients-arrayofsmtpaddresstype"></a><span data-ttu-id="aa0eb-103">收件人 (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="aa0eb-103">Recipients (ArrayOfSmtpAddressType)</span></span>

<span data-ttu-id="aa0eb-104">**收件人**元素指定的邮件收件人的数组。</span><span class="sxs-lookup"><span data-stu-id="aa0eb-104">The **Recipients** element specifies an array of recipients of a message.</span></span> 
  
```xml
<Recipients>   <SmtpAddress/></Recipients>
```

 <span data-ttu-id="aa0eb-105">**ArrayOfSmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-105">**ArrayOfSmtpAddressType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aa0eb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="aa0eb-106">Attributes and elements</span></span>

<span data-ttu-id="aa0eb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="aa0eb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aa0eb-108">属性</span><span class="sxs-lookup"><span data-stu-id="aa0eb-108">Attributes</span></span>

<span data-ttu-id="aa0eb-109">无。</span><span class="sxs-lookup"><span data-stu-id="aa0eb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aa0eb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="aa0eb-110">Child elements</span></span>

|<span data-ttu-id="aa0eb-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-111">**Element**</span></span>|<span data-ttu-id="aa0eb-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa0eb-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="aa0eb-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="aa0eb-114">表示日历或联系人共享请求的收件人简单邮件传输协议 (SMTP) 地址。</span><span class="sxs-lookup"><span data-stu-id="aa0eb-114">Represents the Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="aa0eb-115">父元素</span><span class="sxs-lookup"><span data-stu-id="aa0eb-115">Parent elements</span></span>

|<span data-ttu-id="aa0eb-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-116">**Element**</span></span>|<span data-ttu-id="aa0eb-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="aa0eb-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aa0eb-118">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="aa0eb-118">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="aa0eb-119">定义一个请求以获取标识共享邀请的不透明的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="aa0eb-119">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa0eb-120">备注</span><span class="sxs-lookup"><span data-stu-id="aa0eb-120">Remarks</span></span>

<span data-ttu-id="aa0eb-121">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="aa0eb-121">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aa0eb-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="aa0eb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa0eb-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="aa0eb-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="aa0eb-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="aa0eb-124">Schema Name</span></span>  <br/> |<span data-ttu-id="aa0eb-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="aa0eb-125">Messages schema</span></span>  <br/> |
|<span data-ttu-id="aa0eb-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="aa0eb-126">Validation File</span></span>  <br/> |<span data-ttu-id="aa0eb-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="aa0eb-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="aa0eb-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="aa0eb-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="aa0eb-129">False</span><span class="sxs-lookup"><span data-stu-id="aa0eb-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa0eb-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="aa0eb-130">See also</span></span>



[<span data-ttu-id="aa0eb-131">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="aa0eb-131">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="aa0eb-132">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="aa0eb-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

