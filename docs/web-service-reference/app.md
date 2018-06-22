---
title: 应用程序
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92b776b5-fec6-4443-a606-51ccb06f7afd
description: 应用程序元素包含有关邮箱中安装的邮件应用程序的 XML 清单文件的信息。
ms.openlocfilehash: c63bbbf6eb3bf718b2cf81e67d9ec978b3bc5f8d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753156"
---
# <a name="app"></a><span data-ttu-id="cb2cd-103">应用程序</span><span class="sxs-lookup"><span data-stu-id="cb2cd-103">App</span></span>

<span data-ttu-id="cb2cd-104">**应用程序**元素包含有关邮箱中安装的邮件应用程序的 XML 清单文件的信息。</span><span class="sxs-lookup"><span data-stu-id="cb2cd-104">The **App** element contains information about an XML manifest file for a mail app that is installed in a mailbox.</span></span> 
  
```XML
<App>
    <Metadata/>
    <Manifest/>
</App>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="cb2cd-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb2cd-105">Attributes and elements</span></span>

<span data-ttu-id="cb2cd-106">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb2cd-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb2cd-107">属性</span><span class="sxs-lookup"><span data-stu-id="cb2cd-107">Attributes</span></span>

<span data-ttu-id="cb2cd-108">无。</span><span class="sxs-lookup"><span data-stu-id="cb2cd-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb2cd-109">子元素</span><span class="sxs-lookup"><span data-stu-id="cb2cd-109">Child elements</span></span>

<span data-ttu-id="cb2cd-110">[元数据](metadata-ex15websvcsotherref.md) | [清单](manifest.md)</span><span class="sxs-lookup"><span data-stu-id="cb2cd-110">[Metadata](metadata-ex15websvcsotherref.md) | [Manifest](manifest.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb2cd-111">父元素</span><span class="sxs-lookup"><span data-stu-id="cb2cd-111">Parent elements</span></span>

[<span data-ttu-id="cb2cd-112">应用程序</span><span class="sxs-lookup"><span data-stu-id="cb2cd-112">Apps</span></span>](apps.md)
  
## <a name="remarks"></a><span data-ttu-id="cb2cd-113">备注</span><span class="sxs-lookup"><span data-stu-id="cb2cd-113">Remarks</span></span>

<span data-ttu-id="cb2cd-114">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="cb2cd-114">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="cb2cd-115">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cb2cd-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb2cd-116">元素信息</span><span class="sxs-lookup"><span data-stu-id="cb2cd-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb2cd-117">命名空间</span><span class="sxs-lookup"><span data-stu-id="cb2cd-117">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb2cd-118">架构名称</span><span class="sxs-lookup"><span data-stu-id="cb2cd-118">Schema Name</span></span>  <br/> |<span data-ttu-id="cb2cd-119">类型架构</span><span class="sxs-lookup"><span data-stu-id="cb2cd-119">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb2cd-120">验证文件</span><span class="sxs-lookup"><span data-stu-id="cb2cd-120">Validation File</span></span>  <br/> |<span data-ttu-id="cb2cd-121">不适用</span><span class="sxs-lookup"><span data-stu-id="cb2cd-121">Not applicable</span></span>  <br/> |
|<span data-ttu-id="cb2cd-122">可以为空</span><span class="sxs-lookup"><span data-stu-id="cb2cd-122">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb2cd-123">False</span><span class="sxs-lookup"><span data-stu-id="cb2cd-123">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb2cd-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb2cd-124">See also</span></span>

- [<span data-ttu-id="cb2cd-125">应用程序</span><span class="sxs-lookup"><span data-stu-id="cb2cd-125">Apps</span></span>](apps.md)
- [<span data-ttu-id="cb2cd-126">元数据</span><span class="sxs-lookup"><span data-stu-id="cb2cd-126">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="cb2cd-127">Manifest</span><span class="sxs-lookup"><span data-stu-id="cb2cd-127">Manifest</span></span>](manifest.md)
- [<span data-ttu-id="cb2cd-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cb2cd-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

