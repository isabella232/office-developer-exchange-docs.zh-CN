---
title: ManagedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderId
api_type:
- schema
ms.assetid: 3efb7abb-0e91-4d8a-9fa2-3dec8bd17c30
description: ManagedFolderId 元素包含托管文件夹的文件夹 ID。
ms.openlocfilehash: eacfe580342e6667fd9fc84ad953a5e4070b6ed7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465819"
---
# <a name="managedfolderid"></a><span data-ttu-id="cd12b-103">ManagedFolderId</span><span class="sxs-lookup"><span data-stu-id="cd12b-103">ManagedFolderId</span></span>

<span data-ttu-id="cd12b-104">**ManagedFolderId**元素包含托管文件夹的文件夹 ID。</span><span class="sxs-lookup"><span data-stu-id="cd12b-104">The **ManagedFolderId** element contains the folder ID of the managed folder.</span></span> 
  
```xml
<ManagedFolderId/>
```

 <span data-ttu-id="cd12b-105">**string**</span><span class="sxs-lookup"><span data-stu-id="cd12b-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd12b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cd12b-106">Attributes and elements</span></span>

<span data-ttu-id="cd12b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cd12b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd12b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="cd12b-108">Attributes</span></span>

<span data-ttu-id="cd12b-109">无。</span><span class="sxs-lookup"><span data-stu-id="cd12b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd12b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="cd12b-110">Child elements</span></span>

<span data-ttu-id="cd12b-111">无。</span><span class="sxs-lookup"><span data-stu-id="cd12b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cd12b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="cd12b-112">Parent elements</span></span>

|<span data-ttu-id="cd12b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="cd12b-113">**Element**</span></span>|<span data-ttu-id="cd12b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="cd12b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd12b-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="cd12b-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="cd12b-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="cd12b-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cd12b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="cd12b-117">Text value</span></span>

<span data-ttu-id="cd12b-118">此元素需要一个文本值。</span><span class="sxs-lookup"><span data-stu-id="cd12b-118">A text value is required for this element.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cd12b-119">备注</span><span class="sxs-lookup"><span data-stu-id="cd12b-119">Remarks</span></span>

<span data-ttu-id="cd12b-120">**ManagedFolderId**标识符值等效于 Microsoft Windows Powershell 命令检索的**Guid**属性 `Get-ManagedFolder` 。</span><span class="sxs-lookup"><span data-stu-id="cd12b-120">The **ManagedFolderId** identifier value is the equivalent of the **Guid** property that is retrieved by the  `Get-ManagedFolder` Microsoft Windows Powershell command.</span></span> <span data-ttu-id="cd12b-121">它也是 Active Directory 目录服务中托管文件夹的**objectGUID**属性的值。</span><span class="sxs-lookup"><span data-stu-id="cd12b-121">It is also the value of the **objectGUID** attribute for the managed folder in the Active Directory directory service.</span></span> 
  
<span data-ttu-id="cd12b-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="cd12b-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd12b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="cd12b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd12b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="cd12b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd12b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="cd12b-125">Schema name</span></span>  <br/> |<span data-ttu-id="cd12b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="cd12b-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd12b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="cd12b-127">Validation file</span></span>  <br/> |<span data-ttu-id="cd12b-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd12b-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd12b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="cd12b-129">Can be empty</span></span>  <br/> |<span data-ttu-id="cd12b-130">False</span><span class="sxs-lookup"><span data-stu-id="cd12b-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd12b-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cd12b-131">See also</span></span>



[<span data-ttu-id="cd12b-132">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="cd12b-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="cd12b-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="cd12b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="cd12b-134">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="cd12b-134">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)
  
[<span data-ttu-id="cd12b-135">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="cd12b-135">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

