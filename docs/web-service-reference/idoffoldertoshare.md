---
title: IdOfFolderToShare
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IdOfFolderToShare
api_type:
- schema
ms.assetid: 199d1839-f061-4070-a977-874b0c08e5be
description: IdOfFolderToShare 元素表示服务器上将共享的文件夹的标识符。
ms.openlocfilehash: 93a4740d9adefbb35aae071f0a6bfcb4b2021b4d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457625"
---
# <a name="idoffoldertoshare"></a><span data-ttu-id="52f01-103">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="52f01-103">IdOfFolderToShare</span></span>

<span data-ttu-id="52f01-104">**IdOfFolderToShare**元素表示服务器上将共享的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="52f01-104">The **IdOfFolderToShare** element represents the identifier of the folder on the server that will be shared.</span></span> 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 <span data-ttu-id="52f01-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="52f01-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52f01-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="52f01-106">Attributes and elements</span></span>

<span data-ttu-id="52f01-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="52f01-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52f01-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="52f01-108">Attributes</span></span>

|<span data-ttu-id="52f01-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="52f01-109">**Attribute**</span></span>|<span data-ttu-id="52f01-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="52f01-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52f01-111">Id</span><span class="sxs-lookup"><span data-stu-id="52f01-111">Id</span></span>  <br/> |<span data-ttu-id="52f01-112">包含标识 Exchange 存储中的文件夹的字符串。</span><span class="sxs-lookup"><span data-stu-id="52f01-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="52f01-113">此特性是必需的。</span><span class="sxs-lookup"><span data-stu-id="52f01-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="52f01-114">ChangeKey</span><span class="sxs-lookup"><span data-stu-id="52f01-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="52f01-115">包含标识由 Id 属性标识的文件夹版本的字符串。</span><span class="sxs-lookup"><span data-stu-id="52f01-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="52f01-116">此特性是可选的。</span><span class="sxs-lookup"><span data-stu-id="52f01-116">This attribute is optional.</span></span> <span data-ttu-id="52f01-117">使用此属性可确保使用的是正确的文件夹版本。</span><span class="sxs-lookup"><span data-stu-id="52f01-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="52f01-118">子元素</span><span class="sxs-lookup"><span data-stu-id="52f01-118">Child elements</span></span>

<span data-ttu-id="52f01-119">无。</span><span class="sxs-lookup"><span data-stu-id="52f01-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="52f01-120">父元素</span><span class="sxs-lookup"><span data-stu-id="52f01-120">Parent elements</span></span>

|<span data-ttu-id="52f01-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="52f01-121">**Element**</span></span>|<span data-ttu-id="52f01-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="52f01-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52f01-123">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="52f01-123">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="52f01-124">定义一个请求，以获取标识共享邀请的不透明身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="52f01-124">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52f01-125">说明</span><span class="sxs-lookup"><span data-stu-id="52f01-125">Remarks</span></span>

<span data-ttu-id="52f01-126">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="52f01-126">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52f01-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="52f01-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52f01-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="52f01-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="52f01-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="52f01-129">Schema Name</span></span>  <br/> |<span data-ttu-id="52f01-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="52f01-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="52f01-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="52f01-131">Validation File</span></span>  <br/> |<span data-ttu-id="52f01-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="52f01-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="52f01-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="52f01-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="52f01-134">False</span><span class="sxs-lookup"><span data-stu-id="52f01-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52f01-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="52f01-135">See also</span></span>



[<span data-ttu-id="52f01-136">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="52f01-136">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="52f01-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="52f01-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

