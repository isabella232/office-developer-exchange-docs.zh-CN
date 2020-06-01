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
description: FolderShape 元素标识要包括在 GetFolder、FindFolder 或 SyncFolderHierarchy 响应中的文件夹属性。
ms.openlocfilehash: f841fcc4570604c474387dfa24ec07c9d2784f62
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461343"
---
# <a name="foldershape"></a><span data-ttu-id="8214c-103">FolderShape</span><span class="sxs-lookup"><span data-stu-id="8214c-103">FolderShape</span></span>

<span data-ttu-id="8214c-104">**FolderShape**元素标识要包括在[GetFolder](getfolder.md)、 [FindFolder](findfolder.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)响应中的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="8214c-104">The **FolderShape** element identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span> 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 <span data-ttu-id="8214c-105">**FolderResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="8214c-105">**FolderResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8214c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="8214c-106">Attributes and elements</span></span>

<span data-ttu-id="8214c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="8214c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8214c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="8214c-108">Attributes</span></span>

<span data-ttu-id="8214c-109">无。</span><span class="sxs-lookup"><span data-stu-id="8214c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8214c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="8214c-110">Child elements</span></span>

|<span data-ttu-id="8214c-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="8214c-111">**Element**</span></span>|<span data-ttu-id="8214c-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="8214c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8214c-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="8214c-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="8214c-114">标识要在响应中返回的属性的基本配置。</span><span class="sxs-lookup"><span data-stu-id="8214c-114">Identifies the basic configuration of properties to return in a response.</span></span>  <br/> |
|[<span data-ttu-id="8214c-115">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="8214c-115">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="8214c-116">标识要在响应中返回的其他属性。</span><span class="sxs-lookup"><span data-stu-id="8214c-116">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8214c-117">父元素</span><span class="sxs-lookup"><span data-stu-id="8214c-117">Parent elements</span></span>

|<span data-ttu-id="8214c-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="8214c-118">**Element**</span></span>|<span data-ttu-id="8214c-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="8214c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8214c-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="8214c-120">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="8214c-121">定义用于标识邮箱中的文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="8214c-121">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="8214c-122">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="8214c-122">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
|[<span data-ttu-id="8214c-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="8214c-123">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="8214c-124">定义从 Exchange 存储中获取文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="8214c-124">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="8214c-125">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="8214c-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetFolder` <br/> |
|[<span data-ttu-id="8214c-126">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="8214c-126">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="8214c-127">定义在客户端上同步文件夹层次结构的请求。</span><span class="sxs-lookup"><span data-stu-id="8214c-127">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> <span data-ttu-id="8214c-128">下面是此元素的 XPath 表达式： </span><span class="sxs-lookup"><span data-stu-id="8214c-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8214c-129">备注</span><span class="sxs-lookup"><span data-stu-id="8214c-129">Remarks</span></span>

<span data-ttu-id="8214c-130">**FolderShape**元素是[FindFolder](findfolder.md)元素所需的子元素。</span><span class="sxs-lookup"><span data-stu-id="8214c-130">The **FolderShape** element is a required child element of the [FindFolder](findfolder.md) element.</span></span> 
  
<span data-ttu-id="8214c-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="8214c-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="8214c-132">示例</span><span class="sxs-lookup"><span data-stu-id="8214c-132">Example</span></span>

<span data-ttu-id="8214c-133">下面的请求示例演示如何查找位于收件箱文件夹的第一级中的所有文件夹。</span><span class="sxs-lookup"><span data-stu-id="8214c-133">The following example of a request demonstrates how to find all folders located in the first level of the Inbox folder.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="8214c-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="8214c-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8214c-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="8214c-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="8214c-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="8214c-136">Schema Name</span></span>  <br/> |<span data-ttu-id="8214c-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="8214c-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="8214c-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="8214c-138">Validation File</span></span>  <br/> |<span data-ttu-id="8214c-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8214c-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="8214c-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="8214c-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="8214c-141">False</span><span class="sxs-lookup"><span data-stu-id="8214c-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8214c-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="8214c-142">See also</span></span>



[<span data-ttu-id="8214c-143">FindFolder</span><span class="sxs-lookup"><span data-stu-id="8214c-143">FindFolder</span></span>](findfolder.md)

