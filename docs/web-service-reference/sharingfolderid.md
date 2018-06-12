---
title: SharingFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingFolderId
api_type:
- schema
ms.assetid: 5ad37ceb-2922-4420-9051-c29d0d57c420
description: SharingFolderId 元素均表示共享关系中的本地文件夹的标识符。
ms.openlocfilehash: e0eb1fbd7155040508daf253f5eb4b1352d7426d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827485"
---
# <a name="sharingfolderid"></a><span data-ttu-id="1d683-103">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="1d683-103">SharingFolderId</span></span>

<span data-ttu-id="1d683-104">**SharingFolderId**元素均表示共享关系中的本地文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="1d683-104">The **SharingFolderId** element represents the identifier of the local folder in a sharing relationship.</span></span> 
  
```xml
<SharingFolderId Id="" ChangeKey="" />
```

 <span data-ttu-id="1d683-105">**FolderIdType**</span><span class="sxs-lookup"><span data-stu-id="1d683-105">**FolderIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1d683-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1d683-106">Attributes and elements</span></span>

<span data-ttu-id="1d683-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1d683-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d683-108">属性</span><span class="sxs-lookup"><span data-stu-id="1d683-108">Attributes</span></span>

|<span data-ttu-id="1d683-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="1d683-109">**Attribute**</span></span>|<span data-ttu-id="1d683-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d683-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1d683-111">Id</span><span class="sxs-lookup"><span data-stu-id="1d683-111">Id</span></span>  <br/> |<span data-ttu-id="1d683-112">包含一个字符串，标识 Exchange 存储中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1d683-112">Contains a string that identifies a folder in the Exchange store.</span></span> <span data-ttu-id="1d683-113">此属性是必需的。</span><span class="sxs-lookup"><span data-stu-id="1d683-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="1d683-114">更改密钥</span><span class="sxs-lookup"><span data-stu-id="1d683-114">ChangeKey</span></span>  <br/> |<span data-ttu-id="1d683-115">包含一个字符串，标识的文件夹的 Id 属性标识的版本。</span><span class="sxs-lookup"><span data-stu-id="1d683-115">Contains a string that identifies a version of a folder that is identified by the Id attribute.</span></span> <span data-ttu-id="1d683-116">此属性是可选的。</span><span class="sxs-lookup"><span data-stu-id="1d683-116">This attribute is optional.</span></span> <span data-ttu-id="1d683-117">使用此属性以确保正确版本的文件夹使用。</span><span class="sxs-lookup"><span data-stu-id="1d683-117">Use this attribute to make sure that the correct version of a folder is used.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d683-118">子元素</span><span class="sxs-lookup"><span data-stu-id="1d683-118">Child elements</span></span>

<span data-ttu-id="1d683-119">无。</span><span class="sxs-lookup"><span data-stu-id="1d683-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1d683-120">父元素</span><span class="sxs-lookup"><span data-stu-id="1d683-120">Parent elements</span></span>

|<span data-ttu-id="1d683-121">**元素**</span><span class="sxs-lookup"><span data-stu-id="1d683-121">**Element**</span></span>|<span data-ttu-id="1d683-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="1d683-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d683-123">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="1d683-123">RefreshSharingFolder</span></span>](refreshsharingfolder.md) <br/> |<span data-ttu-id="1d683-124">定义一个请求刷新指定的本地文件夹。</span><span class="sxs-lookup"><span data-stu-id="1d683-124">Defines a request to refresh the specified local folder.</span></span>  <br/> |
|[<span data-ttu-id="1d683-125">GetSharingFolderResponse</span><span class="sxs-lookup"><span data-stu-id="1d683-125">GetSharingFolderResponse</span></span>](getsharingfolderresponse.md) <br/> |<span data-ttu-id="1d683-126">定义[GetSharingFolder 操作](getsharingfolder-operation.md)请求的响应。</span><span class="sxs-lookup"><span data-stu-id="1d683-126">Defines a response to a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="1d683-127">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="1d683-127">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md) <br/> |<span data-ttu-id="1d683-128">包含状态和的单个结果[GetSharingFolder 操作](getsharingfolder-operation.md)请求。</span><span class="sxs-lookup"><span data-stu-id="1d683-128">Contains the status and result of a single [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d683-129">备注</span><span class="sxs-lookup"><span data-stu-id="1d683-129">Remarks</span></span>

<span data-ttu-id="1d683-130">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="1d683-130">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d683-131">元素信息</span><span class="sxs-lookup"><span data-stu-id="1d683-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d683-132">命名空间</span><span class="sxs-lookup"><span data-stu-id="1d683-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1d683-133">架构名称</span><span class="sxs-lookup"><span data-stu-id="1d683-133">Schema Name</span></span>  <br/> |<span data-ttu-id="1d683-134">消息架构</span><span class="sxs-lookup"><span data-stu-id="1d683-134">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1d683-135">验证文件</span><span class="sxs-lookup"><span data-stu-id="1d683-135">Validation File</span></span>  <br/> |<span data-ttu-id="1d683-136">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="1d683-136">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1d683-137">可以为空</span><span class="sxs-lookup"><span data-stu-id="1d683-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d683-138">False</span><span class="sxs-lookup"><span data-stu-id="1d683-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d683-139">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1d683-139">See also</span></span>



- [<span data-ttu-id="1d683-140">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1d683-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

