---
title: EncryptedSharedFolderDataCollection
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderDataCollection
api_type:
- schema
ms.assetid: 25c6ae87-bbb9-4dd5-a85a-d669fcea137f
description: EncryptedSharedFolderDataCollection 元素包含一组数据结构，客户端可以使用这些结构来授权共享其日历或联系人数据与其他客户端的共享。
ms.openlocfilehash: e8ed9221952892abda7b4eac62b16cdc4976c6e2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461266"
---
# <a name="encryptedsharedfolderdatacollection"></a><span data-ttu-id="4b526-103">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="4b526-103">EncryptedSharedFolderDataCollection</span></span>

<span data-ttu-id="4b526-104">**EncryptedSharedFolderDataCollection**元素包含一组数据结构，客户端可以使用这些结构来授权共享其日历或联系人数据与其他客户端的共享。</span><span class="sxs-lookup"><span data-stu-id="4b526-104">The **EncryptedSharedFolderDataCollection** element contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderDataCollection>   <EncryptedSharedFolderData/></EncryptedSharedFolderDataCollection>
```

 <span data-ttu-id="4b526-105">**ArrayOfEncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="4b526-105">**ArrayOfEncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4b526-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4b526-106">Attributes and elements</span></span>

<span data-ttu-id="4b526-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4b526-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b526-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="4b526-108">Attributes</span></span>

<span data-ttu-id="4b526-109">无。</span><span class="sxs-lookup"><span data-stu-id="4b526-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4b526-110">子元素</span><span class="sxs-lookup"><span data-stu-id="4b526-110">Child elements</span></span>

|<span data-ttu-id="4b526-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b526-111">**Element**</span></span>|<span data-ttu-id="4b526-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b526-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b526-113">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="4b526-113">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="4b526-114">包含客户端用于授权与其他客户端共享其日历或联系人数据的加密数据。</span><span class="sxs-lookup"><span data-stu-id="4b526-114">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4b526-115">父元素</span><span class="sxs-lookup"><span data-stu-id="4b526-115">Parent elements</span></span>

|<span data-ttu-id="4b526-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="4b526-116">**Element**</span></span>|<span data-ttu-id="4b526-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="4b526-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4b526-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="4b526-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="4b526-119">定义一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="4b526-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="4b526-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4b526-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="4b526-121">包含状态和一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="4b526-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4b526-122">说明</span><span class="sxs-lookup"><span data-stu-id="4b526-122">Remarks</span></span>

<span data-ttu-id="4b526-123">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="4b526-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b526-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="4b526-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b526-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="4b526-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4b526-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="4b526-126">Schema Name</span></span>  <br/> |<span data-ttu-id="4b526-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="4b526-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4b526-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="4b526-128">Validation File</span></span>  <br/> |<span data-ttu-id="4b526-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4b526-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4b526-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="4b526-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="4b526-131">False</span><span class="sxs-lookup"><span data-stu-id="4b526-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b526-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4b526-132">See also</span></span>

- [<span data-ttu-id="4b526-133">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="4b526-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="4b526-134">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4b526-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

