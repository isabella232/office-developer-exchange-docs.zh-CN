---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: GetSharingFolder元素定义一个请求以获取指定的共享文件夹的本地文件夹标识符。它是GetSharingFolder 操作的基本元素。
ms.openlocfilehash: cb76c534d9b30d0a9d1b267396551eb2871e638a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460503"
---
# <a name="getsharingfolder"></a><span data-ttu-id="195ca-104">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="195ca-104">GetSharingFolder</span></span>

<span data-ttu-id="195ca-p102">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **GetSharingFolder**元素定义一个请求以获取指定的共享文件夹的本地文件夹标识符。它是[GetSharingFolder 操作](getsharingfolder-operation.md)的基本元素。</span><span class="sxs-lookup"><span data-stu-id="195ca-p102">The **GetSharingFolder** element defines a request to get the local folder identifier of a specified shared folder. It is the base element for the [GetSharingFolder operation](getsharingfolder-operation.md).</span></span>
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 <span data-ttu-id="195ca-107">**GetSharingFolderType**</span><span class="sxs-lookup"><span data-stu-id="195ca-107">**GetSharingFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="195ca-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="195ca-108">Attributes and elements</span></span>

<span data-ttu-id="195ca-109">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="195ca-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="195ca-110">Attributes</span><span class="sxs-lookup"><span data-stu-id="195ca-110">Attributes</span></span>

<span data-ttu-id="195ca-111">无。</span><span class="sxs-lookup"><span data-stu-id="195ca-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="195ca-112">子元素</span><span class="sxs-lookup"><span data-stu-id="195ca-112">Child elements</span></span>

|<span data-ttu-id="195ca-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="195ca-113">**Element**</span></span>|<span data-ttu-id="195ca-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="195ca-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="195ca-115">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="195ca-115">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="195ca-p103">表示共享关系中另一方的 SMTP 电子邮件地址。此元素是必需的。</span><span class="sxs-lookup"><span data-stu-id="195ca-p103">Represents the SMTP e-mail address of the other party in the sharing relationship. This element is required.</span></span>  <br/> |
|[<span data-ttu-id="195ca-118">DataType</span><span class="sxs-lookup"><span data-stu-id="195ca-118">DataType</span></span>](datatype.md) <br/> |<span data-ttu-id="195ca-p104">介绍了由一个共享文件夹共享的数据的类型。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="195ca-p104">Describes the type of data that is shared by a shared folder. This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="195ca-121">SharedFolderId</span><span class="sxs-lookup"><span data-stu-id="195ca-121">SharedFolderId</span></span>](sharedfolderid.md) <br/> |<span data-ttu-id="195ca-p105">表示共享文件夹的本地文件夹标识符应返回的标识符。此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="195ca-p105">Represents the identifier of the shared folder whose local folder identifier should be returned. This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="195ca-124">父元素</span><span class="sxs-lookup"><span data-stu-id="195ca-124">Parent elements</span></span>

<span data-ttu-id="195ca-125">无。</span><span class="sxs-lookup"><span data-stu-id="195ca-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="195ca-126">说明</span><span class="sxs-lookup"><span data-stu-id="195ca-126">Remarks</span></span>

<span data-ttu-id="195ca-p106">GetSharingFolder 元素必须包含一个[SmtpAddress](smtpaddress.md)元素。GetSharingFolder 元素还必须包含一个[DataType](datatype.md)元素或一个[SharedFolderId](sharedfolderid.md)元素，但不能包含两个。</span><span class="sxs-lookup"><span data-stu-id="195ca-p106">A GetSharingFolder element must contain an [SmtpAddress](smtpaddress.md) element. A GetSharingFolder element must also contain either a [DataType](datatype.md) element or a [SharedFolderId](sharedfolderid.md) element, but cannot contain both.</span></span> 
  
<span data-ttu-id="195ca-129">描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。</span><span class="sxs-lookup"><span data-stu-id="195ca-129">The schema that describes this element is located in the IIS Virtual directory that hosts Exchange Web Services of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="195ca-130">元素信息</span><span class="sxs-lookup"><span data-stu-id="195ca-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="195ca-131">命名空间</span><span class="sxs-lookup"><span data-stu-id="195ca-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="195ca-132">架构名称</span><span class="sxs-lookup"><span data-stu-id="195ca-132">Schema Name</span></span>  <br/> |<span data-ttu-id="195ca-133">消息架构</span><span class="sxs-lookup"><span data-stu-id="195ca-133">Messages schema</span></span>  <br/> |
|<span data-ttu-id="195ca-134">验证文件</span><span class="sxs-lookup"><span data-stu-id="195ca-134">Validation File</span></span>  <br/> |<span data-ttu-id="195ca-135">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="195ca-135">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="195ca-136">可以为空</span><span class="sxs-lookup"><span data-stu-id="195ca-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="195ca-137">False</span><span class="sxs-lookup"><span data-stu-id="195ca-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="195ca-138">另请参阅</span><span class="sxs-lookup"><span data-stu-id="195ca-138">See also</span></span>



[<span data-ttu-id="195ca-139">GetSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="195ca-139">GetSharingFolder operation</span></span>](getsharingfolder-operation.md)


- [<span data-ttu-id="195ca-140">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="195ca-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

