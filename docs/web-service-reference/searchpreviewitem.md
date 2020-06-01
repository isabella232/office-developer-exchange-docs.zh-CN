---
title: SearchPreviewItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 59b0b2db-a0ae-4162-a2cb-5f37f42fe872
description: SearchPreviewItem 元素指定发现搜索的项预览。
ms.openlocfilehash: ab48353b0ffaf4bc3b9409f1a620d145bffc7a13
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466932"
---
# <a name="searchpreviewitem"></a><span data-ttu-id="fad0e-103">SearchPreviewItem</span><span class="sxs-lookup"><span data-stu-id="fad0e-103">SearchPreviewItem</span></span>

<span data-ttu-id="fad0e-104">**SearchPreviewItem**元素指定发现搜索的项预览。</span><span class="sxs-lookup"><span data-stu-id="fad0e-104">The **SearchPreviewItem** element specifies the item preview for a discovery search.</span></span> 
  
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

 <span data-ttu-id="fad0e-105">**SearchPreviewItemType**</span><span class="sxs-lookup"><span data-stu-id="fad0e-105">**SearchPreviewItemType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fad0e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="fad0e-106">Attributes and elements</span></span>

<span data-ttu-id="fad0e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="fad0e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fad0e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="fad0e-108">Attributes</span></span>

<span data-ttu-id="fad0e-109">无。</span><span class="sxs-lookup"><span data-stu-id="fad0e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fad0e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="fad0e-110">Child elements</span></span>

<span data-ttu-id="fad0e-111">[ID （ItemIdType）](id-itemidtype.md)  | [邮箱（PreviewItemMailboxType）](mailbox-previewitemmailboxtype.md)  | [ParentId](parentid.md)  | [ItemClass](itemclass.md)  | [UniqueHash](uniquehash.md)  | [SortValue](sortvalue.md)  | [OwaLink](owalink.md)  | [发件人（字符串）](sender-string.md)  | [ToRecipients （ArrayOfSmtpAddressType）](torecipients-arrayofsmtpaddresstype.md)  | [CcRecipients](ccrecipients.md)  | [BccRecipients](bccrecipients.md)  | [CreatedTime](createdtime.md)  | [ReceivedTime](receivedtime.md)  | [SentTime](senttime.md)  | [主题](subject.md)  | [大小（long）](size-long.md)  | [预览](preview-ex15websvcsotherref.md)  | [重要性](importance.md)  | [阅读](read.md)  | [HasAttachment](hasattachment.md)  | [ExtendedProperties （NonEmptyArrayOfExtendedPropertyType）](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span><span class="sxs-lookup"><span data-stu-id="fad0e-111">[ID (ItemIdType)](id-itemidtype.md) | [Mailbox (PreviewItemMailboxType)](mailbox-previewitemmailboxtype.md) | [ParentId](parentid.md) | [ItemClass](itemclass.md) | [UniqueHash](uniquehash.md) | [SortValue](sortvalue.md) | [OwaLink](owalink.md) | [Sender (string)](sender-string.md) | [ToRecipients (ArrayOfSmtpAddressType)](torecipients-arrayofsmtpaddresstype.md) | [CcRecipients](ccrecipients.md) | [BccRecipients](bccrecipients.md) | [CreatedTime](createdtime.md) | [ReceivedTime](receivedtime.md) | [SentTime](senttime.md) | [Subject](subject.md) | [Size (long)](size-long.md) | [Preview](preview-ex15websvcsotherref.md) | [Importance](importance.md) | [Read](read.md) | [HasAttachment](hasattachment.md) | [ExtendedProperties (NonEmptyArrayOfExtendedPropertyType)](extendedproperties-nonemptyarrayofextendedpropertytype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fad0e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="fad0e-112">Parent elements</span></span>

[<span data-ttu-id="fad0e-113">项目（ArrayOfSearchPreviewItemsType）</span><span class="sxs-lookup"><span data-stu-id="fad0e-113">Items (ArrayOfSearchPreviewItemsType)</span></span>](items-arrayofsearchpreviewitemstype.md)
  
## <a name="remarks"></a><span data-ttu-id="fad0e-114">备注</span><span class="sxs-lookup"><span data-stu-id="fad0e-114">Remarks</span></span>

<span data-ttu-id="fad0e-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="fad0e-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fad0e-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="fad0e-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fad0e-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="fad0e-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fad0e-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="fad0e-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fad0e-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="fad0e-119">Schema name</span></span>  <br/> |<span data-ttu-id="fad0e-120">类型架构</span><span class="sxs-lookup"><span data-stu-id="fad0e-120">Types schema</span></span>  <br/> |
|<span data-ttu-id="fad0e-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="fad0e-121">Validation file</span></span>  <br/> |<span data-ttu-id="fad0e-122">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fad0e-122">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fad0e-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="fad0e-123">Can be empty</span></span>  <br/> ||
   

