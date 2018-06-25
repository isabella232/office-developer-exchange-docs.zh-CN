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
description: FolderShape 元素标识要在 GetFolder、 FindFolder 或 SyncFolderHierarchy 响应中包含的文件夹属性。
ms.openlocfilehash: 8ebdd70ef13ee9f0cce9020b9212576cba782be4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19754408"
---
# <a name="foldershape"></a><span data-ttu-id="3092f-103">FolderShape</span><span class="sxs-lookup"><span data-stu-id="3092f-103">FolderShape</span></span>

<span data-ttu-id="3092f-104">**FolderShape**元素标识要在[GetFolder](getfolder.md)、 [FindFolder](findfolder.md)或[SyncFolderHierarchy](syncfolderhierarchy.md)响应中包含的文件夹属性。</span><span class="sxs-lookup"><span data-stu-id="3092f-104">The **FolderShape** element identifies the folder properties to include in a [GetFolder](getfolder.md), [FindFolder](findfolder.md), or [SyncFolderHierarchy](syncfolderhierarchy.md) response.</span></span> 
  
```xml
<FolderShape>
   <BaseShape/>
   <AdditionalProperties/>
</FolderShape>
```

 <span data-ttu-id="3092f-105">**FolderResponseShapeType**</span><span class="sxs-lookup"><span data-stu-id="3092f-105">**FolderResponseShapeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3092f-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="3092f-106">Attributes and elements</span></span>

<span data-ttu-id="3092f-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="3092f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3092f-108">属性</span><span class="sxs-lookup"><span data-stu-id="3092f-108">Attributes</span></span>

<span data-ttu-id="3092f-109">无。</span><span class="sxs-lookup"><span data-stu-id="3092f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3092f-110">子元素</span><span class="sxs-lookup"><span data-stu-id="3092f-110">Child elements</span></span>

|<span data-ttu-id="3092f-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="3092f-111">**Element**</span></span>|<span data-ttu-id="3092f-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="3092f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3092f-113">BaseShape</span><span class="sxs-lookup"><span data-stu-id="3092f-113">BaseShape</span></span>](baseshape.md) <br/> |<span data-ttu-id="3092f-114">标识要返回的响应中的属性的基本配置。</span><span class="sxs-lookup"><span data-stu-id="3092f-114">Identifies the basic configuration of properties to return in a response.</span></span>  <br/> |
|[<span data-ttu-id="3092f-115">AdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="3092f-115">AdditionalProperties</span></span>](additionalproperties.md) <br/> |<span data-ttu-id="3092f-116">标识要返回的响应中的其他属性。</span><span class="sxs-lookup"><span data-stu-id="3092f-116">Identifies additional properties to return in a response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3092f-117">父元素</span><span class="sxs-lookup"><span data-stu-id="3092f-117">Parent elements</span></span>

|<span data-ttu-id="3092f-118">**元素**</span><span class="sxs-lookup"><span data-stu-id="3092f-118">**Element**</span></span>|<span data-ttu-id="3092f-119">**说明**</span><span class="sxs-lookup"><span data-stu-id="3092f-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3092f-120">FindFolder</span><span class="sxs-lookup"><span data-stu-id="3092f-120">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="3092f-121">定义一个请求，以确定邮箱中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="3092f-121">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="3092f-122">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="3092f-122">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
|[<span data-ttu-id="3092f-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="3092f-123">GetFolder</span></span>](getfolder.md) <br/> |<span data-ttu-id="3092f-124">定义从 Exchange 存储中获取文件夹的请求。</span><span class="sxs-lookup"><span data-stu-id="3092f-124">Defines a request to get a folder from the Exchange store.</span></span>  <br/> <span data-ttu-id="3092f-125">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="3092f-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetFolder` <br/> |
|[<span data-ttu-id="3092f-126">SyncFolderHierarchy</span><span class="sxs-lookup"><span data-stu-id="3092f-126">SyncFolderHierarchy</span></span>](syncfolderhierarchy.md) <br/> |<span data-ttu-id="3092f-127">定义同步客户端上的文件夹层次结构的请求。</span><span class="sxs-lookup"><span data-stu-id="3092f-127">Defines a request to synchronize a folder hierarchy on a client.</span></span>  <br/> <span data-ttu-id="3092f-128">以下是此元素的 XPath 表达式：</span><span class="sxs-lookup"><span data-stu-id="3092f-128">The following is the XPath expression to this element:</span></span>  <br/>  `/SyncFolderHierarchy` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3092f-129">注解</span><span class="sxs-lookup"><span data-stu-id="3092f-129">Remarks</span></span>

<span data-ttu-id="3092f-130">**FolderShape**元素是[FindFolder](findfolder.md)元素的必需的子元素。</span><span class="sxs-lookup"><span data-stu-id="3092f-130">The **FolderShape** element is a required child element of the [FindFolder](findfolder.md) element.</span></span> 
  
<span data-ttu-id="3092f-131">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="3092f-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="example"></a><span data-ttu-id="3092f-132">示例</span><span class="sxs-lookup"><span data-stu-id="3092f-132">Example</span></span>

<span data-ttu-id="3092f-133">请求的下面的示例演示如何查找位于第一级的收件箱文件夹中的所有文件夹。</span><span class="sxs-lookup"><span data-stu-id="3092f-133">The following example of a request demonstrates how to find all folders located in the first level of the Inbox folder.</span></span>
  
```
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindFolder Traversal="Shallow" xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

## <a name="element-information"></a><span data-ttu-id="3092f-134">元素信息</span><span class="sxs-lookup"><span data-stu-id="3092f-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3092f-135">命名空间</span><span class="sxs-lookup"><span data-stu-id="3092f-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="3092f-136">架构名称</span><span class="sxs-lookup"><span data-stu-id="3092f-136">Schema Name</span></span>  <br/> |<span data-ttu-id="3092f-137">消息架构</span><span class="sxs-lookup"><span data-stu-id="3092f-137">Messages schema</span></span>  <br/> |
|<span data-ttu-id="3092f-138">验证文件</span><span class="sxs-lookup"><span data-stu-id="3092f-138">Validation File</span></span>  <br/> |<span data-ttu-id="3092f-139">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="3092f-139">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="3092f-140">可以为空</span><span class="sxs-lookup"><span data-stu-id="3092f-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="3092f-141">False</span><span class="sxs-lookup"><span data-stu-id="3092f-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3092f-142">另请参阅</span><span class="sxs-lookup"><span data-stu-id="3092f-142">See also</span></span>



[<span data-ttu-id="3092f-143">FindFolder</span><span class="sxs-lookup"><span data-stu-id="3092f-143">FindFolder</span></span>](findfolder.md)

