---
title: IsFolderContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFolderContact
api_type:
- schema
ms.assetid: 8b456255-f4ae-4ca0-845a-13c195f1c867
description: IsFolderContact 元素指示用户是否为文件夹的联系人。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 51a79b4535667685517ff55ef9f6c2b2aaea564c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19826015"
---
# <a name="isfoldercontact"></a><span data-ttu-id="64d66-104">IsFolderContact</span><span class="sxs-lookup"><span data-stu-id="64d66-104">IsFolderContact</span></span>

<span data-ttu-id="64d66-105">**IsFolderContact**元素指示用户是否为文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="64d66-105">The **IsFolderContact** element indicates whether a user is a contact for a folder.</span></span> <span data-ttu-id="64d66-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="64d66-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<IsFolderContact/>
```

 <span data-ttu-id="64d66-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="64d66-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="64d66-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="64d66-108">Attributes and elements</span></span>

<span data-ttu-id="64d66-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="64d66-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64d66-110">属性</span><span class="sxs-lookup"><span data-stu-id="64d66-110">Attributes</span></span>

<span data-ttu-id="64d66-111">无。</span><span class="sxs-lookup"><span data-stu-id="64d66-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64d66-112">子元素</span><span class="sxs-lookup"><span data-stu-id="64d66-112">Child elements</span></span>

<span data-ttu-id="64d66-113">无。</span><span class="sxs-lookup"><span data-stu-id="64d66-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="64d66-114">父元素</span><span class="sxs-lookup"><span data-stu-id="64d66-114">Parent elements</span></span>

|<span data-ttu-id="64d66-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="64d66-115">**Element**</span></span>|<span data-ttu-id="64d66-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="64d66-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64d66-117">权限</span><span class="sxs-lookup"><span data-stu-id="64d66-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="64d66-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="64d66-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="64d66-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="64d66-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="64d66-p104">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="64d66-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="64d66-123">文本值</span><span class="sxs-lookup"><span data-stu-id="64d66-123">Text value</span></span>

<span data-ttu-id="64d66-124">文本值为**true**指示用户是指定的文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="64d66-124">A text value of **true** indicates that the user is a contact for the specified folder.</span></span> <span data-ttu-id="64d66-125">如果值为**false**指示用户不是指定的文件夹的联系人。</span><span class="sxs-lookup"><span data-stu-id="64d66-125">A value of **false** indicates that the user is not a contact for the specified folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="64d66-126">备注</span><span class="sxs-lookup"><span data-stu-id="64d66-126">Remarks</span></span>

<span data-ttu-id="64d66-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="64d66-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="64d66-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="64d66-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64d66-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="64d66-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="64d66-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="64d66-130">Schema Name</span></span>  <br/> |<span data-ttu-id="64d66-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="64d66-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="64d66-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="64d66-132">Validation File</span></span>  <br/> |<span data-ttu-id="64d66-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="64d66-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="64d66-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="64d66-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="64d66-135">False</span><span class="sxs-lookup"><span data-stu-id="64d66-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="64d66-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="64d66-136">See also</span></span>



- [<span data-ttu-id="64d66-137">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="64d66-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="64d66-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="64d66-138">Setting Folder-Level Permissions</span></span>](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

