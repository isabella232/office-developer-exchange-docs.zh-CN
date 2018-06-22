---
title: CopyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: 7d5cd08a-fe81-4cb6-a5a0-6dec2d3c93d4
description: CopyFolder元素定义要在 Exchange 存储中的邮箱复制文件夹的请求。
ms.openlocfilehash: 7bcfcc7f4212b3a3bd339fa5863df2990eb20d6d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753606"
---
# <a name="copyfolder"></a><span data-ttu-id="95792-103">CopyFolder</span><span class="sxs-lookup"><span data-stu-id="95792-103">CopyFolder</span></span>

<span data-ttu-id="95792-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CopyFolder**元素定义要在 Exchange 存储中的邮箱复制文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="95792-104">The **CopyFolder** element defines a request to copy folders in a mailbox in the Exchange store.</span></span> 
  
```xml
<CopyFolder>
   <ToFolderId/>
   <FolderIds/>
</CopyFolder>
```

 <span data-ttu-id="95792-105">**CopyFolderType**</span><span class="sxs-lookup"><span data-stu-id="95792-105">**CopyFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="95792-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="95792-106">Attributes and elements</span></span>

<span data-ttu-id="95792-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="95792-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95792-108">属性</span><span class="sxs-lookup"><span data-stu-id="95792-108">Attributes</span></span>

<span data-ttu-id="95792-109">无。</span><span class="sxs-lookup"><span data-stu-id="95792-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95792-110">子元素</span><span class="sxs-lookup"><span data-stu-id="95792-110">Child elements</span></span>

|<span data-ttu-id="95792-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="95792-111">**Element**</span></span>|<span data-ttu-id="95792-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="95792-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="95792-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="95792-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="95792-114">表示复制的文件夹的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="95792-114">Represents the destination folder for a copied folder.</span></span>  <br/> |
|[<span data-ttu-id="95792-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="95792-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="95792-116">包含文件夹复制到文件夹，由[ToFolderId](tofolderid.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="95792-116">Contains an array of folders to copy to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="95792-117">父元素</span><span class="sxs-lookup"><span data-stu-id="95792-117">Parent elements</span></span>

<span data-ttu-id="95792-118">无。</span><span class="sxs-lookup"><span data-stu-id="95792-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="95792-119">备注</span><span class="sxs-lookup"><span data-stu-id="95792-119">Remarks</span></span>

<span data-ttu-id="95792-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="95792-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95792-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="95792-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95792-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="95792-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="95792-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="95792-123">Schema Name</span></span>  <br/> |<span data-ttu-id="95792-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="95792-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="95792-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="95792-125">Validation File</span></span>  <br/> |<span data-ttu-id="95792-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="95792-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="95792-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="95792-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="95792-128">False</span><span class="sxs-lookup"><span data-stu-id="95792-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95792-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="95792-129">See also</span></span>



[<span data-ttu-id="95792-130">CopyFolder 操作</span><span class="sxs-lookup"><span data-stu-id="95792-130">CopyFolder operation</span></span>](copyfolder-operation.md)

