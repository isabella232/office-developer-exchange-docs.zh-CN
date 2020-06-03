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
ms.openlocfilehash: 003a72507813677484b2d6ee75f8ff577df169e3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468003"
---
# <a name="installapp"></a><span data-ttu-id="46cb0-103">InstallApp</span><span class="sxs-lookup"><span data-stu-id="46cb0-103">InstallApp</span></span>

<span data-ttu-id="46cb0-104">**InstallApp**元素指定安装应用程序的请求。</span><span class="sxs-lookup"><span data-stu-id="46cb0-104">The **InstallApp** element specifies the request to install an app.</span></span> 
  
```XML
<InstallApp>
    <Manifest/>
</InstallApp>
```

 <span data-ttu-id="46cb0-105">**InstallAppType**</span><span class="sxs-lookup"><span data-stu-id="46cb0-105">**InstallAppType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46cb0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="46cb0-106">Attributes and elements</span></span>

<span data-ttu-id="46cb0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="46cb0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46cb0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="46cb0-108">Attributes</span></span>

<span data-ttu-id="46cb0-109">无。</span><span class="sxs-lookup"><span data-stu-id="46cb0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46cb0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="46cb0-110">Child elements</span></span>

|<span data-ttu-id="46cb0-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="46cb0-111">**Element**</span></span>|<span data-ttu-id="46cb0-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="46cb0-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46cb0-113">清单</span><span class="sxs-lookup"><span data-stu-id="46cb0-113">Manifest</span></span>](manifest.md) <br/> |<span data-ttu-id="46cb0-114">包含 base64 编码的应用程序清单文件。</span><span class="sxs-lookup"><span data-stu-id="46cb0-114">Contains the base64-encoded app manifest file.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46cb0-115">父元素</span><span class="sxs-lookup"><span data-stu-id="46cb0-115">Parent elements</span></span>

<span data-ttu-id="46cb0-116">无。</span><span class="sxs-lookup"><span data-stu-id="46cb0-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46cb0-117">说明</span><span class="sxs-lookup"><span data-stu-id="46cb0-117">Remarks</span></span>

<span data-ttu-id="46cb0-118">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="46cb0-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="46cb0-119">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="46cb0-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46cb0-120">元素信息</span><span class="sxs-lookup"><span data-stu-id="46cb0-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46cb0-121">命名空间</span><span class="sxs-lookup"><span data-stu-id="46cb0-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="46cb0-122">架构名称</span><span class="sxs-lookup"><span data-stu-id="46cb0-122">Schema Name</span></span>  <br/> |<span data-ttu-id="46cb0-123">消息架构</span><span class="sxs-lookup"><span data-stu-id="46cb0-123">Message schema</span></span>  <br/> |
|<span data-ttu-id="46cb0-124">验证文件</span><span class="sxs-lookup"><span data-stu-id="46cb0-124">Validation File</span></span>  <br/> |<span data-ttu-id="46cb0-125">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="46cb0-125">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="46cb0-126">可以为空</span><span class="sxs-lookup"><span data-stu-id="46cb0-126">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="46cb0-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="46cb0-127">See also</span></span>



- [<span data-ttu-id="46cb0-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="46cb0-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

