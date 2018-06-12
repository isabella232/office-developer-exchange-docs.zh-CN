---
title: EncryptedSharedFolderData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EncryptedSharedFolderData
api_type:
- schema
ms.assetid: c1d4ca18-c5ce-41ff-bab4-f75e358c8b9f
description: EncryptedSharedFolderData 元素包含客户端可以使用授权其日历共享或与其他客户端联系人数据的加密的数据。
ms.openlocfilehash: 63966e95becaab4b3b1e54aa81f1b20a8b09dfd3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754101"
---
# <a name="encryptedsharedfolderdata"></a><span data-ttu-id="b105f-103">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="b105f-103">EncryptedSharedFolderData</span></span>

<span data-ttu-id="b105f-104">**EncryptedSharedFolderData**元素包含客户端可以使用授权其日历共享或与其他客户端联系人数据的加密的数据。</span><span class="sxs-lookup"><span data-stu-id="b105f-104">The **EncryptedSharedFolderData** element contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span> 
  
```xml
<EncryptedSharedFolderData>   <Token/>   <Data/></EncryptedSharedFolderData>
```

 <span data-ttu-id="b105f-105">**EncryptedSharedFolderDataType**</span><span class="sxs-lookup"><span data-stu-id="b105f-105">**EncryptedSharedFolderDataType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b105f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b105f-106">Attributes and elements</span></span>

<span data-ttu-id="b105f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b105f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b105f-108">属性</span><span class="sxs-lookup"><span data-stu-id="b105f-108">Attributes</span></span>

<span data-ttu-id="b105f-109">无。</span><span class="sxs-lookup"><span data-stu-id="b105f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b105f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b105f-110">Child elements</span></span>

|<span data-ttu-id="b105f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b105f-111">**Element**</span></span>|<span data-ttu-id="b105f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b105f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b105f-113">标记</span><span class="sxs-lookup"><span data-stu-id="b105f-113">Token</span></span>](token.md) <br/> |<span data-ttu-id="b105f-114">包含表示共享数据的标识标记的加密的数据。</span><span class="sxs-lookup"><span data-stu-id="b105f-114">Contains encrypted data that represents the identification token for the shared data.</span></span>  <br/> |
|[<span data-ttu-id="b105f-115">Data</span><span class="sxs-lookup"><span data-stu-id="b105f-115">Data</span></span>](data.md) <br/> |<span data-ttu-id="b105f-116">包含加密的数据值，该值代表共享的数据。</span><span class="sxs-lookup"><span data-stu-id="b105f-116">Contains encrypted data that represents the shared data.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b105f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="b105f-117">Parent elements</span></span>

|<span data-ttu-id="b105f-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="b105f-118">**Element**</span></span>|<span data-ttu-id="b105f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="b105f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b105f-120">EncryptedSharedFolderDataCollection</span><span class="sxs-lookup"><span data-stu-id="b105f-120">EncryptedSharedFolderDataCollection</span></span>](encryptedsharedfolderdatacollection.md) <br/> |<span data-ttu-id="b105f-121">表示数据结构的客户端可以使用授权其日历共享或与其他客户端联系人数据的集合。</span><span class="sxs-lookup"><span data-stu-id="b105f-121">Represents a collection of data structures that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b105f-122">备注</span><span class="sxs-lookup"><span data-stu-id="b105f-122">Remarks</span></span>

<span data-ttu-id="b105f-123">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="b105f-123">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b105f-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="b105f-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b105f-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="b105f-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b105f-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="b105f-126">Schema Name</span></span>  <br/> |<span data-ttu-id="b105f-127">类型架构</span><span class="sxs-lookup"><span data-stu-id="b105f-127">Types schema</span></span>  <br/> |
|<span data-ttu-id="b105f-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="b105f-128">Validation File</span></span>  <br/> |<span data-ttu-id="b105f-129">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b105f-129">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b105f-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="b105f-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="b105f-131">False</span><span class="sxs-lookup"><span data-stu-id="b105f-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b105f-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b105f-132">See also</span></span>

- [<span data-ttu-id="b105f-133">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="b105f-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)
- [<span data-ttu-id="b105f-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b105f-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

