---
title: MoveItem 操作
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoveItem
api_type:
- schema
ms.assetid: dcf40fa7-7796-4a5c-bf5b-7a509a18d208
description: MoveItem 操作用于将一个或多个项目移动到单个目标文件夹。
ms.openlocfilehash: 2d86d06e522e0d42815971c92e754308224f5e8f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544848"
---
# <a name="moveitem-operation"></a>MoveItem 操作

**MoveItem** 操作用于将一个或多个项目移动到单个目标文件夹。 
  
## <a name="moveitem-request-example"></a>MoveItem 请求示例

### <a name="description"></a>说明

下面的 **MoveItem** 请求示例演示如何将项目移动到"草稿"文件夹。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <MoveItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <ToFolderId>
        <t:DistinguishedFolderId Id="drafts"/>
      </ToFolderId>
      <ItemIds>
        <t:ItemId Id="AAAtAEF/swbAAA=" ChangeKey="EwAAABYA/s4b"/>
      </ItemIds>
    </MoveItem>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

[ToFolderId](tofolderid.md)元素指定项目将移动到的文件夹。 请注意 [，ItemIds](itemids.md) 集合中列出的所有项目都将最终在目标文件夹中。 你必须进行单独的 **MoveItem** 调用，以将项目放置到不同的目标文件夹中。 
  
> [!NOTE]
> 已缩短项目标识符和更改键以保持可读性。 
  
### <a name="request-elements"></a>请求元素

请求中会使用下列元素：
  
- [MoveItem](moveitem.md)
    
- [ToFolderId](tofolderid.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [ItemIds](itemids.md)
    
- [ItemId](itemid.md)
    
## <a name="moveitem-response-example"></a>MoveItem 响应示例

### <a name="description"></a>说明

以下示例显示了对 **MoveItem** 请求的成功响应。 
  
在响应消息中返回新项的项目标识符。 在响应跨邮箱或邮箱到公用文件夹 **MoveItem** 操作时不会返回项目标识符。 
  
### <a name="code"></a>代码

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <MoveItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:MoveItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemID Id="AAMkAd" ChangeKey="FwAAABY" />
            </t:Message>
          </m:Items>
        </m:MoveItemResponseMessage>
      </m:ResponseMessages>
    </MoveItemResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>备注

如果 **移动成功，MoveItem** 操作将指示成功。 
  
### <a name="successful-response-elements"></a>成功的响应元素

响应中会使用下列元素：
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [MoveItemResponse](moveitemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [MoveItemResponseMessage](moveitemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Items](items.md)
    
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

