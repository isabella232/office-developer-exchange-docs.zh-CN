---
title: FolderShape
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderShape
api_type:
- schema
ms.assetid: 244f4f46-a33d-4764-92e3-1bddb4dc6a49
description: FolderShape 元素标识要在 GetFolder、 FindFolder 或 SyncFolderHierarchy 响应中包含的文件夹属性。
ms.openlocfilehash: 8ebdd70ef13ee9f0cce9020b9212576cba782be4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754408"
---
# <a name="foldershape"></a>FolderShape

**FolderShape**元素标识要在[GetFolder](getfolder.md)、 [FindFolder](findfolder.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)响应中包含的文件夹属性。 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 **FolderResponseShapeType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[BaseShape](baseshape.md) <br/> |标识要返回的响应中的属性的基本配置。  <br/> |
|[AdditionalProperties](additionalproperties.md) <br/> |标识要返回的响应中的其他属性。  <br/> |
   
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[FindFolder](findfolder.md) <br/> |定义一个请求，以确定邮箱中的文件夹。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/FindFolder` <br/> |
|[GetFolder](getfolder.md) <br/> |定义从 Exchange 存储中获取文件夹的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/GetFolder` <br/> |
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |定义同步客户端上的文件夹层次结构的请求。  <br/> 以下是此元素的 XPath 表达式：  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a>注解

**FolderShape**元素是[FindFolder](findfolder.md)元素的必需的子元素。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="example"></a>示例

请求的下面的示例演示如何查找位于第一级的收件箱文件夹中的所有文件夹。
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[FindFolder](findfolder.md)

