---
title: SourceIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SourceIds
api_type:
- schema
ms.assetid: 0043abd5-ba9c-4d67-8832-325f32bf7651
description: SourceIds 元素包含要转换的源标识符。
ms.openlocfilehash: 1c4990f2185788c5cfaab5483cb6a54a0d850596
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466106"
---
# <a name="sourceids"></a><span data-ttu-id="c1946-103">SourceIds</span><span class="sxs-lookup"><span data-stu-id="c1946-103">SourceIds</span></span>

<span data-ttu-id="c1946-104">**SourceIds**元素包含要转换的源标识符。</span><span class="sxs-lookup"><span data-stu-id="c1946-104">The **SourceIds** element contains the source identifiers to convert.</span></span> 
  
[<span data-ttu-id="c1946-105">ConvertId</span><span class="sxs-lookup"><span data-stu-id="c1946-105">ConvertId</span></span>](convertid.md)
  
[<span data-ttu-id="c1946-106">SourceIds</span><span class="sxs-lookup"><span data-stu-id="c1946-106">SourceIds</span></span>](sourceids.md)
  
```xml
<SourceIds>
   <AlternateId/>
   <AlternatePublicFolderId/>
   <AlternatePublicFolderItemId/>
</SourceIds>
```

 <span data-ttu-id="c1946-107">**NonEmptyArrayOfAlternateIdsType**</span><span class="sxs-lookup"><span data-stu-id="c1946-107">**NonEmptyArrayOfAlternateIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1946-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c1946-108">Attributes and elements</span></span>

<span data-ttu-id="c1946-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c1946-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1946-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="c1946-110">Attributes</span></span>

<span data-ttu-id="c1946-111">无。</span><span class="sxs-lookup"><span data-stu-id="c1946-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1946-112">子元素</span><span class="sxs-lookup"><span data-stu-id="c1946-112">Child elements</span></span>

|<span data-ttu-id="c1946-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1946-113">**Element**</span></span>|<span data-ttu-id="c1946-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1946-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1946-115">AlternateId</span><span class="sxs-lookup"><span data-stu-id="c1946-115">AlternateId</span></span>](alternateid.md) <br/> |<span data-ttu-id="c1946-116">描述要转换的项或文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="c1946-116">Describes an item or folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="c1946-117">AlternatePublicFolderId</span><span class="sxs-lookup"><span data-stu-id="c1946-117">AlternatePublicFolderId</span></span>](alternatepublicfolderid.md) <br/> |<span data-ttu-id="c1946-118">描述要转换的公用文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="c1946-118">Describes a public folder identifier to convert.</span></span>  <br/> |
|[<span data-ttu-id="c1946-119">AlternatePublicFolderItemId</span><span class="sxs-lookup"><span data-stu-id="c1946-119">AlternatePublicFolderItemId</span></span>](alternatepublicfolderitemid.md) <br/> |<span data-ttu-id="c1946-120">描述要转换的公用文件夹项目标识符。</span><span class="sxs-lookup"><span data-stu-id="c1946-120">Describes a public folder item identifier to convert.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c1946-121">父元素</span><span class="sxs-lookup"><span data-stu-id="c1946-121">Parent elements</span></span>

|<span data-ttu-id="c1946-122">**元素**</span><span class="sxs-lookup"><span data-stu-id="c1946-122">**Element**</span></span>|<span data-ttu-id="c1946-123">**说明**</span><span class="sxs-lookup"><span data-stu-id="c1946-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1946-124">ConvertId</span><span class="sxs-lookup"><span data-stu-id="c1946-124">ConvertId</span></span>](convertid.md) <br/> |<span data-ttu-id="c1946-125">定义在 Exchange 支持的格式之间转换项目和文件夹标识符的请求。</span><span class="sxs-lookup"><span data-stu-id="c1946-125">Defines a request to convert item and folder identifiers between Exchange supported formats.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1946-126">备注</span><span class="sxs-lookup"><span data-stu-id="c1946-126">Remarks</span></span>

<span data-ttu-id="c1946-127">描述此元素的架构位于运行 Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c1946-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1946-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="c1946-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1946-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="c1946-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1946-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="c1946-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c1946-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="c1946-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1946-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="c1946-132">Validation File</span></span>  <br/> |<span data-ttu-id="c1946-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1946-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1946-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="c1946-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c1946-135">False</span><span class="sxs-lookup"><span data-stu-id="c1946-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1946-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c1946-136">See also</span></span>



[<span data-ttu-id="c1946-137">ConvertId 操作</span><span class="sxs-lookup"><span data-stu-id="c1946-137">ConvertId operation</span></span>](convertid-operation.md)


- [<span data-ttu-id="c1946-138">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c1946-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="c1946-139">转换标识符</span><span class="sxs-lookup"><span data-stu-id="c1946-139">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

