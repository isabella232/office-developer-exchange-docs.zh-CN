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
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461035"
---
# <a name="fileasmapping"></a><span data-ttu-id="6f2b0-103">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="6f2b0-103">FileAsMapping</span></span>

<span data-ttu-id="6f2b0-104">**FileAsMapping**元素定义如何构建联系人的显示内容。</span><span class="sxs-lookup"><span data-stu-id="6f2b0-104">The **FileAsMapping** element defines how to construct what is displayed for a contact.</span></span> 
  
```xml
<FileAsMapping/>
```

 <span data-ttu-id="6f2b0-105">**FileAsMappingType**</span><span class="sxs-lookup"><span data-stu-id="6f2b0-105">**FileAsMappingType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6f2b0-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6f2b0-106">Attributes and elements</span></span>

<span data-ttu-id="6f2b0-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6f2b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f2b0-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6f2b0-108">Attributes</span></span>

<span data-ttu-id="6f2b0-109">无。</span><span class="sxs-lookup"><span data-stu-id="6f2b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6f2b0-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6f2b0-110">Child elements</span></span>

<span data-ttu-id="6f2b0-111">无。</span><span class="sxs-lookup"><span data-stu-id="6f2b0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6f2b0-112">父元素</span><span class="sxs-lookup"><span data-stu-id="6f2b0-112">Parent elements</span></span>

|<span data-ttu-id="6f2b0-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="6f2b0-113">**Element**</span></span>|<span data-ttu-id="6f2b0-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="6f2b0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f2b0-115">Contact</span><span class="sxs-lookup"><span data-stu-id="6f2b0-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="6f2b0-116">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="6f2b0-116">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="6f2b0-117">文本值</span><span class="sxs-lookup"><span data-stu-id="6f2b0-117">Text value</span></span>

<span data-ttu-id="6f2b0-118">此元素的文本值被限制为以下字符串值之一：</span><span class="sxs-lookup"><span data-stu-id="6f2b0-118">The text value for this element is restricted to one of the following string values:</span></span>
  
- <span data-ttu-id="6f2b0-119">无</span><span class="sxs-lookup"><span data-stu-id="6f2b0-119">None</span></span>
    
- <span data-ttu-id="6f2b0-120">LastCommaFirst</span><span class="sxs-lookup"><span data-stu-id="6f2b0-120">LastCommaFirst</span></span>
    
- <span data-ttu-id="6f2b0-121">FirstSpaceLast</span><span class="sxs-lookup"><span data-stu-id="6f2b0-121">FirstSpaceLast</span></span>
    
- <span data-ttu-id="6f2b0-122">Company</span><span class="sxs-lookup"><span data-stu-id="6f2b0-122">Company</span></span>
    
- <span data-ttu-id="6f2b0-123">LastCommaFirstCompany</span><span class="sxs-lookup"><span data-stu-id="6f2b0-123">LastCommaFirstCompany</span></span>
    
- <span data-ttu-id="6f2b0-124">CompanyLastFirst</span><span class="sxs-lookup"><span data-stu-id="6f2b0-124">CompanyLastFirst</span></span>
    
- <span data-ttu-id="6f2b0-125">名字</span><span class="sxs-lookup"><span data-stu-id="6f2b0-125">LastFirst</span></span>
    
- <span data-ttu-id="6f2b0-126">LastFirstCompany</span><span class="sxs-lookup"><span data-stu-id="6f2b0-126">LastFirstCompany</span></span>
    
- <span data-ttu-id="6f2b0-127">CompanyLastCommaFirst</span><span class="sxs-lookup"><span data-stu-id="6f2b0-127">CompanyLastCommaFirst</span></span>
    
- <span data-ttu-id="6f2b0-128">LastFirstSuffix</span><span class="sxs-lookup"><span data-stu-id="6f2b0-128">LastFirstSuffix</span></span>
    
- <span data-ttu-id="6f2b0-129">LastSpaceFirstCompany</span><span class="sxs-lookup"><span data-stu-id="6f2b0-129">LastSpaceFirstCompany</span></span>
    
- <span data-ttu-id="6f2b0-130">CompanyLastSpaceFirst</span><span class="sxs-lookup"><span data-stu-id="6f2b0-130">CompanyLastSpaceFirst</span></span>
    
- <span data-ttu-id="6f2b0-131">LastSpaceFirst</span><span class="sxs-lookup"><span data-stu-id="6f2b0-131">LastSpaceFirst</span></span>
    
- <span data-ttu-id="6f2b0-132">DisplayName</span><span class="sxs-lookup"><span data-stu-id="6f2b0-132">DisplayName</span></span>
    
- <span data-ttu-id="6f2b0-133">FirstName</span><span class="sxs-lookup"><span data-stu-id="6f2b0-133">FirstName</span></span>
    
- <span data-ttu-id="6f2b0-134">LastFirstMiddleSuffix</span><span class="sxs-lookup"><span data-stu-id="6f2b0-134">LastFirstMiddleSuffix</span></span>
    
- <span data-ttu-id="6f2b0-135">LastName</span><span class="sxs-lookup"><span data-stu-id="6f2b0-135">LastName</span></span>
    
- <span data-ttu-id="6f2b0-136">Empty</span><span class="sxs-lookup"><span data-stu-id="6f2b0-136">Empty</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6f2b0-137">备注</span><span class="sxs-lookup"><span data-stu-id="6f2b0-137">Remarks</span></span>

<span data-ttu-id="6f2b0-138">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6f2b0-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6f2b0-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="6f2b0-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f2b0-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="6f2b0-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6f2b0-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="6f2b0-141">Schema name</span></span>  <br/> |<span data-ttu-id="6f2b0-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="6f2b0-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="6f2b0-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="6f2b0-143">Validation file</span></span>  <br/> |<span data-ttu-id="6f2b0-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6f2b0-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6f2b0-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="6f2b0-145">Can be empty</span></span>  <br/> |<span data-ttu-id="6f2b0-146">False</span><span class="sxs-lookup"><span data-stu-id="6f2b0-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6f2b0-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6f2b0-147">See also</span></span>



- [<span data-ttu-id="6f2b0-148">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6f2b0-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="6f2b0-149">创建联系人（Exchange Web 服务）</span><span class="sxs-lookup"><span data-stu-id="6f2b0-149">Creating Contacts (Exchange Web Services)</span></span>](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="6f2b0-150">更新联系人</span><span class="sxs-lookup"><span data-stu-id="6f2b0-150">Updating Contacts</span></span>](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="6f2b0-151">删除联系人</span><span class="sxs-lookup"><span data-stu-id="6f2b0-151">Deleting Contacts</span></span>](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

