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
description: FileAsMapping 元素定义如何构造联系人显示的内容。
ms.openlocfilehash: 1ba0ae0daa56a72c29d8c0ccad64e3edae5f0b84
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754312"
---
# <a name="fileasmapping"></a><span data-ttu-id="e7448-103">FileAsMapping</span><span class="sxs-lookup"><span data-stu-id="e7448-103">FileAsMapping</span></span>

<span data-ttu-id="e7448-104">**FileAsMapping**元素定义如何构造联系人显示的内容。</span><span class="sxs-lookup"><span data-stu-id="e7448-104">The **FileAsMapping** element defines how to construct what is displayed for a contact.</span></span> 
  
```xml
<FileAsMapping/>
```

 <span data-ttu-id="e7448-105">**FileAsMappingType**</span><span class="sxs-lookup"><span data-stu-id="e7448-105">**FileAsMappingType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7448-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e7448-106">Attributes and elements</span></span>

<span data-ttu-id="e7448-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e7448-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7448-108">属性</span><span class="sxs-lookup"><span data-stu-id="e7448-108">Attributes</span></span>

<span data-ttu-id="e7448-109">无。</span><span class="sxs-lookup"><span data-stu-id="e7448-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7448-110">子元素</span><span class="sxs-lookup"><span data-stu-id="e7448-110">Child elements</span></span>

<span data-ttu-id="e7448-111">无。</span><span class="sxs-lookup"><span data-stu-id="e7448-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e7448-112">父元素</span><span class="sxs-lookup"><span data-stu-id="e7448-112">Parent elements</span></span>

|<span data-ttu-id="e7448-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7448-113">**Element**</span></span>|<span data-ttu-id="e7448-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7448-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7448-115">联系人</span><span class="sxs-lookup"><span data-stu-id="e7448-115">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="e7448-116">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="e7448-116">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e7448-117">文本值</span><span class="sxs-lookup"><span data-stu-id="e7448-117">Text value</span></span>

<span data-ttu-id="e7448-118">此元素的文本值仅限于以下字符串值之一：</span><span class="sxs-lookup"><span data-stu-id="e7448-118">The text value for this element is restricted to one of the following string values:</span></span>
  
- <span data-ttu-id="e7448-119">无</span><span class="sxs-lookup"><span data-stu-id="e7448-119">None</span></span>
    
- <span data-ttu-id="e7448-120">LastCommaFirst</span><span class="sxs-lookup"><span data-stu-id="e7448-120">LastCommaFirst</span></span>
    
- <span data-ttu-id="e7448-121">FirstSpaceLast</span><span class="sxs-lookup"><span data-stu-id="e7448-121">FirstSpaceLast</span></span>
    
- <span data-ttu-id="e7448-122">公司</span><span class="sxs-lookup"><span data-stu-id="e7448-122">Company</span></span>
    
- <span data-ttu-id="e7448-123">LastCommaFirstCompany</span><span class="sxs-lookup"><span data-stu-id="e7448-123">LastCommaFirstCompany</span></span>
    
- <span data-ttu-id="e7448-124">CompanyLastFirst</span><span class="sxs-lookup"><span data-stu-id="e7448-124">CompanyLastFirst</span></span>
    
- <span data-ttu-id="e7448-125">姓名</span><span class="sxs-lookup"><span data-stu-id="e7448-125">LastFirst</span></span>
    
- <span data-ttu-id="e7448-126">LastFirstCompany</span><span class="sxs-lookup"><span data-stu-id="e7448-126">LastFirstCompany</span></span>
    
- <span data-ttu-id="e7448-127">CompanyLastCommaFirst</span><span class="sxs-lookup"><span data-stu-id="e7448-127">CompanyLastCommaFirst</span></span>
    
- <span data-ttu-id="e7448-128">LastFirstSuffix</span><span class="sxs-lookup"><span data-stu-id="e7448-128">LastFirstSuffix</span></span>
    
- <span data-ttu-id="e7448-129">LastSpaceFirstCompany</span><span class="sxs-lookup"><span data-stu-id="e7448-129">LastSpaceFirstCompany</span></span>
    
- <span data-ttu-id="e7448-130">CompanyLastSpaceFirst</span><span class="sxs-lookup"><span data-stu-id="e7448-130">CompanyLastSpaceFirst</span></span>
    
- <span data-ttu-id="e7448-131">LastSpaceFirst</span><span class="sxs-lookup"><span data-stu-id="e7448-131">LastSpaceFirst</span></span>
    
- <span data-ttu-id="e7448-132">DisplayName</span><span class="sxs-lookup"><span data-stu-id="e7448-132">DisplayName</span></span>
    
- <span data-ttu-id="e7448-133">FirstName</span><span class="sxs-lookup"><span data-stu-id="e7448-133">FirstName</span></span>
    
- <span data-ttu-id="e7448-134">LastFirstMiddleSuffix</span><span class="sxs-lookup"><span data-stu-id="e7448-134">LastFirstMiddleSuffix</span></span>
    
- <span data-ttu-id="e7448-135">LastName</span><span class="sxs-lookup"><span data-stu-id="e7448-135">LastName</span></span>
    
- <span data-ttu-id="e7448-136">空</span><span class="sxs-lookup"><span data-stu-id="e7448-136">Empty</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e7448-137">注解</span><span class="sxs-lookup"><span data-stu-id="e7448-137">Remarks</span></span>

<span data-ttu-id="e7448-138">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e7448-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7448-139">元素信息</span><span class="sxs-lookup"><span data-stu-id="e7448-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7448-140">命名空间</span><span class="sxs-lookup"><span data-stu-id="e7448-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e7448-141">架构名称</span><span class="sxs-lookup"><span data-stu-id="e7448-141">Schema name</span></span>  <br/> |<span data-ttu-id="e7448-142">类型架构</span><span class="sxs-lookup"><span data-stu-id="e7448-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="e7448-143">验证文件</span><span class="sxs-lookup"><span data-stu-id="e7448-143">Validation file</span></span>  <br/> |<span data-ttu-id="e7448-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e7448-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e7448-145">可以为空</span><span class="sxs-lookup"><span data-stu-id="e7448-145">Can be empty</span></span>  <br/> |<span data-ttu-id="e7448-146">False</span><span class="sxs-lookup"><span data-stu-id="e7448-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7448-147">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7448-147">See also</span></span>



- [<span data-ttu-id="e7448-148">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7448-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)


[<span data-ttu-id="e7448-149">Creating Contacts (Exchange Web Services)</span><span class="sxs-lookup"><span data-stu-id="e7448-149">Creating Contacts (Exchange Web Services)</span></span>](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[<span data-ttu-id="e7448-150">更新联系人</span><span class="sxs-lookup"><span data-stu-id="e7448-150">Updating Contacts</span></span>](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[<span data-ttu-id="e7448-151">删除联系人</span><span class="sxs-lookup"><span data-stu-id="e7448-151">Deleting Contacts</span></span>](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

