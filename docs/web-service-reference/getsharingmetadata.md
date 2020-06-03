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
description: GetSharingMetadata 元素定义一个请求，以获取标识共享邀请的不透明身份验证令牌。 此元素是 GetSharingMetadata 操作的基本元素。
ms.openlocfilehash: 406908e566d6d4249003b1a19a9ce79b8b328c4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530844"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

**GetSharingMetadata**元素定义一个请求，以获取标识共享邀请的不透明身份验证令牌。 此元素是[GetSharingMetadata 操作](getsharingmetadata-operation.md)的基本元素。
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 **GetSharingMetadataType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |表示服务器上将共享的文件夹的标识符。 此元素是必需的。  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |表示与包含由[IdOfFolderToShare](idoffoldertoshare.md)元素标识的文件夹的邮箱相对应的 SMTP 电子邮件地址。 此元素是必需的。  <br/> |
|[收件人（ArrayOfSmtpAddressType）](recipients-arrayofsmtpaddresstype.md) <br/> |表示一个或多个实体的 SMTP 电子邮件地址，这些实体将被授予对由[IdOfFolderToShare](idoffoldertoshare.md)元素标识的文件夹中的数据的访问权限。 此元素是必需的。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetSharingMetadata 操作](getsharingmetadata-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

