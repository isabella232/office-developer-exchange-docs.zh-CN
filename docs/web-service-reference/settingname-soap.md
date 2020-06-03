---
title: SettingName （SOAP）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 8bcb0411-58b0-4e37-b97e-00c07dcbecb1
description: SettingName 元素表示响应中的设置的名称。
ms.openlocfilehash: d492b82b7385d6403f15c08356db5d0503792d54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466722"
---
# <a name="settingname-soap"></a><span data-ttu-id="f7e87-103">SettingName （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f7e87-103">SettingName (SOAP)</span></span>

<span data-ttu-id="f7e87-104">**SettingName**元素表示响应中的设置的名称。</span><span class="sxs-lookup"><span data-stu-id="f7e87-104">The **SettingName** element represents the name of a setting in the response.</span></span> 
  
```XML
<SettingName/>
```

 <span data-ttu-id="f7e87-105">**string**</span><span class="sxs-lookup"><span data-stu-id="f7e87-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f7e87-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="f7e87-106">Attributes and elements</span></span>

<span data-ttu-id="f7e87-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="f7e87-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f7e87-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="f7e87-108">Attributes</span></span>

<span data-ttu-id="f7e87-109">无。</span><span class="sxs-lookup"><span data-stu-id="f7e87-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f7e87-110">子元素</span><span class="sxs-lookup"><span data-stu-id="f7e87-110">Child elements</span></span>

<span data-ttu-id="f7e87-111">无。</span><span class="sxs-lookup"><span data-stu-id="f7e87-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f7e87-112">父元素</span><span class="sxs-lookup"><span data-stu-id="f7e87-112">Parent elements</span></span>

|<span data-ttu-id="f7e87-113">**元素**</span><span class="sxs-lookup"><span data-stu-id="f7e87-113">**Element**</span></span>|<span data-ttu-id="f7e87-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="f7e87-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f7e87-115">UserSettingError （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f7e87-115">UserSettingError (SOAP)</span></span>](usersettingerror-soap.md) <br/> |<span data-ttu-id="f7e87-116">表示检索用户设置时返回的错误。</span><span class="sxs-lookup"><span data-stu-id="f7e87-116">Represents an error that is returned while retrieving a user setting.</span></span>  <br/> |
|[<span data-ttu-id="f7e87-117">DomainSettingError （SOAP）</span><span class="sxs-lookup"><span data-stu-id="f7e87-117">DomainSettingError (SOAP)</span></span>](domainsettingerror-soap.md) <br/> |<span data-ttu-id="f7e87-118">表示检索域设置时发生的错误。</span><span class="sxs-lookup"><span data-stu-id="f7e87-118">Represents an error that occurred while retrieving a domain setting.</span></span> <span data-ttu-id="f7e87-119">这表示来自**GetDomainSettings**请求的一个错误。</span><span class="sxs-lookup"><span data-stu-id="f7e87-119">This represents an error from a **GetDomainSettings** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f7e87-120">文本值</span><span class="sxs-lookup"><span data-stu-id="f7e87-120">Text value</span></span>

<span data-ttu-id="f7e87-121">**SettingName**元素的值表示响应中的设置的名称。</span><span class="sxs-lookup"><span data-stu-id="f7e87-121">The value of the **SettingName** element represents the name of a setting in a response.</span></span> 
  
<span data-ttu-id="f7e87-122">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="f7e87-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f7e87-123">元素信息</span><span class="sxs-lookup"><span data-stu-id="f7e87-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f7e87-124">命名空间</span><span class="sxs-lookup"><span data-stu-id="f7e87-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="f7e87-125">架构名称</span><span class="sxs-lookup"><span data-stu-id="f7e87-125">Schema Name</span></span>  <br/> |<span data-ttu-id="f7e87-126">自动发现架构</span><span class="sxs-lookup"><span data-stu-id="f7e87-126">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="f7e87-127">验证文件</span><span class="sxs-lookup"><span data-stu-id="f7e87-127">Validation File</span></span>  <br/> |<span data-ttu-id="f7e87-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="f7e87-128">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="f7e87-129">可以为空</span><span class="sxs-lookup"><span data-stu-id="f7e87-129">Can be Empty</span></span>  <br/> |<span data-ttu-id="f7e87-130">True</span><span class="sxs-lookup"><span data-stu-id="f7e87-130">True</span></span>  <br/> |
   

