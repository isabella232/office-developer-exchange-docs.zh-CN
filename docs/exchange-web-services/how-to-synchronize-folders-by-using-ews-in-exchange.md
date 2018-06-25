---
title: 使用 EWS 在 Exchange 同步文件夹
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: 了解如何使用 EWS 托管 API 或 EWS 获取文件夹的列表或已更改，以便同步您的客户端的文件夹的列表。
ms.openlocfilehash: 4b0686134d642da34b2890a0e692e3d03e4a9fb1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752892"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a>使用 EWS 在 Exchange 同步文件夹

了解如何使用 EWS 托管 API 或 EWS 获取文件夹的列表或已更改，以便同步您的客户端的文件夹的列表。
  
Exchange 中的 EWS 使用项目同步和文件夹同步到客户端和服务器之间同步邮箱内容。 文件夹同步从根文件夹中获取的文件夹的初始列表，然后随时间推移，获取对这些文件夹所做的更改以及获取新的文件夹。
  
如果您正在使用 EWS 托管 API，您第一个[获取文件夹的根文件夹中的初始列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)使用[ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法执行文件夹同步。 然后您要获取的新的和更改的文件夹的列表的后续呼叫过程中更新_cSyncState_参数的值。 
  
若要使用 EWS 执行文件夹同步，您请求[的根文件夹中的文件夹的初始列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest)使用[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作、 分析响应，然后某些点将来[到的文件夹中获取所做的更改根](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)，并分析响应。 客户端接收的初始或已更改文件夹的列表后，它[使本地更新](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。 如何以及何时将来检索更改取决于您的应用程序正在使用[同步设计模式](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns)。 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取所有文件夹或已更改的文件夹的列表
<a name="bk_cesyncinitialewsma"> </a>

下面的代码示例演示如何获取根文件夹中的文件夹的初始列表，然后获取文件夹的根文件夹中的自上次同步后发生更改的列表。 初始呼叫期间[ExchangeService.SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法，将_cSyncState_值设置为 null。 该方法完成后，保存_cSyncState_值本地以在下一个**SyncFolderHierarchy**方法调用中使用。 在初始调用和后续呼叫，文件夹将检索批次的 10，直到没有更多更改保持使用连续**SyncFolderHierarchy**方法调用中。 本示例将_属性集_参数设置为 IdOnly 以减少与 Exchange 数据库，这是一种[同步的最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)的呼叫。 本示例中，我们假定**服务**是一个有效的**ExchangeService**对象绑定并该_cSyncState_代表已由以前**SyncFolderHierarchy**调用返回的同步状态。 
  
```cs
// Get a list of all folders in the mailbox by calling SyncFolderHierarchy.
// The folderId parameter must be set to the root folder to synchronize. 
// The propertySet parameter is set to IdOnly to reduce calls to the Exchange database
// because any additional properties result in additional calls to the Exchange database. 
// The syncState parameter is set to cSyncState, which should be null in the initial call, 
// and should be set to the sync state returned by the previous SyncFolderHierarchy call 
// in subsequent calls.
ChangeCollection<FolderChange> fcc = service.SyncFolderHierarchy(new FolderId(WellKnownFolderName.Root), PropertySet.IdOnly, cSyncState);
// If the count of changes is zero, there are no changes to synchronize.
if (fcc.Count == 0)
{
    Console.WriteLine("There are no folders to synchronize.");
}
// Otherwise, write all the changes included in the response 
// to the console. 
// For the initial synchronization, all the changes will be of type
// ChangeType.Create.
else
{
    foreach (FolderChange fc in fcc)
    {
        Console.WriteLine("ChangeType: " + fc.ChangeType.ToString());
        Console.WriteLine("FolderId: " + fc.FolderId);
        Console.WriteLine("===========");
    }
}
// Save the sync state for use in future SyncFolderItems requests.
// The sync state is used by the server to determine what changes to report
// to the client.
string fSyncState = fcc.SyncState;

```

后检索的在服务器上，[创建或更新客户端上的文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)的新的或更改文件夹的列表。
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a>使用 EWS 获取文件夹的初始的列表
<a name="bk_cesyncewsrequest"> </a>

下面的示例演示 XML 请求，若要使用[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作获取初始文件夹层次结构。 这也是 XML 请求 EWS 托管 API 发送时[检索的使用 SyncFolderHierarchy 方法的初始文件夹的列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)。 [SyncFolderHierarchy](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)操作的[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素不包含，因为这是初始同步。 本示例将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly**以减少与 Exchange 数据库，这是一种[同步的最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)的呼叫。
  
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
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

下面的示例演示它处理[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作请求之后，服务器返回的 XML 响应。 初始响应包括[创建](http://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx)元素的所有文件夹，因为所有文件夹被都视为新期间初始同步。 为了提高可读性，变短了某些属性和元素的值和部分**创建**元素块已删除了明了。 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADM="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM="
                            ChangeKey="AQAAABY"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkAD/AAA="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADBh="
                            ChangeKey="AQAAABYA"/>
              </t:Folder>
            </t:Create>
            ...
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>
```

后检索的在服务器上，[创建客户端上的文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)的新文件夹的列表。
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a>使用 EWS 获取上次同步后所做的更改
<a name="bk_cesyncrespews"> </a>

下面的示例演示 XML 请求以获取根文件夹中的文件夹的更改的列表，使用[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作。 这也是 XML 请求 EWS 托管 API 发送时[检索到的根文件夹的更改的列表](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)。 本示例将[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素的值设置为以前的响应中返回的值。 并用于演示，本示例将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**AllProperties**而不是**IdOnly**显示返回的其他属性。 [同步的最佳做法](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)是将[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置为**IdOnly** 。 为便于阅读缩短了**SyncState**的值。 
  
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
    <m:SyncFolderHierarchy>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:SyncFolderId>
        <t:DistinguishedFolderId Id="root" />
      </m:SyncFolderId>
      <m:SyncState>H4sIAA==</m:SyncState>
    </m:SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

下面的示例演示后处理来自客户端的[SyncFolderHierarchy 操作](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)请求服务器返回的 XML 响应。 此响应指示已更新一个文件夹，创建一个文件夹，并且以前同步后已删除一个文件夹。 为便于阅读变短了[SyncState](http://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素、 **Id**属性和**更改密钥**属性的值。 
  
请记住请求包含**AllProperties**[BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)。 这是只是为了演示。 建议在生产中将**BaseShape**元素设置为**IdOnly** 。 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Update>
              <t:Folder>
                <t:FolderId Id="AAMkADM=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQMkADMzADI1==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Meeting Notes</t:DisplayName>
                <t:TotalCount>3</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Update>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AAMkADMzM=" ChangeKey="AQAAABYAA" />
                <t:ParentFolderId Id="AQMkO67A==" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>Schedules</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:EffectiveRights>
                  <t:CreateAssociated>true</t:CreateAssociated>
                  <t:CreateContents>true</t:CreateContents>
                  <t:CreateHierarchy>true</t:CreateHierarchy>
                  <t:Delete>true</t:Delete>
                  <t:Modify>true</t:Modify>
                  <t:Read>true</t:Read>
                  <t:ViewPrivateItems>true</t:ViewPrivateItems>
                </t:EffectiveRights>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
            <t:Delete>
              <t:FolderId Id="AAMkAD/AAA=" ChangeKey="AQAAAA==" />
            </t:Delete>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </m:SyncFolderHierarchyResponse>
  </s:Body>
</s:Envelope>

```

## <a name="update-the-client"></a>更新客户端
<a name="bk_nextsteps"> </a>

如果您使用 EWS 托管 API 获取新的或更改的文件夹的列表、 [Folder.Load](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx)方法用于获取对新的或更改项目的属性、 比较属性设置为本地值，并更新或客户端上创建文件夹之后。 
  
如果您正在使用 EWS，使用[GetFolder 操作](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx)获取新的或更改的文件夹的属性和更新或客户端上创建文件夹。 
  
## <a name="see-also"></a>另请参阅

- [邮箱同步和交换中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)   
- [使用 EWS 在 Exchange 同步的项目](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [在 Exchange 处理同步相关 EWS 中的错误](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

