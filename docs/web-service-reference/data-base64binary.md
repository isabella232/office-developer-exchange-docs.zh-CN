---
title: Data (base64Binary)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Data
api_type:
- schema
ms.assetid: 26d8c2d0-bed2-4aed-b381-20e2ace6892f
description: Data 元素包含要上载到邮箱中的单个导出项目或项目的数据。
ms.openlocfilehash: 69e15746f17febb74a0ec2f56eef0eaa1e298015
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535932"
---
# <a name="data-base64binary"></a>Data (base64Binary)

**Data** 元素包含要上载到邮箱中的单个导出项目或项目的数据。 
  
```XML
<Data/>
```

**xs：base64Binary**

## <a name="attributes-and-elements"></a>属性和元素

下面各部分介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>Attributes

无。
  
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[ExportItemsResponseMessage](exportitemsresponsemessage.md) <br/> |包含导出单个邮箱项目的请求的状态和结果。  <br/> |
|[Item (UploadItemType)](item-uploaditemtype.md) <br/> |表示要上载到邮箱中的单个项目。  <br/> |
   
## <a name="text-value"></a>文本值

**Data** 元素包含要上载到邮箱中的已导出项目或项目的属性名称和值。 
  
## <a name="remarks"></a>注解

描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。Exchange Server 2010 Service Pack 1 (SP1) 中引入了此元素。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [ExportItems 操作](exportitems-operation.md)
- [UploadItems 操作](uploaditems-operation.md)

