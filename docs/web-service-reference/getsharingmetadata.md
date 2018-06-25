---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: GetSharingMetadata 元素定义一个请求以获取标识共享邀请的不透明的身份验证令牌。 此元素是 GetSharingMetadata 操作的基本元素。
ms.openlocfilehash: 5283d35e11350ef10ed8cc01527e787ef54be927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19825677"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

**GetSharingMetadata**元素定义一个请求以获取标识共享邀请的不透明的身份验证令牌。 此元素是[GetSharingMetadata 操作](getsharingmetadata-operation.md)的基本元素。
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 **GetSharingMetadataType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |表示将共享的服务器上的文件夹的标识符。 此元素是必需的。  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |表示邮箱包含由[IdOfFolderToShare](idoffoldertoshare.md)元素标识的文件夹对应的 SMTP 电子邮件地址。 此元素是必需的。  <br/> |
|[收件人 (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |代表将被授予访问权限由[IdOfFolderToShare](idoffoldertoshare.md)元素标识的文件夹中的数据的一个或多个实体的 SMTP 电子邮件地址。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetSharingMetadata 操作](getsharingmetadata-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)

