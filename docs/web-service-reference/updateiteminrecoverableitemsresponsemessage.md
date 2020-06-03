---
title: UpdateItemInRecoverableItemsResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96259756-322e-4c24-ac76-0cd9c32e0d6d
description: UpdateItemInRecoverableItemsResponseMessage 元素指定对 UpdateItemInRecoverableItems 请求的响应。
ms.openlocfilehash: 021631f5c30eebbf4d7ae0aad35a85b99a23925f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466533"
---
# <a name="updateiteminrecoverableitemsresponsemessage"></a><span data-ttu-id="dc03f-103">UpdateItemInRecoverableItemsResponseMessage</span><span class="sxs-lookup"><span data-stu-id="dc03f-103">UpdateItemInRecoverableItemsResponseMessage</span></span>

<span data-ttu-id="dc03f-104">**UpdateItemInRecoverableItemsResponseMessage**元素指定对**UpdateItemInRecoverableItems**请求的响应。</span><span class="sxs-lookup"><span data-stu-id="dc03f-104">The **UpdateItemInRecoverableItemsResponseMessage** element specifies the response to an **UpdateItemInRecoverableItems** request.</span></span> 
  
```XML
<UpdateItemInRecoverableItemsResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKet/>
   <MessageXml/>
   <Items/>
   <Attachments/>
   <ConflictResults/>
</UpdateItemInRecoverableItemsResponseMessage>
```

 <span data-ttu-id="dc03f-105">**UpdateItemInRecoverableItemsResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="dc03f-105">**UpdateItemInRecoverableItemsResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dc03f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="dc03f-106">Attributes and elements</span></span>

<span data-ttu-id="dc03f-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="dc03f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dc03f-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="dc03f-108">Attributes</span></span>

<span data-ttu-id="dc03f-109">无。</span><span class="sxs-lookup"><span data-stu-id="dc03f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dc03f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="dc03f-110">Child elements</span></span>

<span data-ttu-id="dc03f-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [项目](items.md)  | [附件](attachments-ex15websvcsotherref.md)  | [ConflictResults](conflictresults.md)</span><span class="sxs-lookup"><span data-stu-id="dc03f-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [Items](items.md) | [Attachments](attachments-ex15websvcsotherref.md) | [ConflictResults](conflictresults.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dc03f-112">父元素</span><span class="sxs-lookup"><span data-stu-id="dc03f-112">Parent elements</span></span>

<span data-ttu-id="dc03f-113">无。</span><span class="sxs-lookup"><span data-stu-id="dc03f-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dc03f-114">说明</span><span class="sxs-lookup"><span data-stu-id="dc03f-114">Remarks</span></span>

<span data-ttu-id="dc03f-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="dc03f-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="dc03f-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="dc03f-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc03f-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="dc03f-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc03f-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="dc03f-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/message  <br/> |
|<span data-ttu-id="dc03f-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="dc03f-119">Schema name</span></span>  <br/> |<span data-ttu-id="dc03f-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="dc03f-120">Message schema</span></span>  <br/> |
|<span data-ttu-id="dc03f-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="dc03f-121">Validation file</span></span>  <br/> |<span data-ttu-id="dc03f-122">Message .xsd</span><span class="sxs-lookup"><span data-stu-id="dc03f-122">Message.xsd</span></span>  <br/> |
|<span data-ttu-id="dc03f-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="dc03f-123">Can be empty</span></span>  <br/> |<span data-ttu-id="dc03f-124">false</span><span class="sxs-lookup"><span data-stu-id="dc03f-124">false</span></span>  <br/> |
   

