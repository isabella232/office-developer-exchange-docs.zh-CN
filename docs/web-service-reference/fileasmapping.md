---
title: FileAsMapping
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FileAsMapping
api_type:
- schema
ms.assetid: 2c98e7c6-09b0-47b3-bbf7-8c4ef9510280
description: FileAsMapping 元素定义如何构建联系人的显示内容。
ms.openlocfilehash: d846c0af0fbad4df9ee800fe136a4ffcc74c8608
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461035"
---
# <a name="fileasmapping"></a>FileAsMapping

**FileAsMapping**元素定义如何构建联系人的显示内容。 
  
```xml
<FileAsMapping/>
```

 **FileAsMappingType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[Contact](contact.md) <br/> |表示 Exchange 联系人项目。  <br/> |
   
## <a name="text-value"></a>文本值

此元素的文本值被限制为以下字符串值之一：
  
- 无
    
- LastCommaFirst
    
- FirstSpaceLast
    
- Company
    
- LastCommaFirstCompany
    
- CompanyLastFirst
    
- 名字
    
- LastFirstCompany
    
- CompanyLastCommaFirst
    
- LastFirstSuffix
    
- LastSpaceFirstCompany
    
- CompanyLastSpaceFirst
    
- LastSpaceFirst
    
- DisplayName
    
- FirstName
    
- LastFirstMiddleSuffix
    
- LastName
    
- Empty
    
## <a name="remarks"></a>备注

描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



- [Exchange 中的 EWS XML 元素](ews-xml-elements-in-exchange.md)


[创建联系人（Exchange Web 服务）](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[更新联系人](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[删除联系人](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

