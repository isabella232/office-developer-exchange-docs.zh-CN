---
title: CreateManagedFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: 60a668a2-b4e9-4db9-ac76-9b181e47b302
description: CreateManagedFolder 操作在 Exchange 存储中创建的托管的文件夹。
ms.openlocfilehash: 2c2af53dc5dbe1e6fcbc7f3b1174a856e51e4905
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753677"
---
# <a name="createmanagedfolder-operation"></a>CreateManagedFolder 操作

CreateManagedFolder 操作在 Exchange 存储中创建的托管的文件夹。
  
## <a name="using-the-createmanagedfolder-operation"></a>使用 CreateManagedFolder 操作

CreateManagedFolder 操作将托管的自定义文件夹添加到用户的邮箱。 Exchange 命令行管理程序**获取 ManagedFolder** cmdlet 可用于查找可用的托管的文件夹添加。 虽然此 cmdlet 返回托管自定义文件夹和托管的默认文件夹，只能管理自定义可以将其添加文件夹。 由 ManagedCustomFolder 文件夹类型标识托管自定义文件夹。 System.DirectoryServices 命名空间还包括可用于发现可用的托管文件夹的名称的类型。 
  
> [!NOTE]
> Exchange Web 服务不能用于查找可用的托管文件夹添加到邮箱的名称。 
  
您可以使用的 FindFolder 和 GetFolder 操作访问托管的文件夹。 FindFolder 用于搜索中指定的父文件夹的文件夹。 这可以使用，以使托管的文件夹可以尝试添加重复的托管自定义文件夹到相同的目录之前发现文件夹中。 GetFolder FindFolder 操作之后用于获取有关托管自定义文件夹的详细信息。
  
## <a name="remarks"></a>备注

有关如何设置邮件记录管理 (MRM) 策略的信息，请参阅[如何创建托管文件夹邮箱策略](http://go.microsoft.com/fwlink/?LinkId=100975)。
  
有关如何从邮箱中删除托管自定义文件夹的信息，请参阅[删除 ManagedFolder](http://go.microsoft.com/fwlink/?LinkId=100976)。
  
## <a name="createmanagedfolder-request-example"></a>CreateManagedFolder 请求示例

### <a name="description"></a>说明

CreateManagedFolder 请求的下面的示例演示如何添加到邮箱中名为测试托管文件夹的托管的文件夹。
  
> [!NOTE]
> 您还可以使用代理访问添加托管自定义文件夹。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>请求元素

请求中使用以下元素：
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [FolderNames](foldernames.md)
    
- [FolderName](foldername.md)
    
若要查找的请求邮件 CreateManagedFolder 操作的其他选项，浏览的架构层次结构。 启动[CreateManagedFolder](createmanagedfolder.md)元素。 
  
## <a name="successful-createmanagedfolder-response"></a>成功的 CreateManagedFolder 响应

### <a name="description"></a>说明

下面的代码示例演示对 CreateManagedFolder 请求成功响应。
  
> [!NOTE]
> 具有已缩短**Id**和**更改密钥**属性值，以保留可读性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="AS0AdX=" ChangeKey="AACADA=="/>
            </t:Folder>
          </m:Folders>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>成功响应元素

在响应中使用以下元素： 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [文件夹 Id](folderid.md)
    
若要查找的响应消息 CreateManagedFolder 操作的其他选项，浏览的架构层次结构。 启动[CreateManagedFolderResponse](createmanagedfolderresponse.md)元素。 
  
## <a name="createmanagedfolder-error-response"></a>CreateManagedFolder 错误响应

### <a name="description"></a>说明

下面的代码示例演示对 CreateManagedFolder 请求错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateManagedFolderResponseMessage ResponseClass="Error">
          <m:MessageText>A specified managed folder already exists in the mailbox.</m:MessageText>
          <m:ResponseCode>ErrorManagedFolderAlreadyExists</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:Folders/>
        </m:CreateManagedFolderResponseMessage>
      </m:ResponseMessages>
    </CreateManagedFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中使用以下元素：
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [文件夹](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>另请参阅



[GetFolder Operation](getfolder-operation.md)
  
[FindFolder Operation](findfolder-operation.md)


[Finding Folders](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

