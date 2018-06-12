---
title: ImItemList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 556457d5-a730-4131-853f-1198c27c5942
description: ImItemList 元素包含即时消息的组和即时消息联系人的列表。
ms.openlocfilehash: 490ac57da0c7ae7bedc75e94b7e21dc30c9da23f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825896"
---
# <a name="imitemlist"></a><span data-ttu-id="be3e6-103">ImItemList</span><span class="sxs-lookup"><span data-stu-id="be3e6-103">ImItemList</span></span>

<span data-ttu-id="be3e6-104">**ImItemList**元素包含即时消息的组和即时消息联系人的列表。</span><span class="sxs-lookup"><span data-stu-id="be3e6-104">The **ImItemList** element contains a list of instant messaging groups and instant messaging contacts.</span></span> 
  
```XML
<ImItemList>
   <Groups/>
   <Personas/>
</ImItemList>
```

 <span data-ttu-id="be3e6-105">**ImItemListType**</span><span class="sxs-lookup"><span data-stu-id="be3e6-105">**ImItemListType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="be3e6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="be3e6-106">Attributes and elements</span></span>

<span data-ttu-id="be3e6-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="be3e6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="be3e6-108">属性</span><span class="sxs-lookup"><span data-stu-id="be3e6-108">Attributes</span></span>

<span data-ttu-id="be3e6-109">无。</span><span class="sxs-lookup"><span data-stu-id="be3e6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be3e6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="be3e6-110">Child elements</span></span>

<span data-ttu-id="be3e6-111">[组 (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [角色](personas-ex15websvcsotherref.md)</span><span class="sxs-lookup"><span data-stu-id="be3e6-111">[Groups (ArrayOfImGroupType)](groups-arrayofimgrouptype.md) | [Personas](personas-ex15websvcsotherref.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="be3e6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="be3e6-112">Parent elements</span></span>

<span data-ttu-id="be3e6-113">[GetImItemsResponse](getimitemsresponse.md) | [GetImItemListResponse](getimitemlistresponse.md)</span><span class="sxs-lookup"><span data-stu-id="be3e6-113">[GetImItemsResponse](getimitemsresponse.md) | [GetImItemListResponse](getimitemlistresponse.md)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="be3e6-114">备注</span><span class="sxs-lookup"><span data-stu-id="be3e6-114">Remarks</span></span>

<span data-ttu-id="be3e6-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="be3e6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="be3e6-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="be3e6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be3e6-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="be3e6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be3e6-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="be3e6-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="be3e6-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="be3e6-119">Schema name</span></span>  <br/> |<span data-ttu-id="be3e6-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="be3e6-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="be3e6-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="be3e6-121">Validation file</span></span>  <br/> |<span data-ttu-id="be3e6-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="be3e6-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="be3e6-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="be3e6-123">Can be empty</span></span>  <br/> ||
   

