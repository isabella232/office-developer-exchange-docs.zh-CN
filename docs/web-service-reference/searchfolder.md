---
title: SearchFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchFolder
api_type:
- schema
ms.assetid: 1a7d408b-2e98-4391-8834-085ed6d5757c
description: SearchFolder元素表示包含在一个邮箱中的搜索文件夹。
ms.openlocfilehash: d842c54dab7950c68e26804b676834c2d95debad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827302"
---
# <a name="searchfolder"></a><span data-ttu-id="a9369-103">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="a9369-103">SearchFolder</span></span>

<span data-ttu-id="a9369-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **SearchFolder**元素表示包含在一个邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="a9369-104">The **SearchFolder** element represents a search folder that is contained in a mailbox.</span></span> 
  
```xml
<SearchFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <SearchParameters/>
   <PermissionSet/>
      <EffectiveRights/>
</SearchFolder>
```

 <span data-ttu-id="a9369-105">**SearchFolderType**</span><span class="sxs-lookup"><span data-stu-id="a9369-105">**SearchFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a9369-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="a9369-106">Attributes and elements</span></span>

<span data-ttu-id="a9369-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="a9369-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a9369-108">属性</span><span class="sxs-lookup"><span data-stu-id="a9369-108">Attributes</span></span>

<span data-ttu-id="a9369-109">无。</span><span class="sxs-lookup"><span data-stu-id="a9369-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9369-110">子元素</span><span class="sxs-lookup"><span data-stu-id="a9369-110">Child elements</span></span>

|<span data-ttu-id="a9369-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="a9369-111">**Element**</span></span>|<span data-ttu-id="a9369-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="a9369-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9369-113">文件夹 Id</span><span class="sxs-lookup"><span data-stu-id="a9369-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="a9369-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="a9369-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="a9369-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="a9369-116">表示包含该文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="a9369-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="a9369-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="a9369-118">表示给定文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="a9369-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-119">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="a9369-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="a9369-120">包含文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="a9369-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="a9369-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="a9369-122">表示给定文件夹中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="a9369-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="a9369-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="a9369-p101">表示文件夹中包含的子文件夹数。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="a9369-p101">Represents the number of child folders contained within a folder. This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="a9369-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a9369-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="a9369-127">标识文件夹的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="a9369-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="a9369-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="a9369-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="a9369-129">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="a9369-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="a9369-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="a9369-131">表示给定文件夹中未阅读项的计数。</span><span class="sxs-lookup"><span data-stu-id="a9369-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-132">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="a9369-132">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="a9369-133">包含用于定义搜索文件夹的参数。</span><span class="sxs-lookup"><span data-stu-id="a9369-133">Contains the parameters that define a search folder.</span></span>  <br/> |
|[<span data-ttu-id="a9369-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="a9369-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="a9369-p102">包含文件夹的所有配置权限。Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a9369-p102">Contains all the configured permissions for a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="a9369-137">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="a9369-137">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="a9369-p103">包含基于项目或文件夹的权限设置的客户端权限。此元素为只读。Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="a9369-p103">Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9369-141">父元素</span><span class="sxs-lookup"><span data-stu-id="a9369-141">Parent elements</span></span>

|<span data-ttu-id="a9369-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="a9369-142">**Element**</span></span>|<span data-ttu-id="a9369-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="a9369-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9369-144">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="a9369-144">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="a9369-145">指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="a9369-145">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a9369-146">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a9369-146">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="a9369-147">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="a9369-147">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a9369-148">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="a9369-148">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="a9369-149">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="a9369-149">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="a9369-150">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="a9369-150">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="a9369-151">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="a9369-151">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="a9369-152">Folders</span><span class="sxs-lookup"><span data-stu-id="a9369-152">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="a9369-153">包含文件夹在文件夹操作中使用的数组。</span><span class="sxs-lookup"><span data-stu-id="a9369-153">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9369-154">备注</span><span class="sxs-lookup"><span data-stu-id="a9369-154">Remarks</span></span>

 <span data-ttu-id="a9369-p104">**SearchFolder**用于常规搜索文件夹和MicrosoftOfficeOutlook和Outlook Web Access的可见的文件夹中搜索。要对Outlook和Outlook Web Access是可见的搜索文件夹，必须在 SearchFolders 可分辨文件夹下创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="a9369-p104">**SearchFolder** is used for both regular search folders and MicrosoftOfficeOutlook and Outlook Web Access visible search folders. For a search folder to be visible to Outlook and Outlook Web Access, the folder must be created under the SearchFolders distinguished folder.</span></span> 
  
<span data-ttu-id="a9369-157">架构用于描述此元素位于 EWS 虚拟目录运行MicrosoftExchange Server 2007 ，安装了客户端访问服务器角色的计算机。</span><span class="sxs-lookup"><span data-stu-id="a9369-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9369-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="a9369-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9369-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="a9369-159">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a9369-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="a9369-160">Schema Name</span></span>  <br/> |<span data-ttu-id="a9369-161">类型架构</span><span class="sxs-lookup"><span data-stu-id="a9369-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="a9369-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="a9369-162">Validation File</span></span>  <br/> |<span data-ttu-id="a9369-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a9369-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a9369-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="a9369-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9369-165">False</span><span class="sxs-lookup"><span data-stu-id="a9369-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9369-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a9369-166">See also</span></span>



- [<span data-ttu-id="a9369-167">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="a9369-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

