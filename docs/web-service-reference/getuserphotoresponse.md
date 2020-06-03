---
title: GetUserPhotoResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 29b085e8-95c0-4ba6-83e8-40de36a75be3
description: GetUserPhotoResponse 元素包含对 GetUserPhoto 请求的响应。
ms.openlocfilehash: c0dfb6979ade0192b376c3f7115fef78a4cc7e06
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463305"
---
# <a name="getuserphotoresponse"></a><span data-ttu-id="1f014-103">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="1f014-103">GetUserPhotoResponse</span></span>

<span data-ttu-id="1f014-104">**GetUserPhotoResponse**元素包含对 GetUserPhoto 请求的响应。</span><span class="sxs-lookup"><span data-stu-id="1f014-104">The **GetUserPhotoResponse** element contains the response to a GetUserPhoto request.</span></span> 
  
```XML
<GetUserPhotoResponse>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <HasChanged/>
   <PictureData/>
</GetUserPhotoResponse>
```

 <span data-ttu-id="1f014-105">**GetUserPhotoResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="1f014-105">**GetUserPhotoResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1f014-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1f014-106">Attributes and elements</span></span>

<span data-ttu-id="1f014-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1f014-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1f014-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="1f014-108">Attributes</span></span>

<span data-ttu-id="1f014-109">无。</span><span class="sxs-lookup"><span data-stu-id="1f014-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1f014-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1f014-110">Child elements</span></span>

<span data-ttu-id="1f014-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [HasChanged](haschanged.md)  | [PictureData](picturedata.md)</span><span class="sxs-lookup"><span data-stu-id="1f014-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [HasChanged](haschanged.md) | [PictureData](picturedata.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1f014-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1f014-112">Parent elements</span></span>

<span data-ttu-id="1f014-113">无。</span><span class="sxs-lookup"><span data-stu-id="1f014-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1f014-114">说明</span><span class="sxs-lookup"><span data-stu-id="1f014-114">Remarks</span></span>

<span data-ttu-id="1f014-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1f014-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1f014-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1f014-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1f014-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1f014-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1f014-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1f014-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="1f014-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1f014-119">Schema name</span></span>  <br/> |<span data-ttu-id="1f014-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="1f014-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="1f014-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1f014-121">Validation file</span></span>  <br/> |<span data-ttu-id="1f014-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="1f014-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="1f014-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1f014-123">Can be empty</span></span>  <br/> ||
   

