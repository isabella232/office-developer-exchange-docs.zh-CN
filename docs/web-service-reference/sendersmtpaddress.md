---
title: SenderSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderSmtpAddress
api_type:
- schema
ms.assetid: e39c7df7-4bfa-455f-b4bb-1f1d05398eec
description: SenderSmtpAddress 元素表示与包含将共享的文件夹的邮箱相对应的 SMTP 电子邮件地址。
ms.openlocfilehash: 73047dcecfbccb55d74e373891c3154bc7baeeba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464894"
---
# <a name="sendersmtpaddress"></a><span data-ttu-id="6ade0-103">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="6ade0-103">SenderSmtpAddress</span></span>

<span data-ttu-id="6ade0-104">**SenderSmtpAddress**元素表示与包含将共享的文件夹的邮箱相对应的 SMTP 电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="6ade0-104">The **SenderSmtpAddress** element represents the SMTP e-mail address corresponding to the mailbox that contains the folder that will be shared.</span></span> 
  
```xml
<SenderSmtpAddress/>
```

 <span data-ttu-id="6ade0-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="6ade0-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6ade0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6ade0-106">Attributes and elements</span></span>

<span data-ttu-id="6ade0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6ade0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6ade0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6ade0-108">Attributes</span></span>

<span data-ttu-id="6ade0-109">无。</span><span class="sxs-lookup"><span data-stu-id="6ade0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6ade0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6ade0-110">Child elements</span></span>

<span data-ttu-id="6ade0-111">无。</span><span class="sxs-lookup"><span data-stu-id="6ade0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6ade0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6ade0-112">Parent elements</span></span>

|<span data-ttu-id="6ade0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6ade0-113">**Element**</span></span>|<span data-ttu-id="6ade0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6ade0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ade0-115">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="6ade0-115">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="6ade0-116">定义一个请求，以获取标识共享邀请的不透明身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="6ade0-116">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6ade0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6ade0-117">Text value</span></span>

<span data-ttu-id="6ade0-118">需要一个代表 SMTP 地址的文本值。</span><span class="sxs-lookup"><span data-stu-id="6ade0-118">A text value that represents an SMTP address is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ade0-119">说明</span><span class="sxs-lookup"><span data-stu-id="6ade0-119">Remarks</span></span>

<span data-ttu-id="6ade0-120">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="6ade0-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6ade0-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="6ade0-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ade0-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="6ade0-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6ade0-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="6ade0-123">Schema Name</span></span>  <br/> |<span data-ttu-id="6ade0-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="6ade0-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6ade0-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="6ade0-125">Validation File</span></span>  <br/> |<span data-ttu-id="6ade0-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6ade0-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6ade0-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="6ade0-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="6ade0-128">False</span><span class="sxs-lookup"><span data-stu-id="6ade0-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ade0-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6ade0-129">See also</span></span>



[<span data-ttu-id="6ade0-130">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="6ade0-130">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="6ade0-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6ade0-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

