---
title: 使用文件夹中的 EWS 同步Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: d3bbacd1-8e4b-4fd0-8d27-4cbbc045ec3f
description: 了解如何使用 EWS 托管 API 或 EWS 获取文件夹列表或已更改的文件夹列表，以便同步客户端。
ms.openlocfilehash: f22cb3b4ba92da9c044e08e7164d116293cf43ff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521090"
---
# <a name="synchronize-folders-by-using-ews-in-exchange"></a>使用文件夹中的 EWS 同步Exchange

了解如何使用 EWS 托管 API 或 EWS 获取文件夹列表或已更改的文件夹列表，以便同步客户端。
  
Exchange中的 EWS 使用项目同步和文件夹同步在客户端和服务器之间同步邮箱内容。 文件夹同步从根文件夹获取文件夹的初始列表，然后随着时间的推移，获取对这些文件夹所做的更改，并获取新文件夹。
  
如果使用 EWS 托管 API 执行文件夹同步，首先使用[ExchangeService.SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)方法获取根文件夹中的文件夹的初始列表。 [](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma) 然后，在后续调用过程中更新  _cSyncState_ 参数的值，获取新文件夹和已更改文件夹的列表。 
  
若要使用 EWS 执行文件夹同步，可以使用[](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncewsrequest)[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)操作请求根文件夹中的文件夹的初始列表，分析响应，然后在将来的某一时候获取对[根文件夹中的文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncrespews)的更改，然后分析响应。 客户端收到初始或已更改的文件夹列表后，会 [在本地进行更新](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。 将来检索更改的方式和时间取决于 [应用程序使用的](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns) 同步设计模式。 
  
## <a name="get-the-list-of-all-folders-or-changed-folders-by-using-the-ews-managed-api"></a>使用 EWS 托管 API 获取所有文件夹或已更改文件夹的列表
<a name="bk_cesyncinitialewsma"> </a>

下面的代码示例演示如何获取根文件夹中的文件夹的初始列表，然后获取自上一次同步以来对根文件夹中的文件夹所做的更改列表。 在初次调用 [ExchangeService.SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) 方法期间，将  _cSyncState_ 值设置为 null。 方法完成后，在本地保存  _cSyncState_ 值，以用于下一 **个 SyncFolderHierarchy** 方法调用。 在初始调用和后续调用中，通过使用 **对 SyncFolderHierarchy** 方法的连续调用，按十个批次检索文件夹，直到不再有变化。 此示例将 _propertySet_ 参数设置为 IdOnly，以减少对 Exchange 数据库的调用，这是 [一种同步最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)。 本示例中，我们假定 **服务** 是有效的 **ExchangeService** 对象绑定，  _并且 cSyncState_ 表示之前调用 **SyncFolderHierarchy 时返回的同步状态**。 
  
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

检索服务器上新文件夹或已更改文件夹的列表后，在客户端上创建 [或更新文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。
  
## <a name="get-the-initial-list-of-folders-by-using-ews"></a>使用 EWS 获取文件夹的初始列表
<a name="bk_cesyncewsrequest"> </a>

下面的示例展示了使用 [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) 操作获取初始文件夹层次结构的 XML 请求。 这也是 EWS 托管 API 在使用 [SyncFolderHierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)方法检索初始文件夹列表时发送的 XML 请求。 [SyncFolderHierarchy](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)操作中的[SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素不包括在内，因为这是初始同步。 此示例将 [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素设置 **为 IdOnly，** 以减少Exchange数据库的调用，这是 [一种同步最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)。
  
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

以下示例显示服务器处理 [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) 操作请求后返回的 XML 响应。 初始响应包括所有文件夹的 [Create](https://msdn.microsoft.com/library/6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1%28Office.15%29.aspx) 元素，因为所有文件夹在初始同步过程中都被视为新文件夹。 为了可读性，已缩短某些属性和元素的值，为了简洁起见，删除了一些 **Create** 元素块。 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="785"
                         MinorBuildNumber="6"
                         Version="V2_6"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                                   xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

检索服务器上新文件夹的列表后，在客户端 [上创建文件夹](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_nextsteps)。
  
## <a name="get-the-changes-since-the-last-sync-by-using-ews"></a>使用 EWS 获取自上次同步以来的更改
<a name="bk_cesyncrespews"> </a>

下面的示例展示了使用 [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) 操作获取根文件夹中文件夹更改列表的 XML 请求。 这也是 EWS 托管 API 在检索根文件夹的更改列表时 [发送的](how-to-synchronize-folders-by-using-ews-in-exchange.md#bk_cesyncinitialewsma)XML 请求。 本示例将 [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx) 元素值设置成上一个响应中返回的值。 出于演示目的，此示例将 [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)元素（而不是 **IdOnly）** 设置为 **AllProperties，** 以显示返回的其他属性。 将 [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) 元素设置为 **IdOnly** 是 [一种同步最佳实践](mailbox-synchronization-and-ews-in-exchange.md#bk_bestpractices)。 **SyncState** 的值已缩短，可读。 
  
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

以下示例显示服务器处理来自客户端的 [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) 操作请求后返回的 XML 响应。 此响应表示更新了一个文件夹，创建了一个文件夹，并且自之前同步后删除了一个文件夹。 [SyncState](https://msdn.microsoft.com/library/e5ebaae3-0f07-481d-ac67-d9687a3c7ac3%28Office.15%29.aspx)元素 **、Id** 属性和 **ChangeKey** 属性的值已缩短，以用于可读性。 
  
请记住，请求包括 **AllProperties**[BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx)。 这仅仅是出于演示目的。 我们建议在生产中将 **BaseShape** 元素设置为 **IdOnly。** 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
<h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="745" MinorBuildNumber="21" Version="V2_3" 
           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
            xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

如果使用的是 EWS 托管 API，则获取新文件夹或已更改文件夹的列表后，使用 [Folder.Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.load%28v=exchg.80%29.aspx) 方法获取新项或已更改项目的属性，将属性与本地值进行比较，并更新或创建客户端上的文件夹。 
  
如果使用的是 EWS，请使用 [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) 操作获取新文件夹或已更改文件夹的属性，并更新或创建客户端上的文件夹。 
  
## <a name="see-also"></a>另请参阅

- [邮箱同步和 Exchange 中的 EWS](mailbox-synchronization-and-ews-in-exchange.md)   
- [使用 EWS 同步Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)   
- [处理 EWS 中与同步相关的Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    

