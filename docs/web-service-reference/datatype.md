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
description: 数据类型元素描述共享的共享文件夹的数据的类型。
ms.openlocfilehash: b1adac8e3029abd64df96ab1560706babe4b12f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753746"
---
# <a name="datatype"></a><span data-ttu-id="6c719-103">DataType</span><span class="sxs-lookup"><span data-stu-id="6c719-103">DataType</span></span>

<span data-ttu-id="6c719-104">**数据类型**元素描述共享的共享文件夹的数据的类型。</span><span class="sxs-lookup"><span data-stu-id="6c719-104">The **DataType** element describes the type of data that is shared by a shared folder.</span></span> 
  
```xml
<DataType>Calendar or Contacts</DataType>
```

<span data-ttu-id="6c719-105">**SharingDataType**</span><span class="sxs-lookup"><span data-stu-id="6c719-105">**SharingDataType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="6c719-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c719-106">Attributes and elements</span></span>

<span data-ttu-id="6c719-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c719-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c719-108">属性</span><span class="sxs-lookup"><span data-stu-id="6c719-108">Attributes</span></span>

<span data-ttu-id="6c719-109">无。</span><span class="sxs-lookup"><span data-stu-id="6c719-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c719-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6c719-110">Child elements</span></span>

<span data-ttu-id="6c719-111">无。</span><span class="sxs-lookup"><span data-stu-id="6c719-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6c719-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6c719-112">Parent elements</span></span>

|<span data-ttu-id="6c719-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c719-113">**Element**</span></span>|<span data-ttu-id="6c719-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c719-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c719-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="6c719-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="6c719-116">定义一个请求以获取指定的共享文件夹的本地文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="6c719-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6c719-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6c719-117">Text value</span></span>

<span data-ttu-id="6c719-118">下表列出的**数据类型**元素的可能值。</span><span class="sxs-lookup"><span data-stu-id="6c719-118">The following table lists the possible values for the **DataType** element.</span></span> 
  
<span data-ttu-id="6c719-119">**数据类型元素的值**</span><span class="sxs-lookup"><span data-stu-id="6c719-119">**DataType element values**</span></span>

|<span data-ttu-id="6c719-120">**值**</span><span class="sxs-lookup"><span data-stu-id="6c719-120">**Value**</span></span>|<span data-ttu-id="6c719-121">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c719-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6c719-122">日历</span><span class="sxs-lookup"><span data-stu-id="6c719-122">Calendar</span></span>  <br/> |<span data-ttu-id="6c719-123">指示的共享的文件夹包含日历信息。</span><span class="sxs-lookup"><span data-stu-id="6c719-123">Indicates that the shared folder contains calendar information.</span></span>  <br/> |
|<span data-ttu-id="6c719-124">联系人</span><span class="sxs-lookup"><span data-stu-id="6c719-124">Contacts</span></span>  <br/> |<span data-ttu-id="6c719-125">指示的共享的文件夹包含联系人信息。</span><span class="sxs-lookup"><span data-stu-id="6c719-125">Indicates that the shared folder contains contact information.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c719-126">备注</span><span class="sxs-lookup"><span data-stu-id="6c719-126">Remarks</span></span>

<span data-ttu-id="6c719-127">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6c719-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c719-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c719-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c719-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c719-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6c719-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c719-130">Schema Name</span></span>  <br/> |<span data-ttu-id="6c719-131">消息架构</span><span class="sxs-lookup"><span data-stu-id="6c719-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6c719-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c719-132">Validation File</span></span>  <br/> |<span data-ttu-id="6c719-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6c719-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6c719-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c719-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c719-135">False</span><span class="sxs-lookup"><span data-stu-id="6c719-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c719-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c719-136">See also</span></span>

- [<span data-ttu-id="6c719-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6c719-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

