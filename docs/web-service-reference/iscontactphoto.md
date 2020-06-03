---
title: IsContactPhoto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsContactPhoto
api_type:
- schema
ms.assetid: ae36b5f9-a787-4863-9dbc-258ad724801d
description: IsContactPhoto 元素指示文件附件是否为联系人图片。
ms.openlocfilehash: f60e558ab4f20b59c1d5ae51f9dfca430feeff00
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455546"
---
# <a name="iscontactphoto"></a><span data-ttu-id="22e4e-103">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="22e4e-103">IsContactPhoto</span></span>

<span data-ttu-id="22e4e-104">**IsContactPhoto**元素指示文件附件是否为联系人图片。</span><span class="sxs-lookup"><span data-stu-id="22e4e-104">The **IsContactPhoto** element indicates whether the file attachment is a contact picture.</span></span> 
  
```xml
<IsContactPhoto>true or false</IsContactPhoto>
```

 <span data-ttu-id="22e4e-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="22e4e-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22e4e-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22e4e-106">Attributes and elements</span></span>

<span data-ttu-id="22e4e-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22e4e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22e4e-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="22e4e-108">Attributes</span></span>

<span data-ttu-id="22e4e-109">无。</span><span class="sxs-lookup"><span data-stu-id="22e4e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22e4e-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22e4e-110">Child elements</span></span>

<span data-ttu-id="22e4e-111">无。</span><span class="sxs-lookup"><span data-stu-id="22e4e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="22e4e-112">父元素</span><span class="sxs-lookup"><span data-stu-id="22e4e-112">Parent elements</span></span>

|<span data-ttu-id="22e4e-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="22e4e-113">**Element**</span></span>|<span data-ttu-id="22e4e-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="22e4e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="22e4e-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="22e4e-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="22e4e-116">代表附加到 Exchange 存储中的项目的文件。</span><span class="sxs-lookup"><span data-stu-id="22e4e-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="22e4e-117">文本值</span><span class="sxs-lookup"><span data-stu-id="22e4e-117">Text value</span></span>

<span data-ttu-id="22e4e-118">此元素可以是**true** ，也可以是**false**。</span><span class="sxs-lookup"><span data-stu-id="22e4e-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="22e4e-119">默认值为 **false**。</span><span class="sxs-lookup"><span data-stu-id="22e4e-119">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="22e4e-120">备注</span><span class="sxs-lookup"><span data-stu-id="22e4e-120">Remarks</span></span>

<span data-ttu-id="22e4e-121">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22e4e-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22e4e-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="22e4e-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22e4e-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="22e4e-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="22e4e-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="22e4e-124">Schema Name</span></span>  <br/> |<span data-ttu-id="22e4e-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="22e4e-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="22e4e-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="22e4e-126">Validation File</span></span>  <br/> |<span data-ttu-id="22e4e-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="22e4e-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="22e4e-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="22e4e-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="22e4e-129">False</span><span class="sxs-lookup"><span data-stu-id="22e4e-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="22e4e-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="22e4e-130">See also</span></span>



- [<span data-ttu-id="22e4e-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="22e4e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

