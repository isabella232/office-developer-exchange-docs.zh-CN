---
title: RefreshSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RefreshSharingFolder
api_type:
- schema
ms.assetid: 14571c28-effa-430a-802e-82fb99bafa7f
description: RefreshSharingFolder元素定义一个要刷新指定的本地文件夹的请求。它是RefreshSharingFolder 操作的基本元素。
ms.openlocfilehash: 4454607fa2c3114cc7279fd7c30f8aee74707baa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467926"
---
# <a name="refreshsharingfolder"></a><span data-ttu-id="6e6cd-104">RefreshSharingFolder</span><span class="sxs-lookup"><span data-stu-id="6e6cd-104">RefreshSharingFolder</span></span>

<span data-ttu-id="6e6cd-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **RefreshSharingFolder**元素定义一个要刷新指定的本地文件夹的请求。它是[RefreshSharingFolder 操作](refreshsharingfolder-operation.md)的基本元素。</span><span class="sxs-lookup"><span data-stu-id="6e6cd-p102">The **RefreshSharingFolder** element defines a request to refresh the specified local folder. It is the base element for the [RefreshSharingFolder operation](refreshsharingfolder-operation.md).</span></span>
  
```xml
<RefreshSharingFolder>   <SharingFolderId/></RefreshSharingFolder>
```

 <span data-ttu-id="6e6cd-107">**RefreshSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-107">**RefreshSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6e6cd-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6e6cd-108">Attributes and elements</span></span>

<span data-ttu-id="6e6cd-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6e6cd-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e6cd-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="6e6cd-110">Attributes</span></span>

<span data-ttu-id="6e6cd-111">无。</span><span class="sxs-lookup"><span data-stu-id="6e6cd-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6e6cd-112">子元素</span><span class="sxs-lookup"><span data-stu-id="6e6cd-112">Child elements</span></span>

|<span data-ttu-id="6e6cd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-113">**Element**</span></span>|<span data-ttu-id="6e6cd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6e6cd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6e6cd-115">SharingFolderId</span><span class="sxs-lookup"><span data-stu-id="6e6cd-115">SharingFolderId</span></span>](sharingfolderid.md) <br/> |<span data-ttu-id="6e6cd-116">表示共享关系中的本地文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="6e6cd-116">Represents the identifier of the local folder in a sharing relationship.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6e6cd-117">父元素</span><span class="sxs-lookup"><span data-stu-id="6e6cd-117">Parent elements</span></span>

<span data-ttu-id="6e6cd-118">无。</span><span class="sxs-lookup"><span data-stu-id="6e6cd-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e6cd-119">说明</span><span class="sxs-lookup"><span data-stu-id="6e6cd-119">Remarks</span></span>

<span data-ttu-id="6e6cd-120">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="6e6cd-120">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e6cd-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="6e6cd-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e6cd-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="6e6cd-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6e6cd-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="6e6cd-123">Schema Name</span></span>  <br/> |<span data-ttu-id="6e6cd-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="6e6cd-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6e6cd-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="6e6cd-125">Validation File</span></span>  <br/> |<span data-ttu-id="6e6cd-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6e6cd-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6e6cd-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="6e6cd-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="6e6cd-128">False</span><span class="sxs-lookup"><span data-stu-id="6e6cd-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e6cd-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6e6cd-129">See also</span></span>



- [<span data-ttu-id="6e6cd-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6e6cd-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

