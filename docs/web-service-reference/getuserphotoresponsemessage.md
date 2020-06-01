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
ms.openlocfilehash: a6df1204d4ac3a976694afbca008852acef6a76e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463298"
---
# <a name="getuserphotoresponsemessage"></a><span data-ttu-id="ecffb-103">GetUserPhotoResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ecffb-103">GetUserPhotoResponseMessage</span></span>

<span data-ttu-id="ecffb-104">**GetUserPhotoResponseMessage**元素包含对 GetUserPhoto 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="ecffb-104">The **GetUserPhotoResponseMessage** element contains the response to a GetUserPhoto request.</span></span> 
  
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

 <span data-ttu-id="ecffb-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ecffb-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ecffb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ecffb-106">Attributes and elements</span></span>

<span data-ttu-id="ecffb-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ecffb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ecffb-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ecffb-108">Attributes</span></span>

<span data-ttu-id="ecffb-109">无。</span><span class="sxs-lookup"><span data-stu-id="ecffb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ecffb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ecffb-110">Child elements</span></span>

<span data-ttu-id="ecffb-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [HasChanged](haschanged.md)  | [PictureData](picturedata.md)</span><span class="sxs-lookup"><span data-stu-id="ecffb-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [HasChanged](haschanged.md) | [PictureData](picturedata.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ecffb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ecffb-112">Parent elements</span></span>

[<span data-ttu-id="ecffb-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="ecffb-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="ecffb-114">备注</span><span class="sxs-lookup"><span data-stu-id="ecffb-114">Remarks</span></span>

<span data-ttu-id="ecffb-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="ecffb-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ecffb-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ecffb-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ecffb-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="ecffb-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ecffb-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="ecffb-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ecffb-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="ecffb-119">Schema name</span></span>  <br/> |<span data-ttu-id="ecffb-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="ecffb-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ecffb-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="ecffb-121">Validation file</span></span>  <br/> |<span data-ttu-id="ecffb-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="ecffb-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ecffb-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="ecffb-123">Can be empty</span></span>  <br/> ||
   

