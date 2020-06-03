---
title: 使用 Exchange 中的 EWS 处理文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 4b3eb746-74c4-42a0-aa2c-742c147f1871
description: 了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除文件夹。
localization_priority: Priority
ms.openlocfilehash: a184d8da4d6949f01f47afc6a9fb7ed30729fd3b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456379"
---
# <a name="work-with-folders-by-using-ews-in-exchange"></a><span data-ttu-id="d7326-103">使用 Exchange 中的 EWS 处理文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-103">Work with folders by using EWS in Exchange</span></span>

<span data-ttu-id="d7326-104">了解如何使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-104">Learn how to create, get, update, and delete folders by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="d7326-105">Exchange 中的 EWS 使用文件夹来组织和整理邮箱。</span><span class="sxs-lookup"><span data-stu-id="d7326-105">EWS in Exchange uses folders to structure and organize mailboxes.</span></span> <span data-ttu-id="d7326-106">您可以使用 EWS 托管 API 或 EWS 创建新的、获取、更新和删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-106">You can create new, get, update, and delete folders by using the EWS Managed API or EWS.</span></span> <span data-ttu-id="d7326-107">下表中列出的每个方法或操作都是针对[folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)对象、[文件夹](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)类型或[一个派生的文件夹类或类型](folders-and-items-in-ews-in-exchange.md#bk_folders)执行的。</span><span class="sxs-lookup"><span data-stu-id="d7326-107">Each of the methods or operations listed in the following table is performed on a [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) object, a [Folder](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) type, or [one of the derived folder classes or types](folders-and-items-in-ews-in-exchange.md#bk_folders).</span></span>
  
<span data-ttu-id="d7326-108">**表1。用于创建、获取、更新和删除文件夹的方法和操作**</span><span class="sxs-lookup"><span data-stu-id="d7326-108">**Table 1. Methods and operations for creating, getting, updating and deleting folders**</span></span>

|<span data-ttu-id="d7326-109">**若要...**</span><span class="sxs-lookup"><span data-stu-id="d7326-109">**In order to…**</span></span>|<span data-ttu-id="d7326-110">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="d7326-110">**EWS Managed API method**</span></span>|<span data-ttu-id="d7326-111">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="d7326-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7326-112">创建文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-112">Create a folder</span></span>  <br/> |[<span data-ttu-id="d7326-113">文件夹。保存</span><span class="sxs-lookup"><span data-stu-id="d7326-113">Folder.Save</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d7326-114">CreateFolder</span><span class="sxs-lookup"><span data-stu-id="d7326-114">CreateFolder</span></span>](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d7326-115">创建文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="d7326-115">Create a folder hierarchy</span></span>  <br/> |<span data-ttu-id="d7326-116">不可用</span><span class="sxs-lookup"><span data-stu-id="d7326-116">Not available</span></span>  <br/> |[<span data-ttu-id="d7326-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="d7326-117">CreateFolderPath</span></span>](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d7326-118">获取文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-118">Get a folder</span></span>  <br/> |[<span data-ttu-id="d7326-119">文件夹。绑定</span><span class="sxs-lookup"><span data-stu-id="d7326-119">Folder.Bind</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d7326-120">GetFolder</span><span class="sxs-lookup"><span data-stu-id="d7326-120">GetFolder</span></span>](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d7326-121">获取文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="d7326-121">Get a folder hierarchy</span></span>  <br/> |[<span data-ttu-id="d7326-122">FindFolders</span><span class="sxs-lookup"><span data-stu-id="d7326-122">Folder.FindFolders</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d7326-123">FindFolder</span><span class="sxs-lookup"><span data-stu-id="d7326-123">FindFolder</span></span>](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d7326-124">更新文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-124">Update a folder</span></span>  <br/> |[<span data-ttu-id="d7326-125">文件夹。更新</span><span class="sxs-lookup"><span data-stu-id="d7326-125">Folder.Update</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d7326-126">UpdateFolder</span><span class="sxs-lookup"><span data-stu-id="d7326-126">UpdateFolder</span></span>](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="d7326-127">删除文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-127">Delete a folder</span></span>  <br/> |[<span data-ttu-id="d7326-128">文件夹。删除</span><span class="sxs-lookup"><span data-stu-id="d7326-128">Folder.Delete</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="d7326-129">DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="d7326-129">DeleteFolder</span></span>](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |

<span data-ttu-id="d7326-130"><a name="bk_createfolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-130"><a name="bk_createfolderewsma"> </a></span></span>

## <a name="create-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="d7326-131">使用 EWS 托管 API 创建文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-131">Create a folder by using the EWS Managed API</span></span>

<span data-ttu-id="d7326-132">下面的代码示例演示如何使用[Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx)类创建一个显示[DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)为 "Custom Folder" 和[FolderClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx)属性值为 IPF 的新通用文件夹。便笺.</span><span class="sxs-lookup"><span data-stu-id="d7326-132">The following code example shows how to use the [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) class to create a new generic folder with a [DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) of "Custom Folder" and a [FolderClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.folderclass%28v=exchg.80%29.aspx) property value of IPF.Note.</span></span> <span data-ttu-id="d7326-133">[Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx)方法将文件夹另存为 "收件箱" 文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-133">The [Folder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) method saves the folder as a child folder of the Inbox folder.</span></span> 
  
<span data-ttu-id="d7326-134">这些示例假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="d7326-134">These examples assume that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create a custom folder.
Folder folder = new Folder(service);
folder.DisplayName = "Custom Folder";
folder.FolderClass = "IPF.Note";
// Save the folder as a child folder of the Inbox.
folder.Save(WellKnownFolderName.Inbox);
```

<span data-ttu-id="d7326-135">若要创建其他类型的文件夹（如[CalendarFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx)、 [ContactsFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx)、 [SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx)或[TasksFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx)），请创建特定类（而不是通用**folder**类）的新实例，并且不要设置**FolderClass**属性。</span><span class="sxs-lookup"><span data-stu-id="d7326-135">To create a different type of folder, such as a [CalendarFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx), [ContactsFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx), [SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx), or [TasksFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx), create a new instance of the specific class (instead of the generic **Folder** class) and do not set the **FolderClass** property.</span></span> <span data-ttu-id="d7326-136">例如，下面的代码示例演示如何创建新的[TasksFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="d7326-136">For example, the following code example shows how to create a new [TasksFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx).</span></span>
  
```cs
// Create a custom Tasks folder.
TasksFolder folder = new TasksFolder(service);
folder.DisplayName = "Custom Tasks";
// Save the folder as a child folder in the Inbox folder.
// This method call results in a CreateFolder call to EWS.
folder.Save(WellKnownFolderName.Inbox);
```

<span data-ttu-id="d7326-137">如果尝试创建特定类的实例，同时又设置**FolderClass**属性，则会引发[ErrorNoFolderClassOverride](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx)错误。</span><span class="sxs-lookup"><span data-stu-id="d7326-137">If you try to create an instance of a specific class and also set the **FolderClass** property, the [ErrorNoFolderClassOverride](https://msdn.microsoft.com/library/exchangewebservices.responsecodetype%28v=exchg.80%29.aspx) error is thrown.</span></span> 
  
<span data-ttu-id="d7326-138">请注意，使用 EWS 托管 API 无法在单个方法调用中批量创建多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-138">Note that you cannot batch the creation of multiple folders in a single method call by using the EWS Managed API.</span></span>
  
## <a name="create-a-folder-by-using-ews"></a><span data-ttu-id="d7326-139">使用 EWS 创建文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-139">Create a folder by using EWS</span></span>
<span data-ttu-id="d7326-140"><a name="bk_createfolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-140"><a name="bk_createfolderews"> </a></span></span>

<span data-ttu-id="d7326-141">您可以使用 EWS 创建单个文件夹或多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-141">You can create a single folder or multiple of folders by using EWS.</span></span>
  
<span data-ttu-id="d7326-142">若要创建单个文件夹，请发送[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx)操作请求消息。</span><span class="sxs-lookup"><span data-stu-id="d7326-142">To create a single folder, send a [CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) operation request message.</span></span> <span data-ttu-id="d7326-143">**CreateFolder**操作请求指示父文件夹是收件箱， [DisplayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx)为 "Custom Folder"，而[FolderClass](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx)元素值为 IPF。便笺.</span><span class="sxs-lookup"><span data-stu-id="d7326-143">The **CreateFolder** operation request indicates that the parent folder is the Inbox, the [DisplayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx) is "Custom Folder", and the [FolderClass](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) element value is IPF.Note.</span></span> 
  
<span data-ttu-id="d7326-144">这也是在创建新文件夹并调用[folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx)方法时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d7326-144">This is also the XML request that the EWS Managed API sends when you create a new folder and call the [Folder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="d7326-145">服务器使用[CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx)邮件响应**CreateFolder**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，该值指示文件夹已成功创建，以及新创建的邮件的[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d7326-145">The server responds to the **CreateFolder** request with a [CreateFolderResponse](https://msdn.microsoft.com/library/158adecc-491a-47d9-af73-acc2cd3f8566%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the folder was created successfully, and the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="d7326-146">若要创建多个文件夹，请在**CreateFolder**操作请求邮件中包含多个[Folder](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="d7326-146">To create multiple folders, include multiple [Folder](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) elements in the **CreateFolder** operation request message.</span></span> <span data-ttu-id="d7326-147">所有新文件夹都必须位于同一个父文件夹中。</span><span class="sxs-lookup"><span data-stu-id="d7326-147">All the new folders must be in the same parent folder.</span></span> 
  
## <a name="create-a-folder-hierarchy-by-using-ews"></a><span data-ttu-id="d7326-148">使用 EWS 创建文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="d7326-148">Create a folder hierarchy by using EWS</span></span>
<span data-ttu-id="d7326-149"><a name="bk_createfolderhierarchy"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-149"><a name="bk_createfolderhierarchy"> </a></span></span>

<span data-ttu-id="d7326-150">您可以通过使用 EWS [CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx)操作在单个调用中创建文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="d7326-150">You can create a folder hierarchy in a single call by using the EWS [CreateFolderPath](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) operation.</span></span> <span data-ttu-id="d7326-151">在 EWS 托管 API 中不提供相同的功能。</span><span class="sxs-lookup"><span data-stu-id="d7326-151">The same functionality is not available in the EWS Managed API.</span></span> <span data-ttu-id="d7326-152">相反，如果使用 EWS 托管 API，可以逐个创建文件夹，如[使用 EWS 创建文件夹](#bk_createfolderews)中所示。</span><span class="sxs-lookup"><span data-stu-id="d7326-152">Instead, if you are using the EWS Managed API, you can create folders one by one, as shown in [Create a folder by using EWS](#bk_createfolderews).</span></span>
  
> [!NOTE]
> <span data-ttu-id="d7326-153">EWS 托管 API 无法实现此功能。</span><span class="sxs-lookup"><span data-stu-id="d7326-153">The EWS Managed API does not implement this functionality.</span></span> 
  
## <a name="get-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="d7326-154">使用 EWS 托管 API 获取文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-154">Get a folder by using the EWS Managed API</span></span>
<span data-ttu-id="d7326-155"><a name="bk_getfolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-155"><a name="bk_getfolderewsma"> </a></span></span>

<span data-ttu-id="d7326-156">下面的代码示例演示如何使用[Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法获取 "收件箱" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-156">The following code example shows how to use the [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to get the Inbox folder.</span></span> <span data-ttu-id="d7326-157">作为一种最佳做法，仅将返回的属性限制为您的应用程序所需的属性。</span><span class="sxs-lookup"><span data-stu-id="d7326-157">As a best practice, limit the properties returned to only those required for your application.</span></span> <span data-ttu-id="d7326-158">此示例通过创建[PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)对象并将[IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx)值应用于[BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx)属性，将返回的属性限制为仅包含[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="d7326-158">This example limits the return properties to only include the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) property by creating a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) object and applying the [IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) value to the [BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset.basepropertyset%28v=exchg.80%29.aspx) property.</span></span> 
  
<span data-ttu-id="d7326-159">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="d7326-159">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
// In this scenario, you only need the FolderId.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly);
// Bind to an existing folder and get only the properties specified in the PropertySet.
// This method call results in a GetFolder call to EWS.
Folder rootfolder = Folder.Bind(service, WellKnownFolderName.Inbox, propSet);
```

<span data-ttu-id="d7326-160">如果需要返回其他属性，请将[FolderSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx)类中的属性添加到**PropertySet**，或使用返回所有第一个类属性的重载[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法之一。</span><span class="sxs-lookup"><span data-stu-id="d7326-160">If you need to return additional properties, add properties from the [FolderSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderschema%28v=exchg.80%29.aspx) class to the **PropertySet**, or use one of the overloaded [Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) methods that returns all first class properties.</span></span> 
  
<span data-ttu-id="d7326-161">请注意，您不能使用 EWS 托管 API 一次获取多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-161">Note that you cannot get multiple folders at one time by using the EWS Managed API.</span></span> <span data-ttu-id="d7326-162">您必须分别对每个文件夹调用**Bind**方法。</span><span class="sxs-lookup"><span data-stu-id="d7326-162">You have to call the **Bind** method on each folder separately.</span></span> 
  
## <a name="get-a-folder-by-using-ews"></a><span data-ttu-id="d7326-163">使用 EWS 获取文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-163">Get a folder by using EWS</span></span>
<span data-ttu-id="d7326-164"><a name="bk_getfolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-164"><a name="bk_getfolderews"> </a></span></span>

<span data-ttu-id="d7326-165">可以使用 EWS 获取单个文件夹或多个文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-165">You can get a single folder or multiple folders by using EWS.</span></span>
  
<span data-ttu-id="d7326-166">若要获取单个文件夹，请向服务器发送[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求消息。</span><span class="sxs-lookup"><span data-stu-id="d7326-166">To get a single folder, send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to the server.</span></span> <span data-ttu-id="d7326-167">在下面的示例中， [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)设置为**IdOnly**，因此仅返回指定文件夹的[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d7326-167">In the following example, the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) is set to **IdOnly**, so only the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the specified folder is returned.</span></span> <span data-ttu-id="d7326-168">[FolderIds](https://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx)元素指示要检索的文件夹是 "收件箱" 文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-168">The [FolderIds](https://msdn.microsoft.com/library/3ff9d15a-7220-4785-ae6b-583a7eb82005%28Office.15%29.aspx) element indicates that the folder to retrieve is the Inbox folder.</span></span> 
  
<span data-ttu-id="d7326-169">这也是当您使用[folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法绑定到某个文件夹时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d7326-169">This is also the XML request that the EWS Managed API sends when you bind to a folder by using the [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="d7326-170">若要获取多个文件夹，请在**GetFolder**操作请求邮件中包含多个[FolderIds](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="d7326-170">To get multiple folders, include multiple [FolderIds](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) elements in the **GetFolder** operation request message.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="d7326-171">下面的 XML 示例展示了从服务器发送到客户端以响应**GetFolder**操作请求的[GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx)消息。</span><span class="sxs-lookup"><span data-stu-id="d7326-171">The following XML example shows the [GetFolderResponse](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) message that is sent from the server to the client in response to the **GetFolder** operation request.</span></span> <span data-ttu-id="d7326-172">它只包含 "收件箱" 文件夹的[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)值。</span><span class="sxs-lookup"><span data-stu-id="d7326-172">It only contains the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) value of the Inbox folder.</span></span> <span data-ttu-id="d7326-173">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="d7326-173">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="800"
                         MinorBuildNumber="16"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="get-a-folder-hierarchy-by-using-the-ews-managed-api"></a><span data-ttu-id="d7326-174">使用 EWS 托管 API 获取文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="d7326-174">Get a folder hierarchy by using the EWS Managed API</span></span>
<span data-ttu-id="d7326-175"><a name="bk_getfolderhierarchyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-175"><a name="bk_getfolderhierarchyewsma"> </a></span></span>

<span data-ttu-id="d7326-176">下面的代码示例演示如何检索指定根文件夹的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-176">The following code example shows how to retrieve the subfolders for a specified root folder.</span></span> <span data-ttu-id="d7326-177">本示例将检索**MsgFolderRoot**文件夹的子文件夹，该文件夹是 IPM 子树（存储邮箱文件夹和项目）的根目录。</span><span class="sxs-lookup"><span data-stu-id="d7326-177">This example retrieves the subfolders of the **MsgFolderRoot** folder, which is the root of the IPM Subtree (where your mailbox folders and items are stored).</span></span> 
  
<span data-ttu-id="d7326-178">在此示例中，将创建一个[FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx)类对象来限制[FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)方法响应的结果。</span><span class="sxs-lookup"><span data-stu-id="d7326-178">In this example, a [FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview%28v=exchg.80%29.aspx) class object is created to limit the results of the [Folder.FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method response.</span></span> <span data-ttu-id="d7326-179">此方案将属性限制为返回以下内容： [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx)、 [DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)和扩展属性，以指示文件夹是否为隐藏文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-179">This scenario limits the properties to return to the following: [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx), [DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx), and the extended property that indicates whether the folder is a hidden folder.</span></span> <span data-ttu-id="d7326-180">将[FolderView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx)值设置为 Deep 以执行递归搜索，以便服务器检索子文件夹，并将根文件夹设置为**MsgFolderRoot**，以便服务器返回用户的所有文件夹（并且服务器不在非 IPM 子树中返回系统文件夹）。</span><span class="sxs-lookup"><span data-stu-id="d7326-180">Set the [FolderView.Traversal](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderview.traversal%28v=EXCHG.80%29.aspx) value to Deep to perform a recursive search so that the server retrieves the subfolders, and set the root folder to **MsgFolderRoot**, so that the server returns all the user's folders (and the server does not return system folders in the Non-IPM Subtree).</span></span>
  
<span data-ttu-id="d7326-181">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="d7326-181">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="get-a-folder-hierarchy-by-using-ews"></a><span data-ttu-id="d7326-182">使用 EWS 获取文件夹层次结构</span><span class="sxs-lookup"><span data-stu-id="d7326-182">Get a folder hierarchy by using EWS</span></span>
<span data-ttu-id="d7326-183"><a name="bk_getfolderhierarchyews"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-183"><a name="bk_getfolderhierarchyews"> </a></span></span>

<span data-ttu-id="d7326-184">下面的 XML 示例演示如何使用[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx)操作检索文件夹层次结构（使用 EWS）。</span><span class="sxs-lookup"><span data-stu-id="d7326-184">The following XML examples show how to use the [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) operation to retrieve a folder hierarchy by using EWS.</span></span> <span data-ttu-id="d7326-185">本示例将检索**msgfolderroot**文件夹，该文件夹是 IPM 子树的根目录及其所有子文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-185">This example retrieves the **msgfolderroot** folder, which is the root of the IPM Subtree, and all its subfolders.</span></span> <span data-ttu-id="d7326-186">将 "**遍历**" 属性设置为 "**深度**"，以便服务器执行文件夹层次结构的递归搜索，并且仅在响应中的指定根下返回文件夹和子文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-186">The **Traversal** attribute is set to **Deep** so that the server performs a recursive search of the folder hierarchy and only returns folders and subfolders under the specified root in the response.</span></span> <span data-ttu-id="d7326-187">在此示例中， [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly** ，以便服务器仅返回[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)元素。</span><span class="sxs-lookup"><span data-stu-id="d7326-187">In this example, the [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) element is set to **IdOnly** so that the server only returns the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) element.</span></span> <span data-ttu-id="d7326-188">若要使输出更易于理解，请将**DisplayName**元素包含在请求中的[AdditionalProperties](https://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx)元素中，并将其包括在结果中的**ExtendedFieldURI**值和**PR_ATTR_HIDDEN**属性的值中，以便您知道这些文件夹是否为隐藏文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-188">To make the output easier to understand, include the **DisplayName** element in your results by including it in the [AdditionalProperties](https://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) element in the request, along with the **ExtendedFieldURI** value for the **PR_ATTR_HIDDEN** property, so that you know whether the folders are hidden folders.</span></span> 
  
<span data-ttu-id="d7326-189">这也是当您调用[FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx)方法时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d7326-189">This is also the XML request that the EWS Managed API sends when you call the [FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="d7326-190">下面的 XML 示例展示了从服务器发送到客户端以响应**FindFolder**操作请求的[FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx)消息。</span><span class="sxs-lookup"><span data-stu-id="d7326-190">The following XML example shows the [FindFolderResponse](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) message that is sent from the server to the client in response to the **FindFolder** operation request.</span></span> <span data-ttu-id="d7326-191">它仅包含**msgrootfolder**文件夹下所有子文件夹的**PR_ATTR_HIDDEN**扩展属性的[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx)、 [DisplayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx)和值。</span><span class="sxs-lookup"><span data-stu-id="d7326-191">It contains only the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx), the [DisplayName](https://msdn.microsoft.com/library/e7efbbe1-6629-4d11-bed1-ed899e3f9d77%28Office.15%29.aspx), and the value of the **PR_ATTR_HIDDEN** extended property for all the subfolders under the **msgrootfolder** folder.</span></span> <span data-ttu-id="d7326-192">如果[Value](https://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx)元素设置为 true，则该文件夹应在客户端视图中隐藏。</span><span class="sxs-lookup"><span data-stu-id="d7326-192">If the [Value](https://msdn.microsoft.com/library/9a30cadd-909e-41b1-b4e9-291643dd89c6%28Office.15%29.aspx) element is set to true, the folder should be hidden in the client view.</span></span> 
  
<span data-ttu-id="d7326-193">这也是在使用[FindFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx)方法获取多个文件夹时，EWS 托管 API 发送的 XML 响应。</span><span class="sxs-lookup"><span data-stu-id="d7326-193">This is also the XML response that the EWS Managed API sends when you get multiple folders by using the [FindFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="d7326-194">某些属性和元素的值已缩短以提高可读性，并且为了简洁起见，一些文件夹未包含在内。</span><span class="sxs-lookup"><span data-stu-id="d7326-194">The values of some attributes and elements have been shortened for readability, and some folders have not been included for brevity.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="815"
                         MinorBuildNumber="6"
                         Version="V2_7"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="update-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="d7326-195">使用 EWS 托管 API 更新文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-195">Update a folder by using the EWS Managed API</span></span>
<span data-ttu-id="d7326-196"><a name="bk_updatefolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-196"><a name="bk_updatefolderewsma"> </a></span></span>

<span data-ttu-id="d7326-197">下面的代码示例演示如何使用 EWS 托管 API 更新文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d7326-197">The following code example shows how to update the display name of a folder by using the EWS Managed API.</span></span>
  
<span data-ttu-id="d7326-198">首先，创建一个[PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx)以限制服务器在文件夹中返回的属性的数目。[绑定](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)响应。</span><span class="sxs-lookup"><span data-stu-id="d7326-198">First, create a [PropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to limit the number of properties that the server returns in the [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) response.</span></span> <span data-ttu-id="d7326-199">建议使用**IdOnly** **BasePropertySet**来减少对 Exchange 数据库的调用。</span><span class="sxs-lookup"><span data-stu-id="d7326-199">We recommend that you use the **IdOnly** **BasePropertySet** to reduce calls to the Exchange database.</span></span> <span data-ttu-id="d7326-200">接下来，使用**bind**方法绑定到要更新的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-200">Next, use the **Bind** method to bind to the folder to update.</span></span> <span data-ttu-id="d7326-201">然后，更新[DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx)属性，并使用[文件夹. update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法保存更改。</span><span class="sxs-lookup"><span data-stu-id="d7326-201">Then, update the [DisplayName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.displayname%28v=exchg.80%29.aspx) property, and use the [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method to save the changes.</span></span> 
  
<span data-ttu-id="d7326-202">在此示例中，我们假定**service**是有效的[ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)对象，并且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="d7326-202">In this example, we assume that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="d7326-203">本地变量*folderId*是要更新的文件夹的[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d7326-203">The local variable  *folderId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) of the folder to update.</span></span> 
  
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

## <a name="update-a-folder-by-using-ews"></a><span data-ttu-id="d7326-204">使用 EWS 更新文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-204">Update a folder by using EWS</span></span>
<span data-ttu-id="d7326-205"><a name="bk_updatefolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-205"><a name="bk_updatefolderews"> </a></span></span>

<span data-ttu-id="d7326-206">下面的 XML 示例演示如何使用 EWS 更新文件夹的显示名称。</span><span class="sxs-lookup"><span data-stu-id="d7326-206">The following XML examples show how to update the display name of a folder by using EWS.</span></span>
  
<span data-ttu-id="d7326-207">首先，发送[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求邮件以获取要更新的文件夹，如通过[使用 EWS 获取文件夹层次结构](#bk_getfolderhierarchyews)中所示。</span><span class="sxs-lookup"><span data-stu-id="d7326-207">First, send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to get the folder to update, as shown in [Get a folder hierarchy by using EWS](#bk_getfolderhierarchyews).</span></span>
  
<span data-ttu-id="d7326-208">接下来，向服务器发送[UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx)操作请求邮件，以更新文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-208">Next, send an [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) operation request message to the server to update a folder.</span></span> <span data-ttu-id="d7326-209">**UpdateFolder**操作请求将[DisplayName](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)更新为 "更新的自定义文件夹"。</span><span class="sxs-lookup"><span data-stu-id="d7326-209">The **UpdateFolder** operation request updates the [DisplayName](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) to "Updated Custom Folder".</span></span> 
  
<span data-ttu-id="d7326-210">这也是在使用[folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx)方法更新文件夹时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d7326-210">This is also the XML request that the EWS Managed API sends when you update a folder by using the [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="d7326-211">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="d7326-211">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="d7326-212">服务器使用[UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx)邮件响应**UpdateFolder**请求，其中包括 ResponseCode 值为**NoError**的[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值，以及使用更新的**FolderId**属性值更新的文件夹的[ChangeKey](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d7326-212">The server responds to the **UpdateFolder** request with a [UpdateFolderResponse](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) message that includes the a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, and the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the folder that was updated with an updated **ChangeKey** attribute value.</span></span> 
  
## <a name="delete-a-folder-by-using-the-ews-managed-api"></a><span data-ttu-id="d7326-213">使用 EWS 托管 API 删除文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-213">Delete a folder by using the EWS Managed API</span></span>
<span data-ttu-id="d7326-214"><a name="bk_deletefolderewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-214"><a name="bk_deletefolderewsma"> </a></span></span>

<span data-ttu-id="d7326-215">本文提供的基本示例展示了如何使用 EWS 托管 API 删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-215">This article provides a basic example that shows you how to delete a folder by using the EWS Managed API.</span></span> <span data-ttu-id="d7326-216">有关删除文件夹的更多详细信息，请参阅[使用 Exchange 中的 EWS 删除项目](deleting-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d7326-216">For more details about deleting folders, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="d7326-217">若要使用 EWS 托管 API 删除文件夹，请先使用[folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx)方法将该服务对象绑定到要删除的文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-217">To delete a folder by using the EWS Managed API, first, use the [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) method to bind to the service object to the folder to delete.</span></span> <span data-ttu-id="d7326-218">下一步，使用[HardDelete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx)删除模式删除[文件夹。](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d7326-218">Next, use the [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) method to delete the folder by using the [HardDelete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx) deletion mode.</span></span> 
  
<span data-ttu-id="d7326-219">此示例假定 **service** 是有效的 [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，且用户已通过 Exchange 服务器的身份验证。</span><span class="sxs-lookup"><span data-stu-id="d7326-219">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="d7326-220">本地变量*folderId*是要删除的文件夹的[Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d7326-220">The local variable  *folderId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) of the folder to delete.</span></span> 
  
```cs
// Bind to an existing folder and get all its properties.
// This method call results in a GetFolder call to EWS.
Folder folder = Folder.Bind(service, folderId);
// HardDelete the folder.
// This method call results in a DeleteFolder call to EWS.
folder.Delete(DeleteMode.HardDelete);
```

## <a name="delete-a-folder-by-using-ews"></a><span data-ttu-id="d7326-221">使用 EWS 删除文件夹</span><span class="sxs-lookup"><span data-stu-id="d7326-221">Delete a folder by using EWS</span></span>
<span data-ttu-id="d7326-222"><a name="bk_deletefolderews"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-222"><a name="bk_deletefolderews"> </a></span></span>

<span data-ttu-id="d7326-223">本文提供了一个基本的 XML 示例，演示如何使用 EWS 删除文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-223">This article provides a basic XML example that shows you how to delete a folder by using EWS.</span></span> <span data-ttu-id="d7326-224">有关删除文件夹的更多详细信息，请参阅[使用 Exchange 中的 EWS 删除项目](deleting-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d7326-224">For more details about deleting folders, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="d7326-225">若要使用 EWS 删除文件夹，请先发送[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)操作请求邮件，以获取要更新的文件夹，如[使用 EWS 获取文件夹](#bk_getfolderews)中所示。</span><span class="sxs-lookup"><span data-stu-id="d7326-225">To delete a folder by using EWS, first, send a [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) operation request message to get the folder to update as shown in [Get a folder by using EWS](#bk_getfolderews).</span></span> 
  
<span data-ttu-id="d7326-226">接下来，向服务器发送[DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx)操作请求邮件以删除该文件夹。</span><span class="sxs-lookup"><span data-stu-id="d7326-226">Next, send a [DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) operation request message to the server to delete the folder.</span></span> <span data-ttu-id="d7326-227">**DeleteFolder**操作请求指示**DeleteType**为**HardDelete** ，并包含要删除的文件夹的[FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="d7326-227">The **DeleteFolder** operation request indicates that the **DeleteType** is **HardDelete** and it includes the [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) of the folder to delete.</span></span> 
  
<span data-ttu-id="d7326-228">这也是在使用[folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx)方法删除文件夹时，EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="d7326-228">This is also the XML request that the EWS Managed API sends when you delete a folder by using the [Folder.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="d7326-229">为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="d7326-229">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="d7326-230">服务器使用[DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx)邮件响应**DeleteFolder**请求，其中包括[ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx)值**NoError**，这表示文件夹删除成功。</span><span class="sxs-lookup"><span data-stu-id="d7326-230">The server responds to the **DeleteFolder** request with a [DeleteFolderResponse](https://msdn.microsoft.com/library/27578bda-ef0a-4a33-bccc-2c1bc1735424%28Office.15%29.aspx) message that includes the a [ResponseCode](https://msdn.microsoft.com/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the folder deletion was successful.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="d7326-231">后续步骤</span><span class="sxs-lookup"><span data-stu-id="d7326-231">Next steps</span></span>
<span data-ttu-id="d7326-232"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="d7326-232"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="d7326-233">在检索了服务器上的文件夹或对文件夹进行了更改之后，您可能需要将[文件夹层次结构同步](how-to-synchronize-folders-by-using-ews-in-exchange.md)或订阅有关服务器上的[文件夹更改的通知](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="d7326-233">After you have retrieved the folders on the server, or made changes to folders, you might want to [synchronize your folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [subscribe to notifications about folder changes](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) on the server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d7326-234">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d7326-234">See also</span></span>

- [<span data-ttu-id="d7326-235">Exchange 中的 EWS 中的文件夹和项目</span><span class="sxs-lookup"><span data-stu-id="d7326-235">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)   
- [<span data-ttu-id="d7326-236">使用 Exchange 中的 EWS 处理 Exchange 邮箱项目</span><span class="sxs-lookup"><span data-stu-id="d7326-236">Work with Exchange mailbox items by using EWS in Exchange</span></span>](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="d7326-237">使用 Exchange 中的 EWS 删除项目</span><span class="sxs-lookup"><span data-stu-id="d7326-237">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)   
- [<span data-ttu-id="d7326-238">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="d7326-238">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

