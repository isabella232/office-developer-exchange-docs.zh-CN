---
title: 使用 Exchange 中的 EWS 管理持久应用程序设置
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、查找、获取、更新和删除持久应用程序设置。
ms.openlocfilehash: ab7b3ef5f87d8a26a412ca7187dc93c58d73112f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455728"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a><span data-ttu-id="2d391-103">使用 Exchange 中的 EWS 管理持久应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-103">Manage persistent application settings by using EWS in Exchange</span></span>

<span data-ttu-id="2d391-104">了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、查找、获取、更新和删除持久应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="2d391-104">Learn how to create, find, get, update, and delete persistent application settings by using the EWS Managed API or EWS in Exchange.</span></span> 
  
<span data-ttu-id="2d391-105">用户配置对象是存储 Exchange 客户端应用程序的配置设置的最佳选择，主要是因为它们在大多数客户端应用程序中的搜索结果中是隐藏的。</span><span class="sxs-lookup"><span data-stu-id="2d391-105">User configuration objects are the best option for storing configuration settings for your Exchange client application, primarily because they are hidden from search results in most client applications.</span></span> <span data-ttu-id="2d391-106">客户端应用程序通常会隐藏这些设置，因为最终用户不需要查看这些设置，因此用户不会意外地访问此信息。</span><span class="sxs-lookup"><span data-stu-id="2d391-106">Client applications typically hide these settings because the end user doesn't need to see them, and so that the user doesn't accidentally access this information.</span></span> <span data-ttu-id="2d391-107">本文中的代码示例展示了如何使用用户配置对象来管理持久设置，包括如何创建、查找、获取、更新和删除存储在用户配置对象中的持久应用程序设置。</span><span class="sxs-lookup"><span data-stu-id="2d391-107">The code examples in this article show you how you can use user configuration objects to manage persistent settings, including how to create, find, get, update, and delete persistent application settings that are stored in user configuration objects.</span></span>

<span data-ttu-id="2d391-108"><a name="createconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-108"><a name="createconfiguration"> </a></span></span>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="2d391-109">使用 EWS 托管 API 创建应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-109">Create an application setting by using the EWS Managed API</span></span>

<span data-ttu-id="2d391-110">您可以使用[UserConfiguration 中](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx)的 "保存 EWS" API 方法来创建自定义配置设置。</span><span class="sxs-lookup"><span data-stu-id="2d391-110">You can use the [UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS Managed API method to create a custom configuration setting.</span></span> <span data-ttu-id="2d391-111">用户配置对象可以包含 XML、二进制、数据字典或这三种数据类型的组合。</span><span class="sxs-lookup"><span data-stu-id="2d391-111">A user configuration object can contain XML, binary, a data dictionary, or a combination of those three data types.</span></span> <span data-ttu-id="2d391-112">下面的示例演示如何使用 EWS 托管 API 将包含二进制数据的名为 ContosoDraftSettings 的用户配置对象保存到您的 "草稿" 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="2d391-112">The following example shows how to save a user configuration object named ContosoDraftSettings that contains binary data to your Drafts folder by using the EWS Managed API.</span></span> <span data-ttu-id="2d391-113">如果要存储有关草稿项目在客户端应用程序中的显示方式的配置信息，这可能很有用。</span><span class="sxs-lookup"><span data-stu-id="2d391-113">This might be useful if you want to store configuration information about how draft items are displayed in your client application.</span></span> 
  
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

## <a name="create-an-application-setting-by-using-ews"></a><span data-ttu-id="2d391-114">使用 EWS 创建应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-114">Create an application setting by using EWS</span></span>
<span data-ttu-id="2d391-115"><a name="bk_createEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-115"><a name="bk_createEWS"> </a></span></span>

<span data-ttu-id="2d391-116">您可以使用[CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS 操作创建自定义配置设置。</span><span class="sxs-lookup"><span data-stu-id="2d391-116">You can use the [CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS operation to create a custom configuration setting.</span></span> <span data-ttu-id="2d391-117">下面的示例演示用于创建名为 ContosoDraftSettings 的用户配置对象的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-117">The following example shows the request XML for creating a user configuration object named ContosoDraftSettings.</span></span> <span data-ttu-id="2d391-118">请求尝试将二进制流保存到 "草稿" 文件夹上的 "用户配置" 对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-118">The request attempts to save a binary stream to a user configuration object on the Drafts folder.</span></span> <span data-ttu-id="2d391-119">这是由 EWS 托管 API 示例生成的 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-119">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2d391-120">[响应 XML](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx)很简单，指示创建请求是否成功，或者是否发生了错误。</span><span class="sxs-lookup"><span data-stu-id="2d391-120">The [response XML](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) is simple and indicates whether the create request was successful or whether an error occurred.</span></span> 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="2d391-121">使用 EWS 托管 API 查找应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-121">Find an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="2d391-122"><a name="findconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-122"><a name="findconfiguration"> </a></span></span>

<span data-ttu-id="2d391-123">您可以使用[FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS 托管 API 方法和关联的遍历选项来查找用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-123">You can use the [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS Managed API method with the associated traversal option to find user configuration objects.</span></span> <span data-ttu-id="2d391-124">下面的代码示例演示如何使用 EWS 托管 API 查找存储在 "草稿" 文件夹中的用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-124">The following code example shows you how to find user configuration objects stored on the Drafts folder by using the EWS Managed API.</span></span> 
  
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

## <a name="find-an-application-setting-by-using-ews"></a><span data-ttu-id="2d391-125">使用 EWS 查找应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-125">Find an application setting by using EWS</span></span>
<span data-ttu-id="2d391-126"><a name="bk_findEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-126"><a name="bk_findEWS"> </a></span></span>

<span data-ttu-id="2d391-127">您可以使用[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作查找用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-127">You can use the [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS operation to find user configuration objects.</span></span> 
  
<span data-ttu-id="2d391-128">下面的示例演示用于查找用户配置对象的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-128">The following example shows the request XML for finding user configuration objects.</span></span> <span data-ttu-id="2d391-129">这是由 EWS 托管 API 示例生成的 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-129">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2d391-130">下面的示例演示用于查找用户配置对象的成功响应 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-130">The following example shows the successful response XML for finding user configuration objects.</span></span> <span data-ttu-id="2d391-131">这是由 EWS 托管 API 示例处理的 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-131">This is the same XML that is processed by the EWS Managed API example.</span></span> <span data-ttu-id="2d391-132">请注意此响应 XML 中的以下内容：</span><span class="sxs-lookup"><span data-stu-id="2d391-132">Note the following in this response XML:</span></span> 
  
- <span data-ttu-id="2d391-133">我们缩短了标识符，并更改了可读性的键。</span><span class="sxs-lookup"><span data-stu-id="2d391-133">We shortened the identifier and change keys for readability.</span></span>
    
- <span data-ttu-id="2d391-134">这两个用户配置对象以邮件的形式返回。</span><span class="sxs-lookup"><span data-stu-id="2d391-134">The two user configuration objects are returned as messages.</span></span> <span data-ttu-id="2d391-135">这是因为**FindItem**操作返回在 EWS 架构中未定义为邮件项目的所有项目。</span><span class="sxs-lookup"><span data-stu-id="2d391-135">This is because the **FindItem** operation returns all items that are not defined in the EWS schema as message items.</span></span> 
    
- <span data-ttu-id="2d391-136">两个用户配置对象的[ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx)属性不同。</span><span class="sxs-lookup"><span data-stu-id="2d391-136">The [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) properties for the two user configuration objects are different.</span></span> <span data-ttu-id="2d391-137">第一个用户配置对象是使用 EWS 创建的。</span><span class="sxs-lookup"><span data-stu-id="2d391-137">The first user configuration object was created by using EWS.</span></span> <span data-ttu-id="2d391-138">第二个对象是由另一个 API 创建的。</span><span class="sxs-lookup"><span data-stu-id="2d391-138">The second object was created by another API.</span></span> 
    
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a><span data-ttu-id="2d391-139">使用 EWS 托管 API 获取和更新应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-139">Get and update application settings by using the EWS Managed API</span></span>
<span data-ttu-id="2d391-140"><a name="getconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-140"><a name="getconfiguration"> </a></span></span>

<span data-ttu-id="2d391-141">在找到用户配置对象之后，可以使用[UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS 托管 API 方法从邮箱中获取配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-141">After you find a user configuration object, you can use the [UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS Managed API method to get the configuration object from the mailbox.</span></span> <span data-ttu-id="2d391-142">获取 configuration 对象后，可以使用[UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx)方法对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="2d391-142">After you get the configuration object, you can use the [UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) method to update it.</span></span> <span data-ttu-id="2d391-143">下面的示例演示如何使用 EWS 托管 API 获取和更新用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-143">The following example shows how to get and update a user configuration object by using the EWS Managed API.</span></span> 
  
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

## <a name="get-and-update-application-settings-by-using-ews"></a><span data-ttu-id="2d391-144">使用 EWS 获取和更新应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-144">Get and update application settings by using EWS</span></span>
<span data-ttu-id="2d391-145"><a name="bk_getEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-145"><a name="bk_getEWS"> </a></span></span>

<span data-ttu-id="2d391-146">您可以使用[GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS 操作检索邮箱中的配置对象，并使用[UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx)更新对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-146">You can use the [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS operation to retrieve the configuration object from the mailbox, and the [UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) to update the object.</span></span> <span data-ttu-id="2d391-147">下面的示例演示用于获取名为 TestConfig 的用户配置对象的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-147">The following example shows the request XML for getting a user configuration object named TestConfig.</span></span> <span data-ttu-id="2d391-148">请求声明应在响应中返回所有配置。</span><span class="sxs-lookup"><span data-stu-id="2d391-148">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="2d391-149">这是由 EWS 托管 API 示例生成的 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-149">This is the same XML that is generated by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2d391-150">下面的示例演示用于获取用户配置对象的成功响应 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-150">The following example shows the successful response XML for getting a user configuration objects.</span></span> <span data-ttu-id="2d391-151">响应包含数据字典。</span><span class="sxs-lookup"><span data-stu-id="2d391-151">The response contains a data dictionary.</span></span> <span data-ttu-id="2d391-152">这是由 EWS 托管 API 示例处理的 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-152">This is the same XML that is processed by the EWS Managed API example.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="800" 
                         MinorBuildNumber="5" 
                         Version="V2_6" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

<span data-ttu-id="2d391-153">下面的示例演示用于更新用户配置对象的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-153">The following example shows the request XML for updating a user configuration object.</span></span> <span data-ttu-id="2d391-154">请求声明应在响应中返回所有配置。</span><span class="sxs-lookup"><span data-stu-id="2d391-154">The request states that all configurations should be returned in the response.</span></span> <span data-ttu-id="2d391-155">此 XML 与调用**UserConfiguration**方法的 EWS 托管 API 示例生成的 XML 相同。</span><span class="sxs-lookup"><span data-stu-id="2d391-155">This is the same XML that is generated by the EWS Managed API example that calls the **UserConfiguration.Update** method.</span></span> <span data-ttu-id="2d391-156">您可以看到，更新 XML 包含现有词典条目和更新前添加的内容。</span><span class="sxs-lookup"><span data-stu-id="2d391-156">You can see that the update XML contains the existing dictionary entries and the additional one that was added before the update.</span></span> 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2d391-157">[响应 XML](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx)很简单，并指示更新是否成功或是否发生了错误。</span><span class="sxs-lookup"><span data-stu-id="2d391-157">The [response XML](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) is simple and indicates whether the update was successful or whether an error occurred.</span></span> 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a><span data-ttu-id="2d391-158">使用 EWS 托管 API 删除应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-158">Delete an application setting by using the EWS Managed API</span></span>
<span data-ttu-id="2d391-159"><a name="deleteconfiguration"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-159"><a name="deleteconfiguration"> </a></span></span>

<span data-ttu-id="2d391-160">您可以使用[UserConfiguration 中](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx)的 EWS 托管 API 方法删除用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-160">You can use the [UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS Managed API method to delete user configuration objects.</span></span> <span data-ttu-id="2d391-161">下面的代码示例演示如何使用 EWS 托管 API 删除 ContosoDraftSettings 用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-161">The following code example shows you how to delete the ContosoDraftSettings user configuration object by using the EWS Managed API.</span></span> 
  
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

## <a name="delete-an-application-setting-by-using-ews"></a><span data-ttu-id="2d391-162">使用 EWS 删除应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-162">Delete an application setting by using EWS</span></span>
<span data-ttu-id="2d391-163"><a name="bk_deleteEWS"> </a></span><span class="sxs-lookup"><span data-stu-id="2d391-163"><a name="bk_deleteEWS"> </a></span></span>

<span data-ttu-id="2d391-164">您可以使用[DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS 操作删除用户配置对象。</span><span class="sxs-lookup"><span data-stu-id="2d391-164">You can use the [DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS operation to delete user configuration objects.</span></span> 
  
<span data-ttu-id="2d391-165">以下示例显示了用于删除应用于 "草稿" 文件夹的名为 "ContosoDraftSettings" 的用户配置对象的请求 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-165">The following example shows the request XML for deleting a user configuration object named ContosoDraftSettings that was applied to the Drafts folder.</span></span> <span data-ttu-id="2d391-166">这是由 EWS 托管 API 示例生成的 XML。</span><span class="sxs-lookup"><span data-stu-id="2d391-166">This is the same XML that is generated by the EWS Managed API example.</span></span>
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
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

<span data-ttu-id="2d391-167">[响应 XML](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx)很简单，指示删除请求是成功还是发生错误。</span><span class="sxs-lookup"><span data-stu-id="2d391-167">The [response XML](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) is simple and indicates whether the delete request was a success or whether an error occurred.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2d391-168">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2d391-168">See also</span></span>

- [<span data-ttu-id="2d391-169">在交换 EWS 持久应用程序设置</span><span class="sxs-lookup"><span data-stu-id="2d391-169">Persistent application settings in EWS in Exchange</span></span>](persistent-application-settings-in-ews-in-exchange.md)
- [<span data-ttu-id="2d391-170">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="2d391-170">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)   
- [<span data-ttu-id="2d391-171">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="2d391-171">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    

