---
title: SendItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SendItem
api_type:
- schema
ms.assetid: 337b89ef-e1b7-45ed-92f3-8abe4200e4c7
description: SendItem 操作用于发送位于邮件存储Exchange电子邮件。
ms.openlocfilehash: d1e43cdceb3a594c3fa2f028502a3bfedbbf85a1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521583"
---
# <a name="senditem-operation"></a>SendItem 操作

SendItem 操作用于发送位于邮件存储Exchange电子邮件。
  
## <a name="senditem-e-mail-message-request-example"></a>SendItem (电子邮件) 请求示例

### <a name="description"></a>Description

以下示例演示如何发送电子邮件。
  
### <a name="code"></a>代码

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="AAAtAEF=" ChangeKey="CQAAABY+T" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

已缩短项目标识符以保持可读性。
  
### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [SendItem](senditem.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="successful-senditem-e-mail-message-response"></a>成功的 SendItem (电子邮件) 响应

### <a name="description"></a>Description

以下示例显示了成功的 SendItem 响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>成功的响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SendItemResponse](senditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SendItemResponseMessage](senditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
### <a name="comments"></a>备注

如果代理尝试发送一封电子邮件，而该电子邮件位于主体的"草稿"文件夹中，并且将 SendAndSaveCopy 选项设置为在"已发送邮件"可分辨文件夹中保存副本，则代理将无提示地无法将已发送邮件的副本移动到"已发送邮件"可分辨文件夹。 项目将保留在主体的"草稿"文件夹中。 此问题的解决方法是在 [DistinguishedFolderId](distinguishedfolderid.md) 元素中指定主体的邮箱。 
  
要考虑的其他方案是当代理创建电子邮件，并保存到代理邮箱的"草稿"文件夹时。 如果代理尝试发送项目并将副本保存到主体的"已发送邮件"可分辨文件夹中，则邮件发送正确，草稿邮件仍保留在代理的"草稿"文件夹中，已发送邮件不会显示在代理或主体的"已发送邮件"文件夹中，且响应成功。
  
## <a name="invalid-senditem-e-mail-message-request-example"></a>无效的 SendItem (电子邮件) 请求示例

### <a name="description"></a>Description

下面的代码示例演示了一个标识符无效的请求示例。
  
### <a name="code"></a>代码

```XML
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <SendItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
              SaveItemToFolder="true">
      <ItemIds>
        <t:ItemId Id="%BadItemId%" ChangeKey="CQAAABYAAA" />
      </ItemIds>
    </SendItem>
  </soap:Body>
</soap:Envelope>
```

## <a name="senditem-e-mail-message-error-response"></a>SendItem (电子邮件) 错误响应

### <a name="description"></a>Description

以下示例显示对包含无效标识符的 SendItem 请求的错误响应。
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="602" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </SendItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SendItemResponse](senditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SendItemResponseMessage](senditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>另请参阅



[SendItem 操作](senditem-operation.md)
  
 **SendItemType**


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

