---
title: FindPeopleResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ba686738-e654-404d-ab54-83c71d030350
description: FindPeopleResponseMessage 元素指定 FindPeople 请求的响应消息。
ms.openlocfilehash: 5a2ce7b8643fff9d4a93b62459638d3a99605c98
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466372"
---
# <a name="findpeopleresponsemessage"></a><span data-ttu-id="3ffe6-103">FindPeopleResponseMessage</span><span class="sxs-lookup"><span data-stu-id="3ffe6-103">FindPeopleResponseMessage</span></span>

<span data-ttu-id="3ffe6-104">**FindPeopleResponseMessage**元素指定**FindPeople**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="3ffe6-104">The **FindPeopleResponseMessage** element specifies the response message for a **FindPeople** request.</span></span> 
  
```XML
<FindPeopleResponseMessage>
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <People/>
   <TotalNumberOfPeopleInView/>
</FindPeopleResponseMessage>
```

 <span data-ttu-id="3ffe6-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="3ffe6-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3ffe6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3ffe6-106">Attributes and elements</span></span>

<span data-ttu-id="3ffe6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3ffe6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ffe6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="3ffe6-108">Attributes</span></span>

<span data-ttu-id="3ffe6-109">无。</span><span class="sxs-lookup"><span data-stu-id="3ffe6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ffe6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3ffe6-110">Child elements</span></span>

<span data-ttu-id="3ffe6-111">[MessageText](messagetext.md)  | [ResponseCode](responsecode.md)  | [DescriptiveLinkKey](descriptivelinkkey.md)  | [MessageXml](messagexml.md)  | [人员](people.md)  | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span><span class="sxs-lookup"><span data-stu-id="3ffe6-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [People](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3ffe6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="3ffe6-112">Parent elements</span></span>

[<span data-ttu-id="3ffe6-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="3ffe6-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="3ffe6-114">备注</span><span class="sxs-lookup"><span data-stu-id="3ffe6-114">Remarks</span></span>

<span data-ttu-id="3ffe6-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="3ffe6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="3ffe6-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3ffe6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ffe6-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="3ffe6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ffe6-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="3ffe6-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3ffe6-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="3ffe6-119">Schema name</span></span>  <br/> |<span data-ttu-id="3ffe6-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="3ffe6-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3ffe6-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="3ffe6-121">Validation file</span></span>  <br/> |<span data-ttu-id="3ffe6-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3ffe6-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3ffe6-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="3ffe6-123">Can be empty</span></span>  <br/> |<span data-ttu-id="3ffe6-124">false</span><span class="sxs-lookup"><span data-stu-id="3ffe6-124">false</span></span>  <br/> |
   

