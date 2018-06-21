---
title: CreateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateFolder
api_type:
- schema
ms.assetid: 110bada1-517b-4bd6-870d-7086dc879e5d
description: CreateFolder元素定义要在 Exchange 存储区中创建文件夹的请求。
ms.openlocfilehash: e30af23b8ed8669053b94be460d62fbf7abf24c9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2018
ms.locfileid: "19753637"
---
# <a name="createfolder"></a><span data-ttu-id="0d289-103">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="0d289-103">CreateFolder</span></span>

<span data-ttu-id="0d289-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CreateFolder**元素定义要在 Exchange 存储区中创建文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="0d289-104">The **CreateFolder** element defines a request to create a folder in the Exchange store.</span></span> 
  
```xml
<CreateFolder>
   <ParentFolderId/>
   <Folders/>
</CreateFolder>
```

 <span data-ttu-id="0d289-105">**CreateFolderType**</span><span class="sxs-lookup"><span data-stu-id="0d289-105">**CreateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0d289-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0d289-106">Attributes and elements</span></span>

<span data-ttu-id="0d289-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0d289-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d289-108">属性</span><span class="sxs-lookup"><span data-stu-id="0d289-108">Attributes</span></span>

<span data-ttu-id="0d289-109">无。</span><span class="sxs-lookup"><span data-stu-id="0d289-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d289-110">子元素</span><span class="sxs-lookup"><span data-stu-id="0d289-110">Child elements</span></span>

|<span data-ttu-id="0d289-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="0d289-111">**Element**</span></span>|<span data-ttu-id="0d289-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="0d289-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d289-113">ParentFolderId (TargetFolderIdType)</span><span class="sxs-lookup"><span data-stu-id="0d289-113">ParentFolderId (TargetFolderIdType)</span></span>](parentfolderid-targetfolderidtype.md) <br/> |<span data-ttu-id="0d289-114">该元素标识在其中创建新文件夹的位置。</span><span class="sxs-lookup"><span data-stu-id="0d289-114">The element that identifies the location where the new folder is created.</span></span>  <br/> |
|[<span data-ttu-id="0d289-115">Folders</span><span class="sxs-lookup"><span data-stu-id="0d289-115">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="0d289-116">包含要创建的所有文件夹的元素。</span><span class="sxs-lookup"><span data-stu-id="0d289-116">The element that contains all the folders to create.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0d289-117">父元素</span><span class="sxs-lookup"><span data-stu-id="0d289-117">Parent elements</span></span>

<span data-ttu-id="0d289-118">无。</span><span class="sxs-lookup"><span data-stu-id="0d289-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d289-119">备注</span><span class="sxs-lookup"><span data-stu-id="0d289-119">Remarks</span></span>

<span data-ttu-id="0d289-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0d289-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0d289-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="0d289-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d289-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="0d289-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0d289-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="0d289-123">Schema Name</span></span>  <br/> |<span data-ttu-id="0d289-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="0d289-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="0d289-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="0d289-125">Validation File</span></span>  <br/> |<span data-ttu-id="0d289-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0d289-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0d289-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="0d289-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d289-128">False</span><span class="sxs-lookup"><span data-stu-id="0d289-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d289-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0d289-129">See also</span></span>



[<span data-ttu-id="0d289-130">CreateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="0d289-130">CreateFolder operation</span></span>](createfolder-operation.md)


[<span data-ttu-id="0d289-131">Creating Folders (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="0d289-131">Creating Folders (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

