---
title: GetUserRetentionPolicyTags 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57c6ff23-5c2c-42ee-824b-5a1b6dafab8c
description: 查找信息 GetUserRetentionPolicyTags EWS 操作。
ms.openlocfilehash: 2b1267ce6822c7bad05ad2ef88547ba75c632ab0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825700"
---
# <a name="getuserretentionpolicytags-operation"></a><span data-ttu-id="cb755-103">GetUserRetentionPolicyTags 操作</span><span class="sxs-lookup"><span data-stu-id="cb755-103">GetUserRetentionPolicyTags operation</span></span>

<span data-ttu-id="cb755-104">查找有关**GetUserRetentionPolicyTags** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="cb755-104">Find information about the **GetUserRetentionPolicyTags** EWS operation.</span></span> 
  
<span data-ttu-id="cb755-105">**GetUserRetentionPolicyTags**操作获取所有默认、 系统文件夹和与用户通过系统策略关联或已由用户应用个人标记的列表。</span><span class="sxs-lookup"><span data-stu-id="cb755-105">The **GetUserRetentionPolicyTags** operation gets a list of all default, system folder, and personal tags that are associated with a user by means of a system policy or that were applied by the user.</span></span> 
  
<span data-ttu-id="cb755-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="cb755-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getuserretentionpolicytags-operation"></a><span data-ttu-id="cb755-107">使用 GetUserRetentionPolicyTags 操作</span><span class="sxs-lookup"><span data-stu-id="cb755-107">Using the GetUserRetentionPolicyTags operation</span></span>

<span data-ttu-id="cb755-108">此操作返回的显示名称、 保留 ID、 保留期、 保留类型、 保留操作和说明标记和**IsVisible**、 **OptedInto**和**IsArchive**属性的值。</span><span class="sxs-lookup"><span data-stu-id="cb755-108">This operation returns the display name, retention ID, retention period, retention type, retention action, and description tags, and the values for the **IsVisible**, **OptedInto**, and **IsArchive** properties.</span></span> 
  
### <a name="getuserretentionpolicytags-operation-soap-headers"></a><span data-ttu-id="cb755-109">GetUserRetentionPolicyTags 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="cb755-109">GetUserRetentionPolicyTags operation SOAP headers</span></span>

<span data-ttu-id="cb755-110">**GetUserRetentionPolicyTags**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="cb755-110">The **GetUserRetentionPolicyTags** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="cb755-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="cb755-111">**Header name**</span></span>|<span data-ttu-id="cb755-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb755-112">**Element**</span></span>|<span data-ttu-id="cb755-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb755-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cb755-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="cb755-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="cb755-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="cb755-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="cb755-116">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="cb755-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="cb755-117">这是适用于请求。</span><span class="sxs-lookup"><span data-stu-id="cb755-117">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="cb755-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="cb755-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="cb755-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cb755-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="cb755-120">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="cb755-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="cb755-121">这是适用于响应。</span><span class="sxs-lookup"><span data-stu-id="cb755-121">This is applicable to a response.</span></span>  <br/> |
   
## <a name="getuserretentionpolicytags-operation-request-example"></a><span data-ttu-id="cb755-122">GetUserRetentionPolicyTags 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="cb755-122">GetUserRetentionPolicyTags operation request example</span></span>

<span data-ttu-id="cb755-123">**GetUserRetentionPolicyTags**操作请求的下面的示例演示如何获取当前用户标记的列表。</span><span class="sxs-lookup"><span data-stu-id="cb755-123">The following example of a **GetUserRetentionPolicyTags** operation request shows how to get a list of tags for the current user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:GetUserRetentionPolicyTags />
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="cb755-124">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="cb755-124">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="cb755-125">GetUserRetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="cb755-125">GetUserRetentionPolicyTags</span></span>](getuserretentionpolicytags.md)
    
## <a name="successful-getuserretentionpolicytags-operation-response"></a><span data-ttu-id="cb755-126">成功 GetUserRetentionPolicyTags 操作响应</span><span class="sxs-lookup"><span data-stu-id="cb755-126">Successful GetUserRetentionPolicyTags operation response</span></span>

<span data-ttu-id="cb755-127">下面的示例演示对**GetUserRetentionPolicyTags**操作请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="cb755-127">The following example shows a successful response to a **GetUserRetentionPolicyTags** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="179" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserRetentionPolicyTagsResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <RetentionPolicyTags>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>1 Year Delete</DisplayName>
               <RetentionId>e66252f9-794f-4b36-b55e-d6d95fdf87a3</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>Personal</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description/>
               <IsVisible>true</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Personal 1 year move to archive</DisplayName>
               <RetentionId>b2a29464-649c-4174-932b-6aaac9811c89</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>Personal</Type>
               <RetentionAction>MoveToArchive</RetentionAction>
               <Description/>
               <IsVisible>true</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>true</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Sent Items</DisplayName>
               <RetentionId>b0d32f1b-fbd0-4c1d-ba3e-ddd1086ea1d3</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>SentItems</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description/>
               <IsVisible>false</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Default 1 year delete</DisplayName>
               <RetentionId>29fc9b9d-98b0-4c01-acf8-3996e2afce98</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>All</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description/>
               <IsVisible>false</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Two Year Retention</DisplayName>
               <RetentionId>a1a38957-2557-404e-9f32-53d77c948f62</RetentionId>
               <RetentionPeriod>730</RetentionPeriod>
               <Type>Personal</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description>Use this tag for all items to be retained for two years.</Description>
               <IsVisible>true</IsVisible>
               <OptedInto>true</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Default two year move to archive</DisplayName>
               <RetentionId>75bc8dbe-a0e8-4e09-9fa3-fd4c21f49318</RetentionId>
               <RetentionPeriod>730</RetentionPeriod>
               <Type>All</Type>
               <RetentionAction>MoveToArchive</RetentionAction>
               <Description/>
               <IsVisible>false</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>true</IsArchive>
            </RetentionPolicyTag>
         </RetentionPolicyTags>
      </GetUserRetentionPolicyTagsResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="cb755-128">响应 SOAP 正文中包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="cb755-128">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="cb755-129">GetUserRetentionPolicyTagsResponse</span><span class="sxs-lookup"><span data-stu-id="cb755-129">GetUserRetentionPolicyTagsResponse</span></span>](getuserretentionpolicytagsresponse.md)
    
- [<span data-ttu-id="cb755-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="cb755-130">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="cb755-131">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="cb755-131">RetentionPolicyTags</span></span>](retentionpolicytags.md)
    
- [<span data-ttu-id="cb755-132">RetentionPolicyTag</span><span class="sxs-lookup"><span data-stu-id="cb755-132">RetentionPolicyTag</span></span>](retentionpolicytag.md)
    
- [<span data-ttu-id="cb755-133">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="cb755-133">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="cb755-134">RetentionId</span><span class="sxs-lookup"><span data-stu-id="cb755-134">RetentionId</span></span>](retentionid.md)
    
- [<span data-ttu-id="cb755-135">RetentionPeriod</span><span class="sxs-lookup"><span data-stu-id="cb755-135">RetentionPeriod</span></span>](retentionperiod.md)
    
- [<span data-ttu-id="cb755-136">类型 (ElcFolderType)</span><span class="sxs-lookup"><span data-stu-id="cb755-136">Type (ElcFolderType)</span></span>](type-elcfoldertype.md)
    
- [<span data-ttu-id="cb755-137">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="cb755-137">RetentionAction</span></span>](retentionaction.md)
    
- [<span data-ttu-id="cb755-138">说明</span><span class="sxs-lookup"><span data-stu-id="cb755-138">Description</span></span>](description.md)
    
- [<span data-ttu-id="cb755-139">IsVisible</span><span class="sxs-lookup"><span data-stu-id="cb755-139">IsVisible</span></span>](isvisible.md)
    
- [<span data-ttu-id="cb755-140">OptedInto</span><span class="sxs-lookup"><span data-stu-id="cb755-140">OptedInto</span></span>](optedinto.md)
    
- [<span data-ttu-id="cb755-141">IsArchive</span><span class="sxs-lookup"><span data-stu-id="cb755-141">IsArchive</span></span>](isarchive.md)
    
## <a name="getuserretentionpolicytags-operation-error-response"></a><span data-ttu-id="cb755-142">GetUserRetentionPolicyTags 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="cb755-142">GetUserRetentionPolicyTags operation error response</span></span>

<span data-ttu-id="cb755-143">是通用的 EWS 的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="cb755-143">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb755-144">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb755-144">See also</span></span>



[<span data-ttu-id="cb755-145">EWS 中的保留策略</span><span class="sxs-lookup"><span data-stu-id="cb755-145">Retention policies in EWS</span></span>](http://msdn.microsoft.com/library/a132872f-0228-4bcb-aac2-bf64fb07e58e%28Office.15%29.aspx)

