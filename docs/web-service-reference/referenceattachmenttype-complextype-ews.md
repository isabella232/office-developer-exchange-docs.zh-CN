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
# <a name="referenceattachmenttype-complextype-ews"></a><span data-ttu-id="8b1be-102">ReferenceAttachmentType 复杂类型（EWS）</span><span class="sxs-lookup"><span data-stu-id="8b1be-102">ReferenceAttachmentType complexType (EWS)</span></span>

## <a name="type-information"></a><span data-ttu-id="8b1be-103">类型信息</span><span class="sxs-lookup"><span data-stu-id="8b1be-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b1be-104">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="8b1be-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8b1be-105">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="8b1be-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8b1be-106">类型 .xsd</span><span class="sxs-lookup"><span data-stu-id="8b1be-106">types.xsd</span></span>  <br/> |
|<span data-ttu-id="8b1be-107">**扩展基**</span><span class="sxs-lookup"><span data-stu-id="8b1be-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8b1be-108">t:AttachmentType</span><span class="sxs-lookup"><span data-stu-id="8b1be-108">t:AttachmentType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b1be-109">定义</span><span class="sxs-lookup"><span data-stu-id="8b1be-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8b1be-110">元素和属性</span><span class="sxs-lookup"><span data-stu-id="8b1be-110">Elements and attributes</span></span>

<span data-ttu-id="8b1be-111">如果架构定义了具体要求，如**sequence**、 **minOccurs**、 **maxOccurs**和**choice**，请参阅 "定义" 部分。</span><span class="sxs-lookup"><span data-stu-id="8b1be-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8b1be-112">子元素</span><span class="sxs-lookup"><span data-stu-id="8b1be-112">Child elements</span></span>

|<span data-ttu-id="8b1be-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="8b1be-113">**Element**</span></span>|<span data-ttu-id="8b1be-114">**类型**</span><span class="sxs-lookup"><span data-stu-id="8b1be-114">**Type**</span></span>|<span data-ttu-id="8b1be-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="8b1be-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b1be-116">AttachLongPathName</span><span class="sxs-lookup"><span data-stu-id="8b1be-116">AttachLongPathName</span></span>](attachlongpathname.md) <br/> |<span data-ttu-id="8b1be-117">xs： string</span><span class="sxs-lookup"><span data-stu-id="8b1be-117">xs:string</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8b1be-118">Attributes</span><span class="sxs-lookup"><span data-stu-id="8b1be-118">Attributes</span></span>

<span data-ttu-id="8b1be-119">无。</span><span class="sxs-lookup"><span data-stu-id="8b1be-119">None.</span></span>
  

