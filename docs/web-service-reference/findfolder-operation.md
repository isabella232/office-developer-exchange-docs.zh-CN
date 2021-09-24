---
title: FindFolder 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: FindFolder 操作使用 Exchange Web 服务查找已标识文件夹的子文件夹，并返回描述子文件夹集的一组属性。
ms.openlocfilehash: 8c2776a9d60244fe77b6012a09ffbad230d86f63
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518468"
---
# <a name="findfolder-operation"></a>FindFolder 操作

**FindFolder** 操作使用 Exchange Web 服务查找已标识文件夹的子文件夹，并返回描述子文件夹集的一组属性。 
  
## <a name="remarks"></a>注解

FindFolder 仅返回任何可流式传输属性的前 512 个字节。 对于 Unicode，它使用以 null 结尾的 Unicode 字符串返回前 255 个字符。
  
无法对公用文件夹执行深层遍历查询。
  
限制是允许的，并且应该只使用文件夹属性，而不是项目属性。 排序功能对 **FindFolder 响应** 不可用。 分组查询对 **FindFolder** 查询不可用。 
  
 **注意****FindFolder** 操作还用于查找托管文件夹。 
  
### <a name="soap-headers"></a>SOAP 标头

**FindFolder** 操作可以使用下表中列出的和描述的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|模拟  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识客户端应用程序正在模拟的用户。  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识用于访问邮箱的 RFC3066 区域性。  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应请求的服务器的版本。  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |标识用于服务器的所有响应的时区。  <br/> |
   
## <a name="findfolder-request-example"></a>FindFolder 请求示例

### <a name="description"></a>Description

**FindFolder** 请求的以下示例显示如何形成请求以查找位于"收件箱"中的所有文件夹。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

通过使用 [BaseShape](baseshape.md)的默认值，响应将返回文件夹名称、文件夹 ID、子文件夹数量、文件夹中找到的子文件夹数以及未读项目数。
  
### <a name="request-elements"></a>请求元素

此 **FindFolder** 请求包括以下元素： 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 有关其他 **FindFolder** 请求元素，请参阅架构。 
  
## <a name="findfolder-response-example"></a>FindFolder 响应示例

### <a name="description"></a>Description

下面的 SOAP Simple Object Access Protocol (SOAP) 示例展示了 **对 FindFolder** 请求的成功响应。 该响应包含使用 [BaseShape](baseshape.md) 的默认值时返回的元素。 
  
> [!NOTE]
> 已缩短文件夹 ID 和更改键以保持可读性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="1" IncludesLastItemInRange="true">
            <t:Folders>
              <t:Folder>
                <t:FolderId Id="AQAnAH" ChangeKey="AQAAABY" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:TotalCount>0</t:TotalCount>
                <t:ChildFolderCount>0</t:ChildFolderCount>
                <t:UnreadCount>0</t:UnreadCount>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="response-elements"></a>Response 元素

响应中返回的属性由 [BaseShape](baseshape.md) 和 [AdditionalProperties](additionalproperties.md) 确定（如果使用）。 成功的 **FindFolder** 响应包括以下元素： 
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindFolderResponseMessage](findfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [FolderId](folderid.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
### <a name="comments"></a>备注

 使用 **AllProperties** 响应形状对请求的 **FindFolder** 响应不会返回公用文件夹搜索的 [TotalCount](totalcount.md)和 [UnreadCount](unreadcount.md)元素。 
  
## <a name="findfolder-error-response-example"></a>FindFolder 错误响应示例

### <a name="description"></a>Description

以下 SOAP 正文示例显示当您搜索由格式不正确的文件夹标识符标识的文件夹时发生的错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </FindFolderResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

**FindFolder** 错误响应包括以下元素： 
  
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="additional-information"></a>其他信息

- The folder [DisplayName (string) ](displayname-string.md) element is always included in the default shape. 
    
- [UnreadCount](unreadcount.md)元素包含在"任务"和"便笺"文件夹中。 
    
- 使用属性类型为 Integer 0x672D属性类型的 **PropertyTag** 值，通过 [ExtendedFieldURI](extendedfielduri.md)元素标识托管文件夹。 
    
## <a name="see-also"></a>另请参阅



[Finding Folders](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

