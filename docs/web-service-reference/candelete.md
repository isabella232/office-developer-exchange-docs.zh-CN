---
title: CanDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanDelete
api_type:
- schema
ms.assetid: 55e17121-aad0-4f90-889f-2c3512e9579c
description: CanDelete 元素指示客户是否可以删除的托管的文件夹。
ms.openlocfilehash: b70b28bd6b3c9452f5d7f249f453218d555754da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753433"
---
# <a name="candelete"></a><span data-ttu-id="1e8bb-103">CanDelete</span><span class="sxs-lookup"><span data-stu-id="1e8bb-103">CanDelete</span></span>

<span data-ttu-id="1e8bb-104">**CanDelete**元素指示客户是否可以删除的托管的文件夹。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-104">The **CanDelete** element indicates whether a managed folder can be deleted by a customer.</span></span> 
  
```xml
<CanDelete/>
```

 <span data-ttu-id="1e8bb-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="1e8bb-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1e8bb-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="1e8bb-106">Attributes and elements</span></span>

<span data-ttu-id="1e8bb-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e8bb-108">属性</span><span class="sxs-lookup"><span data-stu-id="1e8bb-108">Attributes</span></span>

<span data-ttu-id="1e8bb-109">无。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e8bb-110">子元素</span><span class="sxs-lookup"><span data-stu-id="1e8bb-110">Child elements</span></span>

<span data-ttu-id="1e8bb-111">无。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1e8bb-112">父元素</span><span class="sxs-lookup"><span data-stu-id="1e8bb-112">Parent elements</span></span>

|<span data-ttu-id="1e8bb-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="1e8bb-113">**Element**</span></span>|<span data-ttu-id="1e8bb-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="1e8bb-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e8bb-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="1e8bb-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="1e8bb-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1e8bb-117">文本值</span><span class="sxs-lookup"><span data-stu-id="1e8bb-117">Text value</span></span>

<span data-ttu-id="1e8bb-118">如果此元素是存在，则需要一个文本值，它代表一个布尔值。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="1e8bb-119">值为**true**指示可以删除该文件夹;如果值为**false**意味着不能删除该文件夹。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-119">A value of **true** indicates that the folder can be deleted; a value of **false** means that the folder cannot be deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1e8bb-120">注解</span><span class="sxs-lookup"><span data-stu-id="1e8bb-120">Remarks</span></span>

<span data-ttu-id="1e8bb-121">若要删除的托管的文件夹，使用[DeleteFolder 操作](deletefolder-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-121">To delete a managed folder, use the [DeleteFolder operation](deletefolder-operation.md).</span></span>
  
<span data-ttu-id="1e8bb-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="1e8bb-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e8bb-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="1e8bb-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e8bb-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="1e8bb-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e8bb-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="1e8bb-125">Schema name</span></span>  <br/> |<span data-ttu-id="1e8bb-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="1e8bb-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="1e8bb-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="1e8bb-127">Validation file</span></span>  <br/> |<span data-ttu-id="1e8bb-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1e8bb-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e8bb-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="1e8bb-129">Can be empty</span></span>  <br/> |<span data-ttu-id="1e8bb-130">False</span><span class="sxs-lookup"><span data-stu-id="1e8bb-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e8bb-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="1e8bb-131">See also</span></span>



[<span data-ttu-id="1e8bb-132">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="1e8bb-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="1e8bb-133">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="1e8bb-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="1e8bb-134">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="1e8bb-134">Deleting Folders</span></span>](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

