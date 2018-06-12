---
title: ExpandDL
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDL
api_type:
- schema
ms.assetid: affe84a5-ad98-4aba-83f4-8732938b763d
description: ExpandDL 元素定义一个请求以展开通讯组列表。
ms.openlocfilehash: ef93ed4684427a74a4fd2c38b4020ecb743fbaaf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754195"
---
# <a name="expanddl"></a><span data-ttu-id="d5fc4-103">ExpandDL</span><span class="sxs-lookup"><span data-stu-id="d5fc4-103">ExpandDL</span></span>

<span data-ttu-id="d5fc4-104">**ExpandDL**元素定义一个请求以展开通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-104">The **ExpandDL** element defines a request to expand a distribution list.</span></span> 
  
```xml
<ExpandDL>
   <Mailbox/>
</ExpandDL>
```

 <span data-ttu-id="d5fc4-105">**ExpandDLType**</span><span class="sxs-lookup"><span data-stu-id="d5fc4-105">**ExpandDLType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d5fc4-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="d5fc4-106">Attributes and elements</span></span>

<span data-ttu-id="d5fc4-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d5fc4-108">属性</span><span class="sxs-lookup"><span data-stu-id="d5fc4-108">Attributes</span></span>

<span data-ttu-id="d5fc4-109">无</span><span class="sxs-lookup"><span data-stu-id="d5fc4-109">None</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d5fc4-110">子元素</span><span class="sxs-lookup"><span data-stu-id="d5fc4-110">Child elements</span></span>

|<span data-ttu-id="d5fc4-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="d5fc4-111">**Element**</span></span>|<span data-ttu-id="d5fc4-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="d5fc4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d5fc4-113">Mailbox</span><span class="sxs-lookup"><span data-stu-id="d5fc4-113">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="d5fc4-114">标识一个完全解析电子邮件地址或通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-114">Identifies a fully resolved e-mail address or a distribution list.</span></span> <span data-ttu-id="d5fc4-115">此邮箱代表展开通讯组列表。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-115">This mailbox represents the distribution list to expand.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d5fc4-116">父元素</span><span class="sxs-lookup"><span data-stu-id="d5fc4-116">Parent elements</span></span>

<span data-ttu-id="d5fc4-117">无。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-117">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d5fc4-118">备注</span><span class="sxs-lookup"><span data-stu-id="d5fc4-118">Remarks</span></span>

<span data-ttu-id="d5fc4-119">只能将一个通讯组列表执行通讯组列表扩展。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-119">A distribution list expansion will only be performed for a single distribution list.</span></span> <span data-ttu-id="d5fc4-120">通讯组列表扩展不递归。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-120">A distribution list expansion is not recursive.</span></span>
  
<span data-ttu-id="d5fc4-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="d5fc4-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5fc4-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="d5fc4-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5fc4-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="d5fc4-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="d5fc4-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="d5fc4-124">Schema Name</span></span>  <br/> |<span data-ttu-id="d5fc4-125">消息架构</span><span class="sxs-lookup"><span data-stu-id="d5fc4-125">Message schema</span></span>  <br/> |
|<span data-ttu-id="d5fc4-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="d5fc4-126">Validation File</span></span>  <br/> |<span data-ttu-id="d5fc4-127">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="d5fc4-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="d5fc4-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="d5fc4-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="d5fc4-129">False</span><span class="sxs-lookup"><span data-stu-id="d5fc4-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d5fc4-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d5fc4-130">See also</span></span>



[<span data-ttu-id="d5fc4-131">ExpandDL 操作</span><span class="sxs-lookup"><span data-stu-id="d5fc4-131">ExpandDL operation</span></span>](expanddl-operation.md)

