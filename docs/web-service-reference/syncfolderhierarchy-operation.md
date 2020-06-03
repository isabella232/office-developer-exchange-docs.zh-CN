---
title: SyncFolderHierarchy 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: b31916b1-bc6c-4451-a475-b7c5417f752d
description: SyncFolderHierarchy 操作将在运行 Microsoft Exchange Server 2010 的计算机和客户端之间同步文件夹。
ms.openlocfilehash: 1c7ad2413064161ba54e8a7a30bfcd6f23f218bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456428"
---
# <a name="syncfolderhierarchy-operation"></a>SyncFolderHierarchy 操作

SyncFolderHierarchy 操作将在运行 Microsoft Exchange Server 2010 的计算机和客户端之间同步文件夹。
  
> [!NOTE]
> 当[UnreadCount](unreadcount.md)或[TotalCount](totalcount.md)属性发生更改时，SyncFolderHierarchy 操作不会返回文件夹。 
  
## <a name="syncfolderhierarchy-request-example"></a>SyncFolderHierarchy 请求示例

### <a name="description"></a>Description

以下示例的 SyncFolderHierarchy 请求显示如何将客户端文件夹层次结构与 Exchange 服务器同步。 此示例显示至少已同步一次的文件夹层次结构。 在第一次尝试将客户端与 Exchange 服务器同步时，请求中不包含[SyncState](syncstate-ex15websvcsotherref.md)元素。 第一个请求将返回邮箱中的所有文件夹。 [SyncState](syncstate-ex15websvcsotherref.md)元素将在[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)中返回。 此元素用于同步后续 SyncFolderHierarchy 请求的状态。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SyncFolderHierarchy  xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </FolderShape>
      <SyncState>H4sIA=</SyncState>
    </SyncFolderHierarchy>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据已缩短，以保持可读性。 
  
### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [SyncFolderHierarchy](syncfolderhierarchy.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [SyncState](syncstate-ex15websvcsotherref.md)
    
> [!NOTE]
> 描述这些元素的架构位于运行 MicrosoftExchange Server 2007 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。 
  
## <a name="successful-syncfolderhierarchy-response"></a>成功的 SyncFolderHierarchy 响应

### <a name="description"></a>Description

下面的示例演示对 SyncFolderHierarchy 请求的成功响应。 在此示例中，已同步一个新文件夹。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SyncState>H4sIAAA==</m:SyncState>
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
          <m:Changes>
            <t:Create>
              <t:Folder>
                <t:FolderId Id="AQApAHR=" ChangeKey="AQAAABY" />
                <t:ParentFolderId Id="AQApA=" ChangeKey="AQAAAA==" />
                <t:FolderClass>IPF.Note</t:FolderClass>
                <t:DisplayName>NewFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Create>
          </m:Changes>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

[SyncState](syncstate-ex15websvcsotherref.md)元素 base64 编码的数据和文件夹标识符数据已缩短，以保持可读性。 
  
### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SyncState](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastFolderInRange](includeslastfolderinrange.md)
    
- [更改（层次结构）](changes-hierarchy.md)
    
- [创建 (FolderSync)](create-foldersync.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
- [ParentFolderId](parentfolderid.md)
    
- [FolderClass](folderclass.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
## <a name="syncfolderhierarchy-error-response"></a>SyncFolderHierarchy 错误响应

### <a name="description"></a>Description

下面的示例演示对 SyncFolderHierarchy 请求的错误响应。 此错误是由无效的 SyncState 所致。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" 
                         MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SyncFolderHierarchyResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SyncFolderHierarchyResponseMessage ResponseClass="Error">
          <m:MessageText>Synchronization state data is corrupted or otherwise invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidSyncStateData</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:SyncState />
          <m:IncludesLastFolderInRange>true</m:IncludesLastFolderInRange>
        </m:SyncFolderHierarchyResponseMessage>
      </m:ResponseMessages>
    </SyncFolderHierarchyResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [SyncState](syncstate-ex15websvcsotherref.md)
    
- [IncludesLastFolderInRange](includeslastfolderinrange.md)
    
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

