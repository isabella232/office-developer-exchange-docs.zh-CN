---
title: AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cff8ef19-3e19-4107-9b35-c8a2b87a41bc
description: AddNewTelUriContactToGroup 元素指定 AddNewTelUriContactToGroup WSDL 操作的输入的数据。
ms.openlocfilehash: d99d557530397aa9edd2c23b595bdcb348783dd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753118"
---
# <a name="addnewteluricontacttogroup"></a><span data-ttu-id="7b511-103">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="7b511-103">AddNewTelUriContactToGroup</span></span>

<span data-ttu-id="7b511-104">**AddNewTelUriContactToGroup**元素指定**AddNewTelUriContactToGroup** WSDL 操作的输入的数据。</span><span class="sxs-lookup"><span data-stu-id="7b511-104">The **AddNewTelUriContactToGroup** element specifies the input data for the **AddNewTelUriContactToGroup** WSDL operation.</span></span> 
  
```XML
<AddNewTelUriContactToGroup>
   <TelUriAddress/>
   <ImContactSipUriAddress/>
   <ImTelephoneNumber/>
   <GroupId/>
</AddNewTelUriContactToGroup>
```

 <span data-ttu-id="7b511-105">**AddNewTelUriContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="7b511-105">**AddNewTelUriContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b511-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="7b511-106">Attributes and elements</span></span>

<span data-ttu-id="7b511-107">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="7b511-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b511-108">属性</span><span class="sxs-lookup"><span data-stu-id="7b511-108">Attributes</span></span>

<span data-ttu-id="7b511-109">无。</span><span class="sxs-lookup"><span data-stu-id="7b511-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7b511-110">子元素</span><span class="sxs-lookup"><span data-stu-id="7b511-110">Child elements</span></span>

<span data-ttu-id="7b511-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="7b511-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7b511-112">父元素</span><span class="sxs-lookup"><span data-stu-id="7b511-112">Parent elements</span></span>

<span data-ttu-id="7b511-113">无。</span><span class="sxs-lookup"><span data-stu-id="7b511-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7b511-114">备注</span><span class="sxs-lookup"><span data-stu-id="7b511-114">Remarks</span></span>

<span data-ttu-id="7b511-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="7b511-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="7b511-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="7b511-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b511-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="7b511-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b511-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="7b511-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b511-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="7b511-119">Schema name</span></span>  <br/> |<span data-ttu-id="7b511-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="7b511-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b511-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="7b511-121">Validation file</span></span>  <br/> |<span data-ttu-id="7b511-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7b511-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b511-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="7b511-123">Can be empty</span></span>  <br/> |<span data-ttu-id="7b511-124">False</span><span class="sxs-lookup"><span data-stu-id="7b511-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b511-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7b511-125">See also</span></span>

- [<span data-ttu-id="7b511-126">AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="7b511-126">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md)
- [<span data-ttu-id="7b511-127">在交换 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="7b511-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

