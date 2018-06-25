---
title: 内容
manager: sethgros
ms.date: 09/17/2015
ms.audience: ITPro
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Content
api_type:
- schema
ms.assetid: 24f8c54a-505f-4fc0-b7e7-93ad50b97070
description: 内容元素包含 Base64 编码的文件附件内容。
ms.openlocfilehash: 20afe6286d3efaa5da6cdc88e397e88fddb1d8c6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753556"
---
# <a name="content"></a><span data-ttu-id="6511f-103">内容</span><span class="sxs-lookup"><span data-stu-id="6511f-103">Content</span></span>

<span data-ttu-id="6511f-104">**内容**元素包含 Base64 编码的文件附件内容。</span><span class="sxs-lookup"><span data-stu-id="6511f-104">The **Content** element contains the Base64-encoded contents of a file attachment.</span></span> 
  
```xml
<Content/>
```

 <span data-ttu-id="6511f-105">**Base64Binary**</span><span class="sxs-lookup"><span data-stu-id="6511f-105">**Base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6511f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6511f-106">Attributes and elements</span></span>

<span data-ttu-id="6511f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6511f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6511f-108">属性</span><span class="sxs-lookup"><span data-stu-id="6511f-108">Attributes</span></span>

<span data-ttu-id="6511f-109">无。</span><span class="sxs-lookup"><span data-stu-id="6511f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6511f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6511f-110">Child elements</span></span>

<span data-ttu-id="6511f-111">无。</span><span class="sxs-lookup"><span data-stu-id="6511f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6511f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6511f-112">Parent elements</span></span>

|<span data-ttu-id="6511f-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6511f-113">**Element**</span></span>|<span data-ttu-id="6511f-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6511f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6511f-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="6511f-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="6511f-116">代表一个文件 t thattached 到 Exchange 存储中的项。</span><span class="sxs-lookup"><span data-stu-id="6511f-116">Represents a file t is thattached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6511f-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6511f-117">Text value</span></span>

<span data-ttu-id="6511f-118">字符串值表示的文件附件的 Base64 编码的二进制数据。</span><span class="sxs-lookup"><span data-stu-id="6511f-118">The string value represents the Base64-encoded binary data of the file attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6511f-119">备注</span><span class="sxs-lookup"><span data-stu-id="6511f-119">Remarks</span></span>

<span data-ttu-id="6511f-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6511f-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6511f-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="6511f-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6511f-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="6511f-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6511f-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="6511f-123">Schema name</span></span>  <br/> |<span data-ttu-id="6511f-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="6511f-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="6511f-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="6511f-125">Validation file</span></span>  <br/> |<span data-ttu-id="6511f-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6511f-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6511f-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="6511f-127">Can be empty</span></span>  <br/> |<span data-ttu-id="6511f-128">False</span><span class="sxs-lookup"><span data-stu-id="6511f-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6511f-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6511f-129">See also</span></span>



- [<span data-ttu-id="6511f-130">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6511f-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

