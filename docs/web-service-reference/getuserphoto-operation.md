---
title: GetUserPhoto 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: 查找有关 GetUserPhoto EWS 操作的信息。
ms.openlocfilehash: 6769842d31519f0aac2cf9bda10c1cab70558301
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461812"
---
# <a name="getuserphoto-operation"></a><span data-ttu-id="04b94-103">GetUserPhoto 操作</span><span class="sxs-lookup"><span data-stu-id="04b94-103">GetUserPhoto operation</span></span>

<span data-ttu-id="04b94-104">查找有关**GetUserPhoto** EWS 操作的信息。</span><span class="sxs-lookup"><span data-stu-id="04b94-104">Find information about the **GetUserPhoto** EWS operation.</span></span> 
  
<span data-ttu-id="04b94-105">**GetUserPhoto**操作从 Active Directory 域服务（AD DS）中获取用户照片。</span><span class="sxs-lookup"><span data-stu-id="04b94-105">The **GetUserPhoto** operation gets a user photo from Active Directory Domain Services (AD DS).</span></span> 
  
<span data-ttu-id="04b94-106">Exchange Server 2013 中引入了此操作。</span><span class="sxs-lookup"><span data-stu-id="04b94-106">This operation was introduced in Exchange Server 2013.</span></span>
  
## <a name="using-the-getuserphoto-operation"></a><span data-ttu-id="04b94-107">使用 GetUserPhoto 操作</span><span class="sxs-lookup"><span data-stu-id="04b94-107">Using the GetUserPhoto operation</span></span>

<span data-ttu-id="04b94-108">**RemoveContactFromImList**操作是一个简单的操作，它接受用户的电子邮件地址和请求的照片大小，并在响应中返回照片流。</span><span class="sxs-lookup"><span data-stu-id="04b94-108">The **RemoveContactFromImList** operation is a simple operation that accepts a user's email address and the requested photo size and returns the photo stream in the response.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="04b94-109">EWS 同时具有 SOAP 和基于 REST 的操作来获取用户照片。</span><span class="sxs-lookup"><span data-stu-id="04b94-109">EWS has both a SOAP and a REST-based operation to get user photos.</span></span> <span data-ttu-id="04b94-110">有关 REST 接口的信息，请参阅[使用 Exchange 中的 EWS 获取用户照片](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="04b94-110">For information about the REST interface, see [Get user photos by using EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx).</span></span> 
  
### <a name="getuserphoto-operation-soap-headers"></a><span data-ttu-id="04b94-111">GetUserPhoto 操作 SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="04b94-111">GetUserPhoto operation SOAP headers</span></span>

<span data-ttu-id="04b94-112">**GetUserPhoto**操作可以使用下表中列出的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="04b94-112">The **GetUserPhoto** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="04b94-113">**标头名称**</span><span class="sxs-lookup"><span data-stu-id="04b94-113">**Header name**</span></span>|<span data-ttu-id="04b94-114">**元素**</span><span class="sxs-lookup"><span data-stu-id="04b94-114">**Element**</span></span>|<span data-ttu-id="04b94-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="04b94-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="04b94-116">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="04b94-116">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="04b94-117">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="04b94-117">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="04b94-118">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="04b94-118">Identifies the schema version for the operation request.</span></span> <span data-ttu-id="04b94-119">此标头适用于请求。</span><span class="sxs-lookup"><span data-stu-id="04b94-119">This header is applicable to a request.</span></span>  <br/> |
|<span data-ttu-id="04b94-120">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="04b94-120">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="04b94-121">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="04b94-121">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="04b94-122">标识响应请求的服务器版本。</span><span class="sxs-lookup"><span data-stu-id="04b94-122">Identifies the version of the server that responded to the request.</span></span> <span data-ttu-id="04b94-123">此标头适用于响应。</span><span class="sxs-lookup"><span data-stu-id="04b94-123">This header is applicable to a response.</span></span>  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a><span data-ttu-id="04b94-124">GetUserPhoto 操作请求示例：获取用户照片</span><span class="sxs-lookup"><span data-stu-id="04b94-124">GetUserPhoto operation request example: Get a user's photo</span></span>

<span data-ttu-id="04b94-125">以下示例的**GetUserPhoto**操作请求显示如何获取用户的照片。</span><span class="sxs-lookup"><span data-stu-id="04b94-125">The following example of a **GetUserPhoto** operation request shows how to get a user's photo.</span></span> <span data-ttu-id="04b94-126">此示例请求48x48 像素的用户照片。</span><span class="sxs-lookup"><span data-stu-id="04b94-126">This example requests a user photo that is 48x48 pixels.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>user1@contoso.com</m:Email>
         <m:SizeRequested>HR48x48</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="04b94-127">请求 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="04b94-127">The following elements are used in the request SOAP body:</span></span>
  
- [<span data-ttu-id="04b94-128">GetUserPhoto</span><span class="sxs-lookup"><span data-stu-id="04b94-128">GetUserPhoto</span></span>](getuserphoto.md)
    
- [<span data-ttu-id="04b94-129">Email （String）</span><span class="sxs-lookup"><span data-stu-id="04b94-129">Email (String)</span></span>](email-string.md)
    
- [<span data-ttu-id="04b94-130">SizeRequested</span><span class="sxs-lookup"><span data-stu-id="04b94-130">SizeRequested</span></span>](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a><span data-ttu-id="04b94-131">成功的 GetUserPhoto 操作响应</span><span class="sxs-lookup"><span data-stu-id="04b94-131">Successful GetUserPhoto operation response</span></span>

<span data-ttu-id="04b94-132">下面的示例演示对**GetUserPhoto**操作的成功响应，以获取用户的照片。</span><span class="sxs-lookup"><span data-stu-id="04b94-132">The following example shows a successful response to a **GetUserPhoto** operation to get a user's photo.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

<span data-ttu-id="04b94-133">响应 SOAP 正文中使用以下元素：</span><span class="sxs-lookup"><span data-stu-id="04b94-133">The following elements are used in the response SOAP body:</span></span>
  
- [<span data-ttu-id="04b94-134">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="04b94-134">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
- [<span data-ttu-id="04b94-135">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="04b94-135">ResponseCode</span></span>](responsecode.md)
    
- [<span data-ttu-id="04b94-136">HasChanged</span><span class="sxs-lookup"><span data-stu-id="04b94-136">HasChanged</span></span>](haschanged.md)
    
- [<span data-ttu-id="04b94-137">GetUserPhotoResponse</span><span class="sxs-lookup"><span data-stu-id="04b94-137">GetUserPhotoResponse</span></span>](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a><span data-ttu-id="04b94-138">GetUserPhoto 操作错误响应</span><span class="sxs-lookup"><span data-stu-id="04b94-138">GetUserPhoto operation error response</span></span>

<span data-ttu-id="04b94-139">如果尝试获取组织中不存在的电子邮件地址的用户照片，则 SOAP 信封不会返回错误代码。</span><span class="sxs-lookup"><span data-stu-id="04b94-139">The SOAP envelope will not return an error code if an attempt is made to get a user photo for an email address that doesn't exist in the organization.</span></span> <span data-ttu-id="04b94-140">将在响应中返回一个 500 HTTP 状态代码，以指示请求未成功。</span><span class="sxs-lookup"><span data-stu-id="04b94-140">A 500 HTTP status code will be returned in the response to indicate that the request was unsuccessful.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04b94-141">另请参阅</span><span class="sxs-lookup"><span data-stu-id="04b94-141">See also</span></span>

- [<span data-ttu-id="04b94-142">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="04b94-142">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)   
- [<span data-ttu-id="04b94-143">使用 Exchange 中的 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="04b94-143">Get user photos by using EWS in Exchange</span></span>](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

