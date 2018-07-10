---
title: 在 Exchange 使用 EWS 使用文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4b3eb746-74c4-42a0-aa2c-742c147f1871
description: 了解如何创建、 获取、 更新和删除文件夹在 Exchange 使用 EWS 托管 API 或 EWS。
ms.openlocfilehash: a9a9e5974b2751268f37a1c9faacce43a333bcdb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752917"
---
# <a name="work-with-folders-by-using-ews-in-exchange"></a><span data-ttu-id="37eb5-103">在 Exchange 使用 EWS 使用文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-103">Work with folders by using EWS in Exchange</span></span>

<span data-ttu-id="37eb5-104">了解如何创建、 获取、 更新和删除文件夹在 Exchange 使用 EWS 托管 API 或 EWS。</span><span class="sxs-lookup"><span data-stu-id="37eb5-104">Learn how to create, get, update, and delete folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="37eb5-105">Exchange 中的 EWS 使用文件夹结构和组织的邮箱。</span><span class="sxs-lookup"><span data-stu-id="37eb5-105">EWS in Exchange uses folders to structure and organize mailboxes.</span></span> <span data-ttu-id="37eb5-106">您可以创建新、 获取、 更新和删除使用 EWS 托管 API 或 EWS 的文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-106">You can create new, get, update, and delete folders by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="37eb5-107">每个方法或下表中列出的操作是一个[Folder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)对象，[文件夹](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)类型，或执行[派生的文件夹类或类型之一](folders-and-items-in-ews-in-exchange.md#bk_folders)。</span><span class="sxs-lookup"><span data-stu-id="37eb5-107">Each of the methods or operations listed in the following table is performed on a [Folder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) object, a [Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) type, or [one of the derived folder classes or types](folders-and-items-in-ews-in-exchange.md#bk_folders).</span></span>
  
<span data-ttu-id="37eb5-108">**表 1。方法和操作的创建、 获取、 更新和删除文件夹**</span><span class="sxs-lookup"><span data-stu-id="37eb5-108">**Table 1. Methods and operations for creating, getting, updating and deleting folders**</span></span>

|<span data-ttu-id="37eb5-109">**若要...**</span><span class="sxs-lookup"><span data-stu-id="37eb5-109">**In order to…**</span></span>|<span data-ttu-id="37eb5-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="37eb5-110">**EWS Managed API method**</span></span>|<span data-ttu-id="37eb5-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="37eb5-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37eb5-112">创建一个文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-112">Create a folder</span></span>  <br/> |[<span data-ttu-id="37eb5-113">Folder.Save</span><span class="sxs-lookup"><span data-stu-id="37eb5-113">Folder.Save</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="37eb5-114">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="37eb5-114">CreateFolder</span></span>](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="37eb5-115">创建文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="37eb5-115">Create a folder hierarchy</span></span>  <br/> |<span data-ttu-id="37eb5-116">不适用</span><span class="sxs-lookup"><span data-stu-id="37eb5-116">Not available</span></span>  <br/> |[<span data-ttu-id="37eb5-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="37eb5-117">CreateFolderPath</span></span>](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="37eb5-118">获取文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-118">Get a folder</span></span>  <br/> |[<span data-ttu-id="37eb5-119">Folder.Bind</span><span class="sxs-lookup"><span data-stu-id="37eb5-119">Folder.Bind</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="37eb5-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="37eb5-120">GetFolder</span></span>](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="37eb5-121">获取文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="37eb5-121">Get a folder hierarchy</span></span>  <br/> |[<span data-ttu-id="37eb5-122">Folder.FindFolders</span><span class="sxs-lookup"><span data-stu-id="37eb5-122">Folder.FindFolders</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="37eb5-123">FindFolder</span><span class="sxs-lookup"><span data-stu-id="37eb5-123">FindFolder</span></span>](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="37eb5-124">更新文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-124">Update a folder</span></span>  <br/> |[<span data-ttu-id="37eb5-125">Folder.Update</span><span class="sxs-lookup"><span data-stu-id="37eb5-125">Folder.Update</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="37eb5-126">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="37eb5-126">UpdateFolder</span></span>](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="37eb5-127">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-127">Delete a folder</span></span>  <br/> |[<span data-ttu-id="37eb5-128">Folder.Delete</span><span class="sxs-lookup"><span data-stu-id="37eb5-128">Folder.Delete</span></span>](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="37eb5-129">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="37eb5-129">DeleteFolder</span></span>](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |

<span data-ttu-id="37eb5-130"><a name="bk_createfolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-130"></span></span>

## <a name="create-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="37eb5-131">通过使用 EWS 托管 API 创建文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-131">Create a folder by using the EWS Managed API</span></span>

<span data-ttu-id="37eb5-132">下面的代码示例演示如何使用[文件夹](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)类创建新的一般文件夹的"自定义文件夹" [DisplayName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)和 IPF [FolderClass](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx)属性值。请注意。</span><span class="sxs-lookup"><span data-stu-id="37eb5-132">The following code example shows how to use the [Folder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) class to create a new generic folder with a [DisplayName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) of "Custom Folder" and a [FolderClass](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx) property value of IPF.Note.</span></span> <span data-ttu-id="37eb5-133">[Folder.Save](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx)方法将文件夹另存为收件箱文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-133">The [Folder.Save](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) method saves the folder as a child folder of the Inbox folder.</span></span> 
  
<span data-ttu-id="37eb5-134">这些示例假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="37eb5-134">These examples assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create a custom folder.
Folder folder = new Folder(service);
folder.DisplayName = "Custom Folder";
folder.FolderClass = "IPF.Note";
// Save the folder as a child folder of the Inbox.
folder.Save(WellKnownFolderName.Inbox);
```

<span data-ttu-id="37eb5-135">若要创建不同类型的文件夹，如[CalendarFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx)、 [ContactsFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx)、 [SearchFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)或[TasksFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx)，创建 （而不是通用的**文件夹**类中） 的特定类的新实例并不设置**FolderClass**属性。</span><span class="sxs-lookup"><span data-stu-id="37eb5-135">To create a different type of folder, such as a [CalendarFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx), [ContactsFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx), [SearchFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), or [TasksFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx), create a new instance of the specific class (instead of the generic **Folder** class) and do not set the **FolderClass** property.</span></span> <span data-ttu-id="37eb5-136">例如，下面的代码示例演示如何创建新[TasksFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="37eb5-136">For example, the following code example shows how to create a new [TasksFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx).</span></span>
  
```cs
// Create a custom Tasks folder.
TasksFolder folder = new TasksFolder(service);
folder.DisplayName = "Custom Tasks";
// Save the folder as a child folder in the Inbox folder.
// This method call results in a CreateFolder call to EWS.
folder.Save(WellKnownFolderName.Inbox);
```

<span data-ttu-id="37eb5-137">如果您尝试创建的特定类的实例并设置**FolderClass**属性，则引发[ErrorNoFolderClassOverride](http://msdn.microsoft.com/zh-cn/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx)错误。</span><span class="sxs-lookup"><span data-stu-id="37eb5-137">If you try to create an instance of a specific class and also set the **FolderClass** property, the [ErrorNoFolderClassOverride](http://msdn.microsoft.com/zh-cn/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) error is thrown.</span></span> 
  
<span data-ttu-id="37eb5-138">请注意，您无法使用 EWS 托管 API 批处理创建一个方法调用中的多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-138">Note that you cannot batch the creation of multiple folders in a single method call by using the EWS Managed API.</span></span>
  
## <a name="create-a-folder-by-using-ews"></a><span data-ttu-id="37eb5-139">通过使用 EWS 创建文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-139">Create a folder by using EWS</span></span>
<span data-ttu-id="37eb5-140"><a name="bk_createfolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-140"></span></span>

<span data-ttu-id="37eb5-141">您可以使用 EWS 创建一个文件夹的倍数。</span><span class="sxs-lookup"><span data-stu-id="37eb5-141">You can create a single folder or multiple of folders by using EWS.</span></span>
  
<span data-ttu-id="37eb5-142">若要创建一个文件夹，请发送[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)操作请求消息。</span><span class="sxs-lookup"><span data-stu-id="37eb5-142">To create a single folder, send a [CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) operation request message.</span></span> <span data-ttu-id="37eb5-143">**CreateFolder**操作请求指示父文件夹收件箱、 [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx)是"自定义文件夹"，并且[FolderClass](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)元素值都 IPF。请注意。</span><span class="sxs-lookup"><span data-stu-id="37eb5-143">The **CreateFolder** operation request indicates that the parent folder is the Inbox, the [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx) is "Custom Folder", and the [FolderClass](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) element value is IPF.Note.</span></span> 
  
<span data-ttu-id="37eb5-144">这也是创建一个新文件夹，然后调用[Folder.Save](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx)方法时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="37eb5-144">This is also the XML request that the EWS Managed API sends when you create a new folder and call the [Folder.Save](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateFolder>
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderId>
      <m:Folders>
        <t:Folder>
          <t:FolderClass>IPF.Note</t:FolderClass>
          <t:DisplayName>Custom Folder</t:DisplayName>
        </t:Folder>
      </m:Folders>
    </m:CreateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="37eb5-145">服务器响应**CreateFolder**请求[CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx)邮件包含**NoError**，这表明已成功创建文件夹，并[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)的[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值新创建的消息。</span><span class="sxs-lookup"><span data-stu-id="37eb5-145">The server responds to the **CreateFolder** request with a [CreateFolderResponse](http://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the folder was created successfully, and the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="37eb5-146">若要创建多个文件夹，请在**CreateFolder**操作请求邮件中包含多个[文件夹](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="37eb5-146">To create multiple folders, include multiple [Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) elements in the **CreateFolder** operation request message.</span></span> <span data-ttu-id="37eb5-147">所有新的文件夹必须位于同一个父文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-147">All the new folders must be in the same parent folder.</span></span> 
  
## <a name="create-a-folder-hierarchy-by-using-ews"></a><span data-ttu-id="37eb5-148">使用 EWS 创建文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="37eb5-148">Create a folder hierarchy by using EWS</span></span>
<span data-ttu-id="37eb5-149"><a name="bk_createfolderhierarchy"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-149"></span></span>

<span data-ttu-id="37eb5-150">通过使用 EWS [CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx)操作，可以在单个调用中创建文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="37eb5-150">You can create a folder hierarchy in a single call by using the EWS [CreateFolderPath](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="37eb5-151">相同的功能不可用 EWS 托管 API 中。</span><span class="sxs-lookup"><span data-stu-id="37eb5-151">The same functionality is not available in the EWS Managed API.</span></span> <span data-ttu-id="37eb5-152">相反，如果您使用 EWS 托管 API，您可以创建文件夹，逐个[创建通过使用 EWS 文件夹](#bk_createfolderews)中所示。</span><span class="sxs-lookup"><span data-stu-id="37eb5-152">Instead, if you are using the EWS Managed API, you can create folders one by one, as shown in [Create a folder by using EWS](#bk_createfolderews).</span></span>
  
> [!NOTE]
> <span data-ttu-id="37eb5-153">EWS 托管 API 无法实现此功能。</span><span class="sxs-lookup"><span data-stu-id="37eb5-153">The EWS Managed API does not implement this functionality.</span></span> 
  
## <a name="get-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="37eb5-154">使用 EWS 托管 API 获取文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-154">Get a folder by using the EWS Managed API</span></span>
<span data-ttu-id="37eb5-155"><a name="bk_getfolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-155"></span></span>

<span data-ttu-id="37eb5-156">下面的代码示例演示如何使用[Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法来获取收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-156">The following code example shows how to use the [Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to get the Inbox folder.</span></span> <span data-ttu-id="37eb5-157">作为最佳实践，限制返回到仅所需要的应用程序的属性。</span><span class="sxs-lookup"><span data-stu-id="37eb5-157">As a best practice, limit the properties returned to only those required for your application.</span></span> <span data-ttu-id="37eb5-158">此示例将限制要创建[属性集](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)对象，并将[IdOnly](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx)值应用于[BasePropertySet](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx)属性仅包含[Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx)属性的返回属性。</span><span class="sxs-lookup"><span data-stu-id="37eb5-158">This example limits the return properties to only include the [Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) property by creating a [PropertySet](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) object and applying the [IdOnly](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) value to the [BasePropertySet](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx) property.</span></span> 
  
<span data-ttu-id="37eb5-159">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="37eb5-159">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
// In this scenario, you only need the FolderId.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get only the properties specified in the PropertySet.
// This method call results in a GetFolder call to EWS.
Folder rootfolder = Folder.Bind(service, WellKnownFolderName.Inbox, propSet);
```

<span data-ttu-id="37eb5-160">如果需要返回其他属性，将从[FolderSchema](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx)类的属性添加到**属性集**，或使用重载之一返回第一个类的所有属性的[绑定](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)的方法。</span><span class="sxs-lookup"><span data-stu-id="37eb5-160">If you need to return additional properties, add properties from the [FolderSchema](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx) class to the **PropertySet**, or use one of the overloaded [Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) methods that returns all first class properties.</span></span> 
  
<span data-ttu-id="37eb5-161">请注意，您无法使用 EWS 托管 API 获取多个文件夹一次。</span><span class="sxs-lookup"><span data-stu-id="37eb5-161">Note that you cannot get multiple folders at one time by using the EWS Managed API.</span></span> <span data-ttu-id="37eb5-162">您必须单独对每个文件夹调用**绑定**方法。</span><span class="sxs-lookup"><span data-stu-id="37eb5-162">You have to call the **Bind** method on each folder separately.</span></span> 
  
## <a name="get-a-folder-by-using-ews"></a><span data-ttu-id="37eb5-163">使用 EWS 获取文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-163">Get a folder by using EWS</span></span>
<span data-ttu-id="37eb5-164"><a name="bk_getfolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-164"></span></span>

<span data-ttu-id="37eb5-165">您可以通过使用 EWS 获取一个文件夹或多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-165">You can get a single folder or multiple folders by using EWS.</span></span>
  
<span data-ttu-id="37eb5-166">若要获取一个文件夹，请向服务器发送[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求消息。</span><span class="sxs-lookup"><span data-stu-id="37eb5-166">To get a single folder, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to the server.</span></span> <span data-ttu-id="37eb5-167">在以下示例中，设置[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)到**IdOnly**，返回因此只有[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)指定的文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-167">In the following example, the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) is set to **IdOnly**, so only the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the specified folder is returned.</span></span> <span data-ttu-id="37eb5-168">[FolderIds](http://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx)元素表示检索文件夹收件箱文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-168">The [FolderIds](http://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx) element indicates that the folder to retrieve is the Inbox folder.</span></span> 
  
<span data-ttu-id="37eb5-169">这也是 EWS 托管 API 时您绑定到文件夹，使用[Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="37eb5-169">This is also the XML request that the EWS Managed API sends when you bind to a folder by using the [Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="37eb5-170">若要获取多个文件夹，请在**GetFolder**操作请求邮件中包含多个[FolderIds](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="37eb5-170">To get multiple folders, include multiple [FolderIds](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) elements in the **GetFolder** operation request message.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="inbox" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="37eb5-171">下面的 XML 示例演示从服务器发送到客户端以响应**GetFolder**操作请求[GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息。</span><span class="sxs-lookup"><span data-stu-id="37eb5-171">The following XML example shows the [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that is sent from the server to the client in response to the **GetFolder** operation request.</span></span> <span data-ttu-id="37eb5-172">它只包含收件箱文件夹的[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="37eb5-172">It only contains the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) value of the Inbox folder.</span></span> <span data-ttu-id="37eb5-173">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="37eb5-173">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="800"
                         MinorBuildNumber="16"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAENAAA=" ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAEkbCr"/>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="get-a-folder-hierarchy-by-using-the-ews-managed-api"></a><span data-ttu-id="37eb5-174">通过使用 EWS 托管 API 获取文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="37eb5-174">Get a folder hierarchy by using the EWS Managed API</span></span>
<span data-ttu-id="37eb5-175"><a name="bk_getfolderhierarchyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-175"></span></span>

<span data-ttu-id="37eb5-176">下面的代码示例演示如何检索指定的根文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-176">The following code example shows how to retrieve the subfolders for a specified root folder.</span></span> <span data-ttu-id="37eb5-177">此示例检索**MsgFolderRoot**文件夹，是 （邮箱文件夹和项目存储） IPM 子树的根的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-177">This example retrieves the subfolders of the **MsgFolderRoot** folder, which is the root of the IPM Subtree (where your mailbox folders and items are stored).</span></span> 
  
<span data-ttu-id="37eb5-178">本示例中，创建[FolderView](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)类对象来限制[Folder.FindFolders](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)方法响应的结果。</span><span class="sxs-lookup"><span data-stu-id="37eb5-178">In this example, a [FolderView](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class object is created to limit the results of the [Folder.FindFolders](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method response.</span></span> <span data-ttu-id="37eb5-179">此方案限制属性可返回与以下： [Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx)、 [DisplayName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)和扩展的属性，指示是否文件夹是隐藏的文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-179">This scenario limits the properties to return to the following: [Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx), [DisplayName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx), and the extended property that indicates whether the folder is a hidden folder.</span></span> <span data-ttu-id="37eb5-180">[FolderView.Traversal](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx)值设置为深入执行递归搜索，以便服务器检索子文件夹，并将根文件夹设置为**MsgFolderRoot**，，，以便服务器将返回所有用户的文件夹 （和服务器不会返回系统文件夹的非 IPM 子树中）。</span><span class="sxs-lookup"><span data-stu-id="37eb5-180">Set the [FolderView.Traversal](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx) value to Deep to perform a recursive search so that the server retrieves the subfolders, and set the root folder to **MsgFolderRoot**, so that the server returns all the user's folders (and the server does not return system folders in the Non-IPM Subtree).</span></span>
  
<span data-ttu-id="37eb5-181">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="37eb5-181">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```XML
// Create a new folder view, and pass in the maximum number of folders to return.
FolderView view = new FolderView(folderViewSize);
// Create an extended property definition for the PR_ATTR_HIDDEN property,
// so that your results will indicate whether the folder is a hidden folder.
ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
// As a best practice, limit the properties returned to only those required.
// In this case, return the folder ID, DisplayName, and the value of the isHiddenProp
// extended property.
view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, isHiddenProp);
// Indicate a Traversal value of Deep, so that all subfolders are retrieved.
view.Traversal = FolderTraversal.Deep;
// Call FindFolders to retrieve the folder hierarchy, starting with the MsgFolderRoot folder.
// This method call results in a FindFolder call to EWS.
FindFoldersResults findFolderResults = service.FindFolders(WellKnownFolderName.MsgFolderRoot, view);
```

## <a name="get-a-folder-hierarchy-by-using-ews"></a><span data-ttu-id="37eb5-182">通过使用 EWS 获取文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="37eb5-182">Get a folder hierarchy by using EWS</span></span>
<span data-ttu-id="37eb5-183"><a name="bk_getfolderhierarchyews"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-183"></span></span>

<span data-ttu-id="37eb5-184">下面的 XML 示例演示如何使用[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)操作使用 EWS 检索文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="37eb5-184">The following XML examples show how to use the [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation to retrieve a folder hierarchy by using EWS.</span></span> <span data-ttu-id="37eb5-185">此示例检索**msgfolderroot**文件夹，是 IPM 子树，及其所有子文件夹的根目录。</span><span class="sxs-lookup"><span data-stu-id="37eb5-185">This example retrieves the **msgfolderroot** folder, which is the root of the IPM Subtree, and all its subfolders.</span></span> <span data-ttu-id="37eb5-186">**遍历**属性设置为**深入**，以便服务器执行递归搜索文件夹层次结构，并仅在响应中返回文件夹和指定的根目录下的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-186">The **Traversal** attribute is set to **Deep** so that the server performs a recursive search of the folder hierarchy and only returns folders and subfolders under the specified root in the response.</span></span> <span data-ttu-id="37eb5-187">本示例中， [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly** ，以便服务器仅返回[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="37eb5-187">In this example, the [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element is set to **IdOnly** so that the server only returns the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="37eb5-188">若要使输出更易于理解，包括[AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx)元素中请求，以及**PR_ATTR_HIDDEN** **ExtendedFieldURI**值在结果中包含的**DisplayName**元素属性，以便您知道是否文件夹是隐藏的文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-188">To make the output easier to understand, include the **DisplayName** element in your results by including it in the [AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) element in the request, along with the **ExtendedFieldURI** value for the **PR_ATTR_HIDDEN** property, so that you know whether the folders are hidden folders.</span></span> 
  
<span data-ttu-id="37eb5-189">这也是在调用[FindFolders](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)方法时，将发送 EWS 托管 API 的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="37eb5-189">This is also the XML request that the EWS Managed API sends when you call the [FindFolders](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="37eb5-190">下面的 XML 示例演示从服务器发送到客户端以响应**FindFolder**操作请求[FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx)消息。</span><span class="sxs-lookup"><span data-stu-id="37eb5-190">The following XML example shows the [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that is sent from the server to the client in response to the **FindFolder** operation request.</span></span> <span data-ttu-id="37eb5-191">它包含仅[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)， [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx)，并且的**PR_ATTR_HIDDEN**值扩展**msgrootfolder**文件夹下的所有子文件夹的属性。</span><span class="sxs-lookup"><span data-stu-id="37eb5-191">It contains only the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx), the [DisplayName](http://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx), and the value of the **PR_ATTR_HIDDEN** extended property for all the subfolders under the **msgrootfolder** folder.</span></span> <span data-ttu-id="37eb5-192">如果[Value](http://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx)元素设置为 true，则文件夹应隐藏客户端视图中。</span><span class="sxs-lookup"><span data-stu-id="37eb5-192">If the [Value](http://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx) element is set to true, the folder should be hidden in the client view.</span></span> 
  
<span data-ttu-id="37eb5-193">这也是 EWS 托管 API 发送时使用[FindFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)方法获取多个文件夹的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="37eb5-193">This is also the XML response that the EWS Managed API sends when you get multiple folders by using the [FindFolder](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="37eb5-194">具有已的某些属性和元素的值可以缩短为便于阅读，并且尚未为简便起见包含某些文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-194">The values of some attributes and elements have been shortened for readability, and some folders have not been included for brevity.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="815"
                         MinorBuildNumber="6"
                         Version="V2_7"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="16"
                        TotalItemsInView="16"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:CalendarFolder>
                <t:FolderId Id="AAAEOAAA="
                            ChangeKey="AgAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA3"/>
                <t:DisplayName>Calendar</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:CalendarFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAEPAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAA4"/>
                <t:DisplayName>Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>false</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="AAAUKAAA="
                            ChangeKey="AwAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAAS5"/>
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AAAUJAAA="
                            ChangeKey="AQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAAAASx"/>
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean"/>
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
…
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

## <a name="update-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="37eb5-195">使用 EWS 托管 API 更新文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-195">Update a folder by using the EWS Managed API</span></span>
<span data-ttu-id="37eb5-196"><a name="bk_updatefolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-196"></span></span>

<span data-ttu-id="37eb5-197">下面的代码示例演示如何通过使用 EWS 托管 API 更新文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="37eb5-197">The following code example shows how to update the display name of a folder by using the EWS Managed API.</span></span>
  
<span data-ttu-id="37eb5-198">首先，创建[属性集](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)来限制服务器[Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)响应中返回的属性的数目。</span><span class="sxs-lookup"><span data-stu-id="37eb5-198">First, create a [PropertySet](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to limit the number of properties that the server returns in the [Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) response.</span></span> <span data-ttu-id="37eb5-199">我们建议使用**IdOnly** **BasePropertySet**以减少与 Exchange 数据库的呼叫。</span><span class="sxs-lookup"><span data-stu-id="37eb5-199">We recommend that you use the **IdOnly** **BasePropertySet** to reduce calls to the Exchange database.</span></span> <span data-ttu-id="37eb5-200">接下来，使用**Bind**方法绑定到的文件夹更新。</span><span class="sxs-lookup"><span data-stu-id="37eb5-200">Next, use the **Bind** method to bind to the folder to update.</span></span> <span data-ttu-id="37eb5-201">然后，更新的[DisplayName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)属性，并使用[Folder.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法以保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="37eb5-201">Then, update the [DisplayName](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) property, and use the [Folder.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
  
<span data-ttu-id="37eb5-202">本示例中，我们假定该**服务**是有效的[ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象和用户已经过身份验证到 Exchange 服务器。</span><span class="sxs-lookup"><span data-stu-id="37eb5-202">In this example, we assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="37eb5-203">本地变量*文件夹 Id*是文件夹的[Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx)的更新。</span><span class="sxs-lookup"><span data-stu-id="37eb5-203">The local variable  *folderId*  is the [Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) of the folder to update.</span></span> 
  
```cs
// As a best practice, only include the ID value in the PropertySet.
PropertySet propertySet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get the FolderId.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId, propertySet);
// Update the display name of the folder.
folder.DisplayName = "Updated folder name";
// Save the updates.
// This method call results in an UpdateFolder call to EWS.
folder.Update();

```

## <a name="update-a-folder-by-using-ews"></a><span data-ttu-id="37eb5-204">使用 EWS 更新文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-204">Update a folder by using EWS</span></span>
<span data-ttu-id="37eb5-205"><a name="bk_updatefolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-205"></span></span>

<span data-ttu-id="37eb5-206">下面的 XML 示例演示如何使用 EWS 更新文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="37eb5-206">The following XML examples show how to update the display name of a folder by using EWS.</span></span>
  
<span data-ttu-id="37eb5-207">首先，发送[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求邮件以获取更新的文件夹中[获取文件夹层次结构使用 EWS](#bk_getfolderhierarchyews)所示。</span><span class="sxs-lookup"><span data-stu-id="37eb5-207">First, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to get the folder to update, as shown in [Get a folder hierarchy by using EWS](#bk_getfolderhierarchyews).</span></span>
  
<span data-ttu-id="37eb5-208">接下来，向要更新文件夹的服务器发送[UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)操作请求消息。</span><span class="sxs-lookup"><span data-stu-id="37eb5-208">Next, send an [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation request message to the server to update a folder.</span></span> <span data-ttu-id="37eb5-209">**UpdateFolder**操作请求更新[DisplayName](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)为"更新自定义文件夹"。</span><span class="sxs-lookup"><span data-stu-id="37eb5-209">The **UpdateFolder** operation request updates the [DisplayName](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) to "Updated Custom Folder".</span></span> 
  
<span data-ttu-id="37eb5-210">这也是 XML 请求 EWS 托管 API 发送时使用[Folder.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法更新文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-210">This is also the XML request that the EWS Managed API sends when you update a folder by using the [Folder.Update](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="37eb5-211">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="37eb5-211">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWb" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName" />
              <t:Folder>
                <t:DisplayName>Updated Custom Folder</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="37eb5-212">服务器响应包含[UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)消息**UpdateFolder**请求的[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，以及与更新**已更新的文件夹的[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)更改密钥**属性值。</span><span class="sxs-lookup"><span data-stu-id="37eb5-212">The server responds to the **UpdateFolder** request with a [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, and the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the folder that was updated with an updated **ChangeKey** attribute value.</span></span> 
  
## <a name="delete-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="37eb5-213">使用 EWS 托管 API 删除文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-213">Delete a folder by using the EWS Managed API</span></span>
<span data-ttu-id="37eb5-214"><a name="bk_deletefolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-214"></span></span>

<span data-ttu-id="37eb5-215">本文提供了一个基本示例，演示如何使用 EWS 托管 API 中删除一个文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-215">This article provides a basic example that shows you how to delete a folder by using the EWS Managed API.</span></span> <span data-ttu-id="37eb5-216">有关删除文件夹的详细信息，请参阅[删除在 Exchange 使用 EWS 的项](deleting-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="37eb5-216">For more details about deleting folders, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="37eb5-217">要通过使用 EWS 托管 API 中删除一个文件夹，首先，使用[Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法绑定到的文件夹的服务对象删除。</span><span class="sxs-lookup"><span data-stu-id="37eb5-217">To delete a folder by using the EWS Managed API, first, use the [Folder.Bind](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to bind to the service object to the folder to delete.</span></span> <span data-ttu-id="37eb5-218">接下来，使用[Folder.Delete](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx)方法使用[HardDelete](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx)删除模式中删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-218">Next, use the [Folder.Delete](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) method to delete the folder by using the [HardDelete](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx) deletion mode.</span></span> 
  
<span data-ttu-id="37eb5-219">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="37eb5-219">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="37eb5-220">本地变量*文件夹 Id*是[Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx)的文件夹中删除。</span><span class="sxs-lookup"><span data-stu-id="37eb5-220">The local variable  *folderId*  is the [Id](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) of the folder to delete.</span></span> 
  
```cs
// Bind to an existing folder and get all its properties.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId);
// HardDelete the folder.
// This method call results in a DeleteFolder call to EWS.
folder.Delete(DeleteMode.HardDelete);
```

## <a name="delete-a-folder-by-using-ews"></a><span data-ttu-id="37eb5-221">使用 EWS 删除文件夹</span><span class="sxs-lookup"><span data-stu-id="37eb5-221">Delete a folder by using EWS</span></span>
<span data-ttu-id="37eb5-222"><a name="bk_deletefolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-222"></span></span>

<span data-ttu-id="37eb5-223">本文提供的基本的 XML 示例，演示如何使用 EWS 删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-223">This article provides a basic XML example that shows you how to delete a folder by using EWS.</span></span> <span data-ttu-id="37eb5-224">有关删除文件夹的详细信息，请参阅[删除在 Exchange 使用 EWS 的项](deleting-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="37eb5-224">For more details about deleting folders, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="37eb5-225">使用 EWS 中删除一个文件夹，首先，发送[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求邮件以获取更新[获取使用 EWS 文件夹](#bk_getfolderews)中所示的文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-225">To delete a folder by using EWS, first, send a [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to get the folder to update as shown in [Get a folder by using EWS](#bk_getfolderews).</span></span> 
  
<span data-ttu-id="37eb5-226">接下来，向服务器删除文件夹发送[DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)操作请求消息。</span><span class="sxs-lookup"><span data-stu-id="37eb5-226">Next, send a [DeleteFolder](http://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) operation request message to the server to delete the folder.</span></span> <span data-ttu-id="37eb5-227">**DeleteFolder**操作请求指示**DeleteType** **HardDelete** ，它包括[文件夹 Id](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)的文件夹中删除。</span><span class="sxs-lookup"><span data-stu-id="37eb5-227">The **DeleteFolder** operation request indicates that the **DeleteType** is **HardDelete** and it includes the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the folder to delete.</span></span> 
  
<span data-ttu-id="37eb5-228">这也是 XML 请求 EWS 托管 API 发送时使用[Folder.Delete](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx)方法删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="37eb5-228">This is also the XML request that the EWS Managed API sends when you delete a folder by using the [Folder.Delete](http://msdn.microsoft.com/zh-cn/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="37eb5-229">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="37eb5-229">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteFolder DeleteType="HardDelete">
      <m:FolderIds>
        <t:FolderId Id="OrV9ZAAA=" ChangeKey="AQAAABYAAABVzRdyy/cHS4XTC9itCRdUAAAOrXWf" />
      </m:FolderIds>
    </m:DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="37eb5-230">服务器响应包含[DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx)消息**DeleteFolder**请求**NoError**，这表明文件夹删除成功[ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="37eb5-230">The server responds to the **DeleteFolder** request with a [DeleteFolderResponse](http://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/zh-cn/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the folder deletion was successful.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="37eb5-231">后续步骤</span><span class="sxs-lookup"><span data-stu-id="37eb5-231">Next steps</span></span>
<span data-ttu-id="37eb5-232"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="37eb5-232"></span></span>

<span data-ttu-id="37eb5-233">您已检索到的文件夹的服务器上，或对文件夹进行更改之后，您可能希望为[同步文件夹层次结构](how-to-synchronize-folders-by-using-ews-in-exchange.md)或服务器上的[订阅有关文件夹更改的通知](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="37eb5-233">After you have retrieved the folders on the server, or made changes to folders, you might want to [synchronize your folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [subscribe to notifications about folder changes](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) on the server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="37eb5-234">另请参阅</span><span class="sxs-lookup"><span data-stu-id="37eb5-234">See also</span></span>

- [<span data-ttu-id="37eb5-235">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="37eb5-235">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)   
- [<span data-ttu-id="37eb5-236">通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目</span><span class="sxs-lookup"><span data-stu-id="37eb5-236">Work with Exchange mailbox items by using EWS in Exchange</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="37eb5-237">通过在 Exchange 使用 EWS 中删除项目</span><span class="sxs-lookup"><span data-stu-id="37eb5-237">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="37eb5-238">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="37eb5-238">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

