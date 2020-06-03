---
title: ReferenceAttachmentType 复杂类型（EWS）
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: 24f5a62eadd490b5b0000dfe048850c44540f266
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528732"
---
# <a name="referenceattachmenttype-complextype-ews"></a>ReferenceAttachmentType 复杂类型（EWS）

## <a name="type-information"></a>类型信息

|||
|:-----|:-----|
|**命名空间** <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|**架构文件** <br/> |类型 .xsd  <br/> |
|**扩展基** <br/> |t:AttachmentType  <br/> |
   
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

如果架构定义了具体要求，如**sequence**、 **minOccurs**、 **maxOccurs**和**choice**，请参阅 "定义" 部分。 
  
### <a name="child-elements"></a>子元素

|**元素**|**类型**|**说明**|
|:-----|:-----|:-----|
|[AttachLongPathName](attachlongpathname.md) <br/> |xs： string  <br/> ||
   
### <a name="attributes"></a>Attributes

无。
  

