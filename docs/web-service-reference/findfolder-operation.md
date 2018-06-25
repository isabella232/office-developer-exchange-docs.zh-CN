---
title: FindFolder Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindFolder
api_type:
- schema
ms.assetid: 7a9855aa-06cc-45ba-ad2a-645c15b7d031
description: FindFolder 操作使用 Exchange Web 服务来查找标识的文件夹的子文件夹，并返回描述这组子文件夹的属性集。
ms.openlocfilehash: 655455b46d4a3192b294bee9d85352d95ded49ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754328"
---
# <a name="findfolder-operation"></a>FindFolder Operation

**FindFolder**操作使用 Exchange Web 服务来查找标识的文件夹的子文件夹，并返回描述这组子文件夹的属性集。 
  
## <a name="remarks"></a>注解

FindFolder 返回仅第一个 512 个字节的任何流式属性。 对于 Unicode，它使用以 null 结尾的 Unicode 字符串中返回的前 255 个字符。
  
在公用文件夹，无法执行遍历查询。
  
限制允许和应使用仅文件夹属性中，不是项目的属性。 排序功能不可用的**FindFolder**响应。 组合的查询不能用于**FindFolder**查询。 
  
 **注释****FindFolder**操作还用于查找托管的文件夹。 
  
### <a name="soap-headers"></a>SOAP 标头

**FindFolder**操作可以使用列出并在下表中所述的 SOAP 标头。 
  
|**Header**|**元素**|**说明**|
|:-----|:-----|:-----|
|模拟  <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |标识模拟客户端应用程序的用户。  <br/> |
|MailboxCulture  <br/> |[MailboxCulture](mailboxculture.md) <br/> |标识用于访问邮箱的 RFC3066 区域性。  <br/> |
|RequestVersion  <br/> |[RequestServerVersion](requestserverversion.md) <br/> |标识操作请求的架构版本。  <br/> |
|ServerVersion  <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |标识响应该请求的服务器的版本。  <br/> |
|TimeZoneContext  <br/> |[TimeZoneContext](timezonecontext.md) <br/> |确定要用于来自服务器的所有响应的时区。  <br/> |
   
## <a name="findfolder-request-example"></a>FindFolder 请求示例

### <a name="description"></a>说明

**FindFolder**请求的下面的示例演示如何以形成一个请求，以查找所有收件箱中位于的文件夹。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="comments"></a>注释

响应[BaseShape](baseshape.md)使用默认值，它返回文件夹名称，文件夹 ID，子文件夹，该文件夹，以及的未读项目计数中找到的子文件夹数的数量。
  
### <a name="request-elements"></a>请求元素

此**FindFolder**请求中包括以下元素： 
  
- [FindFolder](findfolder.md)
    
- [FolderShape](foldershape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
 其他**FindFolder**请求元素，请参阅 schema。 
  
## <a name="findfolder-response-example"></a>FindFolder 响应示例

### <a name="description"></a>说明

下面的简单对象访问协议 (SOAP) 正文示例演示对**FindFolder**请求成功响应。 则响应中包含的默认值为[BaseShape](baseshape.md)时返回的元素。 
  
> [!NOTE]
> 已缩短文件夹 ID 和更改密钥，以保留可读性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="response-elements"></a>响应元素

如果它们使用由[BaseShape](baseshape.md)和[AdditionalProperties](additionalproperties.md)决定响应中返回的属性。 成功的**FindFolder**响应包括以下元素： 
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindFolderResponseMessage](findfolderresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Folders](folders-ex15websvcsotherref.md)
    
- [Folder](folder.md)
    
- [文件夹 Id](folderid.md)
    
- [显示名称 (字符串)](displayname-string.md)
    
- [TotalCount](totalcount.md)
    
- [ChildFolderCount](childfoldercount.md)
    
- [UnreadCount](unreadcount.md)
    
### <a name="comments"></a>注释

 [TotalCount](totalcount.md)和[UnreadCount](unreadcount.md)元素的公用文件夹搜索，不会返回**FindFolder**エ ・ 复 ハ 与**AllProperties**响应形状的请求。 
  
## <a name="findfolder-error-response-example"></a>FindFolder 错误响应示例

### <a name="description"></a>说明

下面的 SOAP 正文示例演示您搜索由格式不正确的文件夹标识符标识的文件夹时发生错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
                 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="652" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

**FindFolder**错误响应包括以下元素： 
  
- [FindFolderResponse](findfolderresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="additional-information"></a>其他信息

- 默认形状中始终包含文件夹[DisplayName （字符串）](displayname-string.md)元素。 
    
- 任务和便笺文件夹中包含的[UnreadCount](unreadcount.md)元素。 
    
- 使用与属性类型的**整数**的 0x672D **PropertyTag**值使用[ExtendedFieldURI](extendedfielduri.md)元素标识托管的文件夹。 
    
## <a name="see-also"></a>另请参阅



[Finding Folders](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

