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
ms.openlocfilehash: e1d5893e00f3b199451622061785e2566c6f32e5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464005"
---
# <a name="searchfolder"></a><span data-ttu-id="32e9a-103">SearchFolder</span><span class="sxs-lookup"><span data-stu-id="32e9a-103">SearchFolder</span></span>

<span data-ttu-id="32e9a-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **SearchFolder**元素表示包含在一个邮箱中的搜索文件夹。</span><span class="sxs-lookup"><span data-stu-id="32e9a-104">The **SearchFolder** element represents a search folder that is contained in a mailbox.</span></span> 
  
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

 <span data-ttu-id="32e9a-105">**SearchFolderType**</span><span class="sxs-lookup"><span data-stu-id="32e9a-105">**SearchFolderType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="32e9a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="32e9a-106">Attributes and elements</span></span>

<span data-ttu-id="32e9a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="32e9a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="32e9a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="32e9a-108">Attributes</span></span>

<span data-ttu-id="32e9a-109">无。</span><span class="sxs-lookup"><span data-stu-id="32e9a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="32e9a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="32e9a-110">Child elements</span></span>

|<span data-ttu-id="32e9a-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="32e9a-111">**Element**</span></span>|<span data-ttu-id="32e9a-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="32e9a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32e9a-113">FolderId</span><span class="sxs-lookup"><span data-stu-id="32e9a-113">FolderId</span></span>](folderid.md) <br/> |<span data-ttu-id="32e9a-114">包含一个文件夹的标识符和更改键。</span><span class="sxs-lookup"><span data-stu-id="32e9a-114">Contains the identifier and change key of a folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-115">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="32e9a-115">ParentFolderId</span></span>](parentfolderid.md) <br/> |<span data-ttu-id="32e9a-116">表示包含该文件夹的父文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="32e9a-116">Represents the identifier of the parent folder that contains the folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-117">FolderClass</span><span class="sxs-lookup"><span data-stu-id="32e9a-117">FolderClass</span></span>](folderclass.md) <br/> |<span data-ttu-id="32e9a-118">表示给定文件夹的文件夹类。</span><span class="sxs-lookup"><span data-stu-id="32e9a-118">Represents the folder class for a given folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-119">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="32e9a-119">DisplayName (string)</span></span>](displayname-string.md) <br/> |<span data-ttu-id="32e9a-120">包含文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="32e9a-120">Contains the display name of a folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-121">TotalCount</span><span class="sxs-lookup"><span data-stu-id="32e9a-121">TotalCount</span></span>](totalcount.md) <br/> |<span data-ttu-id="32e9a-122">表示给定文件夹中的项目总数。</span><span class="sxs-lookup"><span data-stu-id="32e9a-122">Represents the total count of items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-123">ChildFolderCount</span><span class="sxs-lookup"><span data-stu-id="32e9a-123">ChildFolderCount</span></span>](childfoldercount.md) <br/> |<span data-ttu-id="32e9a-p101">表示文件夹中包含的子文件夹数。此属性是只读的。</span><span class="sxs-lookup"><span data-stu-id="32e9a-p101">Represents the number of child folders contained within a folder. This property is read-only.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-126">ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="32e9a-126">ExtendedProperty</span></span>](extendedproperty.md) <br/> |<span data-ttu-id="32e9a-127">标识文件夹的扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="32e9a-127">Identifies extended properties on folders.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-128">ManagedFolderInformation</span><span class="sxs-lookup"><span data-stu-id="32e9a-128">ManagedFolderInformation</span></span>](managedfolderinformation.md) <br/> |<span data-ttu-id="32e9a-129">包含有关托管文件夹的信息。</span><span class="sxs-lookup"><span data-stu-id="32e9a-129">Contains information about a managed folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-130">UnreadCount</span><span class="sxs-lookup"><span data-stu-id="32e9a-130">UnreadCount</span></span>](unreadcount.md) <br/> |<span data-ttu-id="32e9a-131">表示给定文件夹中未阅读项的计数。</span><span class="sxs-lookup"><span data-stu-id="32e9a-131">Represents the count of unread items within a given folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-132">SearchParameters</span><span class="sxs-lookup"><span data-stu-id="32e9a-132">SearchParameters</span></span>](searchparameters.md) <br/> |<span data-ttu-id="32e9a-133">包含用于定义搜索文件夹的参数。</span><span class="sxs-lookup"><span data-stu-id="32e9a-133">Contains the parameters that define a search folder.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-134">PermissionSet (PermissionSetType)</span><span class="sxs-lookup"><span data-stu-id="32e9a-134">PermissionSet (PermissionSetType)</span></span>](permissionset-permissionsettype.md) <br/> |<span data-ttu-id="32e9a-p102">包含文件夹的所有配置权限。Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="32e9a-p102">Contains all the configured permissions for a folder. This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
|[<span data-ttu-id="32e9a-137">EffectiveRights</span><span class="sxs-lookup"><span data-stu-id="32e9a-137">EffectiveRights</span></span>](effectiverights.md) <br/> |<span data-ttu-id="32e9a-p103">包含基于项目或文件夹的权限设置的客户端权限。此元素为只读。Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="32e9a-p103">Contains the client's rights based on the permission settings for the item or folder. This element is read-only. This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="32e9a-141">父元素</span><span class="sxs-lookup"><span data-stu-id="32e9a-141">Parent elements</span></span>

|<span data-ttu-id="32e9a-142">**元素**</span><span class="sxs-lookup"><span data-stu-id="32e9a-142">**Element**</span></span>|<span data-ttu-id="32e9a-143">**说明**</span><span class="sxs-lookup"><span data-stu-id="32e9a-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="32e9a-144">AppendToFolderField</span><span class="sxs-lookup"><span data-stu-id="32e9a-144">AppendToFolderField</span></span>](appendtofolderfield.md) <br/> |<span data-ttu-id="32e9a-145">指定要在[UpdateFolder Operation](updatefolder-operation.md)期间追加到文件夹属性数据。</span><span class="sxs-lookup"><span data-stu-id="32e9a-145">Specifies data to append to a folder property during an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="32e9a-146">创建 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="32e9a-146">Create (FolderSync)</span></span>](create-foldersync.md) <br/> |<span data-ttu-id="32e9a-147">标识要在本地客户端存储中创建一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="32e9a-147">Identifies a single folder to create in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-148">SetFolderField</span><span class="sxs-lookup"><span data-stu-id="32e9a-148">SetFolderField</span></span>](setfolderfield.md) <br/> |<span data-ttu-id="32e9a-149">表示对[UpdateFolder Operation](updatefolder-operation.md)中的文件夹上的单个属性的更新。</span><span class="sxs-lookup"><span data-stu-id="32e9a-149">Represents an update to a single property on a folder in an [UpdateFolder operation](updatefolder-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="32e9a-150">更新 (FolderSync)</span><span class="sxs-lookup"><span data-stu-id="32e9a-150">Update (FolderSync)</span></span>](update-foldersync.md) <br/> |<span data-ttu-id="32e9a-151">标识要在本地客户端存储中更新单个文件夹。</span><span class="sxs-lookup"><span data-stu-id="32e9a-151">Identifies a single folder to update in the local client store.</span></span>  <br/> |
|[<span data-ttu-id="32e9a-152">Folders</span><span class="sxs-lookup"><span data-stu-id="32e9a-152">Folders</span></span>](folders-ex15websvcsotherref.md) <br/> |<span data-ttu-id="32e9a-153">包含文件夹在文件夹操作中使用的数组。</span><span class="sxs-lookup"><span data-stu-id="32e9a-153">Contains an array of folders used in folder operations.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="32e9a-154">备注</span><span class="sxs-lookup"><span data-stu-id="32e9a-154">Remarks</span></span>

 <span data-ttu-id="32e9a-p104">**SearchFolder**用于常规搜索文件夹和MicrosoftOfficeOutlook和Outlook Web Access的可见的文件夹中搜索。要对Outlook和Outlook Web Access是可见的搜索文件夹，必须在 SearchFolders 可分辨文件夹下创建文件夹。</span><span class="sxs-lookup"><span data-stu-id="32e9a-p104">**SearchFolder** is used for both regular search folders and MicrosoftOfficeOutlook and Outlook Web Access visible search folders. For a search folder to be visible to Outlook and Outlook Web Access, the folder must be created under the SearchFolders distinguished folder.</span></span> 
  
<span data-ttu-id="32e9a-157">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="32e9a-157">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32e9a-158">元素信息</span><span class="sxs-lookup"><span data-stu-id="32e9a-158">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32e9a-159">命名空间</span><span class="sxs-lookup"><span data-stu-id="32e9a-159">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="32e9a-160">架构名称</span><span class="sxs-lookup"><span data-stu-id="32e9a-160">Schema Name</span></span>  <br/> |<span data-ttu-id="32e9a-161">类型架构</span><span class="sxs-lookup"><span data-stu-id="32e9a-161">Types schema</span></span>  <br/> |
|<span data-ttu-id="32e9a-162">验证文件</span><span class="sxs-lookup"><span data-stu-id="32e9a-162">Validation File</span></span>  <br/> |<span data-ttu-id="32e9a-163">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="32e9a-163">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="32e9a-164">可以为空</span><span class="sxs-lookup"><span data-stu-id="32e9a-164">Can be Empty</span></span>  <br/> |<span data-ttu-id="32e9a-165">False</span><span class="sxs-lookup"><span data-stu-id="32e9a-165">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="32e9a-166">另请参阅</span><span class="sxs-lookup"><span data-stu-id="32e9a-166">See also</span></span>



- [<span data-ttu-id="32e9a-167">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="32e9a-167">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

