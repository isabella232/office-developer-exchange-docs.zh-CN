---
title: Data （base64Binary）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: Data 元素包含要上载到邮箱中的单个导出项目或项目的数据。
ms.openlocfilehash: 43ee16ca7caf634756ca00a88715d9834adad92b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526968"
---
# <a name="data-base64binary"></a><span data-ttu-id="30b45-103">Data （base64Binary）</span><span class="sxs-lookup"><span data-stu-id="30b45-103">Data (base64Binary)</span></span>

<span data-ttu-id="30b45-104">**Data**元素包含要上载到邮箱中的单个导出项目或项目的数据。</span><span class="sxs-lookup"><span data-stu-id="30b45-104">The **Data** element contains the data of a single exported item or an item to upload into a mailbox.</span></span> 
  
```XML
<Data/>
```

<span data-ttu-id="30b45-105">**xs： base64Binary**</span><span class="sxs-lookup"><span data-stu-id="30b45-105">**xs:base64Binary**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="30b45-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="30b45-106">Attributes and elements</span></span>

<span data-ttu-id="30b45-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="30b45-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="30b45-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="30b45-108">Attributes</span></span>

<span data-ttu-id="30b45-109">无。</span><span class="sxs-lookup"><span data-stu-id="30b45-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="30b45-110">子元素</span><span class="sxs-lookup"><span data-stu-id="30b45-110">Child elements</span></span>

<span data-ttu-id="30b45-111">无。</span><span class="sxs-lookup"><span data-stu-id="30b45-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="30b45-112">父元素</span><span class="sxs-lookup"><span data-stu-id="30b45-112">Parent elements</span></span>

|<span data-ttu-id="30b45-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="30b45-113">**Element**</span></span>|<span data-ttu-id="30b45-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="30b45-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="30b45-115">ExportItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="30b45-115">ExportItemsResponseMessage</span></span>](exportitemsresponsemessage.md) <br/> |<span data-ttu-id="30b45-116">包含导出单个邮箱项目的请求的状态和结果。</span><span class="sxs-lookup"><span data-stu-id="30b45-116">Contains the status and results of a request to export a single mailbox item.</span></span>  <br/> |
|[<span data-ttu-id="30b45-117">Item （UploadItemType）</span><span class="sxs-lookup"><span data-stu-id="30b45-117">Item (UploadItemType)</span></span>](item-uploaditemtype.md) <br/> |<span data-ttu-id="30b45-118">代表要上传到邮箱中的单个项目。</span><span class="sxs-lookup"><span data-stu-id="30b45-118">Represents a single item to upload into a mailbox.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="30b45-119">文本值</span><span class="sxs-lookup"><span data-stu-id="30b45-119">Text value</span></span>

<span data-ttu-id="30b45-120">**Data**元素包含导出项目的属性名称和值，或将上载到邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="30b45-120">The **Data** element contains the property names and values for an exported item or an item that will be uploaded into a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="30b45-121">备注</span><span class="sxs-lookup"><span data-stu-id="30b45-121">Remarks</span></span>

<span data-ttu-id="30b45-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="30b45-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="30b45-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="30b45-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30b45-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="30b45-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="30b45-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="30b45-125">Schema Name</span></span>  <br/> |<span data-ttu-id="30b45-126">消息架构</span><span class="sxs-lookup"><span data-stu-id="30b45-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="30b45-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="30b45-127">Validation File</span></span>  <br/> |<span data-ttu-id="30b45-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="30b45-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="30b45-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="30b45-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="30b45-130">False</span><span class="sxs-lookup"><span data-stu-id="30b45-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30b45-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="30b45-131">See also</span></span>

- [<span data-ttu-id="30b45-132">ExportItems 操作</span><span class="sxs-lookup"><span data-stu-id="30b45-132">ExportItems operation</span></span>](exportitems-operation.md)
- [<span data-ttu-id="30b45-133">UploadItems 操作</span><span class="sxs-lookup"><span data-stu-id="30b45-133">UploadItems operation</span></span>](uploaditems-operation.md)

