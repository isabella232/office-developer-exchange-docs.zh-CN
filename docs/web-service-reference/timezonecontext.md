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
description: 当为使用 Exchange Web 服务（EWS）创建、更新和检索的对象的 DateTime 属性分配时区时，在简单对象访问协议（SOAP）头中使用 TimeZoneContext 元素来指定要用作默认的时区定义。
ms.openlocfilehash: 26727317ccf34338e8d62ec92bd7a44d43a6cfdb
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460251"
---
# <a name="timezonecontext"></a><span data-ttu-id="6c6e9-103">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="6c6e9-103">TimeZoneContext</span></span>

<span data-ttu-id="6c6e9-104">当为使用 Exchange Web 服务（EWS）创建、更新和检索的对象的 DateTime 属性分配时区时，在简单对象访问协议（SOAP）头中使用**TimeZoneContext**元素来指定要用作默认的时区定义。</span><span class="sxs-lookup"><span data-stu-id="6c6e9-104">The **TimeZoneContext** element is used in the Simple Object Access Protocol (SOAP) header to specify the time zone definition that is to be used as the default when assigning the time zone for the DateTime properties of objects that are created, updated, and retrieved by using Exchange Web Services (EWS).</span></span> 
  
```xml
<TimeZoneContext>
   <TimeZoneDefinition/>
</TimeZoneContext>
```

 <span data-ttu-id="6c6e9-105">**TimeZoneContextType**</span><span class="sxs-lookup"><span data-stu-id="6c6e9-105">**TimeZoneContextType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6c6e9-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="6c6e9-106">Attributes and elements</span></span>

<span data-ttu-id="6c6e9-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="6c6e9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6c6e9-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="6c6e9-108">Attributes</span></span>

<span data-ttu-id="6c6e9-109">无。</span><span class="sxs-lookup"><span data-stu-id="6c6e9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6c6e9-110">子元素</span><span class="sxs-lookup"><span data-stu-id="6c6e9-110">Child elements</span></span>

|<span data-ttu-id="6c6e9-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="6c6e9-111">**Element**</span></span>|<span data-ttu-id="6c6e9-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="6c6e9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6c6e9-113">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="6c6e9-113">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="6c6e9-114">指定用于定义时区的周期和转换。</span><span class="sxs-lookup"><span data-stu-id="6c6e9-114">Specifies the periods and transitions that define a time zone.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6c6e9-115">父元素</span><span class="sxs-lookup"><span data-stu-id="6c6e9-115">Parent elements</span></span>

<span data-ttu-id="6c6e9-116">无。</span><span class="sxs-lookup"><span data-stu-id="6c6e9-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6c6e9-117">说明</span><span class="sxs-lookup"><span data-stu-id="6c6e9-117">Remarks</span></span>

<span data-ttu-id="6c6e9-118">描述此元素的架构位于运行 Microsoft Exchange Server 且安装了客户端访问服务器角色的计算机的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="6c6e9-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6c6e9-119">元素信息</span><span class="sxs-lookup"><span data-stu-id="6c6e9-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c6e9-120">命名空间</span><span class="sxs-lookup"><span data-stu-id="6c6e9-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="6c6e9-121">架构名称</span><span class="sxs-lookup"><span data-stu-id="6c6e9-121">Schema Name</span></span>  <br/> |<span data-ttu-id="6c6e9-122">类型架构</span><span class="sxs-lookup"><span data-stu-id="6c6e9-122">Types schema</span></span>  <br/> |
|<span data-ttu-id="6c6e9-123">验证文件</span><span class="sxs-lookup"><span data-stu-id="6c6e9-123">Validation File</span></span>  <br/> |<span data-ttu-id="6c6e9-124">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="6c6e9-124">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="6c6e9-125">可以为空</span><span class="sxs-lookup"><span data-stu-id="6c6e9-125">Can be Empty</span></span>  <br/> |<span data-ttu-id="6c6e9-126">False</span><span class="sxs-lookup"><span data-stu-id="6c6e9-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6c6e9-127">另请参阅</span><span class="sxs-lookup"><span data-stu-id="6c6e9-127">See also</span></span>



- [<span data-ttu-id="6c6e9-128">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="6c6e9-128">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

