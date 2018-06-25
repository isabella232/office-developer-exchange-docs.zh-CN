---
title: SharedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharedFolderId
api_type:
- schema
ms.assetid: 21181ba3-9626-4284-9717-0b1c16948e8f
description: SharedFolderId 元素表示的本地文件夹标识符应返回 GetSharingFolder 操作请求的共享文件夹的标识符。
ms.openlocfilehash: 6d4e541ef3cae89e413efa8cc5f1beaf651dc4dd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827477"
---
# <a name="sharedfolderid"></a><span data-ttu-id="f2099-103">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="f2099-103">SharedFolderId</span></span>

<span data-ttu-id="f2099-104">**SharedFolderId**元素表示的本地文件夹标识符应返回[GetSharingFolder 操作](getsharingfolder-operation.md)请求的共享文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f2099-104">The **SharedFolderId** element represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<SharedFolderId/>
```

 <span data-ttu-id="f2099-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="f2099-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2099-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f2099-106">Attributes and elements</span></span>

<span data-ttu-id="f2099-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f2099-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2099-108">属性</span><span class="sxs-lookup"><span data-stu-id="f2099-108">Attributes</span></span>

<span data-ttu-id="f2099-109">无。</span><span class="sxs-lookup"><span data-stu-id="f2099-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2099-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f2099-110">Child elements</span></span>

<span data-ttu-id="f2099-111">无。</span><span class="sxs-lookup"><span data-stu-id="f2099-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f2099-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f2099-112">Parent elements</span></span>

|<span data-ttu-id="f2099-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f2099-113">**Element**</span></span>|<span data-ttu-id="f2099-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f2099-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2099-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="f2099-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="f2099-116">定义一个请求以获取指定的共享文件夹的本地文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="f2099-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f2099-117">文本值</span><span class="sxs-lookup"><span data-stu-id="f2099-117">Text value</span></span>

<span data-ttu-id="f2099-118">文本值是一个字符串，表示为其的本地文件夹标识符应返回[GetSharingFolder 操作](getsharingfolder-operation.md)请求的共享文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="f2099-118">The text value is a string that represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f2099-119">备注</span><span class="sxs-lookup"><span data-stu-id="f2099-119">Remarks</span></span>

<span data-ttu-id="f2099-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f2099-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2099-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="f2099-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2099-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="f2099-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f2099-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="f2099-123">Schema Name</span></span>  <br/> |<span data-ttu-id="f2099-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="f2099-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f2099-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="f2099-125">Validation File</span></span>  <br/> |<span data-ttu-id="f2099-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f2099-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f2099-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="f2099-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2099-128">False</span><span class="sxs-lookup"><span data-stu-id="f2099-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2099-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f2099-129">See also</span></span>



[<span data-ttu-id="f2099-130">GetSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f2099-130">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="f2099-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="f2099-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

