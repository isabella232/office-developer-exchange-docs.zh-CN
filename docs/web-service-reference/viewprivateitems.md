---
title: ViewPrivateItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ViewPrivateItems
api_type:
- schema
ms.assetid: 80b949ac-440c-4a01-b428-ebafb5b1b802
description: ViewPrivateItems 元素指示委托用户或客户端应用程序是否有权查看的主体的邮箱中的专用的项目。
ms.openlocfilehash: c35f24ae79e907424cb5cfb0efeec2307334ca12
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19838530"
---
# <a name="viewprivateitems"></a>ViewPrivateItems

**ViewPrivateItems**元素指示委托用户或客户端应用程序是否有权查看的主体的邮箱中的专用的项目。 
  
```XML
<ViewPrivateItems>true | false</ViewPrivateItems>
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
|[DelegateUser](delegateuser.md) <br/> |标识要添加或更新的邮箱中的单个委托。  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |包含客户端的权利基础的项或文件夹的权限设置。此元素是只读的。  <br/> |
   
## <a name="text-value"></a>文本值

值为**true**指示委托或客户端可以的主体的邮箱中查看的私有项目。 如果值为**false**指示的专用项目看不到委托或客户端。 
  
## <a name="remarks"></a>备注

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[AddDelegate 操作](adddelegate-operation.md)
  
[UpdateDelegate 操作](updatedelegate-operation.md)


- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)


[添加代理人](http://msdn.microsoft.com/library/3a744150-66a3-4a13-9433-793603ba5038%28Office.15%29.aspx)

