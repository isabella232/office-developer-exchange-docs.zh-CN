---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: GetSharingMetadata 元素定义一个请求，以获取标识共享邀请的不透明身份验证令牌。 此元素是 GetSharingMetadata 操作的基本元素。
ms.openlocfilehash: 406908e566d6d4249003b1a19a9ce79b8b328c4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530844"
---
# <a name="getsharingmetadata"></a><span data-ttu-id="0111a-104">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="0111a-104">GetSharingMetadata</span></span>

<span data-ttu-id="0111a-105">**GetSharingMetadata**元素定义一个请求，以获取标识共享邀请的不透明身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="0111a-105">The **GetSharingMetadata** element defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span> <span data-ttu-id="0111a-106">此元素是[GetSharingMetadata 操作](getsharingmetadata-operation.md)的基本元素。</span><span class="sxs-lookup"><span data-stu-id="0111a-106">This element is the base element for the [GetSharingMetadata operation](getsharingmetadata-operation.md).</span></span>
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 <span data-ttu-id="0111a-107">**GetSharingMetadataType**</span><span class="sxs-lookup"><span data-stu-id="0111a-107">**GetSharingMetadataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0111a-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0111a-108">Attributes and elements</span></span>

<span data-ttu-id="0111a-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0111a-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0111a-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="0111a-110">Attributes</span></span>

<span data-ttu-id="0111a-111">无。</span><span class="sxs-lookup"><span data-stu-id="0111a-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0111a-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0111a-112">Child elements</span></span>

|<span data-ttu-id="0111a-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0111a-113">**Element**</span></span>|<span data-ttu-id="0111a-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0111a-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0111a-115">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="0111a-115">IdOfFolderToShare</span></span>](idoffoldertoshare.md) <br/> |<span data-ttu-id="0111a-116">表示服务器上将共享的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="0111a-116">Represents the identifier of the folder on the server that will be shared.</span></span> <span data-ttu-id="0111a-117">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0111a-117">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0111a-118">SenderSmtpAddress</span><span class="sxs-lookup"><span data-stu-id="0111a-118">SenderSmtpAddress</span></span>](sendersmtpaddress.md) <br/> |<span data-ttu-id="0111a-119">表示与包含由[IdOfFolderToShare](idoffoldertoshare.md)元素标识的文件夹的邮箱相对应的 SMTP 电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="0111a-119">Represents the SMTP email address that corresponds to the mailbox that contains the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="0111a-120">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0111a-120">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="0111a-121">收件人（ArrayOfSmtpAddressType）</span><span class="sxs-lookup"><span data-stu-id="0111a-121">Recipients (ArrayOfSmtpAddressType)</span></span>](recipients-arrayofsmtpaddresstype.md) <br/> |<span data-ttu-id="0111a-122">表示一个或多个实体的 SMTP 电子邮件地址，这些实体将被授予对由[IdOfFolderToShare](idoffoldertoshare.md)元素标识的文件夹中的数据的访问权限。</span><span class="sxs-lookup"><span data-stu-id="0111a-122">Represents the SMTP email addresses of one or more entities that will be granted access to the data in the folder that is identified by the [IdOfFolderToShare](idoffoldertoshare.md) element.</span></span> <span data-ttu-id="0111a-123">此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="0111a-123">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0111a-124">父元素</span><span class="sxs-lookup"><span data-stu-id="0111a-124">Parent elements</span></span>

<span data-ttu-id="0111a-125">无。</span><span class="sxs-lookup"><span data-stu-id="0111a-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0111a-126">元素信息</span><span class="sxs-lookup"><span data-stu-id="0111a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0111a-127">命名空间</span><span class="sxs-lookup"><span data-stu-id="0111a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0111a-128">架构名称</span><span class="sxs-lookup"><span data-stu-id="0111a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0111a-129">消息架构</span><span class="sxs-lookup"><span data-stu-id="0111a-129">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0111a-130">验证文件</span><span class="sxs-lookup"><span data-stu-id="0111a-130">Validation File</span></span>  <br/> |<span data-ttu-id="0111a-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0111a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0111a-132">可以为空</span><span class="sxs-lookup"><span data-stu-id="0111a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0111a-133">False</span><span class="sxs-lookup"><span data-stu-id="0111a-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0111a-134">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0111a-134">See also</span></span>



[<span data-ttu-id="0111a-135">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="0111a-135">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="0111a-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="0111a-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

