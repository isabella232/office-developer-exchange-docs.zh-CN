---
title: CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: CreateManagedFolder元素定义添加到邮箱托管自定义文件夹的请求。
ms.openlocfilehash: 01fe8b7341c38ad33089c56271434ad3f9a4e5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458360"
---
# <a name="createmanagedfolder"></a><span data-ttu-id="f5dba-103">CreateManagedFolder</span><span class="sxs-lookup"><span data-stu-id="f5dba-103">CreateManagedFolder</span></span>

<span data-ttu-id="f5dba-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CreateManagedFolder**元素定义添加到邮箱托管自定义文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="f5dba-104">The **CreateManagedFolder** element defines a request to add managed custom folders to a mailbox.</span></span> 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 <span data-ttu-id="f5dba-105">**CreateManagedFolderRequestType**</span><span class="sxs-lookup"><span data-stu-id="f5dba-105">**CreateManagedFolderRequestType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f5dba-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f5dba-106">Attributes and elements</span></span>

<span data-ttu-id="f5dba-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f5dba-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f5dba-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f5dba-108">Attributes</span></span>

<span data-ttu-id="f5dba-109">无。</span><span class="sxs-lookup"><span data-stu-id="f5dba-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f5dba-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f5dba-110">Child elements</span></span>

|<span data-ttu-id="f5dba-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="f5dba-111">**Element**</span></span>|<span data-ttu-id="f5dba-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="f5dba-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f5dba-113">FolderNames</span><span class="sxs-lookup"><span data-stu-id="f5dba-113">FolderNames</span></span>](foldernames.md) <br/> |<span data-ttu-id="f5dba-114">包含一数组的已命名托管文件夹添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="f5dba-114">Contains an array of named managed folders to add to a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="f5dba-115">Mailbox</span><span class="sxs-lookup"><span data-stu-id="f5dba-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="f5dba-116">标识已启用邮件的Active Directory目录服务对象。</span><span class="sxs-lookup"><span data-stu-id="f5dba-116">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f5dba-117">父元素</span><span class="sxs-lookup"><span data-stu-id="f5dba-117">Parent elements</span></span>

<span data-ttu-id="f5dba-118">无。</span><span class="sxs-lookup"><span data-stu-id="f5dba-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f5dba-119">说明</span><span class="sxs-lookup"><span data-stu-id="f5dba-119">Remarks</span></span>

<span data-ttu-id="f5dba-p101">发出请求的用户帐户必须具有在其中创建托管的文件夹邮箱 FullAccess 权限。您可以使用与 Exchange 管理外壳 **Add-MailboxPermission** cmdlet  _ -AccessRights _参数分配 FullAccess 权限。</span><span class="sxs-lookup"><span data-stu-id="f5dba-p101">The account of the person who is making the request must have FullAccess permissions on the mailbox where the managed folders are created. You can use the _ -AccessRights _ parameter with the Exchange Management Shell **Add-MailboxPermission** cmdlet to assign the FullAccess permission.</span></span> 
  
<span data-ttu-id="f5dba-p102">尽管可以使用 Exchange Web 服务添加到邮箱的托管的文件夹，不能使用 Exchange Web 服务来访问可用的托管文件夹的列表。要获取可用的托管文件夹的列表，请使用 **get-managedfolder** Exchange 管理外壳 cmdlet。 **get-managedfolder cmdlet** 返回的列表将包含托管自定义文件夹和托管的默认文件夹。通过使用 CreateManagedFolder 操作可以只将类型为 **managedcustomfolder**的文件夹添加到邮箱。</span><span class="sxs-lookup"><span data-stu-id="f5dba-p102">Although you can use Exchange Web Services to add managed folders to a mailbox, you cannot use Exchange Web Services to access the list of managed folders that are available. To obtain a list of available managed folders, use the **get-managedfolder** Exchange Management Shell cmdlet. The list that is returned by the **get-managedfolder cmdlet** will contain both managed custom folders and managed default folders. You can only add folders of type **managedcustomfolder** to the mailbox by using the CreateManagedFolder operation.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f5dba-126">[!注释] 此外可以使用 DirectoryServices Microsoft.NET Framework 的 API 的托管文件夹的列表。</span><span class="sxs-lookup"><span data-stu-id="f5dba-126">You can also get a list of managed folders by using the DirectoryServices API of the Microsoft .NET Framework.</span></span> 
  
<span data-ttu-id="f5dba-p103">您可以使用[FindFolder Operation](findfolder-operation.md)查找邮箱中的托管的文件夹。可以通过将[BaseShape](baseshape.md)元素设置为AllProperties ，在请求中区分托管的文件夹。响应将包含要区分从 Exchange 存储文件夹的托管的文件夹的 [ManagedFolderInformation](managedfolderinformation.md)元素。以同样的方式删除其他文件夹类型，您可以删除托管的文件夹。</span><span class="sxs-lookup"><span data-stu-id="f5dba-p103">You can use the [FindFolder operation](findfolder-operation.md) to find managed folders in a mailbox. Managed folders can be distinguished by setting the [BaseShape](baseshape.md) element to AllProperties in the request. The response will contain a [ManagedFolderInformation](managedfolderinformation.md) element to distinguish the managed folders from the Exchange store folders. You can delete managed folders in the same manner that you delete other folder types.</span></span> 
  
<span data-ttu-id="f5dba-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f5dba-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5dba-132">元素信息</span><span class="sxs-lookup"><span data-stu-id="f5dba-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5dba-133">命名空间</span><span class="sxs-lookup"><span data-stu-id="f5dba-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="f5dba-134">架构名称</span><span class="sxs-lookup"><span data-stu-id="f5dba-134">Schema Name</span></span>  <br/> |<span data-ttu-id="f5dba-135">消息架构</span><span class="sxs-lookup"><span data-stu-id="f5dba-135">Messages schema</span></span>  <br/> |
|<span data-ttu-id="f5dba-136">验证文件</span><span class="sxs-lookup"><span data-stu-id="f5dba-136">Validation File</span></span>  <br/> |<span data-ttu-id="f5dba-137">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f5dba-137">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f5dba-138">可以为空</span><span class="sxs-lookup"><span data-stu-id="f5dba-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="f5dba-139">False</span><span class="sxs-lookup"><span data-stu-id="f5dba-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f5dba-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="f5dba-140">See also</span></span>



[<span data-ttu-id="f5dba-141">CreateManagedFolder 操作</span><span class="sxs-lookup"><span data-stu-id="f5dba-141">CreateManagedFolder operation</span></span>](createmanagedfolder-operation.md)
  
[<span data-ttu-id="f5dba-142">FindFolder Operation</span><span class="sxs-lookup"><span data-stu-id="f5dba-142">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="f5dba-143">Finding Folders</span><span class="sxs-lookup"><span data-stu-id="f5dba-143">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[<span data-ttu-id="f5dba-144">Adding Managed Folders</span><span class="sxs-lookup"><span data-stu-id="f5dba-144">Adding Managed Folders</span></span>](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

