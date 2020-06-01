---
title: ImItemList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 556457d5-a730-4131-853f-1198c27c5942
description: ImItemList 元素包含即时消息组和即时消息联系人的列表。
ms.openlocfilehash: 976897fd999b61207a94a8b1dc60cc1b1308acd8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460671"
---
# <a name="imitemlist"></a><span data-ttu-id="20ba2-103">ImItemList</span><span class="sxs-lookup"><span data-stu-id="20ba2-103">ImItemList</span></span>

<span data-ttu-id="20ba2-104">**ImItemList**元素包含即时消息组和即时消息联系人的列表。</span><span class="sxs-lookup"><span data-stu-id="20ba2-104">The **ImItemList** element contains a list of instant messaging groups and instant messaging contacts.</span></span> 
  
```XML
<ImItemList>
   <Groups/>
   <Personas/>
</ImItemList>
```

 <span data-ttu-id="20ba2-105">**ImItemListType**</span><span class="sxs-lookup"><span data-stu-id="20ba2-105">**ImItemListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20ba2-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="20ba2-106">Attributes and elements</span></span>

<span data-ttu-id="20ba2-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="20ba2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20ba2-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="20ba2-108">Attributes</span></span>

<span data-ttu-id="20ba2-109">无。</span><span class="sxs-lookup"><span data-stu-id="20ba2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20ba2-110">子元素</span><span class="sxs-lookup"><span data-stu-id="20ba2-110">Child elements</span></span>

<span data-ttu-id="20ba2-111">[组（ArrayOfImGroupType）](groups-arrayofimgrouptype.md)  | [角色](personas-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="20ba2-111">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [Personas](personas-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20ba2-112">父元素</span><span class="sxs-lookup"><span data-stu-id="20ba2-112">Parent elements</span></span>

<span data-ttu-id="20ba2-113">[GetImItemsResponse](getimitemsresponse.md)  | [GetImItemListResponse](getimitemlistresponse.md)</span><span class="sxs-lookup"><span data-stu-id="20ba2-113">[GetImItemsResponse](getimitemsresponse.md) | [GetImItemListResponse](getimitemlistresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20ba2-114">备注</span><span class="sxs-lookup"><span data-stu-id="20ba2-114">Remarks</span></span>

<span data-ttu-id="20ba2-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="20ba2-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="20ba2-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="20ba2-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20ba2-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="20ba2-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20ba2-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="20ba2-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="20ba2-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="20ba2-119">Schema name</span></span>  <br/> |<span data-ttu-id="20ba2-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="20ba2-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="20ba2-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="20ba2-121">Validation file</span></span>  <br/> |<span data-ttu-id="20ba2-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="20ba2-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="20ba2-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="20ba2-123">Can be empty</span></span>  <br/> ||
   

