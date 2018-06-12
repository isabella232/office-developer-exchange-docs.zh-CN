---
title: UpdateFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 412d0683-2819-40c5-a0ae-f613499a7b66
description: UpdateFolder元素表示用于更新属性指定文件夹的操作。
ms.openlocfilehash: 9a86bf6b3b5917600b3b09f23b3ee4e9cdc0364f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838373"
---
# <a name="updatefolder"></a><span data-ttu-id="70494-103">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="70494-103">UpdateFolder</span></span>

<span data-ttu-id="70494-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **UpdateFolder**元素表示用于更新属性指定文件夹的操作。</span><span class="sxs-lookup"><span data-stu-id="70494-104">The **UpdateFolder** element represents the operation that is used to update properties for a specified folder.</span></span> 
  
```xml
<UpdateFolder>
   <FolderChanges/>
</UpdateFolder>
```

 <span data-ttu-id="70494-105">**UpdateFolderType**</span><span class="sxs-lookup"><span data-stu-id="70494-105">**UpdateFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="70494-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="70494-106">Attributes and elements</span></span>

<span data-ttu-id="70494-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="70494-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="70494-108">属性</span><span class="sxs-lookup"><span data-stu-id="70494-108">Attributes</span></span>

<span data-ttu-id="70494-109">无。</span><span class="sxs-lookup"><span data-stu-id="70494-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="70494-110">子元素</span><span class="sxs-lookup"><span data-stu-id="70494-110">Child elements</span></span>

|<span data-ttu-id="70494-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="70494-111">**Element**</span></span>|<span data-ttu-id="70494-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="70494-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="70494-113">FolderChanges</span><span class="sxs-lookup"><span data-stu-id="70494-113">FolderChanges</span></span>](folderchanges.md) <br/> |<span data-ttu-id="70494-114">包含更改为指定文件夹的集合。</span><span class="sxs-lookup"><span data-stu-id="70494-114">Contains a collection of changes for a specified folder.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="70494-115">父元素</span><span class="sxs-lookup"><span data-stu-id="70494-115">Parent elements</span></span>

<span data-ttu-id="70494-116">无。</span><span class="sxs-lookup"><span data-stu-id="70494-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70494-117">备注</span><span class="sxs-lookup"><span data-stu-id="70494-117">Remarks</span></span>

<span data-ttu-id="70494-118">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="70494-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="70494-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="70494-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70494-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="70494-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="70494-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="70494-121">Schema Name</span></span>  <br/> |<span data-ttu-id="70494-122">消息架构</span><span class="sxs-lookup"><span data-stu-id="70494-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="70494-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="70494-123">Validation File</span></span>  <br/> |<span data-ttu-id="70494-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="70494-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="70494-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="70494-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="70494-126">False</span><span class="sxs-lookup"><span data-stu-id="70494-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70494-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="70494-127">See also</span></span>



[<span data-ttu-id="70494-128">UpdateFolder Operation</span><span class="sxs-lookup"><span data-stu-id="70494-128">UpdateFolder operation</span></span>](updatefolder-operation.md)

