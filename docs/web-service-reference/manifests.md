---
title: 清单
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 650d9fc0-1504-4db4-95d6-d3ba86df66ca
description: 清单元素包含为电子邮件帐户安装的 base64 编码的应用程序清单的集合。
ms.openlocfilehash: 91239e2337f7a1886d8947f558a86110755a93df
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44450814"
---
# <a name="manifests"></a><span data-ttu-id="22fe6-103">清单</span><span class="sxs-lookup"><span data-stu-id="22fe6-103">Manifests</span></span>

<span data-ttu-id="22fe6-104">**清单**元素包含为电子邮件帐户安装的 base64 编码的应用程序清单的集合。</span><span class="sxs-lookup"><span data-stu-id="22fe6-104">The **Manifests** element contains a collection of base64-encoded app manifests that are installed for the email account.</span></span> 
  
```XML
<Manifests>
   <Manifest/>
</Manifests>
```

 <span data-ttu-id="22fe6-105">**ArrayOfAppManifestsType**</span><span class="sxs-lookup"><span data-stu-id="22fe6-105">**ArrayOfAppManifestsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="22fe6-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="22fe6-106">Attributes and elements</span></span>

<span data-ttu-id="22fe6-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="22fe6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="22fe6-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="22fe6-108">Attributes</span></span>

<span data-ttu-id="22fe6-109">无。</span><span class="sxs-lookup"><span data-stu-id="22fe6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="22fe6-110">子元素</span><span class="sxs-lookup"><span data-stu-id="22fe6-110">Child elements</span></span>

[<span data-ttu-id="22fe6-111">清单</span><span class="sxs-lookup"><span data-stu-id="22fe6-111">Manifest</span></span>](manifest.md)
  
### <a name="parent-elements"></a><span data-ttu-id="22fe6-112">父元素</span><span class="sxs-lookup"><span data-stu-id="22fe6-112">Parent elements</span></span>

[<span data-ttu-id="22fe6-113">GetAppManifestsResponse</span><span class="sxs-lookup"><span data-stu-id="22fe6-113">GetAppManifestsResponse</span></span>](getappmanifestsresponse.md)
  
## <a name="remarks"></a><span data-ttu-id="22fe6-114">备注</span><span class="sxs-lookup"><span data-stu-id="22fe6-114">Remarks</span></span>

<span data-ttu-id="22fe6-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="22fe6-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="22fe6-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="22fe6-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="22fe6-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="22fe6-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="22fe6-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="22fe6-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="22fe6-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="22fe6-119">Schema name</span></span>  <br/> |<span data-ttu-id="22fe6-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="22fe6-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="22fe6-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="22fe6-121">Validation file</span></span>  <br/> |<span data-ttu-id="22fe6-122">消息 .xsd</span><span class="sxs-lookup"><span data-stu-id="22fe6-122">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="22fe6-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="22fe6-123">Can be empty</span></span>  <br/> ||
   

