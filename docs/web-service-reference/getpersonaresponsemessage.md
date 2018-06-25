---
title: GetPersonaResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a5bf44c6-c46b-442d-98d4-8b49fdf14b30
description: GetPersonaResponseMessage 包含生成 GetPersona 请求的响应数据。
ms.openlocfilehash: 7d38daac9c7c3a74ba9d9670c2bd16dcf2cd47e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754659"
---
# <a name="getpersonaresponsemessage"></a><span data-ttu-id="6d797-103">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="6d797-103">GetPersonaResponseMessage</span></span>

<span data-ttu-id="6d797-104">**GetPersonaResponseMessage**包含生成**GetPersona**请求的响应数据。</span><span class="sxs-lookup"><span data-stu-id="6d797-104">The **GetPersonaResponseMessage** contains the response data resulting from a **GetPersona** request.</span></span> 
  
```XML
<GetPersonaResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Persona/>
</GetPersonaResponseMessage>
```

 <span data-ttu-id="6d797-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="6d797-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d797-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6d797-106">Attributes and elements</span></span>

<span data-ttu-id="6d797-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6d797-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d797-108">属性</span><span class="sxs-lookup"><span data-stu-id="6d797-108">Attributes</span></span>

<span data-ttu-id="6d797-109">无。</span><span class="sxs-lookup"><span data-stu-id="6d797-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d797-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6d797-110">Child elements</span></span>

<span data-ttu-id="6d797-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [角色](persona.md)</span><span class="sxs-lookup"><span data-stu-id="6d797-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Persona](persona.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d797-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6d797-112">Parent elements</span></span>

[<span data-ttu-id="6d797-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="6d797-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="6d797-114">备注</span><span class="sxs-lookup"><span data-stu-id="6d797-114">Remarks</span></span>

<span data-ttu-id="6d797-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="6d797-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6d797-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6d797-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d797-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="6d797-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d797-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="6d797-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6d797-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="6d797-119">Schema name</span></span>  <br/> |<span data-ttu-id="6d797-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="6d797-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6d797-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="6d797-121">Validation file</span></span>  <br/> |<span data-ttu-id="6d797-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="6d797-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6d797-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="6d797-123">Can be empty</span></span>  <br/> ||
   

