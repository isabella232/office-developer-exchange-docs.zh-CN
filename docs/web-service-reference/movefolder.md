---
title: MoveFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: f2bb0a73-94d7-4bc7-8902-bd9c69120221
description: MoveFolder元素定义要移动文件夹，请在 Exchange 存储中的请求。
ms.openlocfilehash: 42a990ced18cc13c7694042df786d33c018f346c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826485"
---
# <a name="movefolder"></a><span data-ttu-id="12f20-103">MoveFolder</span><span class="sxs-lookup"><span data-stu-id="12f20-103">MoveFolder</span></span>

<span data-ttu-id="12f20-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **MoveFolder**元素定义要移动文件夹，请在 Exchange 存储中的请求。</span><span class="sxs-lookup"><span data-stu-id="12f20-104">The **MoveFolder** element defines a request to move a folder in the Exchange store.</span></span> 
  
```xml
<MoveFolder>
   <ToFolderId/>
   <FolderIds/>
</MoveFolder>
```

 <span data-ttu-id="12f20-105">**MoveFolderType**</span><span class="sxs-lookup"><span data-stu-id="12f20-105">**MoveFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="12f20-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="12f20-106">Attributes and elements</span></span>

<span data-ttu-id="12f20-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="12f20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="12f20-108">属性</span><span class="sxs-lookup"><span data-stu-id="12f20-108">Attributes</span></span>

<span data-ttu-id="12f20-109">无。</span><span class="sxs-lookup"><span data-stu-id="12f20-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="12f20-110">子元素</span><span class="sxs-lookup"><span data-stu-id="12f20-110">Child elements</span></span>

|<span data-ttu-id="12f20-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="12f20-111">**Element**</span></span>|<span data-ttu-id="12f20-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="12f20-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12f20-113">ToFolderId</span><span class="sxs-lookup"><span data-stu-id="12f20-113">ToFolderId</span></span>](tofolderid.md) <br/> |<span data-ttu-id="12f20-114">表示移动文件夹的目标文件夹。</span><span class="sxs-lookup"><span data-stu-id="12f20-114">Represents the destination folder for a moved folder.</span></span>  <br/> |
|[<span data-ttu-id="12f20-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="12f20-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="12f20-116">包含文件夹移至文件夹由[ToFolderId](tofolderid.md)元素的数组。</span><span class="sxs-lookup"><span data-stu-id="12f20-116">Contains an array of folders to move to the folder identified by the [ToFolderId](tofolderid.md) element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="12f20-117">父元素</span><span class="sxs-lookup"><span data-stu-id="12f20-117">Parent elements</span></span>

<span data-ttu-id="12f20-118">无。</span><span class="sxs-lookup"><span data-stu-id="12f20-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="12f20-119">备注</span><span class="sxs-lookup"><span data-stu-id="12f20-119">Remarks</span></span>

<span data-ttu-id="12f20-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="12f20-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="12f20-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="12f20-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12f20-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="12f20-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="12f20-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="12f20-123">Schema Name</span></span>  <br/> |<span data-ttu-id="12f20-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="12f20-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="12f20-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="12f20-125">Validation File</span></span>  <br/> |<span data-ttu-id="12f20-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="12f20-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="12f20-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="12f20-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="12f20-128">False</span><span class="sxs-lookup"><span data-stu-id="12f20-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="12f20-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="12f20-129">See also</span></span>



[<span data-ttu-id="12f20-130">MoveFolder 操作</span><span class="sxs-lookup"><span data-stu-id="12f20-130">MoveFolder operation</span></span>](movefolder-operation.md)

