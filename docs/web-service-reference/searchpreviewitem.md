---
title: SearchPreviewItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59b0b2db-a0ae-4162-a2cb-5f37f42fe872
description: SearchPreviewItem 元素指定发现搜索的项目预览。
ms.openlocfilehash: 46b9d6049f856ce6e93b9e49e07516ec4b52d932
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827308"
---
# <a name="searchpreviewitem"></a><span data-ttu-id="1b048-103">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="1b048-103">SearchPreviewItem</span></span>

<span data-ttu-id="1b048-104">**SearchPreviewItem**元素指定发现搜索的项目预览。</span><span class="sxs-lookup"><span data-stu-id="1b048-104">The **SearchPreviewItem** element specifies the item preview for a discovery search.</span></span> 
  
```XML
<SearchPreviewItem>
   <Id/>
   <Mailbox/>
   <ParentId/>
   <ItemClass/>
   <UniqueHash/>
   <SortValue/>
   <OwaLink/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <CreatedTime/>
   <ReceivedTime/>
   <SentTime/>
   <Subject/>
   <Size/>
   <Preview/>
   <Importance/>
   <Read/>
   <HasAttachment/>
   <ExtendedProperties/>
</SearchPreviewItem>
```

 <span data-ttu-id="1b048-105">**SearchPreviewItemType**</span><span class="sxs-lookup"><span data-stu-id="1b048-105">**SearchPreviewItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1b048-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1b048-106">Attributes and elements</span></span>

<span data-ttu-id="1b048-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1b048-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1b048-108">属性</span><span class="sxs-lookup"><span data-stu-id="1b048-108">Attributes</span></span>

<span data-ttu-id="1b048-109">无。</span><span class="sxs-lookup"><span data-stu-id="1b048-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b048-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1b048-110">Child elements</span></span>

<span data-ttu-id="1b048-111">[ID (ItemIdType)](id-itemidtype.md) | [邮箱 (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md) | [ParentId](parentid.md) | [ItemClass](itemclass.md) | [UniqueHash](uniquehash.md) | [SortValue](sortvalue.md) | [OwaLink](owalink.md)  |  [发件人 （字符串）](sender-string.md) | [ToRecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md) | [CcRecipients](ccrecipients.md) | [BccRecipients](bccrecipients.md) | [CreatedTime](createdtime.md) | [ReceivedTime](receivedtime.md)  | [SentTime](senttime.md) | [主题](subject.md) | [大小 (long)](size-long.md) | [预览](preview-ex15websvcsotherref.md) | [重要性](importance.md) | [读取](read.md) | [HasAttachment](hasattachment.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span><span class="sxs-lookup"><span data-stu-id="1b048-111">[ID (ItemIdType)](id-itemidtype.md) | [Mailbox (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md) | [ParentId](parentid.md) | [ItemClass](itemclass.md) | [UniqueHash](uniquehash.md) | [SortValue](sortvalue.md) | [OwaLink](owalink.md) | [Sender (string)](sender-string.md) | [ToRecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md) | [CcRecipients](ccrecipients.md) | [BccRecipients](bccrecipients.md) | [CreatedTime](createdtime.md) | [ReceivedTime](receivedtime.md) | [SentTime](senttime.md) | [Subject](subject.md) | [Size (long)](size-long.md) | [Preview](preview-ex15websvcsotherref.md) | [Importance](importance.md) | [Read](read.md) | [HasAttachment](hasattachment.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1b048-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1b048-112">Parent elements</span></span>

[<span data-ttu-id="1b048-113">项目 (ArrayOfSearchPreviewItemsType)</span><span class="sxs-lookup"><span data-stu-id="1b048-113">Items (ArrayOfSearchPreviewItemsType)</span></span>](items-arrayofsearchpreviewitemstype.md)
  
## <a name="remarks"></a><span data-ttu-id="1b048-114">备注</span><span class="sxs-lookup"><span data-stu-id="1b048-114">Remarks</span></span>

<span data-ttu-id="1b048-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="1b048-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="1b048-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1b048-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b048-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="1b048-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b048-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="1b048-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1b048-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="1b048-119">Schema name</span></span>  <br/> |<span data-ttu-id="1b048-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="1b048-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="1b048-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="1b048-121">Validation file</span></span>  <br/> |<span data-ttu-id="1b048-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1b048-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1b048-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="1b048-123">Can be empty</span></span>  <br/> ||
   

