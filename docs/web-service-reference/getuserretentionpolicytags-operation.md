---
title: GetUserRetentionPolicyTags 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57c6ff23-5c2c-42ee-824b-5a1b6dafab8c
description: 查找有关 GetUserRetentionPolicyTags EWS 操作的信息。
ms.openlocfilehash: 6505945f8ad110af714da1a3011c2d504acdc75f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530830"
---
# <a name="getuserretentionpolicytags-operation"></a><span data-ttu-id="9cfb8-103">GetUserRetentionPolicyTags 操作</span><span class="sxs-lookup"><span data-stu-id="9cfb8-103">GetUserRetentionPolicyTags operation</span></span>

<span data-ttu-id="9cfb8-104">查找有关**GetUserRetentionPolicyTags** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-104">Find information about the **GetUserRetentionPolicyTags** EWS operation.</span></span> 
  
<span data-ttu-id="9cfb8-105">**GetUserRetentionPolicyTags**操作通过系统策略获取与用户关联的所有默认、系统文件夹和个人标记的列表，或由用户应用的个人标记。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-105">The **GetUserRetentionPolicyTags** operation gets a list of all default, system folder, and personal tags that are associated with a user by means of a system policy or that were applied by the user.</span></span> 
  
<span data-ttu-id="9cfb8-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getuserretentionpolicytags-operation"></a><span data-ttu-id="9cfb8-107">使用 GetUserRetentionPolicyTags 操作</span><span class="sxs-lookup"><span data-stu-id="9cfb8-107">Using the GetUserRetentionPolicyTags operation</span></span>

<span data-ttu-id="9cfb8-108">此操作返回显示名称、保留 ID、保留期、保留类型、保留操作和说明标记，以及**IsVisible**、 **OptedInto**和**IsArchive**属性的值。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-108">This operation returns the display name, retention ID, retention period, retention type, retention action, and description tags, and the values for the **IsVisible**, **OptedInto**, and **IsArchive** properties.</span></span> 
  
### <a name="getuserretentionpolicytags-operation-soap-headers"></a><span data-ttu-id="9cfb8-109">GetUserRetentionPolicyTags 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="9cfb8-109">GetUserRetentionPolicyTags operation SOAP headers</span></span>

<span data-ttu-id="9cfb8-110">**GetUserRetentionPolicyTags**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-110">The **GetUserRetentionPolicyTags** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="9cfb8-111">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="9cfb8-111">**Header name**</span></span>|<span data-ttu-id="9cfb8-112">**元素**</span><span class="sxs-lookup"><span data-stu-id="9cfb8-112">**Element**</span></span>|<span data-ttu-id="9cfb8-113">**说明**</span><span class="sxs-lookup"><span data-stu-id="9cfb8-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9cfb8-114">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="9cfb8-114">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="9cfb8-115">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="9cfb8-115">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="9cfb8-116">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-116">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="9cfb8-117">这适用于请求。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-117">This is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="9cfb8-118">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="9cfb8-118">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="9cfb8-119">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="9cfb8-119">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="9cfb8-120">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-120">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="9cfb8-121">这适用于响应。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-121">This is applicable to a response.</span></span>  <br/> |
   
## <a name="getuserretentionpolicytags-operation-request-example"></a><span data-ttu-id="9cfb8-122">GetUserRetentionPolicyTags 操作请求示例</span><span class="sxs-lookup"><span data-stu-id="9cfb8-122">GetUserRetentionPolicyTags operation request example</span></span>

<span data-ttu-id="9cfb8-123">以下示例的**GetUserRetentionPolicyTags**操作请求显示如何获取当前用户的标记列表。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-123">The following example of a **GetUserRetentionPolicyTags** operation request shows how to get a list of tags for the current user.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:GetUserRetentionPolicyTags />
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="9cfb8-124">请求 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9cfb8-124">The request SOAP body contains the following element:</span></span>
  
- [<span data-ttu-id="9cfb8-125">GetUserRetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="9cfb8-125">GetUserRetentionPolicyTags</span></span>](getuserretentionpolicytags.md)
    
## <a name="successful-getuserretentionpolicytags-operation-response"></a><span data-ttu-id="9cfb8-126">成功的 GetUserRetentionPolicyTags 操作响应</span><span class="sxs-lookup"><span data-stu-id="9cfb8-126">Successful GetUserRetentionPolicyTags operation response</span></span>

<span data-ttu-id="9cfb8-127">下面的示例演示对**GetUserRetentionPolicyTags**操作请求的成功响应。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-127">The following example shows a successful response to a **GetUserRetentionPolicyTags** operation request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="179" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserRetentionPolicyTagsResponse ResponseClass="Success" 
                                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <RetentionPolicyTags>
            <RetentionPolicyTag xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
            <RetentionPolicyTag xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
            <RetentionPolicyTag xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
            <RetentionPolicyTag xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
            <RetentionPolicyTag xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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
            <RetentionPolicyTag xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="9cfb8-128">响应 SOAP 正文包含以下元素：</span><span class="sxs-lookup"><span data-stu-id="9cfb8-128">The response SOAP body contains the following elements:</span></span>
  
- [<span data-ttu-id="9cfb8-129">GetUserRetentionPolicyTagsResponse</span><span class="sxs-lookup"><span data-stu-id="9cfb8-129">GetUserRetentionPolicyTagsResponse</span></span>](getuserretentionpolicytagsresponse.md)
    
- [<span data-ttu-id="9cfb8-130">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="9cfb8-130">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="9cfb8-131">RetentionPolicyTags</span><span class="sxs-lookup"><span data-stu-id="9cfb8-131">RetentionPolicyTags</span></span>](retentionpolicytags.md)
    
- [<span data-ttu-id="9cfb8-132">Get-retentionpolicytag</span><span class="sxs-lookup"><span data-stu-id="9cfb8-132">RetentionPolicyTag</span></span>](retentionpolicytag.md)
    
- [<span data-ttu-id="9cfb8-133">显示名称 (字符串)</span><span class="sxs-lookup"><span data-stu-id="9cfb8-133">DisplayName (string)</span></span>](displayname-string.md)
    
- [<span data-ttu-id="9cfb8-134">RetentionId</span><span class="sxs-lookup"><span data-stu-id="9cfb8-134">RetentionId</span></span>](retentionid.md)
    
- [<span data-ttu-id="9cfb8-135">RetentionPeriod</span><span class="sxs-lookup"><span data-stu-id="9cfb8-135">RetentionPeriod</span></span>](retentionperiod.md)
    
- [<span data-ttu-id="9cfb8-136">类型（ElcFolderType）</span><span class="sxs-lookup"><span data-stu-id="9cfb8-136">Type (ElcFolderType)</span></span>](type-elcfoldertype.md)
    
- [<span data-ttu-id="9cfb8-137">RetentionAction</span><span class="sxs-lookup"><span data-stu-id="9cfb8-137">RetentionAction</span></span>](retentionaction.md)
    
- [<span data-ttu-id="9cfb8-138">说明</span><span class="sxs-lookup"><span data-stu-id="9cfb8-138">Description</span></span>](description.md)
    
- [<span data-ttu-id="9cfb8-139">IsVisible</span><span class="sxs-lookup"><span data-stu-id="9cfb8-139">IsVisible</span></span>](isvisible.md)
    
- [<span data-ttu-id="9cfb8-140">OptedInto</span><span class="sxs-lookup"><span data-stu-id="9cfb8-140">OptedInto</span></span>](optedinto.md)
    
- [<span data-ttu-id="9cfb8-141">IsArchive</span><span class="sxs-lookup"><span data-stu-id="9cfb8-141">IsArchive</span></span>](isarchive.md)
    
## <a name="getuserretentionpolicytags-operation-error-response"></a><span data-ttu-id="9cfb8-142">GetUserRetentionPolicyTags 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="9cfb8-142">GetUserRetentionPolicyTags operation error response</span></span>

<span data-ttu-id="9cfb8-143">有关对 EWS 通用的错误代码，请参阅[ResponseCode](responsecode.md)。</span><span class="sxs-lookup"><span data-stu-id="9cfb8-143">For error codes that are generic to EWS, see [ResponseCode](responsecode.md).</span></span>
  
