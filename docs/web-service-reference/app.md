---
title: 应用
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92b776b5-fec6-4443-a606-51ccb06f7afd
description: App 元素包含有关安装在邮箱中的邮件应用程序的 XML 清单文件的信息。
ms.openlocfilehash: b5870164b059d2e50930ee33c09cbd030501f171
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460356"
---
# <a name="app"></a><span data-ttu-id="3e47a-103">应用</span><span class="sxs-lookup"><span data-stu-id="3e47a-103">App</span></span>

<span data-ttu-id="3e47a-104">**App**元素包含有关安装在邮箱中的邮件应用程序的 XML 清单文件的信息。</span><span class="sxs-lookup"><span data-stu-id="3e47a-104">The **App** element contains information about an XML manifest file for a mail app that is installed in a mailbox.</span></span> 
  
```XML
<App>
    <Metadata/>
    <Manifest/>
</App>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="3e47a-105">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3e47a-105">Attributes and elements</span></span>

<span data-ttu-id="3e47a-106">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3e47a-106">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e47a-107">Attributes</span><span class="sxs-lookup"><span data-stu-id="3e47a-107">Attributes</span></span>

<span data-ttu-id="3e47a-108">无。</span><span class="sxs-lookup"><span data-stu-id="3e47a-108">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e47a-109">子元素</span><span class="sxs-lookup"><span data-stu-id="3e47a-109">Child elements</span></span>

<span data-ttu-id="3e47a-110">[元数据](metadata-ex15websvcsotherref.md)  | [清单](manifest.md)</span><span class="sxs-lookup"><span data-stu-id="3e47a-110">[Metadata](metadata-ex15websvcsotherref.md) | [Manifest](manifest.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3e47a-111">父元素</span><span class="sxs-lookup"><span data-stu-id="3e47a-111">Parent elements</span></span>

[<span data-ttu-id="3e47a-112">应用</span><span class="sxs-lookup"><span data-stu-id="3e47a-112">Apps</span></span>](apps.md)
  
## <a name="remarks"></a><span data-ttu-id="3e47a-113">说明</span><span class="sxs-lookup"><span data-stu-id="3e47a-113">Remarks</span></span>

<span data-ttu-id="3e47a-114">Exchange Server 2013 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3e47a-114">This element was introduced in Exchange Server 2013 Service Pack 1 (SP1).</span></span>
  
<span data-ttu-id="3e47a-115">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3e47a-115">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e47a-116">元素信息</span><span class="sxs-lookup"><span data-stu-id="3e47a-116">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e47a-117">命名空间</span><span class="sxs-lookup"><span data-stu-id="3e47a-117">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e47a-118">架构名称</span><span class="sxs-lookup"><span data-stu-id="3e47a-118">Schema Name</span></span>  <br/> |<span data-ttu-id="3e47a-119">类型架构</span><span class="sxs-lookup"><span data-stu-id="3e47a-119">Types schema</span></span>  <br/> |
|<span data-ttu-id="3e47a-120">验证文件</span><span class="sxs-lookup"><span data-stu-id="3e47a-120">Validation File</span></span>  <br/> |<span data-ttu-id="3e47a-121">不适用</span><span class="sxs-lookup"><span data-stu-id="3e47a-121">Not applicable</span></span>  <br/> |
|<span data-ttu-id="3e47a-122">可以为空</span><span class="sxs-lookup"><span data-stu-id="3e47a-122">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e47a-123">False</span><span class="sxs-lookup"><span data-stu-id="3e47a-123">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e47a-124">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3e47a-124">See also</span></span>

- [<span data-ttu-id="3e47a-125">应用</span><span class="sxs-lookup"><span data-stu-id="3e47a-125">Apps</span></span>](apps.md)
- [<span data-ttu-id="3e47a-126">元数据</span><span class="sxs-lookup"><span data-stu-id="3e47a-126">Metadata</span></span>](metadata-ex15websvcsotherref.md)
- [<span data-ttu-id="3e47a-127">清单</span><span class="sxs-lookup"><span data-stu-id="3e47a-127">Manifest</span></span>](manifest.md)
- [<span data-ttu-id="3e47a-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="3e47a-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

