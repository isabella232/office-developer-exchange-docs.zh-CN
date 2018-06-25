---
title: RemoveDelegate
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RemoveDelegate
api_type:
- schema
ms.assetid: f21c5171-62e7-47c8-99b1-22e1ff5883bb
description: RemoveDelegate 元素定义从邮箱中删除代理人的请求。 Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。
ms.openlocfilehash: 27618b1767c99b26a5f4c06e97a20e063b598d9d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19827085"
---
# <a name="removedelegate"></a><span data-ttu-id="e7906-104">RemoveDelegate</span><span class="sxs-lookup"><span data-stu-id="e7906-104">RemoveDelegate</span></span>

<span data-ttu-id="e7906-105">**RemoveDelegate**元素定义从邮箱中删除代理人的请求。</span><span class="sxs-lookup"><span data-stu-id="e7906-105">The **RemoveDelegate** element defines a request to remove delegates from a mailbox.</span></span> <span data-ttu-id="e7906-106">Microsoft Exchange Server 2007 Service Pack 1 (SP1) 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e7906-106">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span> 
  
```xml
<RemoveDelegate>
      <Mailbox/>
   <UserIds/>
</RemoveDelegate>
```

 <span data-ttu-id="e7906-107">**RemoveDelegateType**</span><span class="sxs-lookup"><span data-stu-id="e7906-107">**RemoveDelegateType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e7906-108">属性和元素</span><span class="sxs-lookup"><span data-stu-id="e7906-108">Attributes and elements</span></span>

<span data-ttu-id="e7906-109">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="e7906-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e7906-110">属性</span><span class="sxs-lookup"><span data-stu-id="e7906-110">Attributes</span></span>

<span data-ttu-id="e7906-111">无。</span><span class="sxs-lookup"><span data-stu-id="e7906-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e7906-112">子元素</span><span class="sxs-lookup"><span data-stu-id="e7906-112">Child elements</span></span>

|<span data-ttu-id="e7906-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="e7906-113">**Element**</span></span>|<span data-ttu-id="e7906-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="e7906-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7906-115">Mailbox</span><span class="sxs-lookup"><span data-stu-id="e7906-115">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="e7906-116">标识的主体的邮箱。</span><span class="sxs-lookup"><span data-stu-id="e7906-116">Identifies the principal's mailbox.</span></span>  <br/> |
|[<span data-ttu-id="e7906-117">UserIds</span><span class="sxs-lookup"><span data-stu-id="e7906-117">UserIds</span></span>](userids.md) <br/> |<span data-ttu-id="e7906-118">包含委派用户从主体的邮箱中删除一个数组。</span><span class="sxs-lookup"><span data-stu-id="e7906-118">Contains an array of delegate users to remove from a principal's mailbox.</span></span> <span data-ttu-id="e7906-119">Exchange 2007 SP1 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="e7906-119">This element was introduced in Exchange 2007 SP1.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e7906-120">父元素</span><span class="sxs-lookup"><span data-stu-id="e7906-120">Parent elements</span></span>

<span data-ttu-id="e7906-121">无。</span><span class="sxs-lookup"><span data-stu-id="e7906-121">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e7906-122">备注</span><span class="sxs-lookup"><span data-stu-id="e7906-122">Remarks</span></span>

<span data-ttu-id="e7906-123">描述此元素的架构位于正在运行 Microsoft Exchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="e7906-123">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e7906-124">元素信息</span><span class="sxs-lookup"><span data-stu-id="e7906-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7906-125">命名空间</span><span class="sxs-lookup"><span data-stu-id="e7906-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e7906-126">架构名称</span><span class="sxs-lookup"><span data-stu-id="e7906-126">Schema Name</span></span>  <br/> |<span data-ttu-id="e7906-127">消息架构</span><span class="sxs-lookup"><span data-stu-id="e7906-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e7906-128">验证文件</span><span class="sxs-lookup"><span data-stu-id="e7906-128">Validation File</span></span>  <br/> |<span data-ttu-id="e7906-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e7906-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e7906-130">可以为空</span><span class="sxs-lookup"><span data-stu-id="e7906-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="e7906-131">False</span><span class="sxs-lookup"><span data-stu-id="e7906-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e7906-132">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e7906-132">See also</span></span>



[<span data-ttu-id="e7906-133">RemoveDelegate 操作</span><span class="sxs-lookup"><span data-stu-id="e7906-133">RemoveDelegate operation</span></span>](removedelegate-operation.md)


- [<span data-ttu-id="e7906-134">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="e7906-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

