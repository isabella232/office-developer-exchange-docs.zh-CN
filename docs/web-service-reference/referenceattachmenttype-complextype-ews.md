---
title: 'ReferenceAttachmentType complexType (EWS) '
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: d0e425d5493f9155aff7e16c306a785663f5b89f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522661"
---
# <a name="referenceattachmenttype-complextype-ews"></a>ReferenceAttachmentType complexType (EWS) 

## <a name="type-information"></a>类型信息

|||
|:-----|:-----|
|**命名空间** <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|**架构文件** <br/> |types.xsd  <br/> |
|**扩展基** <br/> |t：AttachmentType  <br/> |
   
## <a name="definition"></a>定义

```XML
<xs:complexType name="ReferenceAttachmentType">
    <xs:complexContent>
        <xs:extension base="t:AttachmentType">
            <xs:sequence>
                <xs:element name="AttachLongPathName" type="xs:string" maxOccurs="1" minOccurs="0"></xs:element>
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>

```

## <a name="elements-and-attributes"></a>元素和属性

如果架构定义了特定要求，如 **sequence** **、minOccurs、maxOccurs** 和 **choice，** 请参阅定义部分。 
  
### <a name="child-elements"></a>子元素

|**元素**|**类型**|**说明**|
|:-----|:-----|:-----|
|[AttachLongPathName](attachlongpathname.md) <br/> |xs：string  <br/> ||
   
### <a name="attributes"></a>Attributes

无。
  

