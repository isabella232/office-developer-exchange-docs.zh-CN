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
description: CreateManagedFolder 操作在 Exchange 存储中创建一个托管文件夹。
ms.openlocfilehash: 779c730b55b9b441644108a6837f9e22d39cc2f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44444591"
---
# <a name="createmanagedfolder-operation"></a>CreateManagedFolder 操作

CreateManagedFolder 操作在 Exchange 存储中创建一个托管文件夹。
  
## <a name="using-the-createmanagedfolder-operation"></a>使用 CreateManagedFolder 操作

CreateManagedFolder 操作将托管自定义文件夹添加到用户的邮箱中。 您可以使用 Exchange 命令行管理程序**get-managedfolder** cmdlet 查找要添加的可用托管文件夹。 虽然此 cmdlet 返回托管自定义文件夹和托管默认文件夹，但只能添加托管自定义文件夹。 托管自定义文件夹由 ManagedCustomFolder 文件夹类型标识。 System.directoryservices 命名空间还包含可用于发现可用托管文件夹的名称的类型。 
  
> [!NOTE]
> 您不能使用 Exchange Web 服务查找要添加到邮箱中的可用托管文件夹的名称。 
  
您可以使用 FindFolder 和 GetFolder 操作来访问托管文件夹。 FindFolder 用于搜索指定父文件夹中的文件夹。 可以使用此操作，以便在尝试将重复的托管自定义文件夹添加到同一目录中之前，可以在文件夹中发现托管文件夹。 GetFolder 在 FindFolder 操作之后使用，以获取有关托管自定义文件夹的详细信息。
  
## <a name="remarks"></a>备注

有关如何设置邮件记录管理（MRM）策略的信息，请参阅[如何创建托管文件夹邮箱策略](https://go.microsoft.com/fwlink/?LinkId=100975)。
  
有关如何从邮箱中删除托管自定义文件夹的信息，请参阅[get-managedfolder](https://go.microsoft.com/fwlink/?LinkId=100976)。
  
## <a name="createmanagedfolder-request-example"></a>CreateManagedFolder 请求示例

### <a name="description"></a>说明

以下示例的 CreateManagedFolder 请求显示如何将名为 Test Managed Folder 的托管文件夹添加到邮箱。
  
> [!NOTE]
> 您还可以使用代理访问来添加托管自定义文件夹。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateManagedFolder xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderNames>
        <t:FolderName>Test Managed Folder</t:FolderName>
      </FolderNames>
    </CreateManagedFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>Request 元素

请求中使用以下元素：
  
- [CreateManagedFolder](createmanagedfolder.md)
    
- [FolderNames](foldernames.md)
    
- [FolderName](foldername.md)
    
若要查找 CreateManagedFolder 操作的请求消息的其他选项，请浏览架构层次结构。 从[CreateManagedFolder](createmanagedfolder.md)元素开始。 
  
## <a name="successful-createmanagedfolder-response"></a>成功的 CreateManagedFolder 响应

### <a name="description"></a>说明

下面的代码示例演示对 CreateManagedFolder 请求的成功响应。
  
> [!NOTE]
> 为了保持可读性， **Id**和**ChangeKey**属性值已缩短。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="successful-response-elements"></a>成功的响应元素

响应中使用以下元素： 
  
- [CreateManagedFolderResponse](createmanagedfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
若要查找 CreateManagedFolder 操作的响应邮件的其他选项，请浏览架构层次结构。 从[CreateManagedFolderResponse](createmanagedfolderresponse.md)元素开始。 
  
## <a name="createmanagedfolder-error-response"></a>CreateManagedFolder 错误响应

### <a name="description"></a>说明

下面的代码示例演示对 CreateManagedFolder 请求的错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="598" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateManagedFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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
    
- [Folders](folders-ex15websvcsotherref.md)
    
## <a name="see-also"></a>另请参阅



[GetFolder 操作](getfolder-operation.md)
  
[FindFolder 操作](findfolder-operation.md)


[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

