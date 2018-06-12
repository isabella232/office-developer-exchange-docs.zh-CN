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
description: FolderNames 元素包含一个数组命名托管文件夹添加到邮箱。
ms.openlocfilehash: 819b3c2df1cfcae3a5d4a48539e369a00b1f7229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754394"
---
# <a name="foldernames"></a><span data-ttu-id="61b1c-103">FolderNames</span><span class="sxs-lookup"><span data-stu-id="61b1c-103">FolderNames</span></span>

<span data-ttu-id="61b1c-104">**FolderNames**元素包含一个数组命名托管文件夹添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="61b1c-104">The **FolderNames** element contains an array of named managed folders to add to a mailbox.</span></span> 
  
[<span data-ttu-id="61b1c-105">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="61b1c-105">CreateManagedFolder</span></span>](createmanagedfolder.md)
  
[<span data-ttu-id="61b1c-106">FolderNames</span><span class="sxs-lookup"><span data-stu-id="61b1c-106">FolderNames</span></span>](foldernames.md)
  
```xml
<FolderNames>
   <FolderName/>
</FolderNames>
```

 <span data-ttu-id="61b1c-107">**NonEmptyArrayOfFolderNamesType**</span><span class="sxs-lookup"><span data-stu-id="61b1c-107">**NonEmptyArrayOfFolderNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="61b1c-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="61b1c-108">Attributes and elements</span></span>

<span data-ttu-id="61b1c-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="61b1c-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="61b1c-110">属性</span><span class="sxs-lookup"><span data-stu-id="61b1c-110">Attributes</span></span>

<span data-ttu-id="61b1c-111">无。</span><span class="sxs-lookup"><span data-stu-id="61b1c-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="61b1c-112">子元素</span><span class="sxs-lookup"><span data-stu-id="61b1c-112">Child elements</span></span>

|<span data-ttu-id="61b1c-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="61b1c-113">**Element**</span></span>|<span data-ttu-id="61b1c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="61b1c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61b1c-115">FolderName</span><span class="sxs-lookup"><span data-stu-id="61b1c-115">FolderName</span></span>](foldername.md) <br/> |<span data-ttu-id="61b1c-116">标识要添加到邮箱的单个托管的文件夹。</span><span class="sxs-lookup"><span data-stu-id="61b1c-116">Identifies a single managed folder to add to mailbox.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="61b1c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="61b1c-117">Parent elements</span></span>

|<span data-ttu-id="61b1c-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="61b1c-118">**Element**</span></span>|<span data-ttu-id="61b1c-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="61b1c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="61b1c-120">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="61b1c-120">CreateManagedFolder</span></span>](createmanagedfolder.md) <br/> |<span data-ttu-id="61b1c-121">中的请求将托管的文件夹添加到邮箱的根元素。</span><span class="sxs-lookup"><span data-stu-id="61b1c-121">The root element in a request to add a managed folder to a mailbox.</span></span>  <br/> <span data-ttu-id="61b1c-122">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="61b1c-122">The following is the XPath expression to this element:</span></span>  <br/>  `/CreateManagedFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61b1c-123">备注</span><span class="sxs-lookup"><span data-stu-id="61b1c-123">Remarks</span></span>

<span data-ttu-id="61b1c-124">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="61b1c-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61b1c-125">元素信息</span><span class="sxs-lookup"><span data-stu-id="61b1c-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61b1c-126">命名空间</span><span class="sxs-lookup"><span data-stu-id="61b1c-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="61b1c-127">架构名称</span><span class="sxs-lookup"><span data-stu-id="61b1c-127">Schema Name</span></span>  <br/> |<span data-ttu-id="61b1c-128">消息架构</span><span class="sxs-lookup"><span data-stu-id="61b1c-128">Messages schema</span></span>  <br/> |
|<span data-ttu-id="61b1c-129">验证文件</span><span class="sxs-lookup"><span data-stu-id="61b1c-129">Validation File</span></span>  <br/> |<span data-ttu-id="61b1c-130">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="61b1c-130">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="61b1c-131">可以为空</span><span class="sxs-lookup"><span data-stu-id="61b1c-131">Can be Empty</span></span>  <br/> |<span data-ttu-id="61b1c-132">False</span><span class="sxs-lookup"><span data-stu-id="61b1c-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="61b1c-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="61b1c-133">See also</span></span>



[<span data-ttu-id="61b1c-134">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="61b1c-134">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="61b1c-135">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="61b1c-135">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="61b1c-136">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="61b1c-136">Adding Managed Folders</span></span>](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

