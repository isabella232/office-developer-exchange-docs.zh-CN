---
title: UpdateFolder 操作
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
description: UpdateFolder 操作用于修改 Exchange 存储中现有项的属性。 每个 UpdateFolder 操作都包含以下内容：
ms.openlocfilehash: fb894d9f42358b67f81e9fe8ae41ba61e6f46460
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467359"
---
# <a name="updatefolder-operation"></a>UpdateFolder 操作

UpdateFolder 操作用于修改 Exchange 存储中现有项的属性。 每个 UpdateFolder 操作都包含以下内容：
  
- 一个[FolderId](folderid.md)元素，指定要更新的文件夹。 
    
- 文件夹中元素的内部路径，由 folder 形状指定，该路径指定要更新的数据。
    
- 包含更新的域的新值的文件夹（如果更新不是删除）。
    
## <a name="remarks"></a>备注

可以对项目执行三个基本的更新操作。 下表中列出了这些操作。
  
|**操作**|**说明**|
|:-----|:-----|
|Append  <br/> |Append 操作将数据添加到现有属性中。 它保留当前在其中的数据。 Append 不适用于所有属性。  <br/> |
|Set  <br/> |如果属性包含数据，则 set 操作将替换该属性的数据，或者创建该属性并设置其值（如果不存在）。 Set 操作仅适用于可写属性。  <br/> |
|删除  <br/> |"删除" 操作从文件夹中删除属性。 这与将其设置为空值不同。 完成后，该文件夹的属性不存在。 删除仅适用于可写属性。  <br/> |
   
## <a name="updatefolder-request-example"></a>UpdateFolder 请求示例

### <a name="description"></a>说明

以下示例的 UpdateFolder 请求显示如何更新文件夹显示名称。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <UpdateFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
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

### <a name="comments"></a>备注

本示例将文件夹的显示名称更改为 NewFolderName。
  
> [!NOTE]
> 为了提高可读性， [FolderId](folderid.md)元素的**Id**和**ChangeKey**属性的值已缩短。 
  
### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [UpdateFolder](updatefolder.md)
    
- [FolderChanges](folderchanges.md)
    
- [FolderChange](folderchange.md)
    
- [FolderId](folderid.md)
    
- [Updates 文件夹](updates-folder.md)
    
- [SetFolderField](setfolderfield.md)
    
- [FieldURI](fielduri.md)
    
- [Folder](folder.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
有关可用于形成 UpdateFolder 请求的其他元素，请参阅架构。
  
> [!NOTE]
> 架构的默认位置在安装了客户端访问服务器角色的计算机上的 EWS 虚拟目录中。 
  
## <a name="updatefolder-response-example"></a>UpdateFolder 响应示例

### <a name="description"></a>说明

下面的示例演示对 UpdateFolder 请求的成功响应。 在此示例中，将返回新的更改密钥，以反映该文件夹的更新状态。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>备注

> [!NOTE]
> 文件夹 ID 和更改密钥已缩短，以保持可读性。 
  
响应中返回的文件夹 ID 表示更新的文件夹。
  
### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="updatefolder-error-response-example"></a>UpdateFolder 错误响应示例

### <a name="description"></a>说明

下面的示例演示对 UpdateFolder 请求的错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UpdateFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>备注

此示例显示了由请求中的无效**ChangeKey**属性导致的错误响应。 
  
### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UpdateFolderResponse](updatefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UpdateFolderResponseMessage](updatefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

