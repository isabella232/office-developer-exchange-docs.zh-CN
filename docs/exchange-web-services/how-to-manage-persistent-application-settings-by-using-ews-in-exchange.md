---
title: 在 Exchange 中使用 EWS 管理持久的应用程序设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: 了解如何创建、 查找、 获取、 更新和删除在 Exchange 使用 EWS 托管 API 或 EWS 持久的应用程序设置。
ms.openlocfilehash: ab5a9cc927bd0a6c4efacce622cc71db1a9b02a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752812"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a><span data-ttu-id="a5672-103">在 Exchange 中使用 EWS 管理持久的应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-103">Manage persistent application settings by using EWS in Exchange</span></span>

<span data-ttu-id="a5672-104">了解如何创建、 查找、 获取、 更新和删除在 Exchange 使用 EWS 托管 API 或 EWS 持久的应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="a5672-104">Learn how to create, find, get, update, and delete persistent application settings by using the EWS Managed API or EWS in Exchange.</span></span> 
  
<span data-ttu-id="a5672-105">主要是因为他们已被隐藏大多数客户端应用程序中的搜索结果中，用户配置对象是用于存储为 Exchange 客户端应用程序，配置设置的最佳选项。</span><span class="sxs-lookup"><span data-stu-id="a5672-105">User configuration objects are the best option for storing configuration settings for your Exchange client application, primarily because they are hidden from search results in most client applications.</span></span> <span data-ttu-id="a5672-106">客户端应用程序通常隐藏这些设置，因为最终用户不需要查看它们，并使用户不意外地访问此信息。</span><span class="sxs-lookup"><span data-stu-id="a5672-106">Client applications typically hide these settings because the end user doesn't need to see them, and so that the user doesn't accidentally access this information.</span></span> <span data-ttu-id="a5672-107">本文中的代码示例显示您如何使用用户配置对象来管理持久的设置，包括如何创建、 查找、 获取、 更新和删除用户配置对象中存储的持久的应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="a5672-107">The code examples in this article show you how you can use user configuration objects to manage persistent settings, including how to create, find, get, update, and delete persistent application settings that are stored in user configuration objects.</span></span>

<span data-ttu-id="a5672-108"><a name="createconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-108"></span></span>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="a5672-109">使用 EWS 托管 API 创建应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-109">Create an application setting by using the EWS Managed API</span></span>

<span data-ttu-id="a5672-110">[UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS 托管 API 方法可用于创建自定义配置设置。</span><span class="sxs-lookup"><span data-stu-id="a5672-110">You can use the [UserConfiguration.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API method to create a custom configuration setting.</span></span> <span data-ttu-id="a5672-111">用户配置对象可以包含 XML，二进制、 数据字典或这三种数据类型的组合。</span><span class="sxs-lookup"><span data-stu-id="a5672-111">A user configuration object can contain XML, binary, a data dictionary, or a combination of those three data types.</span></span> <span data-ttu-id="a5672-112">下面的示例演示如何保存一个名为 ContosoDraftSettings 二进制数据保存到您草稿文件夹包含使用 EWS 托管 API 的用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-112">The following example shows how to save a user configuration object named ContosoDraftSettings that contains binary data to your Drafts folder by using the EWS Managed API.</span></span> <span data-ttu-id="a5672-113">这可能很有用，如果您想要存储有关草稿项客户端应用程序中的显示方式的配置信息。</span><span class="sxs-lookup"><span data-stu-id="a5672-113">This might be useful if you want to store configuration information about how draft items are displayed in your client application.</span></span> 
  
```cs
private static void CreateUserConfiguration(ExchangeService service, byte[] binaryData)
{
    // Create the user configuration object.
    UserConfiguration configDrafts = new UserConfiguration(service);
    // Add user configuration data to the BinaryData property.
    configDrafts.BinaryData = binaryData;
    // Name and save the user configuration object on the Drafts folder.
    // This results in a call to EWS.
    configDrafts.Save("ContosoDraftSettings", WellKnownFolderName.Drafts);
}
```

## <a name="create-an-application-setting-by-using-ews"></a><span data-ttu-id="a5672-114">使用 EWS 创建应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-114">Create an application setting by using EWS</span></span>
<span data-ttu-id="a5672-115"><a name="bk_createEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-115"></span></span>

<span data-ttu-id="a5672-116">[CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS 操作可用于创建自定义配置设置。</span><span class="sxs-lookup"><span data-stu-id="a5672-116">You can use the [CreateUserConfiguration](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS operation to create a custom configuration setting.</span></span> <span data-ttu-id="a5672-117">下面的示例演示请求 XML 创建一个名为 ContosoDraftSettings 的用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-117">The following example shows the request XML for creating a user configuration object named ContosoDraftSettings.</span></span> <span data-ttu-id="a5672-118">请求尝试对用户配置对象上草稿文件夹中保存的二进制流。</span><span class="sxs-lookup"><span data-stu-id="a5672-118">The request attempts to save a binary stream to a user configuration object on the Drafts folder.</span></span> <span data-ttu-id="a5672-119">这是生成的 EWS 托管 API 示例相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-119">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:CreateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="ContosoDraftSettings">
          <t:DistinguishedFolderId Id="drafts" />
        </t:UserConfigurationName>
        <t:BinaryData>iVBORw0KGH5UhKquRSzaeAAAAAElFTkSuQmCC</t:BinaryData>
      </m:UserConfiguration>
    </m:CreateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="a5672-120">[响应 XML](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx)简单，指示是否创建请求是成功还是是否发生错误。</span><span class="sxs-lookup"><span data-stu-id="a5672-120">The [response XML](http://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) is simple and indicates whether the create request was successful or whether an error occurred.</span></span> 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="a5672-121">使用 EWS 托管 API 来查找应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-121">Find an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="a5672-122"><a name="findconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-122"></span></span>

<span data-ttu-id="a5672-123">可以使用带有关联的遍历选项的[Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS 托管 API 方法查找用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-123">You can use the [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API method with the associated traversal option to find user configuration objects.</span></span> <span data-ttu-id="a5672-124">下面的代码示例演示如何查找用户配置对象存储在草稿文件夹，使用 EWS 托管 API。</span><span class="sxs-lookup"><span data-stu-id="a5672-124">The following code example shows you how to find user configuration objects stored on the Drafts folder by using the EWS Managed API.</span></span> 
  
```cs
private static void FindAssociated(ExchangeService service)
{
    // This is the ItemClass prefix of user configuration objects that are created by using EWS.
    const string userConfigPrefix = "IPM.Configuration.";
            
    // This is the name of a configuration setting created by using EWS.
    string userConfigName = "TestConfig";
    // Return the first five items. 
    ItemView view = new ItemView(5);
    // Request only the properties that you need. Because all the results will be user configuration 
    // objects, you won't need to request the ItemSchema.IsAssociated property, which identifies 
    // user configuration objects.
    PropertySet props = new PropertySet(BasePropertySet.IdOnly, 
                                        ItemSchema.ItemClass);
    view.PropertySet = props;
            
    // Set the traversal to find user configuration objects. 
    view.Traversal = ItemTraversal.Associated;
    // Send the request to search the Drafts folder for all the user configuration objects 
    // in the folder. You do not have to use a search restriction because you will not return
    // a large number of search results. For this scenario, it is better to sort the results
    // on the client. This method results in a call to EWS.
    FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Drafts, view);
    // Output a list of the item classes for the associated items. 
    foreach (Item item in findResults)
    {
        if (item.ItemClass == userConfigPrefix + userConfigName)
        {
            Console.WriteLine("You found the configuration: " + userConfigPrefix + userConfigName);
        }
    }
}
```

## <a name="find-an-application-setting-by-using-ews"></a><span data-ttu-id="a5672-125">使用 EWS 查找应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-125">Find an application setting by using EWS</span></span>
<span data-ttu-id="a5672-126"><a name="bk_findEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-126"></span></span>

<span data-ttu-id="a5672-127">[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作可用于查找用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-127">You can use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation to find user configuration objects.</span></span> 
  
<span data-ttu-id="a5672-128">下面的示例演示请求 XML 查找用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-128">The following example shows the request XML for finding user configuration objects.</span></span> <span data-ttu-id="a5672-129">这是生成的 EWS 托管 API 示例相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-129">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Associated">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:ItemClass" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="5" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="drafts" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="a5672-130">下面的示例演示成功响应 XML 查找用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-130">The following example shows the successful response XML for finding user configuration objects.</span></span> <span data-ttu-id="a5672-131">这是由 EWS 托管 API 示例处理相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-131">This is the same XML that is processed by the EWS Managed API example.</span></span> <span data-ttu-id="a5672-132">请注意此响应 XML 中的以下内容：</span><span class="sxs-lookup"><span data-stu-id="a5672-132">Note the following in this response XML:</span></span> 
  
- <span data-ttu-id="a5672-133">我们可以缩短可读性标识符和更改的快捷键。</span><span class="sxs-lookup"><span data-stu-id="a5672-133">We shortened the identifier and change keys for readability.</span></span>
    
- <span data-ttu-id="a5672-134">作为邮件返回两个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-134">The two user configuration objects are returned as messages.</span></span> <span data-ttu-id="a5672-135">这是因为**FindItem**操作返回未定义 EWS 架构中为邮件项目的所有项。</span><span class="sxs-lookup"><span data-stu-id="a5672-135">This is because the **FindItem** operation returns all items that are not defined in the EWS schema as message items.</span></span> 
    
- <span data-ttu-id="a5672-136">不同的两个用户配置对象[ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx)属性。</span><span class="sxs-lookup"><span data-stu-id="a5672-136">The [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) properties for the two user configuration objects are different.</span></span> <span data-ttu-id="a5672-137">使用 EWS 创建第一个用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-137">The first user configuration object was created by using EWS.</span></span> <span data-ttu-id="a5672-138">另一个 API 创建第二个对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-138">The second object was created by another API.</span></span> 
    
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" 
                        TotalItemsInView="2" 
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AAMkDEY9M6AAA=" ChangeKey="CQAAACYnYF5aFMwP0T" />
                <t:ItemClass>IPM.Configuration.TestConfig</t:ItemClass>
              </t:Message>
              <t:Message>
                <t:ItemId Id="AAkADEzOzFAAA=" ChangeKey="CQAAABQAAABAByOw==" />
                <t:ItemClass>IPM.Microsoft.FolderDesign.NamedView</t:ItemClass>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="a5672-139">获取并使用 EWS 托管 API 更新应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-139">Get and update application settings by using the EWS Managed API</span></span>
<span data-ttu-id="a5672-140"><a name="getconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-140"></span></span>

<span data-ttu-id="a5672-141">查找用户配置对象后，您可以使用[UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS 托管 API 方法来获取从邮箱配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-141">After you find a user configuration object, you can use the [UserConfiguration.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API method to get the configuration object from the mailbox.</span></span> <span data-ttu-id="a5672-142">获取配置对象后，您可以使用[UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx)方法对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="a5672-142">After you get the configuration object, you can use the [UserConfiguration.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) method to update it.</span></span> <span data-ttu-id="a5672-143">下面的示例演示如何获取并使用 EWS 托管 API 更新用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-143">The following example shows how to get and update a user configuration object by using the EWS Managed API.</span></span> 
  
```cs
private static void GetAndUpdateUserConfiguration(ExchangeService service)
{
    // Binds to a user configuration object named "TestConfig" in the user's mailbox. 
    // Results in a call to EWS. You can also use the Load method to get the latest
    // server version of the user configuration object.
    UserConfiguration usrConfig = UserConfiguration.Bind(service,
                                                         "TestConfig",
                                                         WellKnownFolderName.Drafts,
                                                         UserConfigurationProperties.All);
            
    // Display the returned configuration object property values.
    if (usrConfig.XmlData != null)
    {
        Console.WriteLine("XmlData: " + Encoding.UTF8.GetString(usrConfig.XmlData));
    }
    if (usrConfig.BinaryData != null)
    {
        Console.WriteLine("BinaryData: " + Encoding.UTF8.GetString(usrConfig.BinaryData));
    }
    if (usrConfig.Dictionary.Count > 0)
    {
        Console.WriteLine("Contains {0} dictionary entries", usrConfig.Dictionary.Count);
    }
    // Add dictionary property values to the local copy of the object.
    usrConfig.Dictionary.Add("Key5", 1);
    // Updates the server version of the user configuration object 
    // if it has changed on the client. Results in a call to EWS.
    if (usrConfig.IsDirty)
    {
        usrConfig.Update();
    }
}
```

## <a name="get-and-update-application-settings-by-using-ews"></a><span data-ttu-id="a5672-144">获取并使用 EWS 更新应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-144">Get and update application settings by using EWS</span></span>
<span data-ttu-id="a5672-145"><a name="bk_getEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-145"></span></span>

<span data-ttu-id="a5672-146">[GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS 操作可用于从该邮箱和[UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx)更新对象检索配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-146">You can use the [GetUserConfiguration](http://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS operation to retrieve the configuration object from the mailbox, and the [UpdateUserConfiguration](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) to update the object.</span></span> <span data-ttu-id="a5672-147">下面的示例演示请求 XML 用于获取名为 TestConfig 的用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-147">The following example shows the request XML for getting a user configuration object named TestConfig.</span></span> <span data-ttu-id="a5672-148">请求状态应在响应中返回的所有配置。</span><span class="sxs-lookup"><span data-stu-id="a5672-148">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="a5672-149">这是生成的 EWS 托管 API 示例相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-149">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts" />
      </m:UserConfigurationName>
      <m:UserConfigurationProperties>All</m:UserConfigurationProperties>
    </m:GetUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="a5672-150">下面的示例演示用于配置对象中获取用户成功响应 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-150">The following example shows the successful response XML for getting a user configuration objects.</span></span> <span data-ttu-id="a5672-151">则响应中包含的数据词典。</span><span class="sxs-lookup"><span data-stu-id="a5672-151">The response contains a data dictionary.</span></span> <span data-ttu-id="a5672-152">这是由 EWS 托管 API 示例处理相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-152">This is the same XML that is processed by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetUserConfigurationResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:UserConfiguration>
            <t:UserConfigurationName Name="TestConfig">
              <t:DistinguishedFolderId Id="drafts" />
            </t:UserConfigurationName>
            <t:ItemId Id="AAMkDEY9M6AAA=" ChangeKey="CQAAACYnYF5aFMwP0T" />
            <t:Dictionary>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>Key1</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>Integer32</t:Type>
                  <t:Value>1</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
              <t:DictionaryEntry>
                <t:DictionaryKey>
                  <t:Type>String</t:Type>
                  <t:Value>PhoneNumber</t:Value>
                </t:DictionaryKey>
                <t:DictionaryValue>
                  <t:Type>String</t:Type>
                  <t:Value>555-555-1111</t:Value>
                </t:DictionaryValue>
              </t:DictionaryEntry>
            </t:Dictionary>
          </m:UserConfiguration>
        </m:GetUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:GetUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="a5672-153">下面的示例演示请求 XML 更新用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-153">The following example shows the request XML for updating a user configuration object.</span></span> <span data-ttu-id="a5672-154">请求状态应在响应中返回的所有配置。</span><span class="sxs-lookup"><span data-stu-id="a5672-154">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="a5672-155">这是生成的调用**UserConfiguration.Update**方法的 EWS 托管 API 示例相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-155">This is the same XML that is generated by the EWS Managed API example that calls the **UserConfiguration.Update** method.</span></span> <span data-ttu-id="a5672-156">您可以看到更新 XML 包含现有的词典条目与其他更新前已添加。</span><span class="sxs-lookup"><span data-stu-id="a5672-156">You can see that the update XML contains the existing dictionary entries and the additional one that was added before the update.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:UpdateUserConfiguration>
      <m:UserConfiguration>
        <t:UserConfigurationName Name="TestConfig">
          <t:DistinguishedFolderId Id="drafts" />
        </t:UserConfigurationName>
        <t:Dictionary>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>Key1</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>Integer32</t:Type>
              <t:Value>1</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>PhoneNumber</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>String</t:Type>
              <t:Value>555-555-1111</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
          <t:DictionaryEntry>
            <t:DictionaryKey>
              <t:Type>String</t:Type>
              <t:Value>Key5</t:Value>
            </t:DictionaryKey>
            <t:DictionaryValue>
              <t:Type>Integer32</t:Type>
              <t:Value>1</t:Value>
            </t:DictionaryValue>
          </t:DictionaryEntry>
        </t:Dictionary>
      </m:UserConfiguration>
    </m:UpdateUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="a5672-157">[响应 XML](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx)简单，指示是否已成功更新或是否发生错误。</span><span class="sxs-lookup"><span data-stu-id="a5672-157">The [response XML](http://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) is simple and indicates whether the update was successful or whether an error occurred.</span></span> 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="a5672-158">使用 EWS 托管 API 中删除应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-158">Delete an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="a5672-159"><a name="deleteconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-159"></span></span>

<span data-ttu-id="a5672-160">[UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS 托管 API 方法用于删除用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-160">You can use the [UserConfiguration.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API method to delete user configuration objects.</span></span> <span data-ttu-id="a5672-161">下面的代码示例演示如何使用 EWS 托管 API 删除 ContosoDraftSettings 用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-161">The following code example shows you how to delete the ContosoDraftSettings user configuration object by using the EWS Managed API.</span></span> 
  
```cs
private static void DeleteUserConfiguration(ExchangeService service)
{
    // Binds to a user configuration object. Results in a call to EWS.
    UserConfiguration usrConfig = UserConfiguration.Bind(service,
                                                        "ContosoDraftSettings",
                                                        WellKnownFolderName.Drafts,
                                                        UserConfigurationProperties.Id);
    // Deletes the user configuration object.
    // Results in a call to EWS.
    usrConfig.Delete();
}
```

## <a name="delete-an-application-setting-by-using-ews"></a><span data-ttu-id="a5672-162">使用 EWS 删除应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-162">Delete an application setting by using EWS</span></span>
<span data-ttu-id="a5672-163"><a name="bk_deleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="a5672-163"></span></span>

<span data-ttu-id="a5672-164">您可以使用[DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS 操作删除用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="a5672-164">You can use the [DeleteUserConfiguration](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS operation to delete user configuration objects.</span></span> 
  
<span data-ttu-id="a5672-165">下面的示例演示请求 XML 名为已应用于草稿文件夹的 ContosoDraftSettings 用户配置对象删除。</span><span class="sxs-lookup"><span data-stu-id="a5672-165">The following example shows the request XML for deleting a user configuration object named ContosoDraftSettings that was applied to the Drafts folder.</span></span> <span data-ttu-id="a5672-166">这是生成的 EWS 托管 API 示例相同的 XML。</span><span class="sxs-lookup"><span data-stu-id="a5672-166">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:DeleteUserConfiguration>
      <m:UserConfigurationName Name="ContosoDraftSettings">
        <t:DistinguishedFolderId Id="drafts" />
      </m:UserConfigurationName>
    </m:DeleteUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="a5672-167">[响应 XML](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx)非常简单，指示是否删除请求是成功还是是否发生错误。</span><span class="sxs-lookup"><span data-stu-id="a5672-167">The [response XML](http://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) is simple and indicates whether the delete request was a success or whether an error occurred.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5672-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="a5672-168">See also</span></span>

- [<span data-ttu-id="a5672-169">在交换 EWS 持久应用程序设置</span><span class="sxs-lookup"><span data-stu-id="a5672-169">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
- [<span data-ttu-id="a5672-170">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="a5672-170">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="a5672-171">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="a5672-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

