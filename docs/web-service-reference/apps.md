---
title: 应用
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6f0a2ca-22dd-4789-9eed-f0c1ec9036c4
description: Apps 元素包含有关在邮箱中安装的应用程序的所有 XML 清单文件的信息。
ms.openlocfilehash: b2d6f13241f68cbed449a9f9821f9a6ec6ff687a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527444"
---
# <a name="apps"></a><span data-ttu-id="cd347-103">应用</span><span class="sxs-lookup"><span data-stu-id="cd347-103">Apps</span></span>

<span data-ttu-id="cd347-104">**Apps**元素包含有关在邮箱中安装的应用程序的所有 XML 清单文件的信息。</span><span class="sxs-lookup"><span data-stu-id="cd347-104">The **Apps** element contains information about all the XML manifest files for apps installed in a mailbox.</span></span> 
  
```XML
<Apps>
    <App/>
</Apps>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="cd347-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd347-105">Attributes and elements</span></span>

<span data-ttu-id="cd347-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd347-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd347-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd347-107">Attributes</span></span>

<span data-ttu-id="cd347-108">无。</span><span class="sxs-lookup"><span data-stu-id="cd347-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd347-109">子元素</span><span class="sxs-lookup"><span data-stu-id="cd347-109">Child elements</span></span>

[<span data-ttu-id="cd347-110">App</span><span class="sxs-lookup"><span data-stu-id="cd347-110">App</span></span>](app.md)
  
### <a name="parent-elements"></a><span data-ttu-id="cd347-111">父元素</span><span class="sxs-lookup"><span data-stu-id="cd347-111">Parent elements</span></span>

[<span data-ttu-id="cd347-112">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="cd347-112">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="cd347-113">说明</span><span class="sxs-lookup"><span data-stu-id="cd347-113">Remarks</span></span>

<span data-ttu-id="cd347-114">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cd347-114">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="cd347-115">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd347-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd347-116">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd347-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd347-117">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd347-117">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="cd347-118">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd347-118">Schema Name</span></span>  <br/> |<span data-ttu-id="cd347-119">消息架构</span><span class="sxs-lookup"><span data-stu-id="cd347-119">Messages schema</span></span>  <br/> |
|<span data-ttu-id="cd347-120">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd347-120">Validation File</span></span>  <br/> |<span data-ttu-id="cd347-121">不适用</span><span class="sxs-lookup"><span data-stu-id="cd347-121">Not applicable</span></span>  <br/> |
|<span data-ttu-id="cd347-122">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd347-122">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd347-123">False</span><span class="sxs-lookup"><span data-stu-id="cd347-123">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd347-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cd347-124">See also</span></span>

- [<span data-ttu-id="cd347-125">App</span><span class="sxs-lookup"><span data-stu-id="cd347-125">App</span></span>](app.md)
- [<span data-ttu-id="cd347-126">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="cd347-126">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
- [<span data-ttu-id="cd347-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cd347-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

