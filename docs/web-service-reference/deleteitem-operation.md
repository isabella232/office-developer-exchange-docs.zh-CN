---
title: DeleteItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteItem
api_type:
- schema
ms.assetid: 3e26c416-fa12-476e-bfd2-5c1f4bb7b348
description: DeleteItem 操作将删除数据存储区Exchange项。
ms.openlocfilehash: b62655b9046678d27ed0f24bc92d1840f3e3b343
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545410"
---
# <a name="deleteitem-operation"></a>DeleteItem 操作

**DeleteItem** 操作将删除数据存储区Exchange项。 
  
> [!NOTE]
> 当代理通过将 DisposalType 设置为 MoveToDeletedItems 来尝试删除主体邮箱中的项目时，将为 **DeleteItem** 操作返回包含 ErrorCannotDeleteObject 错误代码的错误响应。 若要通过将其移动到"已删除邮件"文件夹来删除项目，代理必须使用 [MoveItem 操作](moveitem-operation.md)。 
  
## <a name="deleteitem-request-example"></a>DeleteItem 请求示例

### <a name="description"></a>说明

**DeleteItem** 请求的以下示例显示如何从邮箱执行硬删除项目。 
  
> [!NOTE]
> 项目 ID 已缩短，以保持可读性。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteItem DeleteType="HardDelete" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ItemIds>
        <t:ItemId Id="AS4AUn=="/>
      </ItemIds>
    </DeleteItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [DeleteItem](deleteitem.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
若要查找 **DeleteItem** 操作的请求消息的其他选项，请浏览架构层次结构。 从 [DeleteItem 元素](deleteitem.md) 开始。 
  
## <a name="successful-deleteitem-response"></a>成功的 DeleteItem 响应

### <a name="description"></a>说明

以下示例显示了对 **DeleteItem** 请求的成功响应。 
  
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
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="successful-response-elements"></a>成功的响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteItemResponse](deleteitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
若要查找 **DeleteItem** 操作的响应消息的其他选项，请浏览架构层次结构。 从 [DeleteItemResponse 元素](deleteitemresponse.md) 开始。 
  
## <a name="deleteitem-error-response"></a>DeleteItem 错误响应

### <a name="description"></a>说明

以下示例显示对 **DeleteItem** 请求的错误响应。 创建此错误是因为操作尝试删除未在应用商店中Exchange项。 
  
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
    <DeleteItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteItemResponseMessage ResponseClass="Error">
          <m:MessageText>The specified object was not found in the store.</m:MessageText>
          <m:ResponseCode>ErrorItemNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:DeleteItemResponseMessage>
      </m:ResponseMessages>
    </DeleteItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>错误响应元素

错误响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteItemResponse](deleteitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteItemResponseMessage](deleteitemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
若要查找 **DeleteItem** 操作的错误响应消息的其他选项，请浏览架构层次结构。 从 [DeleteItemResponse 元素](deleteitemresponse.md) 开始。 
  
## <a name="see-also"></a>另请参阅

- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [删除联系人](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)  
- [删除电子邮件](https://msdn.microsoft.com/library/c40f2f0b-dae0-412f-b716-727e8c0949b4%28Office.15%29.aspx) 
- [删除任务](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

