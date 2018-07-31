---
title: ReferenceAttachmentType 复杂类型 (EWS)
manager: sethgros
ms.date: 03/9/2015
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 18bfa012-e903-d7f3-528a-31ccceb65463
ms.openlocfilehash: c53686ccd032cabcc3f64a3a6684f29afe63a9b1
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354174"
---
# <a name="referenceattachmenttype-complextype-ews"></a><span data-ttu-id="0a583-102">ReferenceAttachmentType 复杂类型 (EWS)</span><span class="sxs-lookup"><span data-stu-id="0a583-102">ReferenceAttachmentType complexType (EWS)</span></span>

## <a name="type-information"></a><span data-ttu-id="0a583-103">类型信息</span><span class="sxs-lookup"><span data-stu-id="0a583-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a583-104">**命名空间**</span><span class="sxs-lookup"><span data-stu-id="0a583-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a583-105">**架构文件**</span><span class="sxs-lookup"><span data-stu-id="0a583-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a583-106">types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a583-106">types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a583-107">**扩展基**</span><span class="sxs-lookup"><span data-stu-id="0a583-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a583-108">t:AttachmentType</span><span class="sxs-lookup"><span data-stu-id="0a583-108">t:AttachmentType</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a583-109">定义</span><span class="sxs-lookup"><span data-stu-id="0a583-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0a583-110">元素和属性</span><span class="sxs-lookup"><span data-stu-id="0a583-110">Elements and attributes</span></span>

<span data-ttu-id="0a583-111">如果此架构定义了具体要求，如**sequence**， **minOccurs**、 **maxOccurs**和**choice**，请参阅定义部分。</span><span class="sxs-lookup"><span data-stu-id="0a583-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a583-112">子元素</span><span class="sxs-lookup"><span data-stu-id="0a583-112">Child elements</span></span>

|<span data-ttu-id="0a583-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="0a583-113">**Element**</span></span>|<span data-ttu-id="0a583-114">**类型**</span><span class="sxs-lookup"><span data-stu-id="0a583-114">**Type**</span></span>|<span data-ttu-id="0a583-115">**说明**</span><span class="sxs-lookup"><span data-stu-id="0a583-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0a583-116">AttachLongPathName</span><span class="sxs-lookup"><span data-stu-id="0a583-116">AttachLongPathName</span></span>](attachlongpathname.md) <br/> |<span data-ttu-id="0a583-117">xs:string</span><span class="sxs-lookup"><span data-stu-id="0a583-117">xs:string</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0a583-118">属性</span><span class="sxs-lookup"><span data-stu-id="0a583-118">Attributes</span></span>

<span data-ttu-id="0a583-119">无。</span><span class="sxs-lookup"><span data-stu-id="0a583-119">None.</span></span>
  

