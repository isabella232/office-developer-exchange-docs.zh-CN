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
description: IdOfFolderToShare 元素均表示将共享的服务器上的文件夹的标识符。
ms.openlocfilehash: 1e3e53819f23bbc5753ac21b9e3ea6593ac4826c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825853"
---
# <a name="idoffoldertoshare"></a><span data-ttu-id="667cf-103">IdOfFolderToShare</span><span class="sxs-lookup"><span data-stu-id="667cf-103">IdOfFolderToShare</span></span>

<span data-ttu-id="667cf-104">**IdOfFolderToShare**元素均表示将共享的服务器上的文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="667cf-104">The **IdOfFolderToShare** element represents the identifier of the folder on the server that will be shared.</span></span> 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 <span data-ttu-id="667cf-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="667cf-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="667cf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="667cf-106">Attributes and elements</span></span>

<span data-ttu-id="667cf-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="667cf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="667cf-108">属性</span><span class="sxs-lookup"><span data-stu-id="667cf-108">Attributes</span></span>

|<span data-ttu-id="667cf-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="667cf-109">**Attribute**</span></span>|<span data-ttu-id="667cf-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="667cf-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="667cf-111">Id</span><span class="sxs-lookup"><span data-stu-id="667cf-111">Id</span></span>  <br/> |<span data-ttu-id="667cf-112">包含一个字符串，标识 Exchange 存储中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="667cf-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="667cf-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="667cf-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="667cf-114">更改密钥</span><span class="sxs-lookup"><span data-stu-id="667cf-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="667cf-115">包含一个字符串，标识的文件夹的 Id 属性标识的版本。</span><span class="sxs-lookup"><span data-stu-id="667cf-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="667cf-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="667cf-116">This attribute is optional.</span></span> <span data-ttu-id="667cf-117">使用此属性以确保正确版本的文件夹使用。</span><span class="sxs-lookup"><span data-stu-id="667cf-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="667cf-118">子元素</span><span class="sxs-lookup"><span data-stu-id="667cf-118">Child elements</span></span>

<span data-ttu-id="667cf-119">无。</span><span class="sxs-lookup"><span data-stu-id="667cf-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="667cf-120">父元素</span><span class="sxs-lookup"><span data-stu-id="667cf-120">Parent elements</span></span>

|<span data-ttu-id="667cf-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="667cf-121">**Element**</span></span>|<span data-ttu-id="667cf-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="667cf-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="667cf-123">GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="667cf-123">GetSharingMetadata</span></span>](getsharingmetadata.md) <br/> |<span data-ttu-id="667cf-124">定义一个请求以获取标识共享邀请的不透明的身份验证令牌。</span><span class="sxs-lookup"><span data-stu-id="667cf-124">Defines a request to get an opaque authentication token that identifies the sharing invitation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="667cf-125">备注</span><span class="sxs-lookup"><span data-stu-id="667cf-125">Remarks</span></span>

<span data-ttu-id="667cf-126">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="667cf-126">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="667cf-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="667cf-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="667cf-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="667cf-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="667cf-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="667cf-129">Schema Name</span></span>  <br/> |<span data-ttu-id="667cf-130">消息架构</span><span class="sxs-lookup"><span data-stu-id="667cf-130">Messages schema</span></span>  <br/> |
|<span data-ttu-id="667cf-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="667cf-131">Validation File</span></span>  <br/> |<span data-ttu-id="667cf-132">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="667cf-132">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="667cf-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="667cf-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="667cf-134">False</span><span class="sxs-lookup"><span data-stu-id="667cf-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="667cf-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="667cf-135">See also</span></span>



[<span data-ttu-id="667cf-136">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="667cf-136">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="667cf-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="667cf-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

