---
title: InstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fc2ca69e-eea7-4334-b046-ec0b04d8f8c6
description: InstallApp 元素指定安装应用程序的请求。
ms.openlocfilehash: d9b7412865c003b89eccbdd92aa6ff9968048191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825949"
---
# <a name="installapp"></a><span data-ttu-id="39a6c-103">InstallApp</span><span class="sxs-lookup"><span data-stu-id="39a6c-103">InstallApp</span></span>

<span data-ttu-id="39a6c-104">**InstallApp**元素指定安装应用程序的请求。</span><span class="sxs-lookup"><span data-stu-id="39a6c-104">The **InstallApp** element specifies the request to install an app.</span></span> 
  
```XML
<InstallApp>
    <Manifest/>
</InstallApp>
```

 <span data-ttu-id="39a6c-105">**InstallAppType**</span><span class="sxs-lookup"><span data-stu-id="39a6c-105">**InstallAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="39a6c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="39a6c-106">Attributes and elements</span></span>

<span data-ttu-id="39a6c-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="39a6c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39a6c-108">属性</span><span class="sxs-lookup"><span data-stu-id="39a6c-108">Attributes</span></span>

<span data-ttu-id="39a6c-109">无。</span><span class="sxs-lookup"><span data-stu-id="39a6c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="39a6c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="39a6c-110">Child elements</span></span>

|<span data-ttu-id="39a6c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="39a6c-111">**Element**</span></span>|<span data-ttu-id="39a6c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="39a6c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="39a6c-113">Manifest</span><span class="sxs-lookup"><span data-stu-id="39a6c-113">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="39a6c-114">包含 base64 编码的应用程序清单文件。</span><span class="sxs-lookup"><span data-stu-id="39a6c-114">Contains the base64-encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="39a6c-115">父元素</span><span class="sxs-lookup"><span data-stu-id="39a6c-115">Parent elements</span></span>

<span data-ttu-id="39a6c-116">无。</span><span class="sxs-lookup"><span data-stu-id="39a6c-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39a6c-117">备注</span><span class="sxs-lookup"><span data-stu-id="39a6c-117">Remarks</span></span>

<span data-ttu-id="39a6c-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="39a6c-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="39a6c-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="39a6c-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39a6c-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="39a6c-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39a6c-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="39a6c-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="39a6c-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="39a6c-122">Schema Name</span></span>  <br/> |<span data-ttu-id="39a6c-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="39a6c-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="39a6c-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="39a6c-124">Validation File</span></span>  <br/> |<span data-ttu-id="39a6c-125">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="39a6c-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="39a6c-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="39a6c-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="39a6c-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="39a6c-127">See also</span></span>



- [<span data-ttu-id="39a6c-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="39a6c-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

