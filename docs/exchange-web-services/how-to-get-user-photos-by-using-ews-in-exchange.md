---
title: 使用 Exchange 中的 EWS 获取用户照片
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: f86d1099-1f57-47dc-abf2-4d5ae4e900a9
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 获取与邮箱或联系人相关联的用户照片。
localization_priority: Priority
ms.openlocfilehash: 14f2bc6bef1ce3c3529f03e213e3ada7c45a5a71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455784"
---
# <a name="get-user-photos-by-using-ews-in-exchange"></a><span data-ttu-id="90728-103">使用 Exchange 中的 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-103">Get user photos by using EWS in Exchange</span></span>

<span data-ttu-id="90728-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 获取与邮箱或联系人相关联的用户照片。</span><span class="sxs-lookup"><span data-stu-id="90728-104">Learn how to get user photos that are associated with a mailbox or contact by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="90728-105">将面孔放在某个名称上是很好的。</span><span class="sxs-lookup"><span data-stu-id="90728-105">It's nice to put a face to a name.</span></span> <span data-ttu-id="90728-106">如果您的用户希望将名称放在面孔中，应用程序可以从 Exchange 中请求一个代表电子邮件帐户的图像（通常为照片）。</span><span class="sxs-lookup"><span data-stu-id="90728-106">If your users like to put names to faces, your application can request an image, typically a photo, from Exchange that represents an email account.</span></span> <span data-ttu-id="90728-107">您可以获取存储在邮箱的 Exchange 服务器上的用户照片，也可以从邮箱中存储的联系人处获取联系人照片。</span><span class="sxs-lookup"><span data-stu-id="90728-107">You can get a user photo stored on an Exchange server for a mailbox, or you can get a contact photo from contacts stored in your mailbox.</span></span>
  
<span data-ttu-id="90728-108">您可以使用多种不同的技术从邮箱或 Active Directory 域服务（AD DS）获取照片。</span><span class="sxs-lookup"><span data-stu-id="90728-108">You can use several different technologies to get photos from mailboxes or Active Directory Domain Services (AD DS).</span></span> <span data-ttu-id="90728-109">获取照片的最佳方式取决于要从中获取照片的联系人的类型。</span><span class="sxs-lookup"><span data-stu-id="90728-109">The best way to get a photo depends on the type of contact that you want to get a photo from.</span></span> 
  
<span data-ttu-id="90728-110">**表1。用于基于联系人类型获取用户照片的技术**</span><span class="sxs-lookup"><span data-stu-id="90728-110">**Table 1. Technologies to use to get user photos based on contact type**</span></span>

|<span data-ttu-id="90728-111">**联系人类型**</span><span class="sxs-lookup"><span data-stu-id="90728-111">**Contact type**</span></span>|<span data-ttu-id="90728-112">**要使用的技术**</span><span class="sxs-lookup"><span data-stu-id="90728-112">**Technologies to use**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90728-113">邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-113">Mailbox user photo</span></span>  <br/> |[<span data-ttu-id="90728-114">使用 REST 获取邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-114">Get a mailbox user photo by using REST</span></span>](#bk_REST)<br/><br/> [<span data-ttu-id="90728-115">使用 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-115">Get a user photo by using EWS</span></span>](#bk_EWS) <br/> |
|<span data-ttu-id="90728-116">联系用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-116">Contact user photo</span></span>  <br/> |[<span data-ttu-id="90728-117">使用 EWS 托管 API 获取联系人用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-117">Get a contact user photo by using EWS Managed API</span></span>](#bk_EWSMA)<br/><br/> [<span data-ttu-id="90728-118">使用 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-118">Get a user photo by using EWS</span></span>](#bk_EWS) <br/> |

<span data-ttu-id="90728-119"><a name="bk_REST"> </a></span><span class="sxs-lookup"><span data-stu-id="90728-119"><a name="bk_REST"> </a></span></span>

## <a name="get-a-mailbox-user-photo-by-using-rest"></a><span data-ttu-id="90728-120">使用 REST 获取邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-120">Get a mailbox user photo by using REST</span></span>

<span data-ttu-id="90728-121">您可以使用标准的 HTTPS **GET**请求从 Exchange 服务器请求用户照片。</span><span class="sxs-lookup"><span data-stu-id="90728-121">You can request user photos from an Exchange server by using a standard HTTPS **GET** request.</span></span> <span data-ttu-id="90728-122">在请求中，指定电子邮件帐户地址和图像的大小代码，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="90728-122">In the request, specify the email account address and a size code for the image, as shown in the following example.</span></span> 
  
```HTML
https://Exchange Server/ews/Exchange.asmx/s/GetUserPhoto?email=email address&amp;size=size code
```

<span data-ttu-id="90728-123">使用自动发现服务[GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)操作检索**ExternalEwsUrl**设置，该设置包含 EXCHANGE Web 服务（EWS）终结点的 URL 和返回用户照片的**exchange**的 HTTP 处理程序的位置。</span><span class="sxs-lookup"><span data-stu-id="90728-123">Use the Autodiscover service [GetUserSettings](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) operation to retrieve the **ExternalEwsUrl** setting, which contains the URL of the Exchange Web Services (EWS) endpoint and the location of the **Exchange.asmx** HTTP handler that returns the user photos.</span></span> 
  
<span data-ttu-id="90728-124">每个大小代码指示的图像的高度和宽度（以像素为单位）。</span><span class="sxs-lookup"><span data-stu-id="90728-124">Each size code indicates the height and width of the image in pixels.</span></span> <span data-ttu-id="90728-125">例如，大小代码**HR48x48**返回一个高度为48像素、宽48像素的图像。</span><span class="sxs-lookup"><span data-stu-id="90728-125">For example, the size code **HR48x48** returns an image that is 48 pixels high by 48 pixels wide.</span></span> <span data-ttu-id="90728-126">Size 代码参数的可能值与[SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素的可能值相同。</span><span class="sxs-lookup"><span data-stu-id="90728-126">The possible values for the size code parameter are the same as the possible values for the [SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="90728-127">如果请求指定的大小不可用，则将返回最大可用照片。</span><span class="sxs-lookup"><span data-stu-id="90728-127">If the request specifies a size that is not available, the largest available photo will be returned.</span></span> <span data-ttu-id="90728-128">如果 Exchange 服务器上未存储任何照片，则将返回存储在 AD DS 中的帐户的缩略图图像。</span><span class="sxs-lookup"><span data-stu-id="90728-128">If no photo is stored on the Exchange server, the thumbnail image stored in AD DS for the account will be returned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="90728-129">**HR48x48**大小代码始终返回 AD DS 缩略图（如果可用）。</span><span class="sxs-lookup"><span data-stu-id="90728-129">The **HR48x48** size code always returns the AD DS thumbnail image if it is available.</span></span> 
  
<span data-ttu-id="90728-130">下面的示例演示如何使用 GET 请求检索 Sadie 的用户照片并将其保存到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="90728-130">The following example shows how you can use the GET request to retrieve the user photo for Sadie and save it to your local computer.</span></span>
  
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

<span data-ttu-id="90728-131">请求将返回 HTTP 响应。</span><span class="sxs-lookup"><span data-stu-id="90728-131">The request will return an HTTP response.</span></span> 
  
<span data-ttu-id="90728-132">**表2。GetUserPhoto 请求的响应代码**</span><span class="sxs-lookup"><span data-stu-id="90728-132">**Table 2. Response codes for a GetUserPhoto request**</span></span>

|<span data-ttu-id="90728-133">**响应代码**</span><span class="sxs-lookup"><span data-stu-id="90728-133">**Response code**</span></span>|<span data-ttu-id="90728-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="90728-134">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90728-135">200</span><span class="sxs-lookup"><span data-stu-id="90728-135">200</span></span>  <br/> |<span data-ttu-id="90728-136">图像可用于指定的电子邮件帐户，而二进制图像包含在响应中。</span><span class="sxs-lookup"><span data-stu-id="90728-136">An image is available for the specified email account and the binary image is contained in the response.</span></span>  <br/> |
|<span data-ttu-id="90728-137">304</span><span class="sxs-lookup"><span data-stu-id="90728-137">304</span></span>  <br/> |<span data-ttu-id="90728-138">自上次将**ETag**返回到应用程序后，图像尚未更改。</span><span class="sxs-lookup"><span data-stu-id="90728-138">The image has not changed since the last time the **ETag** was returned to the application.</span></span>  <br/> |
|<span data-ttu-id="90728-139">404</span><span class="sxs-lookup"><span data-stu-id="90728-139">404</span></span>  <br/> |<span data-ttu-id="90728-140">没有可用于指定的电子邮件帐户的图像。</span><span class="sxs-lookup"><span data-stu-id="90728-140">No image is available for the specified email account.</span></span>  <br/> |

<span data-ttu-id="90728-141"><a name="bk_REST"> </a></span><span class="sxs-lookup"><span data-stu-id="90728-141"><a name="bk_REST"> </a></span></span>

## <a name="cache-user-photos"></a><span data-ttu-id="90728-142">缓存用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-142">Cache user photos</span></span>

<span data-ttu-id="90728-143">Exchange 将返回内容类型为 image/jpeg 的数据以及标头值的集合。</span><span class="sxs-lookup"><span data-stu-id="90728-143">Exchange returns the data with a content type of image/jpeg, along with a collection of header values.</span></span> <span data-ttu-id="90728-144">**ETag**标头类似于更改键。</span><span class="sxs-lookup"><span data-stu-id="90728-144">The **ETag** header is similar to a change key.</span></span> <span data-ttu-id="90728-145">值是一个字符串，表示上次更新照片的时间。</span><span class="sxs-lookup"><span data-stu-id="90728-145">The value is a string that represents the last time the photo was updated.</span></span> <span data-ttu-id="90728-146">在照片发生更改之前，该**ETag**对用户照片保持不变。</span><span class="sxs-lookup"><span data-stu-id="90728-146">The **ETag** remains the same for the user photo until the photo is changed.</span></span> <span data-ttu-id="90728-147">可以在 "**如果-无匹配**" 标头中将此**ETag**值发送到 HTTPS **GET**请求中的服务器。</span><span class="sxs-lookup"><span data-stu-id="90728-147">You can send this **ETag** value to the server in the HTTPS **GET** request in an **If-None-Match** header.</span></span> <span data-ttu-id="90728-148">如果自上次请求以来，该照片尚未更改，则服务器将使用 HTTP 304 响应进行响应，以指示这样。</span><span class="sxs-lookup"><span data-stu-id="90728-148">If the photo hasn't changed since the last request, the server will respond with an HTTP 304 response that indicates as such.</span></span> <span data-ttu-id="90728-149">这意味着您可以使用以前请求和保存的用户照片，而不是处理新照片。</span><span class="sxs-lookup"><span data-stu-id="90728-149">This means that you can use the user photo that you previously requested and saved rather than processing a new one.</span></span> 

<span data-ttu-id="90728-150"><a name="bk_EWSMA"> </a></span><span class="sxs-lookup"><span data-stu-id="90728-150"><a name="bk_EWSMA"> </a></span></span>

## <a name="get-a-contact-user-photo-by-using-ews-managed-api"></a><span data-ttu-id="90728-151">使用 EWS 托管 API 获取联系人用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-151">Get a contact user photo by using EWS Managed API</span></span>

<span data-ttu-id="90728-152">如果联系人存储在用户邮箱的联系人文件夹中，则您的应用程序可以使用 EWS 托管 API 检索联系人的照片。</span><span class="sxs-lookup"><span data-stu-id="90728-152">Your application can use the EWS Managed API to retrieve photos for contacts, if the contact is stored in a contact folder in the user's mailbox.</span></span> <span data-ttu-id="90728-153">若要执行此操作，首先请查找您想要使用的联系人的**ItemId** 。</span><span class="sxs-lookup"><span data-stu-id="90728-153">To do this, first, find the **ItemId** for the contact you want use.</span></span> <span data-ttu-id="90728-154">然后，在绑定到该联系人后，将其加载到 "附件" 集合。</span><span class="sxs-lookup"><span data-stu-id="90728-154">Then, after you bind to that contact, load it to the attachments collection.</span></span> <span data-ttu-id="90728-155">如果联系人有照片，则照片将是附件之一。</span><span class="sxs-lookup"><span data-stu-id="90728-155">If the contact has a photo, the photo will be one of the attachments.</span></span> <span data-ttu-id="90728-156">依次通过 "附件" 集合，检查**IsContactPhoto**属性的值。</span><span class="sxs-lookup"><span data-stu-id="90728-156">Loop through the attachments collection, checking the value of the **IsContactPhoto** property.</span></span> <span data-ttu-id="90728-157">当您找到联系人照片时，您可以将其保存到本地计算机，应用程序可以对其进行访问。</span><span class="sxs-lookup"><span data-stu-id="90728-157">When you find the contact photo, you can save it to your local computer, and your application can access it.</span></span> 
  
<span data-ttu-id="90728-158">下面的示例演示了此过程。</span><span class="sxs-lookup"><span data-stu-id="90728-158">The following example shows this process.</span></span> <span data-ttu-id="90728-159">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="90728-159">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="90728-160"><a name="bk_EWS"> </a></span><span class="sxs-lookup"><span data-stu-id="90728-160"><a name="bk_EWS"> </a></span></span>

## <a name="get-a-user-photo-by-using-ews"></a><span data-ttu-id="90728-161">使用 EWS 获取用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-161">Get a user photo by using EWS</span></span>

<span data-ttu-id="90728-162">如果从 AD DS 获取用户照片，则可以使用[GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx)操作（如果您知道电子邮件地址）或[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx)操作（如果您不知道电子邮件地址）。</span><span class="sxs-lookup"><span data-stu-id="90728-162">If you're getting a user photo from AD DS, you can use the [GetUserPhoto](https://msdn.microsoft.com/library/f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e%28Office.15%29.aspx) operation (if you know the email address) or the [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) operation (if you don't know the email address).</span></span> <span data-ttu-id="90728-163">如果要从邮箱的 "联系人" 文件夹中获取用户照片，请使用[GetItem](https://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx)操作，后跟[GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx)操作。</span><span class="sxs-lookup"><span data-stu-id="90728-163">If you're getting a user photo from a contacts folder in the mailbox, use the [GetItem](https://msdn.microsoft.com/library/6b96dace-1260-4b83-869a-7c31c5583daa%28Office.15%29.aspx) operation followed by the [GetAttachment](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="90728-164">在这两种情况下，照片在 XML 响应中作为 Base64 编码的字符串返回。</span><span class="sxs-lookup"><span data-stu-id="90728-164">In either case, the photo is returned as a Base64-encoded string in the XML response.</span></span> 
  
### <a name="get-a-mailbox-user-photo-by-using-the-getuserphoto-operation"></a><span data-ttu-id="90728-165">使用 GetUserPhoto 操作获取邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-165">Get a mailbox user photo by using the GetUserPhoto operation</span></span>

<span data-ttu-id="90728-166">使用**GetUserPhoto**操作非常简单。</span><span class="sxs-lookup"><span data-stu-id="90728-166">Using the **GetUserPhoto** operation is straightforward.</span></span> <span data-ttu-id="90728-167">在 XML 请求中，指定用户的电子邮件地址和要返回的[照片的大小](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)（在[SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx)元素中）。</span><span class="sxs-lookup"><span data-stu-id="90728-167">In the XML request, specify the email address of the user, and the [size of the photo](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) to return (in the [SizeRequested](https://msdn.microsoft.com/library/e86f98b6-83b5-4530-80eb-dc5df42e2c62%28Office.15%29.aspx) element).</span></span> <span data-ttu-id="90728-168">下面的 XML 请求示例演示如何获取 Sadie Daniels 的照片，该照片的宽度为360像素，高为360像素。</span><span class="sxs-lookup"><span data-stu-id="90728-168">The following XML request example shows how to get a photo for Sadie Daniels that's 360 pixels wide by 360 pixels high.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

<span data-ttu-id="90728-169">下面是 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="90728-169">The following is the XML response.</span></span> <span data-ttu-id="90728-170">Base64 编码的照片包含在[PictureData](https://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx)元素中（内容已缩短以提高可读性）。</span><span class="sxs-lookup"><span data-stu-id="90728-170">The Base64-encoded photo is contained in the [PictureData](https://msdn.microsoft.com/library/1124eac3-ebf2-4b81-96d3-96838c840433%28Office.15%29.aspx) element (the content has been shortened for readability).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetUserPhotoResponse ResponseClass="Success" 
         xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <HasChanged>true</HasChanged>
      <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAg... wATRRRSuB//2Q==</PictureData>
    </GetUserPhotoResponse>
  </s:Body>
</s:Envelope>

```

### <a name="get-a-mailbox-user-photo-by-using-the-resolvenames-operation"></a><span data-ttu-id="90728-171">使用 ResolveNames 操作获取邮箱用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-171">Get a mailbox user photo by using the ResolveNames operation</span></span>

<span data-ttu-id="90728-172">如果您不知道要获取其照片的用户的电子邮件地址，则可以[使用 ResolveNames 操作](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)获取可能的匹配项的候选人。</span><span class="sxs-lookup"><span data-stu-id="90728-172">If you don't know the email address of the user for whom you are getting a photo, you can [use the ResolveNames operation](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md) to get candidates for a possible match.</span></span> <span data-ttu-id="90728-173">如果为[ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx)元素的**ContactDataShape**属性指定 "AllProperties"，则会为每个候选人返回大量数据（包括用户照片）。</span><span class="sxs-lookup"><span data-stu-id="90728-173">If you specify "AllProperties" for the **ContactDataShape** attribute of the [ResolveNames](https://msdn.microsoft.com/library/c85207e1-1315-443b-94ec-2b58f405076b%28Office.15%29.aspx) element, a lot of data, including user photos, will be returned for each candidate.</span></span> <span data-ttu-id="90728-174">下面的示例演示对解析名称 "Sadie" 的 XML 请求，并返回每个候选项的所有属性。</span><span class="sxs-lookup"><span data-stu-id="90728-174">The following example shows the XML request to resolve the name "Sadie" and return all the properties for each candidate.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="90728-175">响应中将返回大量数据。</span><span class="sxs-lookup"><span data-stu-id="90728-175">A lot of data will be returned in the response.</span></span> <span data-ttu-id="90728-176">以下示例仅显示与用户照片相关的数据。</span><span class="sxs-lookup"><span data-stu-id="90728-176">The following example shows only the data that is relevant to the user photo.</span></span> <span data-ttu-id="90728-177">**Photo**元素包含 Base64 编码的用户照片（内容已缩短以提高可读性）。</span><span class="sxs-lookup"><span data-stu-id="90728-177">The **Photo** element contains the Base64-encoded user photo (the content has been shortened for readability).</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:ResolveNamesResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="get-a-contact-user-photo-by-using-the-getattachment-operation"></a><span data-ttu-id="90728-178">使用 GetAttachment 操作获取联系人用户照片</span><span class="sxs-lookup"><span data-stu-id="90728-178">Get a contact user photo by using the GetAttachment operation</span></span>

<span data-ttu-id="90728-179">您可以使用 EWS 获取存储在邮箱中的联系人的照片。</span><span class="sxs-lookup"><span data-stu-id="90728-179">You can use EWS to get photos from contacts stored in your mailbox.</span></span> <span data-ttu-id="90728-180">首先，使用**GetItem**操作返回所有属性，以便您可以查找照片。</span><span class="sxs-lookup"><span data-stu-id="90728-180">First, you use the **GetItem** operation to return all properties so you can look for photos.</span></span> <span data-ttu-id="90728-181">下面的示例展示了获取联系人项目的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="90728-181">The following example shows an XML request to get a contact item.</span></span> <span data-ttu-id="90728-182">为了提高可读性，项目 ID 已缩短。</span><span class="sxs-lookup"><span data-stu-id="90728-182">The item ID has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetItem xmlns='https://schemas.microsoft.com/exchange/services/2006/messages'>
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

<span data-ttu-id="90728-183">查找 " [HasPicture](https://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx) " 元素以验证联系人是否有关联的照片。</span><span class="sxs-lookup"><span data-stu-id="90728-183">Look for the [HasPicture](https://msdn.microsoft.com/library/922a43fe-01bd-49f2-9261-e00e4699b8da%28Office.15%29.aspx) element to verify that the contact has an associated photo.</span></span> <span data-ttu-id="90728-184">然后，查看[IsContactPhoto](https://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx)元素的值为 true 的附件的集合。</span><span class="sxs-lookup"><span data-stu-id="90728-184">Then look through the collection of attachments for one that has a value of true for the [IsContactPhoto](https://msdn.microsoft.com/library/ae36b5f9-a787-4863-9dbc-258ad724801d%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="90728-185">以下响应示例仅显示相关数据。</span><span class="sxs-lookup"><span data-stu-id="90728-185">The following response example shows only the relevant data.</span></span> <span data-ttu-id="90728-186">为了提高可读性，可缩短 ID 值。</span><span class="sxs-lookup"><span data-stu-id="90728-186">The ID values are shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

接下来，将**GetAttachment**操作与**AttachmentId**结合使用，以请求具有联系人照片的附件。 下面的示例展示了获取附件的 XML 请求。 <span data-ttu-id="90728-189">为了提高可读性，将缩短 ID。</span><span class="sxs-lookup"><span data-stu-id="90728-189">The ID is shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
         <t:AttachmentId Id="1LGlhgpgoA="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>

```

下面的示例显示包含有关您请求的附件的信息的 XML 响应。 <span data-ttu-id="90728-191">[Content](https://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx)元素包含用户照片的 Base64 编码字符串，在此示例中缩短了可读性。</span><span class="sxs-lookup"><span data-stu-id="90728-191">The [Content](https://msdn.microsoft.com/library/24f8c54a-505f-4fc0-b7e7-93ad50b97070%28Office.15%29.aspx) element contains the Base64-encoded string for the user photo, shortened in this example for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
         xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="90728-192"><a name="bk_EWS"> </a></span><span class="sxs-lookup"><span data-stu-id="90728-192"><a name="bk_EWS"> </a></span></span>

## <a name="decode-a-base64-encoded-string"></a><span data-ttu-id="90728-193">对 Base64 编码的字符串进行解码</span><span class="sxs-lookup"><span data-stu-id="90728-193">Decode a Base64-encoded string</span></span>

<span data-ttu-id="90728-194">无论您用于获取用户照片的操作如何，您都需要对该字符串进行解码，以便您可以在应用程序中使用它。</span><span class="sxs-lookup"><span data-stu-id="90728-194">Regardless of the operation you use to get a user photo, you'll need to decode that string so you can use it in your application.</span></span> <span data-ttu-id="90728-195">下面的示例演示如何对字符串进行解码，然后将其保存到本地计算机，以便应用程序稍后对其进行访问。</span><span class="sxs-lookup"><span data-stu-id="90728-195">The following example shows how to decode the string, and then save it to your local computer so you application can access it later.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="90728-196">另请参阅</span><span class="sxs-lookup"><span data-stu-id="90728-196">See also</span></span>

- [<span data-ttu-id="90728-197">人员和 Exchange 中的 EWS 中的联系人</span><span class="sxs-lookup"><span data-stu-id="90728-197">People and contacts in EWS in Exchange</span></span>](people-and-contacts-in-ews-in-exchange.md)    
- [<span data-ttu-id="90728-198">使用 Exchange 2013 中的 EWS 解析不明确的名称</span><span class="sxs-lookup"><span data-stu-id="90728-198">Resolve ambiguous names by using EWS in Exchange 2013</span></span>](how-to-resolve-ambiguous-names-by-using-ews-in-exchange-2013.md)    
- [<span data-ttu-id="90728-199">使用 Exchange 中的 EWS 在批处理中处理联系人</span><span class="sxs-lookup"><span data-stu-id="90728-199">Process contacts in batches by using EWS in Exchange</span></span>](how-to-process-contacts-in-batches-by-using-ews-in-exchange.md)
    

