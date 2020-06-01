---
title: ServerVersionInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ServerVersionInfo
api_type:
- schema
ms.assetid: c04a6872-ca27-432b-aac2-36b023d0afc6
description: ServerVersionInfo 元素表示 Microsoft Exchange Server 版本号。
ms.openlocfilehash: 5bd1fbd8fdee584a9d272fa8ab82f2a31c1357fe
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466827"
---
# <a name="serverversioninfo"></a><span data-ttu-id="4e2b6-103">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4e2b6-103">ServerVersionInfo</span></span>

<span data-ttu-id="4e2b6-104">**ServerVersionInfo**元素表示 Microsoft Exchange Server 版本号。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-104">The **ServerVersionInfo** element represents the Microsoft Exchange Server version number.</span></span> 
  
```xml
<ServerVersionInfo MajorVersion="" MinorVersion="" MajorBuildNumber="" MinorBuildNumber="" Version="" />
```

## <a name="attributes-and-elements"></a><span data-ttu-id="4e2b6-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="4e2b6-105">Attributes and elements</span></span>

<span data-ttu-id="4e2b6-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4e2b6-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="4e2b6-107">Attributes</span></span>

|<span data-ttu-id="4e2b6-108">**属性**</span><span class="sxs-lookup"><span data-stu-id="4e2b6-108">**Attribute**</span></span>|<span data-ttu-id="4e2b6-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="4e2b6-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4e2b6-110">MajorVersion</span><span class="sxs-lookup"><span data-stu-id="4e2b6-110">MajorVersion</span></span>  <br/> |<span data-ttu-id="4e2b6-111">描述主版本号。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-111">Describes the major version number.</span></span>  <br/> |
|<span data-ttu-id="4e2b6-112">MinorVersion</span><span class="sxs-lookup"><span data-stu-id="4e2b6-112">MinorVersion</span></span>  <br/> |<span data-ttu-id="4e2b6-113">描述次版本号。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-113">Describes the minor version number.</span></span>  <br/> |
|<span data-ttu-id="4e2b6-114">MajorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="4e2b6-114">MajorBuildNumber</span></span>  <br/> |<span data-ttu-id="4e2b6-115">描述主内部版本号。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-115">Describes the major build number.</span></span>  <br/> |
|<span data-ttu-id="4e2b6-116">MinorBuildNumber</span><span class="sxs-lookup"><span data-stu-id="4e2b6-116">MinorBuildNumber</span></span>  <br/> |<span data-ttu-id="4e2b6-117">介绍次要内部版本号。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-117">Describes the minor build number.</span></span>  <br/> |
|<span data-ttu-id="4e2b6-118">版本</span><span class="sxs-lookup"><span data-stu-id="4e2b6-118">Version</span></span>  <br/> |<span data-ttu-id="4e2b6-119">介绍 Exchange Web 服务（EWS）架构版本。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-119">Describes the Exchange Web Services (EWS) schema version.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4e2b6-120">子元素</span><span class="sxs-lookup"><span data-stu-id="4e2b6-120">Child elements</span></span>

<span data-ttu-id="4e2b6-121">无。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="4e2b6-122">父元素</span><span class="sxs-lookup"><span data-stu-id="4e2b6-122">Parent elements</span></span>

<span data-ttu-id="4e2b6-123">无。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-123">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e2b6-124">说明</span><span class="sxs-lookup"><span data-stu-id="4e2b6-124">Remarks</span></span>

<span data-ttu-id="4e2b6-125">此元素在 Exchange Web 服务响应消息的 SOAP 标头中返回。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-125">This element is returned in the SOAP header of an Exchange Web Services response message.</span></span>
  
<span data-ttu-id="4e2b6-126">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="4e2b6-126">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4e2b6-127">元素信息</span><span class="sxs-lookup"><span data-stu-id="4e2b6-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4e2b6-128">命名空间</span><span class="sxs-lookup"><span data-stu-id="4e2b6-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4e2b6-129">架构名称</span><span class="sxs-lookup"><span data-stu-id="4e2b6-129">Schema Name</span></span>  <br/> |<span data-ttu-id="4e2b6-130">类型架构</span><span class="sxs-lookup"><span data-stu-id="4e2b6-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="4e2b6-131">验证文件</span><span class="sxs-lookup"><span data-stu-id="4e2b6-131">Validation File</span></span>  <br/> |<span data-ttu-id="4e2b6-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4e2b6-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4e2b6-133">可以为空</span><span class="sxs-lookup"><span data-stu-id="4e2b6-133">Can Be Empty</span></span>  <br/> |<span data-ttu-id="4e2b6-134">False</span><span class="sxs-lookup"><span data-stu-id="4e2b6-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4e2b6-135">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4e2b6-135">See also</span></span>



- [<span data-ttu-id="4e2b6-136">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4e2b6-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

