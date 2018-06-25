---
title: 要在 Exchange 使用 EWS 获取用户照片
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: 了解如何获取与邮箱关联或联系在 Exchange 使用 EWS 托管 API 或 EWS 的用户照片。
ms.openlocfilehash: f0f5cddd41fc563fb9ed38e75b505830a3992411
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752813"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a><span data-ttu-id="5907f-103">要在 Exchange 使用 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-103">Get user photos by using EWS in Exchange</span></span>

<span data-ttu-id="5907f-104">了解如何获取与邮箱关联或联系在 Exchange 使用 EWS 托管 API 或 EWS 的用户照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-104">Learn how to get user photos that are associated with a mailbox or contact by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="5907f-105">很不错将一个脸放到一个名称。</span><span class="sxs-lookup"><span data-stu-id="5907f-105">It's nice to put a face to a name.</span></span> <span data-ttu-id="5907f-106">如果用户希望将名称放到正面，您的应用程序可以请求图像，通常照片，从 Exchange 表示的电子邮件帐户。</span><span class="sxs-lookup"><span data-stu-id="5907f-106">If your users like to put names to faces, your application can request an image, typically a photo, from Exchange that represents an email account.</span></span> <span data-ttu-id="5907f-107">您可以获取用户照片存储邮箱的 Exchange 服务器上或可以存储在您的邮箱中的联系人中获取联系人的照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-107">You can get a user photo stored on an Exchange server for a mailbox, or you can get a contact photo from contacts stored in your mailbox.</span></span>
  
<span data-ttu-id="5907f-108">您可以使用几个不同的技术获得邮箱或 Active Directory 域服务 (AD DS) 的照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-108">You can use several different technologies to get photos from mailboxes or Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="5907f-109">若要获取照片的最佳方式取决于您希望获取从照片的联系人的类型。</span><span class="sxs-lookup"><span data-stu-id="5907f-109">The best way to get a photo depends on the type of contact that you want to get a photo from.</span></span> 
  
<span data-ttu-id="5907f-110">**表 1。技术，可用于获取基于联系人类型的用户照片**</span><span class="sxs-lookup"><span data-stu-id="5907f-110">**Table 1. Technologies to use to get user photos based on contact type**</span></span>

|<span data-ttu-id="5907f-111">**联系人类型**</span><span class="sxs-lookup"><span data-stu-id="5907f-111">**Contact type**</span></span>|<span data-ttu-id="5907f-112">**若要使用的技术**</span><span class="sxs-lookup"><span data-stu-id="5907f-112">**Technologies to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5907f-113">邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-113">Mailbox user photo</span></span>  <br/> |[<span data-ttu-id="5907f-114">获取使用 REST 的邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-114">Get a mailbox user photo by using REST</span></span>](#bk_REST)<br/><br/> [<span data-ttu-id="5907f-115">通过使用 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-115">Get a user photo by using EWS</span></span>](#bk_EWS) <br/> |
|<span data-ttu-id="5907f-116">联系人的用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-116">Contact user photo</span></span>  <br/> |[<span data-ttu-id="5907f-117">通过使用 EWS 托管 API 获取联系人的用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-117">Get a contact user photo by using EWS Managed API</span></span>](#bk_EWSMA)<br/><br/> [<span data-ttu-id="5907f-118">通过使用 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-118">Get a user photo by using EWS</span></span>](#bk_EWS) <br/> |

<span data-ttu-id="5907f-119"><a name="bk_REST"> </a></span><span class="sxs-lookup"><span data-stu-id="5907f-119"></span></span>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a><span data-ttu-id="5907f-120">获取使用 REST 的邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-120">Get a mailbox user photo by using REST</span></span>

<span data-ttu-id="5907f-121">通过使用标准的 HTTPS **GET**请求，您可以从 Exchange 服务器请求用户照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-121">You can request user photos from an Exchange server by using a standard HTTPS **GET** request.</span></span> <span data-ttu-id="5907f-122">在请求中，指定的电子邮件帐户地址和图像，大小代码在下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="5907f-122">In the request, specify the email account address and a size code for the image, as shown in the following example.</span></span> 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

<span data-ttu-id="5907f-123">使用自动发现服务[GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)操作可以检索**ExternalEwsUrl**设置，其中包含的 Exchange Web Services (EWS) 终结点的 URL 和返回**Exchange.asmx** HTTP 处理程序的位置用户照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-123">Use the Autodiscover service [GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) operation to retrieve the **ExternalEwsUrl** setting, which contains the URL of the Exchange Web Services (EWS) endpoint and the location of the **Exchange.asmx** HTTP handler that returns the user photos.</span></span> 
  
<span data-ttu-id="5907f-124">每个大小代码指示的高度和宽度以像素为单位的图像。</span><span class="sxs-lookup"><span data-stu-id="5907f-124">Each size code indicates the height and width of the image in pixels.</span></span> <span data-ttu-id="5907f-125">例如，大小代码**HR48x48**返回 48 像素高 x 48 像素宽的图像。</span><span class="sxs-lookup"><span data-stu-id="5907f-125">For example, the size code **HR48x48** returns an image that is 48 pixels high by 48 pixels wide.</span></span> <span data-ttu-id="5907f-126">大小代码参数的可能值是[SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素的可能值相同。</span><span class="sxs-lookup"><span data-stu-id="5907f-126">The possible values for the size code parameter are the same as the possible values for the [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="5907f-127">如果请求指定不可用的大小，将返回的最大可用照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-127">If the request specifies a size that is not available, the largest available photo will be returned.</span></span> <span data-ttu-id="5907f-128">如果没有照片存储在 Exchange 服务器上，将返回存储在 AD DS 帐户的缩略图图像。</span><span class="sxs-lookup"><span data-stu-id="5907f-128">If no photo is stored on the Exchange server, the thumbnail image stored in AD DS for the account will be returned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5907f-129">如果可用，则**HR48x48**大小代码将始终返回的 AD DS 缩略图图像。</span><span class="sxs-lookup"><span data-stu-id="5907f-129">The **HR48x48** size code always returns the AD DS thumbnail image if it is available.</span></span> 
  
<span data-ttu-id="5907f-130">下面的示例演示如何使用 GET 请求 Sadie 检索用户照片，并将其保存到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="5907f-130">The following example shows how you can use the GET request to retrieve the user photo for Sadie and save it to your local computer.</span></span>
  
```cs
// Create the web request with the REST URL.
HttpWebRequest request = 
   WebRequest.Create("https://www.contoso.com/ews/exchange.asmx/s/GetUserPhoto?email=sadie@contoso.com&amp;size=HR240x240") 
   as HttpWebRequest;
// Submit the request.
using (HttpWebResponse resp = request.GetResponse() as HttpWebResponse)
{
   // Take the response and save it as an image.
   Bitmap image = new Bitmap(resp.GetResponseStream());
   image.Save("Sadie.jpg");
}

```

<span data-ttu-id="5907f-131">请求将返回的 HTTP 响应。</span><span class="sxs-lookup"><span data-stu-id="5907f-131">The request will return an HTTP response.</span></span> 
  
<span data-ttu-id="5907f-132">**表 2。GetUserPhoto 请求的响应代码**</span><span class="sxs-lookup"><span data-stu-id="5907f-132">**Table 2. Response codes for a GetUserPhoto request**</span></span>

|<span data-ttu-id="5907f-133">**响应代码**</span><span class="sxs-lookup"><span data-stu-id="5907f-133">**Response code**</span></span>|<span data-ttu-id="5907f-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="5907f-134">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5907f-135">200</span><span class="sxs-lookup"><span data-stu-id="5907f-135">200</span></span>  <br/> |<span data-ttu-id="5907f-136">图像是可用于指定电子邮件帐户，在响应中包含的二进制图像。</span><span class="sxs-lookup"><span data-stu-id="5907f-136">An image is available for the specified email account and the binary image is contained in the response.</span></span>  <br/> |
|<span data-ttu-id="5907f-137">304</span><span class="sxs-lookup"><span data-stu-id="5907f-137">304</span></span>  <br/> |<span data-ttu-id="5907f-138">最后一次**ETag**返回到应用程序未更改的图像。</span><span class="sxs-lookup"><span data-stu-id="5907f-138">The image has not changed since the last time the **ETag** was returned to the application.</span></span>  <br/> |
|<span data-ttu-id="5907f-139">404</span><span class="sxs-lookup"><span data-stu-id="5907f-139">404</span></span>  <br/> |<span data-ttu-id="5907f-140">可用于指定电子邮件帐户没有图像。</span><span class="sxs-lookup"><span data-stu-id="5907f-140">No image is available for the specified email account.</span></span>  <br/> |

<span data-ttu-id="5907f-141"><a name="bk_REST"> </a></span><span class="sxs-lookup"><span data-stu-id="5907f-141"></span></span>

## <a name="cache-user-photos"></a><span data-ttu-id="5907f-142">缓存用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-142">Cache user photos</span></span>

<span data-ttu-id="5907f-143">Exchange 返回的数据的内容类型为 image/jpeg，以及标头值的集合。</span><span class="sxs-lookup"><span data-stu-id="5907f-143">Exchange returns the data with a content type of image/jpeg, along with a collection of header values.</span></span> <span data-ttu-id="5907f-144">类似于更改密钥**ETag**标头。</span><span class="sxs-lookup"><span data-stu-id="5907f-144">The **ETag** header is similar to a change key.</span></span> <span data-ttu-id="5907f-145">值为一个字符串，表示的上次更新照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-145">The value is a string that represents the last time the photo was updated.</span></span> <span data-ttu-id="5907f-146">**ETag**保持不变的用户照片直到照片被更改。</span><span class="sxs-lookup"><span data-stu-id="5907f-146">The **ETag** remains the same for the user photo until the photo is changed.</span></span> <span data-ttu-id="5907f-147">您可以向 HTTPS **GET**请求中**无-If-match**标头中的服务器发送此**ETag**值。</span><span class="sxs-lookup"><span data-stu-id="5907f-147">You can send this **ETag** value to the server in the HTTPS **GET** request in an **If-None-Match** header.</span></span> <span data-ttu-id="5907f-148">如果自上次请求以来未更改的照片，服务器将响应 HTTP 304 响应，因为这指示。</span><span class="sxs-lookup"><span data-stu-id="5907f-148">If the photo hasn't changed since the last request, the server will respond with an HTTP 304 response that indicates as such.</span></span> <span data-ttu-id="5907f-149">这意味着，您可以使用您以前请求并保存的用户照片而不是一个新的处理。</span><span class="sxs-lookup"><span data-stu-id="5907f-149">This means that you can use the user photo that you previously requested and saved rather than processing a new one.</span></span> 

<span data-ttu-id="5907f-150"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="5907f-150"></span></span>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a><span data-ttu-id="5907f-151">通过使用 EWS 托管 API 获取联系人的用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-151">Get a contact user photo by using EWS Managed API</span></span>

<span data-ttu-id="5907f-152">应用程序可以使用 EWS 托管 API 检索联系人的照片如果联系人存储在用户的邮箱中的联系人文件夹。</span><span class="sxs-lookup"><span data-stu-id="5907f-152">Your application can use the EWS Managed API to retrieve photos for contacts, if the contact is stored in a contact folder in the user's mailbox.</span></span> <span data-ttu-id="5907f-153">若要执行此操作，首先，查找**ItemId**联系人您希望使用。</span><span class="sxs-lookup"><span data-stu-id="5907f-153">To do this, first, find the **ItemId** for the contact you want use.</span></span> <span data-ttu-id="5907f-154">然后，您将绑定到该联系人后，则加载到的 attachments 集合。</span><span class="sxs-lookup"><span data-stu-id="5907f-154">Then, after you bind to that contact, load it to the attachments collection.</span></span> <span data-ttu-id="5907f-155">如果联系人的照片，照片将其中一个附件。</span><span class="sxs-lookup"><span data-stu-id="5907f-155">If the contact has a photo, the photo will be one of the attachments.</span></span> <span data-ttu-id="5907f-156">循环访问的 attachments 集合，检查**IsContactPhoto**属性的值。</span><span class="sxs-lookup"><span data-stu-id="5907f-156">Loop through the attachments collection, checking the value of the **IsContactPhoto** property.</span></span> <span data-ttu-id="5907f-157">时您查找联系人的照片，可以将其保存到本地计算机，并且您的应用程序可以访问它。</span><span class="sxs-lookup"><span data-stu-id="5907f-157">When you find the contact photo, you can save it to your local computer, and your application can access it.</span></span> 
  
<span data-ttu-id="5907f-158">下面的示例演示此过程。</span><span class="sxs-lookup"><span data-stu-id="5907f-158">The following example shows this process.</span></span> <span data-ttu-id="5907f-159">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="5907f-159">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
private static void GetContactPhoto(ExchangeService service, string ItemId)
{
   // Bind to an existing contact by using the ItemId passed into this function.
   Contact contact = Contact.Bind(service, ItemId);
   // Load the contact to get access to the collection of attachments.
   contact.Load(new PropertySet(ContactSchema.Attachments));
   // Loop through the attachments looking for a contact photo.
   foreach (Attachment attachment in contact.Attachments)
   {
      if ((attachment as FileAttachment).IsContactPhoto)
      {
         // Load the attachment to access the content.
         attachment.Load();
      }
   }
   FileAttachment photo = contact.GetContactPictureAttachment();
   // Create a file stream and save the contact photo to your computer.
   using (FileStream file = new FileStream(photo.Name, FileMode.Create, System.IO.FileAccess.Write))
   {
      photo.Load(file);
   }
}

```

<span data-ttu-id="5907f-160"><a name="bk_EWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5907f-160"></span></span>

## <a name="get-a-user-photo-by-using-ews"></a><span data-ttu-id="5907f-161">通过使用 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-161">Get a user photo by using EWS</span></span>

<span data-ttu-id="5907f-162">如果您正在从 AD DS 获取用户照片，您可以使用[GetUserPhoto](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)操作 （如果您知道电子邮件地址） 或[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作，（如果您不知道的电子邮件地址）。</span><span class="sxs-lookup"><span data-stu-id="5907f-162">If you're getting a user photo from AD DS, you can use the [GetUserPhoto](http://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx) operation (if you know the email address) or the [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation (if you don't know the email address).</span></span> <span data-ttu-id="5907f-163">如果您正在从邮箱中的联系人文件夹中获取用户照片，使用[GetItem](http://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) operation 后, 跟[GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="5907f-163">If you're getting a user photo from a contacts folder in the mailbox, use the [GetItem](http://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) operation followed by the [GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="5907f-164">在任一情况下，作为 Base64 编码的字符串，在 XML 响应中返回的照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-164">In either case, the photo is returned as a Base64-encoded string in the XML response.</span></span> 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a><span data-ttu-id="5907f-165">要使用 GetUserPhoto 操作获取邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-165">Get a mailbox user photo by using the GetUserPhoto operation</span></span>

<span data-ttu-id="5907f-166">使用**GetUserPhoto**操作非常简单。</span><span class="sxs-lookup"><span data-stu-id="5907f-166">Using the **GetUserPhoto** operation is straightforward.</span></span> <span data-ttu-id="5907f-167">在 XML 请求中，指定用户，并返回 （在[SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素中）[的照片大小](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="5907f-167">In the XML request, specify the email address of the user, and the [size of the photo](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) to return (in the [SizeRequested](http://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) element).</span></span> <span data-ttu-id="5907f-168">下面的 XML 请求示例演示如何获取 Sadie Daniels 360 像素宽 x 360 像素高的照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-168">The following XML request example shows how to get a photo for Sadie Daniels that's 360 pixels wide by 360 pixels high.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013 "/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>sadie@contoso.com</m:Email>
         <m:SizeRequested>HR360x360</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="5907f-169">下面是 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="5907f-169">The following is the XML response.</span></span> <span data-ttu-id="5907f-170">[PictureData](http://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx)元素 （内容已缩短为便于阅读） 中包含的 Base64 编码的照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-170">The Base64-encoded photo is contained in the [PictureData](http://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx) element (the content has been shortened for readability).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a><span data-ttu-id="5907f-171">要使用 ResolveNames 操作获取邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-171">Get a mailbox user photo by using the ResolveNames operation</span></span>

<span data-ttu-id="5907f-172">如果您不知道您正在为其获取照片的用户的电子邮件地址，则可以[使用 ResolveNames 操作](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)候选人获得可能的匹配项。</span><span class="sxs-lookup"><span data-stu-id="5907f-172">If you don't know the email address of the user for whom you are getting a photo, you can [use the ResolveNames operation](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md) to get candidates for a possible match.</span></span> <span data-ttu-id="5907f-173">如果[ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx)元素的**ContactDataShape**属性指定"AllProperties"，将为每个候选返回大量数据，包括用户照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-173">If you specify "AllProperties" for the **ContactDataShape** attribute of the [ResolveNames](http://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) element, a lot of data, including user photos, will be returned for each candidate.</span></span> <span data-ttu-id="5907f-174">下面的示例演示 XML 请求以解析名称"Sadie"并为每个候选返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="5907f-174">The following example shows the XML request to resolve the name "Sadie" and return all the properties for each candidate.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
<soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>  
<soap:Body>
  <m:ResolveNames ReturnFullContactData="true" ContactDataShape="AllProperties">
      <m:UnresolvedEntry>sadie</m:UnresolvedEntry>
    </m:ResolveNames>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="5907f-175">将在响应中返回大量数据。</span><span class="sxs-lookup"><span data-stu-id="5907f-175">A lot of data will be returned in the response.</span></span> <span data-ttu-id="5907f-176">下面的示例演示仅与用户照片相关的数据。</span><span class="sxs-lookup"><span data-stu-id="5907f-176">The following example shows only the data that is relevant to the user photo.</span></span> <span data-ttu-id="5907f-177">**照片**元素包含 （内容已缩短为便于阅读） 的 Base64 编码的用户照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-177">The **Photo** element contains the Base64-encoded user photo (the content has been shortened for readability).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:ResolveNamesResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:ResolutionSet TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Resolution>
              <t:Mailbox>
                <t:Name>Sadie Daniels</t:Name>
                <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                <t:RoutingType>SMTP</t:RoutingType>
                <t:MailboxType>Mailbox</t:MailboxType>
              </t:Mailbox>
              <t:Contact>
                <t:DisplayName>Sadie Daniels</t:DisplayName>
                <t:GivenName>Sadie</t:GivenName>
                <t:Initials/>
                <t:CompanyName>CONTOSO</t:CompanyName>
......
                <t:Photo>/9j/4AAQSkZJRgABAQE...qKKKAP/2Q==</t:Photo>
......
              </t:Contact>
            </t:Resolution>
          </m:ResolutionSet>
        </m:ResolveNamesResponseMessage>
      </m:ResponseMessages>
    </m:ResolveNamesResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a><span data-ttu-id="5907f-178">要使用 GetAttachment 操作获取联系人的用户照片</span><span class="sxs-lookup"><span data-stu-id="5907f-178">Get a contact user photo by using the GetAttachment operation</span></span>

<span data-ttu-id="5907f-179">您可以使用 EWS 获取来自存储在您的邮箱中的联系人的照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-179">You can use EWS to get photos from contacts stored in your mailbox.</span></span> <span data-ttu-id="5907f-180">首先，您可以使用**GetItem**操作，您可以查找照片，以便返回所有属性。</span><span class="sxs-lookup"><span data-stu-id="5907f-180">First, you use the **GetItem** operation to return all properties so you can look for photos.</span></span> <span data-ttu-id="5907f-181">下面的示例演示 XML 请求以获取联系人项目。</span><span class="sxs-lookup"><span data-stu-id="5907f-181">The following example shows an XML request to get a contact item.</span></span> <span data-ttu-id="5907f-182">为便于阅读缩短了项目 ID。</span><span class="sxs-lookup"><span data-stu-id="5907f-182">The item ID has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='http://schemas.microsoft.com/exchange/services/2006/messages'>
      <ItemShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </ItemShape>
      <ItemIds>
        <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
      </ItemIds>
    </GetItem>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="5907f-183">查找[HasPicture](http://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx)元素以验证联系人都有关联的照片。</span><span class="sxs-lookup"><span data-stu-id="5907f-183">Look for the [HasPicture](http://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx) element to verify that the contact has an associated photo.</span></span> <span data-ttu-id="5907f-184">然后查找的附件的值为 true，则[IsContactPhoto](http://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx)元素的集合。</span><span class="sxs-lookup"><span data-stu-id="5907f-184">Then look through the collection of attachments for one that has a value of true for the [IsContactPhoto](http://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="5907f-185">以下响应示例显示了相关的数据。</span><span class="sxs-lookup"><span data-stu-id="5907f-185">The following response example shows only the relevant data.</span></span> <span data-ttu-id="5907f-186">为便于阅读缩短的 ID 值。</span><span class="sxs-lookup"><span data-stu-id="5907f-186">The ID values are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Contact>
              <t:ItemId Id="AAAAGECXAAA=" ChangeKey="EQAAABYAAAD2WuN+TpqwSrNP9JCCMKC0AABLzXRv"/>
              <t:ParentFolderId Id="nIxIAAA=" ChangeKey="AQAAAA=="/>
              <t:ItemClass>IPM.Contact</t:ItemClass>
              <t:Subject>Hope Gross</t:Subject>
              <t:Sensitivity>Normal</t:Sensitivity>
......
              <t:Attachments>
                <t:FileAttachment>
                  <t:AttachmentId Id="1LGlhgpgoA="/>
                  <t:Name>ContactPicture.jpg</t:Name>
                  <t:Size>6260</t:Size>
                  <t:LastModifiedTime>2011-03-09T16:55:55</t:LastModifiedTime>
                  <t:IsInline>false</t:IsInline>
                  <t:IsContactPhoto>true</t:IsContactPhoto>
                </t:FileAttachment>
              </t:Attachments>
......
              <t:HasPicture>true</t:HasPicture>
            </t:Contact>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>

```

接下来，使用与**AttachmentId** **GetAttachment**操作请求附件已联系人的照片。 下面的示例演示 XML 请求以获取附件。 <span data-ttu-id="5907f-189">为便于阅读将被截 ID。</span><span class="sxs-lookup"><span data-stu-id="5907f-189">The ID is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

下面的示例演示 XML 响应与您请求的附件有关的信息。 <span data-ttu-id="5907f-191">[内容](http://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx)元素包含在此示例中为便于阅读缩短的用户照片的 Base64 编码字符串。</span><span class="sxs-lookup"><span data-stu-id="5907f-191">The [Content](http://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx) element contains the Base64-encoded string for the user photo, shortened in this example for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="+KsDBEr1LGlhgpgoA="/>
              <t:Name>ContactPicture.jpg</t:Name>
              <t:Content>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg...D//2Q==</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </m:GetAttachmentResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="5907f-192"><a name="bk_EWS"> </a></span><span class="sxs-lookup"><span data-stu-id="5907f-192"></span></span>

## <a name="decode-a-base64-encoded-string"></a><span data-ttu-id="5907f-193">对 Base64 编码字符串进行解码</span><span class="sxs-lookup"><span data-stu-id="5907f-193">Decode a Base64-encoded string</span></span>

<span data-ttu-id="5907f-194">无论您使用获取用户照片的操作，您需要对该字符串进行解码，以便您可以在您的应用程序中使用它。</span><span class="sxs-lookup"><span data-stu-id="5907f-194">Regardless of the operation you use to get a user photo, you'll need to decode that string so you can use it in your application.</span></span> <span data-ttu-id="5907f-195">下面的示例演示如何解码字符串，然后将其保存到本地计算机，使您应用程序能够更高版本访问它。</span><span class="sxs-lookup"><span data-stu-id="5907f-195">The following example shows how to decode the string, and then save it to your local computer so you application can access it later.</span></span>
  
```cs
// Convert the encoded string into a byte array.
byte[] data = System.Convert.FromBase64String(Photo);
// Create a memory stream to read the data.
MemoryStream ms = new MemoryStream(data);
// Save the data on your local computer as a JPG image.
using (FileStream file = new FileStream(ContactName + ".jpg", FileMode.Create, System.IO.FileAccess.Write))
{
   byte[] bytes = new byte[ms.Length];
   ms.Read(bytes, 0, (int)ms.Length);
   file.Write(bytes, 0, bytes.Length);
   ms.Close();
}

```

## <a name="see-also"></a><span data-ttu-id="5907f-196">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5907f-196">See also</span></span>

- [<span data-ttu-id="5907f-197">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="5907f-197">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)    
- [<span data-ttu-id="5907f-198">模糊名称解析使用 EWS 在 Exchange 2013</span><span class="sxs-lookup"><span data-stu-id="5907f-198">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [<span data-ttu-id="5907f-199">在 Exchange 使用 EWS 的批次中的过程联系人</span><span class="sxs-lookup"><span data-stu-id="5907f-199">Process contacts in batches by using EWS in Exchange</span></span>](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

