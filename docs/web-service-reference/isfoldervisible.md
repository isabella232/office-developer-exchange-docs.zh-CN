---
title: IsFolderVisible
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsFolderVisible
api_type:
- schema
ms.assetid: dd611fb5-9424-4ff9-bb27-c882c73c0c74
description: IsFolderVisible 元素指示用户是否可以查看文件夹。 在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。
ms.openlocfilehash: 7efe7eef3c10027c38a3dad2dd3ec1d8684c322a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459298"
---
# <a name="isfoldervisible"></a><span data-ttu-id="9c33f-104">IsFolderVisible</span><span class="sxs-lookup"><span data-stu-id="9c33f-104">IsFolderVisible</span></span>

<span data-ttu-id="9c33f-105">**IsFolderVisible**元素指示用户是否可以查看文件夹。</span><span class="sxs-lookup"><span data-stu-id="9c33f-105">The **IsFolderVisible** element indicates whether a user can view a folder.</span></span> <span data-ttu-id="9c33f-106">在 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9c33f-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<IsFolderVisible/>
```

 <span data-ttu-id="9c33f-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9c33f-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9c33f-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="9c33f-108">Attributes and elements</span></span>

<span data-ttu-id="9c33f-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="9c33f-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9c33f-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="9c33f-110">Attributes</span></span>

<span data-ttu-id="9c33f-111">无。</span><span class="sxs-lookup"><span data-stu-id="9c33f-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9c33f-112">子元素</span><span class="sxs-lookup"><span data-stu-id="9c33f-112">Child elements</span></span>

<span data-ttu-id="9c33f-113">无。</span><span class="sxs-lookup"><span data-stu-id="9c33f-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9c33f-114">父元素</span><span class="sxs-lookup"><span data-stu-id="9c33f-114">Parent elements</span></span>

|<span data-ttu-id="9c33f-115">**元素**</span><span class="sxs-lookup"><span data-stu-id="9c33f-115">**Element**</span></span>|<span data-ttu-id="9c33f-116">**说明**</span><span class="sxs-lookup"><span data-stu-id="9c33f-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9c33f-117">权限</span><span class="sxs-lookup"><span data-stu-id="9c33f-117">Permission</span></span>](permission.md) <br/> |<span data-ttu-id="9c33f-p103">到文件夹定义用户拥有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9c33f-p103">Defines the access that a user has to a folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
|[<span data-ttu-id="9c33f-120">CalendarPermission</span><span class="sxs-lookup"><span data-stu-id="9c33f-120">CalendarPermission</span></span>](calendarpermission.md) <br/> |<span data-ttu-id="9c33f-p104">定义日历文件夹的用户具有的访问权限。在 Exchange 2007 SP1 引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="9c33f-p104">Defines the access that a user has to a Calendar folder. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9c33f-123">文本值</span><span class="sxs-lookup"><span data-stu-id="9c33f-123">Text value</span></span>

<span data-ttu-id="9c33f-124">如果文本值为**true** ，则表示用户可以查看该文件夹。</span><span class="sxs-lookup"><span data-stu-id="9c33f-124">A text value of **true** indicates that the user can view the folder.</span></span> <span data-ttu-id="9c33f-125">**如果值为 false** ，则表示用户无法查看该文件夹。</span><span class="sxs-lookup"><span data-stu-id="9c33f-125">A value of **false** indicates that the user cannot view the folder.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9c33f-126">说明</span><span class="sxs-lookup"><span data-stu-id="9c33f-126">Remarks</span></span>

<span data-ttu-id="9c33f-127">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="9c33f-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9c33f-128">元素信息</span><span class="sxs-lookup"><span data-stu-id="9c33f-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9c33f-129">命名空间</span><span class="sxs-lookup"><span data-stu-id="9c33f-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9c33f-130">架构名称</span><span class="sxs-lookup"><span data-stu-id="9c33f-130">Schema Name</span></span>  <br/> |<span data-ttu-id="9c33f-131">类型架构</span><span class="sxs-lookup"><span data-stu-id="9c33f-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="9c33f-132">验证文件</span><span class="sxs-lookup"><span data-stu-id="9c33f-132">Validation File</span></span>  <br/> |<span data-ttu-id="9c33f-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9c33f-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9c33f-134">可以为空</span><span class="sxs-lookup"><span data-stu-id="9c33f-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="9c33f-135">False</span><span class="sxs-lookup"><span data-stu-id="9c33f-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9c33f-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="9c33f-136">See also</span></span>



- [<span data-ttu-id="9c33f-137">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="9c33f-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="9c33f-138">Setting Folder-Level Permissions</span><span class="sxs-lookup"><span data-stu-id="9c33f-138">Setting Folder-Level Permissions</span></span>](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

