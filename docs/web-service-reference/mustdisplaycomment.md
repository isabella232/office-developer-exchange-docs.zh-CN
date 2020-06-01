---
title: MustDisplayComment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MustDisplayComment
api_type:
- schema
ms.assetid: 11d4d3c3-4652-4ed4-9b29-a0b5f85b82b7
description: MustDisplayComment 元素指示是否必须显示托管文件夹注释。
ms.openlocfilehash: e86b0c6e2c1d7c3cc00561c17c82b3be82d81242
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463207"
---
# <a name="mustdisplaycomment"></a><span data-ttu-id="704fb-103">MustDisplayComment</span><span class="sxs-lookup"><span data-stu-id="704fb-103">MustDisplayComment</span></span>

<span data-ttu-id="704fb-104">**MustDisplayComment**元素指示是否必须显示托管文件夹注释。</span><span class="sxs-lookup"><span data-stu-id="704fb-104">The **MustDisplayComment** element indicates whether the managed folder comment must be displayed.</span></span> 
  
```xml
<MustDisplayComment/>
```

 <span data-ttu-id="704fb-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="704fb-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="704fb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="704fb-106">Attributes and elements</span></span>

<span data-ttu-id="704fb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="704fb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="704fb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="704fb-108">Attributes</span></span>

<span data-ttu-id="704fb-109">无。</span><span class="sxs-lookup"><span data-stu-id="704fb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="704fb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="704fb-110">Child elements</span></span>

<span data-ttu-id="704fb-111">无。</span><span class="sxs-lookup"><span data-stu-id="704fb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="704fb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="704fb-112">Parent elements</span></span>

|<span data-ttu-id="704fb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="704fb-113">**Element**</span></span>|<span data-ttu-id="704fb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="704fb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="704fb-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="704fb-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="704fb-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="704fb-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="704fb-117">文本值</span><span class="sxs-lookup"><span data-stu-id="704fb-117">Text value</span></span>

<span data-ttu-id="704fb-118">该文本值表示一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="704fb-118">The text value represents a Boolean value.</span></span> <span data-ttu-id="704fb-119">**如果值为 true** ，则表示必须显示注释;**如果值为 false** ，则表示不需要显示批注。</span><span class="sxs-lookup"><span data-stu-id="704fb-119">A value of **true** indicates that the comment must be displayed; a value of **false** indicates that the comment does not have to be displayed.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="704fb-120">说明</span><span class="sxs-lookup"><span data-stu-id="704fb-120">Remarks</span></span>

<span data-ttu-id="704fb-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="704fb-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="704fb-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="704fb-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="704fb-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="704fb-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="704fb-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="704fb-124">Schema name</span></span>  <br/> |<span data-ttu-id="704fb-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="704fb-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="704fb-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="704fb-126">Validation file</span></span>  <br/> |<span data-ttu-id="704fb-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="704fb-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="704fb-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="704fb-128">Can be empty</span></span>  <br/> |<span data-ttu-id="704fb-129">False</span><span class="sxs-lookup"><span data-stu-id="704fb-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="704fb-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="704fb-130">See also</span></span>



[<span data-ttu-id="704fb-131">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="704fb-131">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="704fb-132">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="704fb-132">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

