---
title: RemoveImContactFromGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a62b0640-9800-45a6-a297-2105ff36881e
description: RemoveImContactFromGroup 元素定义一个请求，以从即时消息组中删除即时消息联系人。
ms.openlocfilehash: 379994ad5832b05e9f7da61d752f7660a6eec5ad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466960"
---
# <a name="removeimcontactfromgroup"></a><span data-ttu-id="bab1a-103">RemoveImContactFromGroup</span><span class="sxs-lookup"><span data-stu-id="bab1a-103">RemoveImContactFromGroup</span></span>

<span data-ttu-id="bab1a-104">**RemoveImContactFromGroup**元素定义一个请求，以从即时消息组中删除即时消息联系人。</span><span class="sxs-lookup"><span data-stu-id="bab1a-104">The **RemoveImContactFromGroup** element defines a request to remove an instant messaging contact from an instant messaging group.</span></span> 
  
```XML
<RemoveImContactFromGroup>
   <ContactId/>
   <GroupId/>
</RemoveImContactFromGroup>
```

 <span data-ttu-id="bab1a-105">**RemoveImContactFromGroupType**</span><span class="sxs-lookup"><span data-stu-id="bab1a-105">**RemoveImContactFromGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="bab1a-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bab1a-106">Attributes and elements</span></span>

<span data-ttu-id="bab1a-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bab1a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bab1a-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="bab1a-108">Attributes</span></span>

<span data-ttu-id="bab1a-109">无。</span><span class="sxs-lookup"><span data-stu-id="bab1a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bab1a-110">子元素</span><span class="sxs-lookup"><span data-stu-id="bab1a-110">Child elements</span></span>

<span data-ttu-id="bab1a-111">[ContactId](contactid.md)  | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="bab1a-111">[ContactId](contactid.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bab1a-112">父元素</span><span class="sxs-lookup"><span data-stu-id="bab1a-112">Parent elements</span></span>

<span data-ttu-id="bab1a-113">无。</span><span class="sxs-lookup"><span data-stu-id="bab1a-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bab1a-114">说明</span><span class="sxs-lookup"><span data-stu-id="bab1a-114">Remarks</span></span>

<span data-ttu-id="bab1a-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="bab1a-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="bab1a-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="bab1a-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bab1a-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="bab1a-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bab1a-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="bab1a-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="bab1a-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="bab1a-119">Schema name</span></span>  <br/> |<span data-ttu-id="bab1a-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="bab1a-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="bab1a-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="bab1a-121">Validation file</span></span>  <br/> |<span data-ttu-id="bab1a-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="bab1a-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="bab1a-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="bab1a-123">Can be empty</span></span>  <br/> ||
   

