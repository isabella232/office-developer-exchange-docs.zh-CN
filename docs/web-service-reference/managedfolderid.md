---
title: ManagedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ManagedFolderId
api_type:
- schema
ms.assetid: 3efb7abb-0e91-4d8a-9fa2-3dec8bd17c30
description: ManagedFolderId 元素包含托管文件夹的文件夹 ID。
ms.openlocfilehash: 85564ecb8e88b5f03dd74f167b26d065b9f00e0d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524803"
---
# <a name="managedfolderid"></a>ManagedFolderId

**ManagedFolderId** 元素包含托管文件夹的文件夹 ID。 
  
```xml
<ManagedFolderId/>
```

 **string**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |包含有关托管文件夹的信息。  <br/> |
   
## <a name="text-value"></a>文本值

此元素需要文本值。
  
## <a name="remarks"></a>注解

**ManagedFolderId** 标识符值与 Microsoft Windows Powershell 命令检索的 **Guid** `Get-ManagedFolder` 属性等效。 这也是 Active Directory 目录服务中托管文件夹的 **objectGUID** 属性的值。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateManagedFolder 操作](createmanagedfolder-operation.md)


- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[删除文件夹](https://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)
  
[Adding Managed Folders](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

