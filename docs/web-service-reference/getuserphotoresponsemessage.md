---
title: GetUserPhotoResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 54d43fe6-9f7b-4f84-920a-bd686c65b059
description: GetUserPhotoResponseMessage 元素包含对 GetUserPhoto 请求的响应。
ms.openlocfilehash: fa817b59527f616afed84d8548e3a18e6c971e2d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825696"
---
# <a name="getuserphotoresponsemessage"></a><span data-ttu-id="2db19-103">GetUserPhotoResponseMessage</span><span class="sxs-lookup"><span data-stu-id="2db19-103">GetUserPhotoResponseMessage</span></span>

<span data-ttu-id="2db19-104">**GetUserPhotoResponseMessage**元素包含对 GetUserPhoto 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="2db19-104">The **GetUserPhotoResponseMessage** element contains the response to a GetUserPhoto request.</span></span> 
  
```XML
<GetUserPhotoResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <HasChanged/>
   <PictureData/>
</GetUserPhotoResponseMessage>
```

 <span data-ttu-id="2db19-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="2db19-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2db19-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="2db19-106">Attributes and elements</span></span>

<span data-ttu-id="2db19-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="2db19-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2db19-108">属性</span><span class="sxs-lookup"><span data-stu-id="2db19-108">Attributes</span></span>

<span data-ttu-id="2db19-109">无。</span><span class="sxs-lookup"><span data-stu-id="2db19-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2db19-110">子元素</span><span class="sxs-lookup"><span data-stu-id="2db19-110">Child elements</span></span>

<span data-ttu-id="2db19-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [HasChanged](haschanged.md) | [PictureData](picturedata.md)</span><span class="sxs-lookup"><span data-stu-id="2db19-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [HasChanged](haschanged.md) | [PictureData](picturedata.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2db19-112">父元素</span><span class="sxs-lookup"><span data-stu-id="2db19-112">Parent elements</span></span>

[<span data-ttu-id="2db19-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="2db19-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="2db19-114">备注</span><span class="sxs-lookup"><span data-stu-id="2db19-114">Remarks</span></span>

<span data-ttu-id="2db19-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="2db19-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2db19-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="2db19-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2db19-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="2db19-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2db19-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="2db19-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2db19-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="2db19-119">Schema name</span></span>  <br/> |<span data-ttu-id="2db19-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="2db19-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2db19-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="2db19-121">Validation file</span></span>  <br/> |<span data-ttu-id="2db19-122">messages.xsd</span><span class="sxs-lookup"><span data-stu-id="2db19-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2db19-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="2db19-123">Can be empty</span></span>  <br/> ||
   
