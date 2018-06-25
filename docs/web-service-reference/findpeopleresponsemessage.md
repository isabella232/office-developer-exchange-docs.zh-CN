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
ms.openlocfilehash: 205f20b26b5097d24de45c5a5f9681f3557a6f87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754365"
---
# <a name="findpeopleresponsemessage"></a><span data-ttu-id="523e1-103">FindPeopleResponseMessage</span><span class="sxs-lookup"><span data-stu-id="523e1-103">FindPeopleResponseMessage</span></span>

<span data-ttu-id="523e1-104">**FindPeopleResponseMessage**元素指定**FindPeople**请求的响应消息。</span><span class="sxs-lookup"><span data-stu-id="523e1-104">The **FindPeopleResponseMessage** element specifies the response message for a **FindPeople** request.</span></span> 
  
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

 <span data-ttu-id="523e1-105">**FindPeopleResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="523e1-105">**FindPeopleResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="523e1-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="523e1-106">Attributes and elements</span></span>

<span data-ttu-id="523e1-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="523e1-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="523e1-108">属性</span><span class="sxs-lookup"><span data-stu-id="523e1-108">Attributes</span></span>

<span data-ttu-id="523e1-109">无。</span><span class="sxs-lookup"><span data-stu-id="523e1-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="523e1-110">子元素</span><span class="sxs-lookup"><span data-stu-id="523e1-110">Child elements</span></span>

<span data-ttu-id="523e1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [人员](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span><span class="sxs-lookup"><span data-stu-id="523e1-111">[MessageText](messagetext.md) | [ResponseCode](responsecode.md) | [DescriptiveLinkKey](descriptivelinkkey.md) | [MessageXml](messagexml.md) | [People](people.md) | [TotalNumberOfPeopleInView](totalnumberofpeopleinview.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="523e1-112">父元素</span><span class="sxs-lookup"><span data-stu-id="523e1-112">Parent elements</span></span>

[<span data-ttu-id="523e1-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="523e1-113">ResponseMessages</span></span>](responsemessages.md)
  
## <a name="remarks"></a><span data-ttu-id="523e1-114">备注</span><span class="sxs-lookup"><span data-stu-id="523e1-114">Remarks</span></span>

<span data-ttu-id="523e1-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="523e1-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="523e1-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="523e1-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="523e1-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="523e1-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="523e1-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="523e1-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="523e1-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="523e1-119">Schema name</span></span>  <br/> |<span data-ttu-id="523e1-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="523e1-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="523e1-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="523e1-121">Validation file</span></span>  <br/> |<span data-ttu-id="523e1-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="523e1-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="523e1-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="523e1-123">Can be empty</span></span>  <br/> |<span data-ttu-id="523e1-124">false</span><span class="sxs-lookup"><span data-stu-id="523e1-124">false</span></span>  <br/> |
   

