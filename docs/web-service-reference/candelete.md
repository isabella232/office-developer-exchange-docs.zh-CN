---
title: CanDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CanDelete
api_type:
- schema
ms.assetid: 55e17121-aad0-4f90-889f-2c3512e9579c
description: CanDelete 元素指示客户是否可以删除的托管的文件夹。
ms.openlocfilehash: b70b28bd6b3c9452f5d7f249f453218d555754da
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753433"
---
# <a name="candelete"></a>CanDelete

**CanDelete**元素指示客户是否可以删除的托管的文件夹。 
  
```xml
<CanDelete/>
```

 **Boolean**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |包含有关托管文件夹的信息。  <br/> |
   
## <a name="text-value"></a>文本值

如果此元素是存在，则需要一个文本值，它代表一个布尔值。 值为**true**指示可以删除该文件夹;如果值为**false**意味着不能删除该文件夹。 
  
## <a name="remarks"></a>注解

若要删除的托管的文件夹，使用[DeleteFolder 操作](deletefolder-operation.md)。
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateManagedFolder 操作](createmanagedfolder-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[删除文件夹](http://msdn.microsoft.com/library/1958add5-5071-4239-adb2-40f7a7d74aee%28Office.15%29.aspx)

