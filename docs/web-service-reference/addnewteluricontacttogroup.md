---
title: AddNewTelUriContactToGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cff8ef19-3e19-4107-9b35-c8a2b87a41bc
description: AddNewTelUriContactToGroup 元素指定 AddNewTelUriContactToGroup WSDL 操作的输入数据。
ms.openlocfilehash: 151c5b1dab7a3ffc9630fb4e4192b90bd1d4ae38
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464929"
---
# <a name="addnewteluricontacttogroup"></a><span data-ttu-id="c271c-103">AddNewTelUriContactToGroup</span><span class="sxs-lookup"><span data-stu-id="c271c-103">AddNewTelUriContactToGroup</span></span>

<span data-ttu-id="c271c-104">**AddNewTelUriContactToGroup**元素指定**AddNewTelUriContactToGroup** WSDL 操作的输入数据。</span><span class="sxs-lookup"><span data-stu-id="c271c-104">The **AddNewTelUriContactToGroup** element specifies the input data for the **AddNewTelUriContactToGroup** WSDL operation.</span></span> 
  
```XML
<AddNewTelUriContactToGroup>
   <TelUriAddress/>
   <ImContactSipUriAddress/>
   <ImTelephoneNumber/>
   <GroupId/>
</AddNewTelUriContactToGroup>
```

 <span data-ttu-id="c271c-105">**AddNewTelUriContactToGroupType**</span><span class="sxs-lookup"><span data-stu-id="c271c-105">**AddNewTelUriContactToGroupType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c271c-106">属性和元素</span><span class="sxs-lookup"><span data-stu-id="c271c-106">Attributes and elements</span></span>

<span data-ttu-id="c271c-107">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="c271c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c271c-108">Attributes</span><span class="sxs-lookup"><span data-stu-id="c271c-108">Attributes</span></span>

<span data-ttu-id="c271c-109">无。</span><span class="sxs-lookup"><span data-stu-id="c271c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c271c-110">子元素</span><span class="sxs-lookup"><span data-stu-id="c271c-110">Child elements</span></span>

<span data-ttu-id="c271c-111">[TelUriAddress](teluriaddress.md)  | [ImContactSipUriAddress](imcontactsipuriaddress.md)  | [ImTelephoneNumber](imtelephonenumber.md)  | [GroupId](groupid.md)</span><span class="sxs-lookup"><span data-stu-id="c271c-111">[TelUriAddress](teluriaddress.md) | [ImContactSipUriAddress](imcontactsipuriaddress.md) | [ImTelephoneNumber](imtelephonenumber.md) | [GroupId](groupid.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c271c-112">父元素</span><span class="sxs-lookup"><span data-stu-id="c271c-112">Parent elements</span></span>

<span data-ttu-id="c271c-113">无。</span><span class="sxs-lookup"><span data-stu-id="c271c-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c271c-114">说明</span><span class="sxs-lookup"><span data-stu-id="c271c-114">Remarks</span></span>

<span data-ttu-id="c271c-115">Exchange Server 2013 中引入了此元素。</span><span class="sxs-lookup"><span data-stu-id="c271c-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c271c-116">描述此元素的架构位于承载 Exchange Web Services 的 IIS 虚拟目录中。</span><span class="sxs-lookup"><span data-stu-id="c271c-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c271c-117">元素信息</span><span class="sxs-lookup"><span data-stu-id="c271c-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c271c-118">命名空间</span><span class="sxs-lookup"><span data-stu-id="c271c-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c271c-119">架构名称</span><span class="sxs-lookup"><span data-stu-id="c271c-119">Schema name</span></span>  <br/> |<span data-ttu-id="c271c-120">消息架构</span><span class="sxs-lookup"><span data-stu-id="c271c-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c271c-121">验证文件</span><span class="sxs-lookup"><span data-stu-id="c271c-121">Validation file</span></span>  <br/> |<span data-ttu-id="c271c-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c271c-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c271c-123">可以为空</span><span class="sxs-lookup"><span data-stu-id="c271c-123">Can be empty</span></span>  <br/> |<span data-ttu-id="c271c-124">False</span><span class="sxs-lookup"><span data-stu-id="c271c-124">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c271c-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c271c-125">See also</span></span>

- [<span data-ttu-id="c271c-126">AddNewTelUriContactToGroup 操作</span><span class="sxs-lookup"><span data-stu-id="c271c-126">AddNewTelUriContactToGroup operation</span></span>](addnewteluricontacttogroup-operation.md)
- [<span data-ttu-id="c271c-127">Exchange 中的 EWS XML 元素</span><span class="sxs-lookup"><span data-stu-id="c271c-127">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

