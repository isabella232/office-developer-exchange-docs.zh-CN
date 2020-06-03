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
description: Content 元素包含文件附件的 Base64 编码的内容。
ms.openlocfilehash: 81f6acf69ff702bd0645663cb2e499ee5b45ea78
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458948"
---
# <a name="content"></a><span data-ttu-id="7f430-103">内容</span><span class="sxs-lookup"><span data-stu-id="7f430-103">Content</span></span>

<span data-ttu-id="7f430-104">**Content**元素包含文件附件的 Base64 编码的内容。</span><span class="sxs-lookup"><span data-stu-id="7f430-104">The **Content** element contains the Base64-encoded contents of a file attachment.</span></span> 
  
```xml
<Content/>
```

 <span data-ttu-id="7f430-105">**Base64Binary**</span><span class="sxs-lookup"><span data-stu-id="7f430-105">**Base64Binary**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7f430-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7f430-106">Attributes and elements</span></span>

<span data-ttu-id="7f430-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7f430-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7f430-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="7f430-108">Attributes</span></span>

<span data-ttu-id="7f430-109">无。</span><span class="sxs-lookup"><span data-stu-id="7f430-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7f430-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7f430-110">Child elements</span></span>

<span data-ttu-id="7f430-111">无。</span><span class="sxs-lookup"><span data-stu-id="7f430-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7f430-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7f430-112">Parent elements</span></span>

|<span data-ttu-id="7f430-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="7f430-113">**Element**</span></span>|<span data-ttu-id="7f430-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="7f430-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7f430-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="7f430-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="7f430-116">代表文件 t thattached 到 Exchange 存储中的项目。</span><span class="sxs-lookup"><span data-stu-id="7f430-116">Represents a file t is thattached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7f430-117">文本值</span><span class="sxs-lookup"><span data-stu-id="7f430-117">Text value</span></span>

<span data-ttu-id="7f430-118">字符串值代表文件附件的 Base64 编码的二进制数据。</span><span class="sxs-lookup"><span data-stu-id="7f430-118">The string value represents the Base64-encoded binary data of the file attachment.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7f430-119">说明</span><span class="sxs-lookup"><span data-stu-id="7f430-119">Remarks</span></span>

<span data-ttu-id="7f430-120">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7f430-120">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7f430-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="7f430-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7f430-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="7f430-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="7f430-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="7f430-123">Schema name</span></span>  <br/> |<span data-ttu-id="7f430-124">类型架构</span><span class="sxs-lookup"><span data-stu-id="7f430-124">Types schema</span></span>  <br/> |
|<span data-ttu-id="7f430-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="7f430-125">Validation file</span></span>  <br/> |<span data-ttu-id="7f430-126">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="7f430-126">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="7f430-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="7f430-127">Can be empty</span></span>  <br/> |<span data-ttu-id="7f430-128">False</span><span class="sxs-lookup"><span data-stu-id="7f430-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f430-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7f430-129">See also</span></span>



- [<span data-ttu-id="7f430-130">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7f430-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

