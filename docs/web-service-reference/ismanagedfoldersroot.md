---
title: IsManagedFoldersRoot
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsManagedFoldersRoot
api_type:
- schema
ms.assetid: 00823fb9-bf8b-49bb-8e1b-d698c6d4063f
description: IsManagedFoldersRoot 元素指示托管文件夹是否为所有托管文件夹的根。
ms.openlocfilehash: 4373dba9dce92de8e175948d889f0806e100fa6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466022"
---
# <a name="ismanagedfoldersroot"></a>IsManagedFoldersRoot

**IsManagedFoldersRoot**元素指示托管文件夹是否为所有托管文件夹的根。 
  
```xml
<IsManagedFoldersRoot/>
```

 **Boolean**
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

如果存在此元素，则需要一个表示布尔值的文本值。 **如果值为 true** ，则表示该文件夹是托管文件夹的根文件夹;**如果值为 false** ，则表示该文件夹不是托管文件夹的根文件夹。 
  
## <a name="remarks"></a>说明

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)

