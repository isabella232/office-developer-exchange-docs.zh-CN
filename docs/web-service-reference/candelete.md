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
description: CanDelete 元素指示某个托管文件夹是否可由客户删除。
ms.openlocfilehash: 5fe16c276bdb0c5b3b73ca63099559d3e869db3e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461588"
---
# <a name="candelete"></a><span data-ttu-id="ea15b-103">CanDelete</span><span class="sxs-lookup"><span data-stu-id="ea15b-103">CanDelete</span></span>

<span data-ttu-id="ea15b-104">**CanDelete**元素指示某个托管文件夹是否可由客户删除。</span><span class="sxs-lookup"><span data-stu-id="ea15b-104">The **CanDelete** element indicates whether a managed folder can be deleted by a customer.</span></span> 
  
```xml
<CanDelete/>
```

 <span data-ttu-id="ea15b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ea15b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ea15b-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="ea15b-106">Attributes and elements</span></span>

<span data-ttu-id="ea15b-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="ea15b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ea15b-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="ea15b-108">Attributes</span></span>

<span data-ttu-id="ea15b-109">无。</span><span class="sxs-lookup"><span data-stu-id="ea15b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ea15b-110">子元素</span><span class="sxs-lookup"><span data-stu-id="ea15b-110">Child elements</span></span>

<span data-ttu-id="ea15b-111">无。</span><span class="sxs-lookup"><span data-stu-id="ea15b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ea15b-112">父元素</span><span class="sxs-lookup"><span data-stu-id="ea15b-112">Parent elements</span></span>

|<span data-ttu-id="ea15b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="ea15b-113">**Element**</span></span>|<span data-ttu-id="ea15b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="ea15b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ea15b-115">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="ea15b-115">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="ea15b-116">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="ea15b-116">Contains information about a managed folder.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="ea15b-117">文本值</span><span class="sxs-lookup"><span data-stu-id="ea15b-117">Text value</span></span>

<span data-ttu-id="ea15b-118">如果存在此元素，则需要一个表示布尔值的文本值。</span><span class="sxs-lookup"><span data-stu-id="ea15b-118">A text value that represents a Boolean value is required if this element is present.</span></span> <span data-ttu-id="ea15b-119">**如果值为 true** ，则表示可以删除文件夹;**如果值为 false** ，则表示无法删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="ea15b-119">A value of **true** indicates that the folder can be deleted; a value of **false** means that the folder cannot be deleted.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ea15b-120">备注</span><span class="sxs-lookup"><span data-stu-id="ea15b-120">Remarks</span></span>

<span data-ttu-id="ea15b-121">若要删除托管文件夹，请使用[DeleteFolder 操作](deletefolder-operation.md)。</span><span class="sxs-lookup"><span data-stu-id="ea15b-121">To delete a managed folder, use the [DeleteFolder operation](deletefolder-operation.md).</span></span>
  
<span data-ttu-id="ea15b-122">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="ea15b-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ea15b-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="ea15b-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ea15b-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="ea15b-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ea15b-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="ea15b-125">Schema name</span></span>  <br/> |<span data-ttu-id="ea15b-126">类型架构</span><span class="sxs-lookup"><span data-stu-id="ea15b-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="ea15b-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="ea15b-127">Validation file</span></span>  <br/> |<span data-ttu-id="ea15b-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ea15b-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ea15b-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="ea15b-129">Can be empty</span></span>  <br/> |<span data-ttu-id="ea15b-130">False</span><span class="sxs-lookup"><span data-stu-id="ea15b-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ea15b-131">另请参阅</span><span class="sxs-lookup"><span data-stu-id="ea15b-131">See also</span></span>



[<span data-ttu-id="ea15b-132">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="ea15b-132">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)


- [<span data-ttu-id="ea15b-133">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="ea15b-133">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="ea15b-134">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="ea15b-134">Deleting Folders</span></span>](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

