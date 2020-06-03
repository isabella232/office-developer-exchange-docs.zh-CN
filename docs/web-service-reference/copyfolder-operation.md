---
title: CopyFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CopyFolder
api_type:
- schema
ms.assetid: c7ea0d68-9793-4144-b378-d99536776db9
description: CopyFolder 操作会复制邮箱中的文件夹。
ms.openlocfilehash: 1f9a7a3f3ede2d3cf8f9d41677d8ce0487266f17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468892"
---
# <a name="copyfolder-operation"></a>CopyFolder 操作

CopyFolder 操作会复制邮箱中的文件夹。
  
## <a name="using-the-copyfolder-operation"></a>使用 CopyFolder 操作

CopyFolder 操作类似于[MoveFolder 操作](movefolder-operation.md)。 它会复制标识的文件夹，并返回已复制文件夹的**Id**和**ChangeKey** 。 
  
## <a name="copyfolder-request-example"></a>CopyFolder 请求示例

### <a name="description"></a>Description

以下示例的 CopyFolder 请求显示如何将文件夹复制到 "收件箱" 文件夹中。
  
> [!NOTE]
> 为了提高可读性， [FolderId](folderid.md)元素的**Id**属性值已缩短。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CopyFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ToFolderId>
        <t:DistinguishedFolderId Id="inbox"/>
      </ToFolderId>
      <FolderIds>
        <t:FolderId Id="AS4A=" ChangeKey="fsVU4=="/>
        <t:FolderId Id="AS4AU=" ChangeKey="fsVU4o=="/>
      </FolderIds>
    </CopyFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

可以通过[DistinguishedFolderId](distinguishedfolderid.md)元素或[FolderId](folderid.md)元素标识文件夹，以便在[ToFolderId](tofolderid.md)或[FolderIds](folderids.md)元素中使用。 
  
### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [CopyFolder](copyfolder.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
> [!NOTE]
> 描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。 
  
若要查找 CopyFolder 操作的请求消息的其他选项，请浏览架构层次结构。 从[CopyFolder](copyfolder.md)元素开始。 
  
## <a name="successful-copyfolder-response"></a>成功的 CopyFolder 响应

### <a name="description"></a>Description

下面的示例演示对 CopyFolder 请求的成功响应。 
  
> [!NOTE]
> 文件夹 ID 和更改密钥已缩短，以保持可读性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS4AUn=" ChangeKey="fsVU4o==" />
            </t:Folder>
          </m:Folders>
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>评论

响应中返回的[FolderId](folderid.md)元素表示在新文件夹位置中复制的文件夹。 
  
### <a name="response-elements"></a>Response 元素

响应中使用以下元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CopyFolderResponse](copyfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CopyFolderResponseMessage](copyfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
若要查找 CopyFolder 操作的响应邮件的其他选项，请浏览架构层次结构。 从[CopyFolderResponse](copyfolderresponse.md)元素开始。 
  
## <a name="copyfolder-error-response"></a>CopyFolder 错误响应

### <a name="description"></a>Description

下面的示例演示对 CopyFolder 请求的错误响应。 出现此错误的原因是已经存在具有相同显示名称的文件夹。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <CopyFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CopyFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The move or copy operation failed.</m:MessageText>
          <m:ResponseCode>ErrorMoveCopyFailed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders />
        </m:CopyFolderResponseMessage>
      </m:ResponseMessages>
    </CopyFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [CopyFolderResponse](copyfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CopyFolderResponseMessage](copyfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
若要查找 CopyFolder 操作的错误响应消息的其他选项，请浏览架构层次结构。 从[CopyFolderResponse](copyfolderresponse.md)元素开始。 
  
## <a name="see-also"></a>另请参阅

- [MoveFolder 操作](movefolder-operation.md)
- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

