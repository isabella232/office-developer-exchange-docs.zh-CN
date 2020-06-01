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
description: SharedFolderId 元素表示共享文件夹的标识符，该标识符是应由 GetSharingFolder 操作请求返回的本地文件夹标识符。
ms.openlocfilehash: 546e148540708725bcf335f39bf69d193124d210
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466120"
---
# <a name="sharedfolderid"></a><span data-ttu-id="a06bd-103">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="a06bd-103">SharedFolderId</span></span>

<span data-ttu-id="a06bd-104">**SharedFolderId**元素表示共享文件夹的标识符，该标识符是应由[GetSharingFolder 操作](getsharingfolder-operation.md)请求返回的本地文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="a06bd-104">The **SharedFolderId** element represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
```xml
<SharedFolderId/>
```

 <span data-ttu-id="a06bd-105">**NonEmptyStringType**</span><span class="sxs-lookup"><span data-stu-id="a06bd-105">**NonEmptyStringType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a06bd-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a06bd-106">Attributes and elements</span></span>

<span data-ttu-id="a06bd-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a06bd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a06bd-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="a06bd-108">Attributes</span></span>

<span data-ttu-id="a06bd-109">无。</span><span class="sxs-lookup"><span data-stu-id="a06bd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a06bd-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a06bd-110">Child elements</span></span>

<span data-ttu-id="a06bd-111">无。</span><span class="sxs-lookup"><span data-stu-id="a06bd-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a06bd-112">父元素</span><span class="sxs-lookup"><span data-stu-id="a06bd-112">Parent elements</span></span>

|<span data-ttu-id="a06bd-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="a06bd-113">**Element**</span></span>|<span data-ttu-id="a06bd-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="a06bd-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a06bd-115">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="a06bd-115">GetSharingFolder</span></span>](getsharingfolder.md) <br/> |<span data-ttu-id="a06bd-116">定义获取指定共享文件夹的本地文件夹标识符的请求。</span><span class="sxs-lookup"><span data-stu-id="a06bd-116">Defines a request to get the local folder identifier of a specified shared folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a06bd-117">文本值</span><span class="sxs-lookup"><span data-stu-id="a06bd-117">Text value</span></span>

<span data-ttu-id="a06bd-118">Text 值是一个字符串，表示共享文件夹的标识符，该标识符是应由[GetSharingFolder 操作](getsharingfolder-operation.md)请求返回的本地文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="a06bd-118">The text value is a string that represents the identifier of the shared folder the local folder identifier for which should be returned by a [GetSharingFolder operation](getsharingfolder-operation.md) request.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a06bd-119">说明</span><span class="sxs-lookup"><span data-stu-id="a06bd-119">Remarks</span></span>

<span data-ttu-id="a06bd-120">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="a06bd-120">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a06bd-121">元素信息</span><span class="sxs-lookup"><span data-stu-id="a06bd-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a06bd-122">命名空间</span><span class="sxs-lookup"><span data-stu-id="a06bd-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a06bd-123">架构名称</span><span class="sxs-lookup"><span data-stu-id="a06bd-123">Schema Name</span></span>  <br/> |<span data-ttu-id="a06bd-124">消息架构</span><span class="sxs-lookup"><span data-stu-id="a06bd-124">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a06bd-125">验证文件</span><span class="sxs-lookup"><span data-stu-id="a06bd-125">Validation File</span></span>  <br/> |<span data-ttu-id="a06bd-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a06bd-126">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a06bd-127">可以为空</span><span class="sxs-lookup"><span data-stu-id="a06bd-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="a06bd-128">False</span><span class="sxs-lookup"><span data-stu-id="a06bd-128">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a06bd-129">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a06bd-129">See also</span></span>



[<span data-ttu-id="a06bd-130">GetSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="a06bd-130">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="a06bd-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a06bd-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

