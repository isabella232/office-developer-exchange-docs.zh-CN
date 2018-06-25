---
title: ResolveNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolveNames
api_type:
- schema
ms.assetid: c85207e1-1315-443b-94ec-2b58f405076b
description: ResolveNames 元素定义请求解析模糊名称。
ms.openlocfilehash: e97b6e78d99cf8ffa3d680907916882d40963f59
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827172"
---
# <a name="resolvenames"></a><span data-ttu-id="07b11-103">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="07b11-103">ResolveNames</span></span>

<span data-ttu-id="07b11-104">**ResolveNames**元素定义请求解析模糊名称。</span><span class="sxs-lookup"><span data-stu-id="07b11-104">The **ResolveNames** element defines a request to resolve ambiguous names.</span></span> 
  
```XML
<ResolveNames ReturnFullContactData="" SearchScope="" ContactDataShape="">
   <ParentFolderIds/>
   <UnresolvedEntry/>
</ResolveNames>
```

 <span data-ttu-id="07b11-105">**ResolveNamesType**</span><span class="sxs-lookup"><span data-stu-id="07b11-105">**ResolveNamesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07b11-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="07b11-106">Attributes and elements</span></span>

<span data-ttu-id="07b11-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="07b11-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07b11-108">属性</span><span class="sxs-lookup"><span data-stu-id="07b11-108">Attributes</span></span>

|<span data-ttu-id="07b11-109">**属性**</span><span class="sxs-lookup"><span data-stu-id="07b11-109">**Attribute**</span></span>|<span data-ttu-id="07b11-110">**说明**</span><span class="sxs-lookup"><span data-stu-id="07b11-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07b11-111">**ReturnFullContactData**</span><span class="sxs-lookup"><span data-stu-id="07b11-111">**ReturnFullContactData**</span></span> <br/> |<span data-ttu-id="07b11-112">描述是否在响应中返回解析名称的公共联系人的完整联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="07b11-112">Describes whether the full contact details for public contacts for a resolved name are returned in the response.</span></span> <span data-ttu-id="07b11-113">此属性是必需的公共联系人。</span><span class="sxs-lookup"><span data-stu-id="07b11-113">This attribute is required for public contacts.</span></span> <span data-ttu-id="07b11-114">专用的联系人和私人通讯组列表，则始终返回[ItemId](itemid.md) ，就不会影响此值。</span><span class="sxs-lookup"><span data-stu-id="07b11-114">This value does not affect private contacts and private distribution lists, for which [ItemId](itemid.md) is always returned.</span></span>  <br/> |
|<span data-ttu-id="07b11-115">**SearchScope**</span><span class="sxs-lookup"><span data-stu-id="07b11-115">**SearchScope**</span></span> <br/> |<span data-ttu-id="07b11-116">标识的顺序和 ResolveNames 搜索范围。</span><span class="sxs-lookup"><span data-stu-id="07b11-116">Identifies the order and scope for a ResolveNames search.</span></span>  <br/> |
|<span data-ttu-id="07b11-117">ContactDataShape</span><span class="sxs-lookup"><span data-stu-id="07b11-117">ContactDataShape</span></span>  <br/> |<span data-ttu-id="07b11-118">标识设置联系人返回的属性。</span><span class="sxs-lookup"><span data-stu-id="07b11-118">Identifies the property set returned for contacts.</span></span> <span data-ttu-id="07b11-119">此属性是在 Exchange Server 2010 Service Pack 2 (SP2) 中引入的。</span><span class="sxs-lookup"><span data-stu-id="07b11-119">This attribute was introduced in Exchange Server 2010 Service Pack 2 (SP2).</span></span>  <br/> |
   
#### <a name="returnfullcontactdata-attribute-values"></a><span data-ttu-id="07b11-120">ReturnFullContactData 属性值</span><span class="sxs-lookup"><span data-stu-id="07b11-120">ReturnFullContactData attribute values</span></span>

|<span data-ttu-id="07b11-121">**值**</span><span class="sxs-lookup"><span data-stu-id="07b11-121">**Value**</span></span>|<span data-ttu-id="07b11-122">**说明**</span><span class="sxs-lookup"><span data-stu-id="07b11-122">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07b11-123">True</span><span class="sxs-lookup"><span data-stu-id="07b11-123">True</span></span>  <br/> |<span data-ttu-id="07b11-124">返回公共联系人的完整联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="07b11-124">Full contact details for public contacts are returned.</span></span>  <br/> |
|<span data-ttu-id="07b11-125">False</span><span class="sxs-lookup"><span data-stu-id="07b11-125">False</span></span>  <br/> |<span data-ttu-id="07b11-126">不返回公共联系人的完整联系人详细信息。</span><span class="sxs-lookup"><span data-stu-id="07b11-126">Full contact details for public contacts are not returned.</span></span>  <br/> |
   
#### <a name="searchscope-attribute-values"></a><span data-ttu-id="07b11-127">SearchScope 属性值</span><span class="sxs-lookup"><span data-stu-id="07b11-127">SearchScope attribute values</span></span>

|<span data-ttu-id="07b11-128">**值**</span><span class="sxs-lookup"><span data-stu-id="07b11-128">**Value**</span></span>|<span data-ttu-id="07b11-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="07b11-129">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07b11-130">与 active Directory</span><span class="sxs-lookup"><span data-stu-id="07b11-130">ActiveDirectory</span></span>  <br/> |<span data-ttu-id="07b11-131">搜索仅 Active Directory 目录服务。</span><span class="sxs-lookup"><span data-stu-id="07b11-131">Only the Active Directory directory service is searched.</span></span>  <br/> |
|<span data-ttu-id="07b11-132">ActiveDirectoryContacts</span><span class="sxs-lookup"><span data-stu-id="07b11-132">ActiveDirectoryContacts</span></span>  <br/> |<span data-ttu-id="07b11-133">首先，搜索 active Directory，然后搜索[ParentFolderIds](parentfolderids.md)属性中指定的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="07b11-133">Active Directory is searched first, and then the contact folders that are specified in the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="07b11-134">联系人</span><span class="sxs-lookup"><span data-stu-id="07b11-134">Contacts</span></span>  <br/> |<span data-ttu-id="07b11-135">仅由[ParentFolderIds](parentfolderids.md)属性标识的联系人的文件夹中搜索。</span><span class="sxs-lookup"><span data-stu-id="07b11-135">Only the contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched.</span></span>  <br/> |
|<span data-ttu-id="07b11-136">ContactsActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="07b11-136">ContactsActiveDirectory</span></span>  <br/> |<span data-ttu-id="07b11-137">先搜索联系人由[ParentFolderIds](parentfolderids.md)属性标识的文件夹，然后搜索 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="07b11-137">Contact folders that are identified by the [ParentFolderIds](parentfolderids.md) property are searched first and then Active Directory is searched.</span></span>  <br/> |
   
#### <a name="contactdatashape-attribute-values"></a><span data-ttu-id="07b11-138">ContactDataShape 属性值</span><span class="sxs-lookup"><span data-stu-id="07b11-138">ContactDataShape attribute values</span></span>

|<span data-ttu-id="07b11-139">**值**</span><span class="sxs-lookup"><span data-stu-id="07b11-139">**Value**</span></span>|<span data-ttu-id="07b11-140">**说明**</span><span class="sxs-lookup"><span data-stu-id="07b11-140">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07b11-141">IdOnly</span><span class="sxs-lookup"><span data-stu-id="07b11-141">IdOnly</span></span>  <br/> |<span data-ttu-id="07b11-142">联系人项目标识符属性返回。</span><span class="sxs-lookup"><span data-stu-id="07b11-142">The contact item identifier property is returned.</span></span>  <br/> |
|<span data-ttu-id="07b11-143">默认</span><span class="sxs-lookup"><span data-stu-id="07b11-143">Default</span></span>  <br/> |<span data-ttu-id="07b11-144">返回默认的联系人项属性集。</span><span class="sxs-lookup"><span data-stu-id="07b11-144">The Default set of contact item properties is returned.</span></span> <span data-ttu-id="07b11-145">有关详细信息，请参阅[响应形状中的 ews](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="07b11-145">For more information, see [Response shapes in EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="07b11-146">AllProperties</span><span class="sxs-lookup"><span data-stu-id="07b11-146">AllProperties</span></span>  <br/> |<span data-ttu-id="07b11-147">返回了 AllProperties 一组联系人项目属性。</span><span class="sxs-lookup"><span data-stu-id="07b11-147">The AllProperties set of contact item properties are returned.</span></span> <span data-ttu-id="07b11-148">有关详细信息，请参阅[响应形状中的 ews](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="07b11-148">For more information, see [Response shapes in EWS](http://msdn.microsoft.com/library/1c5ddc0a-c4e0-4488-8972-7543b5b464df%28Office.15%29.aspx).</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="07b11-149">子元素</span><span class="sxs-lookup"><span data-stu-id="07b11-149">Child elements</span></span>

|<span data-ttu-id="07b11-150">**元素**</span><span class="sxs-lookup"><span data-stu-id="07b11-150">**Element**</span></span>|<span data-ttu-id="07b11-151">**说明**</span><span class="sxs-lookup"><span data-stu-id="07b11-151">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07b11-152">ParentFolderIds</span><span class="sxs-lookup"><span data-stu-id="07b11-152">ParentFolderIds</span></span>](parentfolderids.md) <br/> |<span data-ttu-id="07b11-153">包含**SearchScope**属性设置为 ActiveDirectoryContacts、 联系人或 ContactsActiveDirectory 将搜索的联系人文件夹标识符的数组。</span><span class="sxs-lookup"><span data-stu-id="07b11-153">Contains an array of contact folder identifiers that would be searched if the **SearchScope** attribute is set to ActiveDirectoryContacts, Contacts, or ContactsActiveDirectory.</span></span> <span data-ttu-id="07b11-154">ParentFolderIds 数组只能包含单个联系人文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="07b11-154">The ParentFolderIds array can only contain a single contact folder identifier.</span></span> <span data-ttu-id="07b11-155">如果**ParentFolderIds**元素不存在，则搜索默认联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="07b11-155">If the **ParentFolderIds** element is not present, the default Contacts folder is searched.</span></span>  <br/> <span data-ttu-id="07b11-156">文件夹标识符可用于代理访问。</span><span class="sxs-lookup"><span data-stu-id="07b11-156">The folder identifier can be used for delegate access.</span></span>  <br/> <span data-ttu-id="07b11-157">使用访问控制列表 (Acl) 执行 active Directory 搜索。</span><span class="sxs-lookup"><span data-stu-id="07b11-157">Active Directory searches are performed by using access control lists (ACLs).</span></span> <span data-ttu-id="07b11-158">某些用户可能没有看到某些 Active Directory 对象的权限。</span><span class="sxs-lookup"><span data-stu-id="07b11-158">Some users might not have the rights to see some Active Directory objects.</span></span>  <br/> <span data-ttu-id="07b11-159">此元素是可选的。</span><span class="sxs-lookup"><span data-stu-id="07b11-159">This element is optional.</span></span>  <br/> |
|[<span data-ttu-id="07b11-160">UnresolvedEntry</span><span class="sxs-lookup"><span data-stu-id="07b11-160">UnresolvedEntry</span></span>](unresolvedentry.md) <br/> |<span data-ttu-id="07b11-161">包含要解析的联系人或通讯组列表的名称。</span><span class="sxs-lookup"><span data-stu-id="07b11-161">Contains the name of a contact or distribution list to resolve.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07b11-162">父元素</span><span class="sxs-lookup"><span data-stu-id="07b11-162">Parent elements</span></span>

<span data-ttu-id="07b11-163">无。</span><span class="sxs-lookup"><span data-stu-id="07b11-163">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="07b11-164">备注</span><span class="sxs-lookup"><span data-stu-id="07b11-164">Remarks</span></span>

<span data-ttu-id="07b11-165">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="07b11-165">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07b11-166">元素信息</span><span class="sxs-lookup"><span data-stu-id="07b11-166">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07b11-167">命名空间</span><span class="sxs-lookup"><span data-stu-id="07b11-167">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="07b11-168">架构名称</span><span class="sxs-lookup"><span data-stu-id="07b11-168">Schema name</span></span>  <br/> |<span data-ttu-id="07b11-169">消息架构</span><span class="sxs-lookup"><span data-stu-id="07b11-169">Messages schema</span></span>  <br/> |
|<span data-ttu-id="07b11-170">验证文件</span><span class="sxs-lookup"><span data-stu-id="07b11-170">Validation file</span></span>  <br/> |<span data-ttu-id="07b11-171">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="07b11-171">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="07b11-172">可以为空</span><span class="sxs-lookup"><span data-stu-id="07b11-172">Can be empty</span></span>  <br/> |<span data-ttu-id="07b11-173">False</span><span class="sxs-lookup"><span data-stu-id="07b11-173">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07b11-174">另请参阅</span><span class="sxs-lookup"><span data-stu-id="07b11-174">See also</span></span>



[<span data-ttu-id="07b11-175">ResolveNames 操作</span><span class="sxs-lookup"><span data-stu-id="07b11-175">ResolveNames operation</span></span>](resolvenames-operation.md)
  
[<span data-ttu-id="07b11-176">ResolveNamesType</span><span class="sxs-lookup"><span data-stu-id="07b11-176">ResolveNamesType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesType.aspx)
  
[<span data-ttu-id="07b11-177">ResolveNamesSearchScopeType</span><span class="sxs-lookup"><span data-stu-id="07b11-177">ResolveNamesSearchScopeType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.ResolveNamesSearchScopeType.aspx)


- [<span data-ttu-id="07b11-178">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="07b11-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="07b11-179">使用名称解析</span><span class="sxs-lookup"><span data-stu-id="07b11-179">Using Name Resolution</span></span>](http://msdn.microsoft.com/library/9257fb07-89d2-46eb-b885-e2173fe6fbc1%28Office.15%29.aspx)

