---
title: UpdateFolder Operation
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateFolder
api_type:
- schema
ms.assetid: 3494c996-b834-4813-b1ca-d99642d8b4e7
description: UpdateFolder 操作用于修改 Exchange 存储中现有项目的属性。 每个 UpdateFolder 操作由以下内容组成：
ms.openlocfilehash: b33937bb09f0dcbe3d3ed61bbf5233423f320d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838372"
---
# <a name="updatefolder-operation"></a>UpdateFolder Operation

UpdateFolder 操作用于修改 Exchange 存储中现有项目的属性。 每个 UpdateFolder 操作由以下内容组成：
  
- 指定要更新的文件夹的[文件夹 Id](folderid.md)元素。 
    
- 在文件夹中，指定该文件夹形状，它指定要更新的数据元素的内部路径。
    
- 包含新值更新字段中，如果更新不删除文件夹。
    
## <a name="remarks"></a>注解

可对项目执行三个基本 update 操作。 下表列出了这些操作。
  
|**操作**|**说明**|
|:-----|:-----|
|追加  <br/> |Append 操作将数据添加到现有属性。 它保留了当前存在的数据。 追加不适用于所有属性。  <br/> |
|设置  <br/> |如果它包含的数据，或创建属性并设置其值，如果它不存在，则设置操作将替换属性的数据。 设置操作仅适用于可写属性。  <br/> |
|Delete  <br/> |删除操作从文件夹中删除属性。 这是不同于设置为空值。 完成后，该属性不存在的文件夹。 删除才适用于可写属性。  <br/> |
   
## <a name="updatefolder-request-example"></a>UpdateFolder 请求示例

### <a name="description"></a>说明

UpdateFolder 请求的下面的示例演示如何更新文件夹显示名称。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="AScA" ChangeKey="GO3u/"/>
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:DisplayName"/>
              <t:Folder>
                <t:DisplayName>NewFolderName</t:DisplayName>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </FolderChanges>
    </UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

此示例更改为 NewFolderName 文件夹的显示名称。
  
> [!NOTE]
> 为便于阅读，具有已缩短的**Id**值和[文件夹 Id](folderid.md)元素的**更改密钥**属性。 
  
### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [UpdateFolder](updatefolder.md)
    
- [FolderChanges](folderchanges.md)
    
- [FolderChange](folderchange.md)
    
- [文件夹 Id](folderid.md)
    
- [更新 （项）](updates-item.md)
    
- [SetFolderField](setfolderfield.md)
    
- [FieldURI](fielduri.md)
    
- [Folder](folder.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
请参阅可用于窗体的 UpdateFolder 请求的其他元素的架构。
  
> [!NOTE]
> 架构的默认位置是安装了客户端访问服务器角色的计算机上的 EWS 虚拟目录中。 
  
## <a name="updatefolder-response-example"></a>UpdateFolder 响应示例

### <a name="description"></a>说明

下面的示例演示对 UpdateFolder 请求成功响应。 本示例中，新的更改密钥返回以反映更新的状态的文件夹。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFVz" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

> [!NOTE]
> 已缩短文件夹 ID 和更改密钥，以保留可读性。 
  
响应中返回的文件夹 ID 表示已更新的文件夹。
  
### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [文件夹 Id](folderid.md)
    
## <a name="updatefolder-error-response-example"></a>UpdateFolder 错误响应示例

### <a name="description"></a>说明

下面的示例演示 UpdateFolder 请求错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UpdateFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The change key is invalid.</m:MessageText>
          <m:ResponseCode>ErrorInvalidChangeKey</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:UpdateFolderResponseMessage>
      </m:ResponseMessages>
    </UpdateFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>注释

本示例显示错误响应导致的请求中的**更改密钥**属性无效。 
  
### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [文件夹](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>另请参阅



- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

