---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: FolderShape 元素标识要包括在 GetFolder、FindFolder 或 SyncFolderHierarchy 响应中的文件夹属性。
ms.openlocfilehash: 530c9f25f17a3eba8549535bf7be37038a58c921
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518356"
---
# <a name="foldershape"></a>FolderShape

**FolderShape** 元素标识要包括在 [GetFolder、FindFolder](getfolder.md)[](findfolder.md)或 [SyncFolderHierarchy 响应中的文件夹](syncfolderhierarchy.md)属性。 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 **FolderResponseShapeType**
## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |标识响应中要返回的属性的基本配置。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |标识响应中要返回的其他属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义标识邮箱中的文件夹的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/FindFolder` <br/> |
|[GetFolder](getfolder.md) <br/> |定义从应用商店获取文件夹Exchange请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/GetFolder` <br/> |
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |定义在客户端上同步文件夹层次结构的请求。  <br/> 下面是此元素的 XPath 表达式：   <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a>注解

**FolderShape** 元素是 [FindFolder](findfolder.md)元素的必需子元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

请求的以下示例演示了如何查找位于"收件箱"文件夹第一级的所有文件夹。
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <FolderShape>
        <t:BaseShape>Default</t:BaseShape>
      </FolderShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox"/>
      </ParentFolderIds>
    </FindFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder](findfolder.md)

