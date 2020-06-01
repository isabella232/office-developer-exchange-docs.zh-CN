---
title: GetPersonaResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a5bf44c6-c46b-442d-98d4-8b49fdf14b30
description: GetPersonaResponseMessage 包含由 GetPersona 请求生成的响应数据。
ms.openlocfilehash: 6391e1b6682180e292d03c5db651e8edc6f46b52
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458325"
---
# <a name="getpersonaresponsemessage"></a><span data-ttu-id="b7263-103">GetPersonaResponseMessage</span><span class="sxs-lookup"><span data-stu-id="b7263-103">GetPersonaResponseMessage</span></span>

<span data-ttu-id="b7263-104">**GetPersonaResponseMessage**包含由**GetPersona**请求生成的响应数据。</span><span class="sxs-lookup"><span data-stu-id="b7263-104">The **GetPersonaResponseMessage** contains the response data resulting from a **GetPersona** request.</span></span> 
  
```XML
<GetPersonaResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Persona/>
</GetPersonaResponseMessage>
```

 <span data-ttu-id="b7263-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="b7263-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b7263-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b7263-106">Attributes and elements</span></span>

<span data-ttu-id="b7263-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b7263-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7263-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b7263-108">Attributes</span></span>

<span data-ttu-id="b7263-109">无。</span><span class="sxs-lookup"><span data-stu-id="b7263-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b7263-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b7263-110">Child elements</span></span>

<span data-ttu-id="b7263-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [Persona](persona.md)</span><span class="sxs-lookup"><span data-stu-id="b7263-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Persona](persona.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b7263-112">父元素</span><span class="sxs-lookup"><span data-stu-id="b7263-112">Parent elements</span></span>

[<span data-ttu-id="b7263-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="b7263-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="b7263-114">备注</span><span class="sxs-lookup"><span data-stu-id="b7263-114">Remarks</span></span>

<span data-ttu-id="b7263-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="b7263-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b7263-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b7263-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7263-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="b7263-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7263-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="b7263-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b7263-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="b7263-119">Schema name</span></span>  <br/> |<span data-ttu-id="b7263-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="b7263-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b7263-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="b7263-121">Validation file</span></span>  <br/> |<span data-ttu-id="b7263-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="b7263-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b7263-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="b7263-123">Can be empty</span></span>  <br/> ||
   

