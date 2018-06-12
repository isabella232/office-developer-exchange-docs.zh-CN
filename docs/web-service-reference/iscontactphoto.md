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
description: IsContactPhoto 元素指示文件附件是否是联系人的图片。
ms.openlocfilehash: a015cd9bdb34ea9275952d5fe252a30cacf888ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825999"
---
# <a name="iscontactphoto"></a><span data-ttu-id="47963-103">IsContactPhoto</span><span class="sxs-lookup"><span data-stu-id="47963-103">IsContactPhoto</span></span>

<span data-ttu-id="47963-104">**IsContactPhoto**元素指示文件附件是否是联系人的图片。</span><span class="sxs-lookup"><span data-stu-id="47963-104">The **IsContactPhoto** element indicates whether the file attachment is a contact picture.</span></span> 
  
```xml
<IsContactPhoto>true or false</IsContactPhoto>
```

 <span data-ttu-id="47963-105">**boolean**</span><span class="sxs-lookup"><span data-stu-id="47963-105">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="47963-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="47963-106">Attributes and elements</span></span>

<span data-ttu-id="47963-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="47963-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="47963-108">属性</span><span class="sxs-lookup"><span data-stu-id="47963-108">Attributes</span></span>

<span data-ttu-id="47963-109">无。</span><span class="sxs-lookup"><span data-stu-id="47963-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="47963-110">子元素</span><span class="sxs-lookup"><span data-stu-id="47963-110">Child elements</span></span>

<span data-ttu-id="47963-111">无。</span><span class="sxs-lookup"><span data-stu-id="47963-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="47963-112">父元素</span><span class="sxs-lookup"><span data-stu-id="47963-112">Parent elements</span></span>

|<span data-ttu-id="47963-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="47963-113">**Element**</span></span>|<span data-ttu-id="47963-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="47963-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="47963-115">FileAttachment</span><span class="sxs-lookup"><span data-stu-id="47963-115">FileAttachment</span></span>](fileattachment.md) <br/> |<span data-ttu-id="47963-116">代表附加到 Exchange 存储中的项的文件。</span><span class="sxs-lookup"><span data-stu-id="47963-116">Represents a file that is attached to an item in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="47963-117">文本值</span><span class="sxs-lookup"><span data-stu-id="47963-117">Text value</span></span>

<span data-ttu-id="47963-118">此元素可以是**true**或**false**。</span><span class="sxs-lookup"><span data-stu-id="47963-118">This element can be either **true** or **false**.</span></span> <span data-ttu-id="47963-119">默认值为 **false** 。</span><span class="sxs-lookup"><span data-stu-id="47963-119">The default value is **false**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47963-120">备注</span><span class="sxs-lookup"><span data-stu-id="47963-120">Remarks</span></span>

<span data-ttu-id="47963-121">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="47963-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="47963-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="47963-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="47963-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="47963-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="47963-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="47963-124">Schema Name</span></span>  <br/> |<span data-ttu-id="47963-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="47963-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="47963-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="47963-126">Validation File</span></span>  <br/> |<span data-ttu-id="47963-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="47963-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="47963-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="47963-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="47963-129">False</span><span class="sxs-lookup"><span data-stu-id="47963-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="47963-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="47963-130">See also</span></span>



- [<span data-ttu-id="47963-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="47963-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

