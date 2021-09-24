---
title: MoveFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoveFolder
api_type:
- schema
ms.assetid: c7233966-6c87-4a14-8156-b1610760176d
description: MoveFolder 操作将文件夹从指定文件夹移动，并放在另一个文件夹中。
ms.openlocfilehash: e0b0e93bd070354d03c511382b6096f2d3a07508
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523857"
---
# <a name="movefolder-operation"></a>MoveFolder 操作

MoveFolder 操作将文件夹从指定文件夹移动，并放在另一个文件夹中。
  
## <a name="remarks"></a>注解

MoveFolder 操作类似于 CopyFolder 操作。 不能移动可分辨文件夹。 你可以一次将多个文件夹移动到目标文件夹。
  
## <a name="movefolder-request-example"></a>MoveFolder 请求示例

### <a name="description"></a>Description

下面的 MoveFolder 请求示例演示如何形成一个请求，以移动 [由 FolderId](folderid.md) 标识的文件夹，以及将文件夹放入垃圾邮件可分辨文件夹。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="junkemail"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AScAc"/>
      </FolderIds>
    </MoveFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

> [!NOTE]
> 为可读性，已缩短 [FolderId](folderid.md) 元素的 ID 属性的值。 
  
### <a name="request-elements"></a>请求元素

此 MoveFolder 请求包括以下元素：
  
- [MoveFolder](movefolder.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
有关可用于形成 MoveFolder 请求的其他元素，请参阅架构。
  
> [!NOTE]
> 架构的默认位置在安装了客户端访问服务器角色的计算机上 EWS 虚拟目录中。 
  
## <a name="successful-movefolder-response-example"></a>成功的 MoveFolder 响应示例

### <a name="description"></a>Description

以下示例显示了对 MoveFolder 请求的成功响应。 
  
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
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AAAlAFV" ChangeKey="AQAAAB" />
            </t:Folder>
          </m:Folders>
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

> [!NOTE]
> 已缩短文件夹 ID 和更改键以保持可读性。 
  
响应中返回的 FolderId 表示已移动到新文件夹位置的文件夹。
  
### <a name="response-elements"></a>Response 元素

MoveFolder 响应包括以下元素：
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
## <a name="movefolder-error-response-example"></a>MoveFolder 错误响应示例

### <a name="description"></a>Description

以下示例显示尝试移动可分辨文件夹时发生的错误响应。
  
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
    <MoveFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Cannot move distinguished folder.</m:MessageText>
          <m:ResponseCode>ErrorMoveDistinguishedFolder</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:MoveFolderResponseMessage>
      </m:ResponseMessages>
    </MoveFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

MoveFolder 错误响应包括以下元素：
  
- [MoveFolderResponse](movefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveFolderResponseMessage](movefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>另请参阅



[CopyFolder 操作](copyfolder-operation.md)

