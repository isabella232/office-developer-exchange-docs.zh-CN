---
title: GetFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetFolder
api_type:
- schema
ms.assetid: 34e4c9ea-adcd-46bd-ae8f-7abb256c585a
description: GetFolder元素定义一个请求以获取从 Exchange 存储中的邮箱文件夹。
ms.openlocfilehash: 41d2b1ab5fcd5d2d60c399e8070ca957ee4b66e7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458703"
---
# <a name="getfolder"></a><span data-ttu-id="38f8c-103">GetFolder</span><span class="sxs-lookup"><span data-stu-id="38f8c-103">GetFolder</span></span>

<span data-ttu-id="38f8c-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **GetFolder**元素定义一个请求以获取从 Exchange 存储中的邮箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="38f8c-104">The **GetFolder** element defines a request to get a folder from a mailbox in the Exchange store.</span></span> 
  
```xml
<GetFolder>
   <FolderShape/>
   <FolderIds/>
</GetFolder>
```

 <span data-ttu-id="38f8c-105">**GetFolderType**</span><span class="sxs-lookup"><span data-stu-id="38f8c-105">**GetFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="38f8c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="38f8c-106">Attributes and elements</span></span>

<span data-ttu-id="38f8c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="38f8c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38f8c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="38f8c-108">Attributes</span></span>

<span data-ttu-id="38f8c-109">无。</span><span class="sxs-lookup"><span data-stu-id="38f8c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="38f8c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="38f8c-110">Child elements</span></span>

|<span data-ttu-id="38f8c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="38f8c-111">**Element**</span></span>|<span data-ttu-id="38f8c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="38f8c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="38f8c-113">FolderShape</span><span class="sxs-lookup"><span data-stu-id="38f8c-113">FolderShape</span></span>](foldershape.md) <br/> |<span data-ttu-id="38f8c-114">标识可获得[FolderIds](folderids.md)元素中标识的每个文件夹的属性。</span><span class="sxs-lookup"><span data-stu-id="38f8c-114">Identifies the properties to get for each folder identified in the [FolderIds](folderids.md) element.</span></span>  <br/> |
|[<span data-ttu-id="38f8c-115">FolderIds</span><span class="sxs-lookup"><span data-stu-id="38f8c-115">FolderIds</span></span>](folderids.md) <br/> |<span data-ttu-id="38f8c-116">包含用于标识要获取从 Exchange 存储中的邮箱文件夹的文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="38f8c-116">Contains an array of folder identifiers that are used to identify folders to get from a mailbox in the Exchange store.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="38f8c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="38f8c-117">Parent elements</span></span>

<span data-ttu-id="38f8c-118">无。</span><span class="sxs-lookup"><span data-stu-id="38f8c-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="38f8c-119">说明</span><span class="sxs-lookup"><span data-stu-id="38f8c-119">Remarks</span></span>

<span data-ttu-id="38f8c-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="38f8c-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38f8c-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="38f8c-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38f8c-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="38f8c-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="38f8c-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="38f8c-123">Schema Name</span></span>  <br/> |<span data-ttu-id="38f8c-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="38f8c-124">Message schema</span></span>  <br/> |
|<span data-ttu-id="38f8c-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="38f8c-125">Validation File</span></span>  <br/> |<span data-ttu-id="38f8c-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="38f8c-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="38f8c-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="38f8c-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="38f8c-128">False</span><span class="sxs-lookup"><span data-stu-id="38f8c-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38f8c-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="38f8c-129">See also</span></span>



[<span data-ttu-id="38f8c-130">GetFolder Operation</span><span class="sxs-lookup"><span data-stu-id="38f8c-130">GetFolder operation</span></span>](getfolder-operation.md)

