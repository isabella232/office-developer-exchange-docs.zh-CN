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
description: ImAddresses 元素表示联系人的即时消息地址的集合。
ms.openlocfilehash: 24ff74d29c918d71116e25e097878b6e4e0a8ead
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460426"
---
# <a name="imaddresses"></a><span data-ttu-id="b1ddf-103">ImAddresses</span><span class="sxs-lookup"><span data-stu-id="b1ddf-103">ImAddresses</span></span>

<span data-ttu-id="b1ddf-104">**ImAddresses**元素表示联系人的即时消息地址的集合。</span><span class="sxs-lookup"><span data-stu-id="b1ddf-104">The **ImAddresses** element represents a collection of instant messaging addresses for a contact.</span></span> 
  
```xml
<ImAddresses>
   <Entry/>
</ImAddresses>
```

 <span data-ttu-id="b1ddf-105">**ImAddressDictionaryType**</span><span class="sxs-lookup"><span data-stu-id="b1ddf-105">**ImAddressDictionaryType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b1ddf-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="b1ddf-106">Attributes and elements</span></span>

<span data-ttu-id="b1ddf-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="b1ddf-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b1ddf-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="b1ddf-108">Attributes</span></span>

<span data-ttu-id="b1ddf-109">无。</span><span class="sxs-lookup"><span data-stu-id="b1ddf-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b1ddf-110">子元素</span><span class="sxs-lookup"><span data-stu-id="b1ddf-110">Child elements</span></span>

|<span data-ttu-id="b1ddf-111">**元素**</span><span class="sxs-lookup"><span data-stu-id="b1ddf-111">**Element**</span></span>|<span data-ttu-id="b1ddf-112">**说明**</span><span class="sxs-lookup"><span data-stu-id="b1ddf-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1ddf-113">条目（IMAddress）</span><span class="sxs-lookup"><span data-stu-id="b1ddf-113">Entry (IMAddress)</span></span>](entry-imaddress.md) <br/> |<span data-ttu-id="b1ddf-114">表示联系人的即时消息地址。</span><span class="sxs-lookup"><span data-stu-id="b1ddf-114">Represents an instant messaging address for a contact.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b1ddf-115">父元素</span><span class="sxs-lookup"><span data-stu-id="b1ddf-115">Parent elements</span></span>

|<span data-ttu-id="b1ddf-116">**元素**</span><span class="sxs-lookup"><span data-stu-id="b1ddf-116">**Element**</span></span>|<span data-ttu-id="b1ddf-117">**说明**</span><span class="sxs-lookup"><span data-stu-id="b1ddf-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b1ddf-118">Contact</span><span class="sxs-lookup"><span data-stu-id="b1ddf-118">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="b1ddf-119">表示 Exchange 联系人项目。</span><span class="sxs-lookup"><span data-stu-id="b1ddf-119">Represents an Exchange contact item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b1ddf-120">说明</span><span class="sxs-lookup"><span data-stu-id="b1ddf-120">Remarks</span></span>

<span data-ttu-id="b1ddf-121">描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="b1ddf-121">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b1ddf-122">元素信息</span><span class="sxs-lookup"><span data-stu-id="b1ddf-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b1ddf-123">命名空间</span><span class="sxs-lookup"><span data-stu-id="b1ddf-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b1ddf-124">架构名称</span><span class="sxs-lookup"><span data-stu-id="b1ddf-124">Schema name</span></span>  <br/> |<span data-ttu-id="b1ddf-125">类型架构</span><span class="sxs-lookup"><span data-stu-id="b1ddf-125">Types schema</span></span>  <br/> |
|<span data-ttu-id="b1ddf-126">验证文件</span><span class="sxs-lookup"><span data-stu-id="b1ddf-126">Validation file</span></span>  <br/> |<span data-ttu-id="b1ddf-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b1ddf-127">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b1ddf-128">可以为空</span><span class="sxs-lookup"><span data-stu-id="b1ddf-128">Can be empty</span></span>  <br/> |<span data-ttu-id="b1ddf-129">False</span><span class="sxs-lookup"><span data-stu-id="b1ddf-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b1ddf-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="b1ddf-130">See also</span></span>



- [<span data-ttu-id="b1ddf-131">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="b1ddf-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

