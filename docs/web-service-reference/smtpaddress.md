---
title: SmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SmtpAddress
api_type:
- schema
ms.assetid: 779305a6-ad1e-424e-8a69-4e3bef61d787
description: SmtpAddress 元素表示用于模拟的帐户的简单邮件传输协议 (SMTP) 地址或日历或联系人共享请求的简单邮件传输协议 (SMTP) 收件人地址。
ms.openlocfilehash: 39588f0892cdcec819a1972547155730be5785f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827511"
---
# <a name="smtpaddress"></a><span data-ttu-id="fd2a4-103">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="fd2a4-103">SmtpAddress</span></span>

<span data-ttu-id="fd2a4-104">**SmtpAddress**元素表示用于模拟的帐户的简单邮件传输协议 (SMTP) 地址或日历或联系人共享请求的简单邮件传输协议 (SMTP) 收件人地址。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-104">The **SmtpAddress** element represents the Simple Mail Transfer Protocol (SMTP) address of an account to be used for impersonation or a Simple Mail Transfer Protocol (SMTP) recipient address of a calendar or contact sharing request.</span></span> 
  
```xml
<SmtpAddress/>
```

<span data-ttu-id="fd2a4-105">**SmtpAddressType**</span><span class="sxs-lookup"><span data-stu-id="fd2a4-105">**SmtpAddressType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fd2a4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fd2a4-106">Attributes and elements</span></span>

<span data-ttu-id="fd2a4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd2a4-108">属性</span><span class="sxs-lookup"><span data-stu-id="fd2a4-108">Attributes</span></span>

<span data-ttu-id="fd2a4-109">无。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd2a4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fd2a4-110">Child elements</span></span>

<span data-ttu-id="fd2a4-111">无。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fd2a4-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fd2a4-112">Parent elements</span></span>

|<span data-ttu-id="fd2a4-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="fd2a4-113">**Element**</span></span>|<span data-ttu-id="fd2a4-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="fd2a4-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd2a4-115">ConnectingSID</span><span class="sxs-lookup"><span data-stu-id="fd2a4-115">ConnectingSID</span></span>](connectingsid.md) <br/> |<span data-ttu-id="fd2a4-116">代表用于模拟使用 ExchangeImpersonation SOAP 标头时的帐户。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-116">Represents an account to impersonate when you are using the ExchangeImpersonation SOAP header.</span></span>  <br/> <span data-ttu-id="fd2a4-117">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="fd2a4-117">The following is the XPath expression to this element:</span></span>  <br/>  `/ExchangeImpersonation/ConnectingSID` <br/> |
|[<span data-ttu-id="fd2a4-118">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="fd2a4-118">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="fd2a4-119">代表无效收件人的日历共享或共享邮件的联系人。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-119">Represents an invalid recipient for a calendar sharing or contact sharing message.</span></span>  <br/> |
|[<span data-ttu-id="fd2a4-120">收件人 (ArrayOfSmtpAddressType)</span><span class="sxs-lookup"><span data-stu-id="fd2a4-120">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="fd2a4-121">代表将被授予访问权限的共享文件夹的收件人的集合。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-121">Represents a collection of recipients that will be granted access to the shared folder.</span></span>  <br/> |
|[<span data-ttu-id="fd2a4-122">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="fd2a4-122">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="fd2a4-123">定义一个请求以获取指定的共享文件夹的本地文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-123">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fd2a4-124">文本值</span><span class="sxs-lookup"><span data-stu-id="fd2a4-124">Text value</span></span>

<span data-ttu-id="fd2a4-125">需要安装一个代表 SMTP 地址的文本值。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-125">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fd2a4-126">备注</span><span class="sxs-lookup"><span data-stu-id="fd2a4-126">Remarks</span></span>

<span data-ttu-id="fd2a4-127">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="fd2a4-127">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd2a4-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="fd2a4-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd2a4-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="fd2a4-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd2a4-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="fd2a4-130">Schema Name</span></span>  <br/> |<span data-ttu-id="fd2a4-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="fd2a4-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="fd2a4-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="fd2a4-132">Validation File</span></span>  <br/> |<span data-ttu-id="fd2a4-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd2a4-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd2a4-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="fd2a4-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd2a4-135">False</span><span class="sxs-lookup"><span data-stu-id="fd2a4-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd2a4-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="fd2a4-136">See also</span></span>

- [<span data-ttu-id="fd2a4-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="fd2a4-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

