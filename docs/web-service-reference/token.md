---
title: Token
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Token
api_type:
- schema
ms.assetid: 62b700e1-88c7-41ef-b431-d7af4a8b54a7
description: Token 元素包含表示共享数据标识令牌的加密数据。
ms.openlocfilehash: c2e80082f9b4ecb96defdca8c5f0223a945661ba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458906"
---
# <a name="token"></a><span data-ttu-id="efb6c-103">标记</span><span class="sxs-lookup"><span data-stu-id="efb6c-103">Token</span></span>

<span data-ttu-id="efb6c-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **Token** 元素包含表示共享数据标识令牌的加密数据。</span><span class="sxs-lookup"><span data-stu-id="efb6c-104">The **Token** element contains encrypted data that represents the identification token for the shared data.</span></span> 
  
```xml
<Token/>
```

 <span data-ttu-id="efb6c-105">**EncryptedDataContainerType**</span><span class="sxs-lookup"><span data-stu-id="efb6c-105">**EncryptedDataContainerType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="efb6c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="efb6c-106">Attributes and elements</span></span>

<span data-ttu-id="efb6c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="efb6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="efb6c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="efb6c-108">Attributes</span></span>

<span data-ttu-id="efb6c-109">无。</span><span class="sxs-lookup"><span data-stu-id="efb6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="efb6c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="efb6c-110">Child elements</span></span>

<span data-ttu-id="efb6c-111">无。</span><span class="sxs-lookup"><span data-stu-id="efb6c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="efb6c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="efb6c-112">Parent elements</span></span>

|<span data-ttu-id="efb6c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="efb6c-113">**Element**</span></span>|<span data-ttu-id="efb6c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="efb6c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="efb6c-115">EncryptedSharedFolderData</span><span class="sxs-lookup"><span data-stu-id="efb6c-115">EncryptedSharedFolderData</span></span>](encryptedsharedfolderdata.md) <br/> |<span data-ttu-id="efb6c-116">包含客户端用于授权与其他客户端共享其日历或联系人数据的加密数据。</span><span class="sxs-lookup"><span data-stu-id="efb6c-116">Contains the encrypted data that a client can use to authorize the sharing of its calendar or contact data with other clients.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="efb6c-117">说明</span><span class="sxs-lookup"><span data-stu-id="efb6c-117">Remarks</span></span>

<span data-ttu-id="efb6c-118">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="efb6c-118">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="efb6c-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="efb6c-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efb6c-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="efb6c-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="efb6c-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="efb6c-121">Schema Name</span></span>  <br/> |<span data-ttu-id="efb6c-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="efb6c-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="efb6c-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="efb6c-123">Validation File</span></span>  <br/> |<span data-ttu-id="efb6c-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="efb6c-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="efb6c-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="efb6c-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="efb6c-126">False</span><span class="sxs-lookup"><span data-stu-id="efb6c-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="efb6c-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="efb6c-127">See also</span></span>



[<span data-ttu-id="efb6c-128">GetSharingMetadata 操作</span><span class="sxs-lookup"><span data-stu-id="efb6c-128">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="efb6c-129">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="efb6c-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

