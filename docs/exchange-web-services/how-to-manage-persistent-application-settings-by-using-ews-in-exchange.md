---
title: 在应用程序中使用 EWS 管理永久性Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 90f561f2-e40e-4f5b-b321-f86dbf4a1b71
description: 了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 创建、查找、获取、更新和删除永久性应用程序Exchange。
ms.openlocfilehash: 0756f8dabe5f0b898619102b8565b65a536791b9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522276"
---
# <a name="manage-persistent-application-settings-by-using-ews-in-exchange"></a>在应用程序中使用 EWS 管理永久性Exchange

了解如何使用 EWS 托管 API 或 Exchange 中的 EWS 创建、查找、获取、更新和删除永久性应用程序Exchange。 
  
用户配置对象是存储 Exchange 客户端应用程序配置设置的最佳选项，主要是因为在大多数客户端应用程序中的搜索结果中隐藏它们。 客户端应用程序通常会隐藏这些设置，因为最终用户不需要查看它们，因此用户不会意外访问此信息。 本文中的代码示例介绍了如何使用用户配置对象来管理永久性设置，包括如何创建、查找、获取、更新和删除存储在用户配置对象中的永久应用程序设置。

<a name="createconfiguration"> </a>

## <a name="create-an-application-setting-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 创建应用程序设置

可以使用 [UserConfiguration.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.save%28v=exchg.80%29.aspx) EWS 托管 API 方法创建自定义配置设置。 用户配置对象可以包含 XML、二进制、数据字典或这三种数据类型的组合。 以下示例演示如何使用 EWS 托管 API 将包含二进制数据的用户配置对象 ContosoDraftSettings 保存到"草稿"文件夹中。 如果要存储有关草稿项在客户端应用程序中的显示方式的配置信息，这可能很有用。 
  
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

## <a name="create-an-application-setting-by-using-ews"></a>使用 EWS 创建应用程序设置
<a name="bk_createEWS"> </a>

可以使用 [CreateUserConfiguration](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) EWS 操作创建自定义配置设置。 以下示例显示用于创建名为 ContosoDraftSettings 的用户配置对象的请求 XML。 该请求尝试将二进制流保存到"草稿"文件夹上的用户配置对象。 这是由 EWS 托管 API 示例生成的同一 XML。 
  
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

响应 [XML](https://msdn.microsoft.com/library/eb5b8ab6-9743-481c-aac9-f9aa889bd353%28Office.15%29.aspx) 非常简单，指示创建请求是否成功或是否发生了错误。 
  
## <a name="find-an-application-setting-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 查找应用程序设置
<a name="findconfiguration"> </a>

可以将 [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) EWS 托管 API 方法与关联的遍历选项一起用于查找用户配置对象。 以下代码示例演示如何使用 EWS 托管 API 查找存储在"草稿"文件夹中的用户配置对象。 
  
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

## <a name="find-an-application-setting-by-using-ews"></a>使用 EWS 查找应用程序设置
<a name="bk_findEWS"> </a>

可以使用 [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS 操作查找用户配置对象。 
  
以下示例显示用于查找用户配置对象的请求 XML。 这是由 EWS 托管 API 示例生成的同一 XML。
  
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

以下示例显示查找用户配置对象的成功响应 XML。 这是由 EWS 托管 API 示例处理的同一 XML。 在此响应 XML 中，请注意以下事项： 
  
- 我们缩短了标识符和更改键的可读性。
    
- 两个用户配置对象作为消息返回。 这是因为 **FindItem** 操作返回未在 EWS 架构中定义为邮件项目的所有项。 
    
- 两个用户配置对象的 [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) 属性不同。 第一个用户配置对象是使用 EWS 创建的。 第二个对象由另一个 API 创建。 
    
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

## <a name="get-and-update-application-settings-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取和更新应用程序设置
<a name="getconfiguration"> </a>

找到用户配置对象后，可以使用 [UserConfiguration.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) EWS 托管 API 方法从邮箱获取配置对象。 获取配置对象后，可以使用 [UserConfiguration.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.bind%28v=exchg.80%29.aspx) 方法来更新它。 以下示例演示如何使用 EWS 托管 API 获取和更新用户配置对象。 
  
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

## <a name="get-and-update-application-settings-by-using-ews"></a>使用 EWS 获取和更新应用程序设置
<a name="bk_getEWS"> </a>

您可以使用 [GetUserConfiguration](https://msdn.microsoft.com/library/71d50e3c-92bd-435f-8118-b28bb85f8138%28Office.15%29.aspx) EWS 操作从邮箱检索配置对象，并使用 [UpdateUserConfiguration](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) 更新该对象。 以下示例显示用于获取名为 TestConfig 的用户配置对象的请求 XML。 请求指出应在响应中返回所有配置。 这是由 EWS 托管 API 示例生成的同一 XML。 
  
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

以下示例显示用于获取用户配置对象的成功响应 XML。 该响应包含数据字典。 这是由 EWS 托管 API 示例处理的同一 XML。 
  
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

以下示例显示用于更新用户配置对象的请求 XML。 请求指出应在响应中返回所有配置。 这是由调用 **UserConfiguration.Update** 方法的 EWS 托管 API 示例生成的同一 XML。 可以看到，更新 XML 包含现有词典条目以及更新前添加的其他词典条目。 
  
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

响应 [XML](https://msdn.microsoft.com/library/eda73b62-6a3a-43ae-8fd9-f30892811f27%28Office.15%29.aspx) 非常简单，指示更新是否成功或是否发生了错误。 
  
## <a name="delete-an-application-setting-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 删除应用程序设置
<a name="deleteconfiguration"> </a>

可以使用 [UserConfiguration.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) EWS 托管 API 方法删除用户配置对象。 以下代码示例演示如何使用 EWS 托管 API 删除 ContosoDraftSettings 用户配置对象。 
  
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

## <a name="delete-an-application-setting-by-using-ews"></a>使用 EWS 删除应用程序设置
<a name="bk_deleteEWS"> </a>

可以使用 [DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) EWS 操作删除用户配置对象。 
  
以下示例显示用于删除已应用于"草稿"文件夹的用户配置对象 ContosoDraftSettings 的请求 XML。 这是由 EWS 托管 API 示例生成的同一 XML。
  
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

响应 [XML](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) 非常简单，指示删除请求是否成功或是否发生了错误。 
  
## <a name="see-also"></a>另请参阅

- [在交换 EWS 持久应用程序设置](persistent-application-settings-in-ews-in-exchange.md)
- [Exchange 的 EWS 客户端设计概述](ews-client-design-overview-for-exchange.md)   
- [开发 Exchange Web 服务客户端](develop-web-service-clients-for-exchange.md)
    

