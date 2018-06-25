---
title: TimeZoneContext
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZoneContext
api_type:
- schema
ms.assetid: 573c462b-aa1d-4ba0-8852-e3f48b26873b
description: TimeZoneContext 元素用于简单对象访问协议 (SOAP) 标头中指定是要分配的 DateTime 属性的创建、 更新和检索的对象所在的时区时用作默认时区定义使用 Exchange Web Services (EWS)。
ms.openlocfilehash: 38b7ab4c587adac45fc3bcf351f417ea72313a97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19838239"
---
# <a name="timezonecontext"></a><span data-ttu-id="19194-103">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="19194-103">TimeZoneContext</span></span>

<span data-ttu-id="19194-104">**TimeZoneContext**元素用于简单对象访问协议 (SOAP) 标头中指定是要分配的 DateTime 属性的创建，更新的对象所在的时区时用作默认时区定义和通过使用 Exchange Web Services (EWS) 检索。</span><span class="sxs-lookup"><span data-stu-id="19194-104">The **TimeZoneContext** element is used in the Simple Object Access Protocol (SOAP) header to specify the time zone definition that is to be used as the default when assigning the time zone for the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span> 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 <span data-ttu-id="19194-105">**TimeZoneContextType**</span><span class="sxs-lookup"><span data-stu-id="19194-105">**TimeZoneContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="19194-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="19194-106">Attributes and elements</span></span>

<span data-ttu-id="19194-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="19194-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="19194-108">属性</span><span class="sxs-lookup"><span data-stu-id="19194-108">Attributes</span></span>

<span data-ttu-id="19194-109">无。</span><span class="sxs-lookup"><span data-stu-id="19194-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19194-110">子元素</span><span class="sxs-lookup"><span data-stu-id="19194-110">Child elements</span></span>

|<span data-ttu-id="19194-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="19194-111">**Element**</span></span>|<span data-ttu-id="19194-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="19194-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="19194-113">时区定义</span><span class="sxs-lookup"><span data-stu-id="19194-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="19194-114">指定的时间段和定义时区的切换。</span><span class="sxs-lookup"><span data-stu-id="19194-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="19194-115">父元素</span><span class="sxs-lookup"><span data-stu-id="19194-115">Parent elements</span></span>

<span data-ttu-id="19194-116">无。</span><span class="sxs-lookup"><span data-stu-id="19194-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19194-117">注解</span><span class="sxs-lookup"><span data-stu-id="19194-117">Remarks</span></span>

<span data-ttu-id="19194-118">描述此元素的架构位于运行 Microsoft Exchange Server 已安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="19194-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19194-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="19194-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19194-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="19194-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="19194-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="19194-121">Schema Name</span></span>  <br/> |<span data-ttu-id="19194-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="19194-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="19194-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="19194-123">Validation File</span></span>  <br/> |<span data-ttu-id="19194-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="19194-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="19194-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="19194-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="19194-126">False</span><span class="sxs-lookup"><span data-stu-id="19194-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19194-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="19194-127">See also</span></span>



- [<span data-ttu-id="19194-128">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="19194-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

