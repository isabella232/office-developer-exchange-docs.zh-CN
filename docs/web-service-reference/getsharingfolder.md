---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: GetSharingFolder元素定义一个请求以获取指定的共享文件夹的本地文件夹标识符。它是GetSharingFolder 操作的基本元素。
ms.openlocfilehash: cb76c534d9b30d0a9d1b267396551eb2871e638a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460503"
---
# <a name="getsharingfolder"></a>GetSharingFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **GetSharingFolder**元素定义一个请求以获取指定的共享文件夹的本地文件夹标识符。它是[GetSharingFolder 操作](getsharingfolder-operation.md)的基本元素。
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 **GetSharingFolderType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |表示共享关系中另一方的 SMTP 电子邮件地址。此元素是必需的。  <br/> |
|[DataType](datatype.md) <br/> |介绍了由一个共享文件夹共享的数据的类型。此元素是可选的。  <br/> |
|[SharedFolderId](sharedfolderid.md) <br/> |表示共享文件夹的本地文件夹标识符应返回的标识符。此元素是可选的。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>说明

GetSharingFolder 元素必须包含一个[SmtpAddress](smtpaddress.md)元素。GetSharingFolder 元素还必须包含一个[DataType](datatype.md)元素或一个[SharedFolderId](sharedfolderid.md)元素，但不能包含两个。 
  
描述该元素的架构位于 IIS 虚拟目录正在运行 Microsoft Exchange Server 的计算机的主机交换 Web 服务已安装了客户端访问服务器角色。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[GetSharingFolder 操作](getsharingfolder-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

