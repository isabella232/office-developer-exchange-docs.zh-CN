---
title: GetSharingFolder 操作
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
ms.assetid: 75fee92a-a7f8-4a62-ad2b-17acbaada186
description: GetSharingFolder 操作获取指定的共享文件夹的本地文件夹标识符。
ms.openlocfilehash: 23adb10b22623fcbc1dd6b33bd674afafdaa8b19
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825670"
---
# <a name="getsharingfolder-operation"></a><span data-ttu-id="4cda9-103">GetSharingFolder 操作</span><span class="sxs-lookup"><span data-stu-id="4cda9-103">GetSharingFolder operation</span></span>

<span data-ttu-id="4cda9-104">**GetSharingFolder**操作获取指定的共享文件夹的本地文件夹标识符。</span><span class="sxs-lookup"><span data-stu-id="4cda9-104">The **GetSharingFolder** operation gets the local folder identifier of a specified shared folder.</span></span> 
  
## <a name="soap-headers"></a><span data-ttu-id="4cda9-105">SOAP 标头</span><span class="sxs-lookup"><span data-stu-id="4cda9-105">SOAP Headers</span></span>

<span data-ttu-id="4cda9-106">**GetSharingFolder**操作可以使用列出并在下表中所述的 SOAP 标头。</span><span class="sxs-lookup"><span data-stu-id="4cda9-106">The **GetSharingFolder** operation can use the SOAP headers that are listed and described in the following table.</span></span> 
  
|<span data-ttu-id="4cda9-107">**Header**</span><span class="sxs-lookup"><span data-stu-id="4cda9-107">**Header**</span></span>|<span data-ttu-id="4cda9-108">**元素**</span><span class="sxs-lookup"><span data-stu-id="4cda9-108">**Element**</span></span>|<span data-ttu-id="4cda9-109">**说明**</span><span class="sxs-lookup"><span data-stu-id="4cda9-109">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4cda9-110">RequestVersion</span><span class="sxs-lookup"><span data-stu-id="4cda9-110">RequestVersion</span></span>  <br/> |[<span data-ttu-id="4cda9-111">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="4cda9-111">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="4cda9-112">标识操作请求的架构版本。</span><span class="sxs-lookup"><span data-stu-id="4cda9-112">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="4cda9-113">ServerVersion</span><span class="sxs-lookup"><span data-stu-id="4cda9-113">ServerVersion</span></span>  <br/> |[<span data-ttu-id="4cda9-114">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="4cda9-114">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="4cda9-115">标识响应该请求的服务器的版本。</span><span class="sxs-lookup"><span data-stu-id="4cda9-115">Identifies the version of the server that responded to the request.</span></span>  <br/> |
   
## <a name="getsharingfolder-request-example"></a><span data-ttu-id="4cda9-116">GetSharingFolder 请求示例</span><span class="sxs-lookup"><span data-stu-id="4cda9-116">GetSharingFolder request example</span></span>

### <a name="getting-the-local-folder-identifier-by-specifying-the-sharedfolderid-element-of-the-folder-being-shared"></a><span data-ttu-id="4cda9-117">通过指定 SharedFolderId 元素的共享文件夹中获取的本地文件夹标识符</span><span class="sxs-lookup"><span data-stu-id="4cda9-117">Getting the Local Folder Identifier by Specifying the SharedFolderId Element of the Folder Being Shared</span></span>

<span data-ttu-id="4cda9-118">下面的代码示例演示如何以形成一个请求以获取正在共享的文件夹的相对应的本地文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="4cda9-118">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="4cda9-119">通过包含的共享文件夹的邮箱的 SMTP 地址和[SharedFolderId](sharedfolderid.md)元素表示该文件夹的标识符标识的共享文件夹。</span><span class="sxs-lookup"><span data-stu-id="4cda9-119">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [SharedFolderId](sharedfolderid.md) element that represents the identifier of that folder.</span></span> <span data-ttu-id="4cda9-120">本示例中，由 user1@contoso.com 拥有的共享文件夹。</span><span class="sxs-lookup"><span data-stu-id="4cda9-120">In this example, the folder that is being shared is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4cda9-121">代码</span><span class="sxs-lookup"><span data-stu-id="4cda9-121">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:SharedFolderId>AAMkA=</m:SharedFolderId>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="getting-the-local-folder-identifier-by-specifying-the-datatype-element-of-the-folder-being-shared"></a><span data-ttu-id="4cda9-122">通过指定数据类型元素的共享文件夹中获取的本地文件夹标识符</span><span class="sxs-lookup"><span data-stu-id="4cda9-122">Getting the Local Folder Identifier by Specifying the DataType Element of the Folder Being Shared</span></span>

<span data-ttu-id="4cda9-123">下面的代码示例演示如何以形成一个请求以获取正在共享的文件夹的相对应的本地文件夹的标识符。</span><span class="sxs-lookup"><span data-stu-id="4cda9-123">The following code example shows how to form a request to get the identifier of the local folder that corresponds to the folder that is being shared.</span></span> <span data-ttu-id="4cda9-124">包含的共享文件夹的邮箱的 SMTP 地址和代表该文件夹中的数据类型的[数据类型](datatype.md)元素标识要共享的文件夹。</span><span class="sxs-lookup"><span data-stu-id="4cda9-124">The folder that is being shared is identified by the SMTP address of the mailbox that contains the folder that is being shared and by the [DataType](datatype.md) element that represents the type of data in that folder.</span></span> <span data-ttu-id="4cda9-125">本示例中，共享文件夹是 user1@contoso.com 所拥有的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="4cda9-125">In this example, the folder that is being shared is the Contacts folder that is owned by user1@contoso.com.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4cda9-126">代码</span><span class="sxs-lookup"><span data-stu-id="4cda9-126">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010"/>
  </soap:Header>
  <soap:Body>
    <m:GetSharingFolder>
      <m:SmtpAddress>user1@contoso.com</m:SmtpAddress>
      <m:DataType>Contacts</m:DataType>
    </m:GetSharingFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a><span data-ttu-id="4cda9-127">注释</span><span class="sxs-lookup"><span data-stu-id="4cda9-127">Comments</span></span>

<span data-ttu-id="4cda9-128">有关的**数据类型**元素的可能值的信息，请参阅[数据类型](datatype.md)。</span><span class="sxs-lookup"><span data-stu-id="4cda9-128">For information about the possible values of the **DataType** element, see [DataType](datatype.md).</span></span>
  
## <a name="successful-getsharingfolder-response"></a><span data-ttu-id="4cda9-129">成功的 GetSharingFolder 响应</span><span class="sxs-lookup"><span data-stu-id="4cda9-129">Successful GetSharingFolder Response</span></span>

### <a name="description"></a><span data-ttu-id="4cda9-130">说明</span><span class="sxs-lookup"><span data-stu-id="4cda9-130">Description</span></span>

<span data-ttu-id="4cda9-131">下面的示例演示对**GetSharingFolder**请求成功响应。</span><span class="sxs-lookup"><span data-stu-id="4cda9-131">The following example shows a successful response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="4cda9-132">[SharingFolderId](sharingfolderid.md)元素的**Id**属性代表的本地文件夹中的共享的关系的标识符。</span><span class="sxs-lookup"><span data-stu-id="4cda9-132">The **Id** attribute of the [SharingFolderId](sharingfolderid.md) element represents the identifier of the local folder in the sharing relationship.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4cda9-133">代码</span><span class="sxs-lookup"><span data-stu-id="4cda9-133">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Success"
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseCode>NoError</m:ResponseCode>
      <m:SharingFolderId Id="AAMkAD=" ChangeKey="AwAAA=" />
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="getsharingfolder-error-response"></a><span data-ttu-id="4cda9-134">GetSharingFolder 错误响应</span><span class="sxs-lookup"><span data-stu-id="4cda9-134">GetSharingFolder error response</span></span>

### <a name="description"></a><span data-ttu-id="4cda9-135">说明</span><span class="sxs-lookup"><span data-stu-id="4cda9-135">Description</span></span>

<span data-ttu-id="4cda9-136">下面的示例演示对**GetSharingFolder**请求错误响应。</span><span class="sxs-lookup"><span data-stu-id="4cda9-136">The following example shows an error response to a **GetSharingFolder** request.</span></span> <span data-ttu-id="4cda9-137">本示例中，因为该请求指定的[SharingFolderId](sharingfolderid.md)和[数据类型](datatype.md)元素，将发生错误。</span><span class="sxs-lookup"><span data-stu-id="4cda9-137">In this example, the error occurred because the request specified both the [SharingFolderId](sharingfolderid.md) and [DataType](datatype.md) elements.</span></span> <span data-ttu-id="4cda9-138">请注意，只能有一个或多个这些两个元素可以指定，但不是能同时。</span><span class="sxs-lookup"><span data-stu-id="4cda9-138">Note that only one or the other of those two elements can be specified, but not both.</span></span> 
  
### <a name="code"></a><span data-ttu-id="4cda9-139">代码</span><span class="sxs-lookup"><span data-stu-id="4cda9-139">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="11" 
                         Version="Exchange2010" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <GetSharingFolderResponseMessage ResponseClass="Error" 
                                xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
                                xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:MessageText>Either DataType or SharedFolderId must be specified, but not both.</m:MessageText>
      <m:ResponseCode>ErrorInvalidGetSharingFolderRequest</m:ResponseCode>
      <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
    </GetSharingFolderResponseMessage>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="4cda9-140">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4cda9-140">See also</span></span>



[<span data-ttu-id="4cda9-141">GetSharingFolder</span><span class="sxs-lookup"><span data-stu-id="4cda9-141">GetSharingFolder</span></span>](getsharingfolder.md)
  
[<span data-ttu-id="4cda9-142">GetSharingFolderType</span><span class="sxs-lookup"><span data-stu-id="4cda9-142">GetSharingFolderType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderType.aspx)
  
[<span data-ttu-id="4cda9-143">GetSharingFolderResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4cda9-143">GetSharingFolderResponseMessage</span></span>](getsharingfolderresponsemessage.md)
  
[<span data-ttu-id="4cda9-144">GetSharingFolderResponseMessageType</span><span class="sxs-lookup"><span data-stu-id="4cda9-144">GetSharingFolderResponseMessageType</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.GetSharingFolderResponseMessageType.aspx)


[<span data-ttu-id="4cda9-145">Exchange 中的 EWS 操作</span><span class="sxs-lookup"><span data-stu-id="4cda9-145">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md)
  
- [<span data-ttu-id="4cda9-146">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="4cda9-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

