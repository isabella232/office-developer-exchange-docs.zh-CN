---
title: DataType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DataType
api_type:
- schema
ms.assetid: 267fe5aa-f9b1-4d4c-ac11-0f2e50ec2627
description: DataType 元素描述共享文件夹共享的数据类型。
ms.openlocfilehash: a7df8d38e10f0ab31038d790d8f35208d1be66d5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458829"
---
# <a name="datatype"></a><span data-ttu-id="b7dad-103">DataType</span><span class="sxs-lookup"><span data-stu-id="b7dad-103">DataType</span></span>

<span data-ttu-id="b7dad-104">**DataType**元素描述共享文件夹共享的数据类型。</span><span class="sxs-lookup"><span data-stu-id="b7dad-104">The **DataType** element describes the type of data that is shared by a shared folder.</span></span> 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

<span data-ttu-id="b7dad-105">**SharingDataType**</span><span class="sxs-lookup"><span data-stu-id="b7dad-105">**SharingDataType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="b7dad-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7dad-106">Attributes and elements</span></span>

<span data-ttu-id="b7dad-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7dad-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7dad-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7dad-108">Attributes</span></span>

<span data-ttu-id="b7dad-109">无。</span><span class="sxs-lookup"><span data-stu-id="b7dad-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7dad-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b7dad-110">Child elements</span></span>

<span data-ttu-id="b7dad-111">无。</span><span class="sxs-lookup"><span data-stu-id="b7dad-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7dad-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b7dad-112">Parent elements</span></span>

|<span data-ttu-id="b7dad-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="b7dad-113">**Element**</span></span>|<span data-ttu-id="b7dad-114">**描述**</span><span class="sxs-lookup"><span data-stu-id="b7dad-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b7dad-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="b7dad-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="b7dad-116">定义获取指定共享文件夹的本地文件夹标识符的请求。</span><span class="sxs-lookup"><span data-stu-id="b7dad-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b7dad-117">文本值</span><span class="sxs-lookup"><span data-stu-id="b7dad-117">Text value</span></span>

<span data-ttu-id="b7dad-118">下表列出了**DataType**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="b7dad-118">The following table lists the possible values for the **DataType** element.</span></span> 
  
<span data-ttu-id="b7dad-119">**DataType 元素值**</span><span class="sxs-lookup"><span data-stu-id="b7dad-119">**DataType element values**</span></span>

|<span data-ttu-id="b7dad-120">**值**</span><span class="sxs-lookup"><span data-stu-id="b7dad-120">**Value**</span></span>|<span data-ttu-id="b7dad-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7dad-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b7dad-122">日历</span><span class="sxs-lookup"><span data-stu-id="b7dad-122">Calendar</span></span>  <br/> |<span data-ttu-id="b7dad-123">指示共享文件夹包含日历信息。</span><span class="sxs-lookup"><span data-stu-id="b7dad-123">Indicates that the shared folder contains calendar information.</span></span>  <br/> |
|<span data-ttu-id="b7dad-124">联系人</span><span class="sxs-lookup"><span data-stu-id="b7dad-124">Contacts</span></span>  <br/> |<span data-ttu-id="b7dad-125">指示共享文件夹包含联系人信息。</span><span class="sxs-lookup"><span data-stu-id="b7dad-125">Indicates that the shared folder contains contact information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7dad-126">说明</span><span class="sxs-lookup"><span data-stu-id="b7dad-126">Remarks</span></span>

<span data-ttu-id="b7dad-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7dad-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7dad-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7dad-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7dad-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7dad-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7dad-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7dad-130">Schema Name</span></span>  <br/> |<span data-ttu-id="b7dad-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="b7dad-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b7dad-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7dad-132">Validation File</span></span>  <br/> |<span data-ttu-id="b7dad-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b7dad-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7dad-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7dad-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="b7dad-135">False</span><span class="sxs-lookup"><span data-stu-id="b7dad-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7dad-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b7dad-136">See also</span></span>

- [<span data-ttu-id="b7dad-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b7dad-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

