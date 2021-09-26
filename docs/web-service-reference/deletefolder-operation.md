---
title: DeleteFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: b0f92682-4895-4bcf-a4a1-e4c2e8403979
description: DeleteFolder 操作从邮箱中删除文件夹。
ms.openlocfilehash: fdd8519adbf9e0112f5fdd6a411dd6e7710f7d37
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545431"
---
# <a name="deletefolder-operation"></a>DeleteFolder 操作

**DeleteFolder** 操作从邮箱中删除文件夹。 
  
## <a name="deletefolder-request-example"></a>DeleteFolder 请求示例

### <a name="description"></a>说明

以下 **DeleteFolder** 请求示例显示如何形成删除文件夹的请求。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                  DeleteType="HardDelete" >
      <FolderIds>
        <t:FolderId Id="AS4AUnVz=" />
      </FolderIds>
    </DeleteFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

本示例对文件夹执行硬删除。
  
> [!NOTE]
> 已缩短文件夹 ID 以保持可读性。 
  
### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [DeleteFolder](deletefolder.md)
    
- [FolderIds](folderids.md)
    
- [FolderId](folderid.md)
    
> [!NOTE]
> 描述此元素的架构位于运行安装了客户端访问服务器角色的 Microsoft Exchange Server 2010 的计算机的 EWS 虚拟目录中。 
  
若要查找 **DeleteFolder** 操作的请求消息的其他选项，请浏览架构层次结构。 从 [DeleteFolder 元素](deletefolder.md) 开始。 
  
## <a name="successful-deletefolder-response"></a>成功的 DeleteFolder 响应

### <a name="description"></a>说明

以下示例显示了对 **DeleteFolder** 请求的成功响应。 
  
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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a>Response 元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteFolderResponse](deletefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteFolderResponseMessage](deletefolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
若要查找 **DeleteFolder** 操作的响应消息的其他选项，请浏览架构层次结构。 从 [DeleteFolderResponse 元素](deletefolderresponse.md) 开始。 
  
## <a name="deletefolder-error-response"></a>DeleteFolder 错误响应

### <a name="description"></a>说明

以下示例显示 **DeleteFolder** 请求的错误响应。 错误由删除邮箱中不存在的文件夹的请求导致。 
  
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
    <DeleteFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteFolderResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteFolderResponseMessage>
      </m:ResponseMessages>
    </DeleteFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

**DeleteFolder** 操作不能用于可分辨文件夹。 
  
### <a name="error-response-elements"></a>错误响应元素

错误响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteFolderResponse](deletefolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteFolderResponseMessage](deletefolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
若要查找 **DeleteFolder** 操作的错误响应消息的其他选项，请浏览架构层次结构。 从 [DeleteFolderResponse 元素](deletefolderresponse.md) 开始。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [删除文件夹](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

