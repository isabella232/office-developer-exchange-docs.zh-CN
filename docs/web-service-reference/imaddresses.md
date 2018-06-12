---
title: ImAddresses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ImAddresses
api_type:
- schema
ms.assetid: 29f614a7-7fe6-47fa-b5f2-8feff106aa99
description: ImAddresses 元素均表示一个联系人的即时消息地址的集合。
ms.openlocfilehash: e8c7a22e8537a4526594042905f7bb8454238bf1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19825861"
---
# <a name="imaddresses"></a><span data-ttu-id="b0e55-103">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="b0e55-103">ImAddresses</span></span>

<span data-ttu-id="b0e55-104">**ImAddresses**元素均表示一个联系人的即时消息地址的集合。</span><span class="sxs-lookup"><span data-stu-id="b0e55-104">The **ImAddresses** element represents a collection of instant messaging addresses for a contact.</span></span> 
  
```xml
<ImAddresses>
   <Entry/>
</ImAddresses>
```

 <span data-ttu-id="b0e55-105">**ImAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="b0e55-105">**ImAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b0e55-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b0e55-106">Attributes and elements</span></span>

<span data-ttu-id="b0e55-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b0e55-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0e55-108">属性</span><span class="sxs-lookup"><span data-stu-id="b0e55-108">Attributes</span></span>

<span data-ttu-id="b0e55-109">无。</span><span class="sxs-lookup"><span data-stu-id="b0e55-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b0e55-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b0e55-110">Child elements</span></span>

|<span data-ttu-id="b0e55-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0e55-111">**Element**</span></span>|<span data-ttu-id="b0e55-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0e55-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0e55-113">条目 (IMAddress)</span><span class="sxs-lookup"><span data-stu-id="b0e55-113">Entry (IMAddress)</span></span>](entry-imaddress.md) <br/> |<span data-ttu-id="b0e55-114">代表即时消息联系人的地址。</span><span class="sxs-lookup"><span data-stu-id="b0e55-114">Represents an instant messaging address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b0e55-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b0e55-115">Parent elements</span></span>

|<span data-ttu-id="b0e55-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b0e55-116">**Element**</span></span>|<span data-ttu-id="b0e55-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b0e55-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b0e55-118">联系人</span><span class="sxs-lookup"><span data-stu-id="b0e55-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="b0e55-119">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="b0e55-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0e55-120">备注</span><span class="sxs-lookup"><span data-stu-id="b0e55-120">Remarks</span></span>

<span data-ttu-id="b0e55-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b0e55-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0e55-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b0e55-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0e55-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b0e55-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b0e55-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b0e55-124">Schema name</span></span>  <br/> |<span data-ttu-id="b0e55-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="b0e55-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b0e55-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b0e55-126">Validation file</span></span>  <br/> |<span data-ttu-id="b0e55-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b0e55-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b0e55-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b0e55-128">Can be empty</span></span>  <br/> |<span data-ttu-id="b0e55-129">False</span><span class="sxs-lookup"><span data-stu-id="b0e55-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b0e55-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b0e55-130">See also</span></span>



- [<span data-ttu-id="b0e55-131">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b0e55-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

