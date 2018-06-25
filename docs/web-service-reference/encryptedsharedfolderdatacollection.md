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
description: EncryptedSharedFolderDataCollection 元素包含客户端可以使用授权其日历共享或与其他客户端联系人数据的数据结构的集合。
ms.openlocfilehash: e4d37f5df10f5e270be5126479485239f2205d6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754099"
---
# <a name="encryptedsharedfolderdatacollection"></a><span data-ttu-id="1e698-103">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="1e698-103">EncryptedSharedFolderDataCollection</span></span>

<span data-ttu-id="1e698-104">**EncryptedSharedFolderDataCollection**元素包含客户端可以使用授权其日历共享或与其他客户端联系人数据的数据结构的集合。</span><span class="sxs-lookup"><span data-stu-id="1e698-104">The **EncryptedSharedFolderDataCollection** element contains a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderDataCollection>   <EncryptedSharedFolderData/></EncryptedSharedFolderDataCollection>
```

 <span data-ttu-id="1e698-105">**ArrayOfEncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="1e698-105">**ArrayOfEncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e698-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e698-106">Attributes and elements</span></span>

<span data-ttu-id="1e698-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e698-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e698-108">属性</span><span class="sxs-lookup"><span data-stu-id="1e698-108">Attributes</span></span>

<span data-ttu-id="1e698-109">无。</span><span class="sxs-lookup"><span data-stu-id="1e698-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e698-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1e698-110">Child elements</span></span>

|<span data-ttu-id="1e698-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e698-111">**Element**</span></span>|<span data-ttu-id="1e698-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e698-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e698-113">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="1e698-113">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="1e698-114">包含客户端用于授权与其他客户端共享其日历或联系人数据的加密数据。</span><span class="sxs-lookup"><span data-stu-id="1e698-114">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1e698-115">父元素</span><span class="sxs-lookup"><span data-stu-id="1e698-115">Parent elements</span></span>

|<span data-ttu-id="1e698-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e698-116">**Element**</span></span>|<span data-ttu-id="1e698-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e698-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e698-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="1e698-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="1e698-119">定义一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="1e698-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1e698-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1e698-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="1e698-121">包含状态和一个[GetSharingMetadata 操作](getsharingmetadata-operation.md)请求的结果。</span><span class="sxs-lookup"><span data-stu-id="1e698-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e698-122">备注</span><span class="sxs-lookup"><span data-stu-id="1e698-122">Remarks</span></span>

<span data-ttu-id="1e698-123">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="1e698-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e698-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e698-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e698-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e698-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1e698-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e698-126">Schema Name</span></span>  <br/> |<span data-ttu-id="1e698-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="1e698-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1e698-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e698-128">Validation File</span></span>  <br/> |<span data-ttu-id="1e698-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1e698-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1e698-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e698-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="1e698-131">False</span><span class="sxs-lookup"><span data-stu-id="1e698-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e698-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1e698-132">See also</span></span>

- [<span data-ttu-id="1e698-133">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="1e698-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="1e698-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1e698-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

