---
title: FolderNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderNames
api_type:
- schema
ms.assetid: 6cbe4083-5705-4695-a54e-8dab3e472662
description: FolderNames 元素包含一个数组，其中包含要添加到邮箱中的已命名托管文件夹。
ms.openlocfilehash: 00cb1a81f420469033ccbc745313d2719b155aff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530984"
---
# <a name="foldernames"></a><span data-ttu-id="0619b-103">FolderNames</span><span class="sxs-lookup"><span data-stu-id="0619b-103">FolderNames</span></span>

<span data-ttu-id="0619b-104">**FolderNames**元素包含一个数组，其中包含要添加到邮箱中的已命名托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="0619b-104">The **FolderNames** element contains an array of named managed folders to add to a mailbox.</span></span> 
  
[<span data-ttu-id="0619b-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="0619b-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="0619b-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="0619b-106">FolderNames</span></span>](foldernames.md)
  
```xml
<FolderNames>
   <FolderName/>
</FolderNames>
```

 <span data-ttu-id="0619b-107">**NonEmptyArrayOfFolderNamesType**</span><span class="sxs-lookup"><span data-stu-id="0619b-107">**NonEmptyArrayOfFolderNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0619b-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="0619b-108">Attributes and elements</span></span>

<span data-ttu-id="0619b-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="0619b-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0619b-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="0619b-110">Attributes</span></span>

<span data-ttu-id="0619b-111">无。</span><span class="sxs-lookup"><span data-stu-id="0619b-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0619b-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0619b-112">Child elements</span></span>

|<span data-ttu-id="0619b-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0619b-113">**Element**</span></span>|<span data-ttu-id="0619b-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="0619b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0619b-115">FolderName</span><span class="sxs-lookup"><span data-stu-id="0619b-115">FolderName</span></span>](foldername.md) <br/> |<span data-ttu-id="0619b-116">标识要添加到邮箱中的单个托管文件夹。</span><span class="sxs-lookup"><span data-stu-id="0619b-116">Identifies a single managed folder to add to mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0619b-117">父元素</span><span class="sxs-lookup"><span data-stu-id="0619b-117">Parent elements</span></span>

|<span data-ttu-id="0619b-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="0619b-118">**Element**</span></span>|<span data-ttu-id="0619b-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="0619b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0619b-120">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="0619b-120">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="0619b-121">将托管文件夹添加到邮箱的请求中的根元素。</span><span class="sxs-lookup"><span data-stu-id="0619b-121">The root element in a request to add a managed folder to a mailbox.</span></span>  <br/> <span data-ttu-id="0619b-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="0619b-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0619b-123">说明</span><span class="sxs-lookup"><span data-stu-id="0619b-123">Remarks</span></span>

<span data-ttu-id="0619b-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="0619b-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0619b-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="0619b-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0619b-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="0619b-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="0619b-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="0619b-127">Schema Name</span></span>  <br/> |<span data-ttu-id="0619b-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="0619b-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="0619b-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="0619b-129">Validation File</span></span>  <br/> |<span data-ttu-id="0619b-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="0619b-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0619b-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="0619b-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="0619b-132">False</span><span class="sxs-lookup"><span data-stu-id="0619b-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0619b-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="0619b-133">See also</span></span>



[<span data-ttu-id="0619b-134">FindFolder 操作</span><span class="sxs-lookup"><span data-stu-id="0619b-134">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="0619b-135">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="0619b-135">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="0619b-136">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="0619b-136">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

