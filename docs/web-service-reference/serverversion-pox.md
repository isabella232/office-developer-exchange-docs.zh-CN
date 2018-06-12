---
title: ServerVersion (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a
description: ServerVersion 元素均表示运行 Microsoft Exchange Server 的计算机的版本号。
ms.openlocfilehash: ef0562e166094d75d0dd92f5f48bb558e11a2cad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19827391"
---
# <a name="serverversion-pox"></a><span data-ttu-id="cb094-103">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="cb094-103">ServerVersion (POX)</span></span>

<span data-ttu-id="cb094-104">**ServerVersion**元素均表示运行 Microsoft Exchange Server 的计算机的版本号。</span><span class="sxs-lookup"><span data-stu-id="cb094-104">The **ServerVersion** element represents the version number of the computer that is running Microsoft Exchange Server.</span></span> 
  
- [<span data-ttu-id="cb094-105">自动发现 (POX)</span><span class="sxs-lookup"><span data-stu-id="cb094-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="cb094-106">响应 (POX)</span><span class="sxs-lookup"><span data-stu-id="cb094-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="cb094-107">帐户 (POX)</span><span class="sxs-lookup"><span data-stu-id="cb094-107">Account (POX)</span></span>](account-pox.md)
- [<span data-ttu-id="cb094-108">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="cb094-108">Protocol (POX)</span></span>](protocol-pox.md)
- [<span data-ttu-id="cb094-109">ServerVersion (POX)</span><span class="sxs-lookup"><span data-stu-id="cb094-109">ServerVersion (POX)</span></span>](serverversion-pox.md)
  
```xml
<ServerVersion/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="cb094-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="cb094-110">Attributes and elements</span></span>

<span data-ttu-id="cb094-111">如下章节中介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="cb094-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb094-112">属性</span><span class="sxs-lookup"><span data-stu-id="cb094-112">Attributes</span></span>

<span data-ttu-id="cb094-113">无。</span><span class="sxs-lookup"><span data-stu-id="cb094-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb094-114">子元素</span><span class="sxs-lookup"><span data-stu-id="cb094-114">Child elements</span></span>

<span data-ttu-id="cb094-115">无。</span><span class="sxs-lookup"><span data-stu-id="cb094-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb094-116">父元素</span><span class="sxs-lookup"><span data-stu-id="cb094-116">Parent elements</span></span>

|<span data-ttu-id="cb094-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="cb094-117">**Element**</span></span>|<span data-ttu-id="cb094-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="cb094-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb094-119">协议 (POX)</span><span class="sxs-lookup"><span data-stu-id="cb094-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="cb094-120">包含客户端连接到运行 Microsoft Exchange 已安装了客户端访问服务器角色的计算机的规格。</span><span class="sxs-lookup"><span data-stu-id="cb094-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb094-121">文本值</span><span class="sxs-lookup"><span data-stu-id="cb094-121">Text value</span></span>

<span data-ttu-id="cb094-122">文本值表示 Exchange server 版本数。</span><span class="sxs-lookup"><span data-stu-id="cb094-122">The text value represents the Exchange server version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb094-123">备注</span><span class="sxs-lookup"><span data-stu-id="cb094-123">Remarks</span></span>

<span data-ttu-id="cb094-124">**ServerVersion**值才等于 EXCH 或 EXPR[类型 (POX)](type-pox.md)元素是否有效。</span><span class="sxs-lookup"><span data-stu-id="cb094-124">The **ServerVersion** value is only valid if the [Type (POX)](type-pox.md) element is equal to EXCH or EXPR.</span></span> <span data-ttu-id="cb094-125">**ServerVersion**值是一个十六进制数字，包含 MajorVersion、 MinorVersion 和 MajorBuildNumber 的服务器。</span><span class="sxs-lookup"><span data-stu-id="cb094-125">The **ServerVersion** value is a hexadecimal number that contains the MajorVersion, MinorVersion, and MajorBuildNumber of the server.</span></span> 
  
## <a name="example"></a><span data-ttu-id="cb094-126">示例</span><span class="sxs-lookup"><span data-stu-id="cb094-126">Example</span></span>

<span data-ttu-id="cb094-127">下面的示例 coverts **ServerVersion**值，它是以获取和显示 MajorVersion、 MinorVersion 和 MajorBuildNumber 自动发现响应中返回。</span><span class="sxs-lookup"><span data-stu-id="cb094-127">The following example coverts a **ServerVersion** value that is returned in an Autodiscover response to obtain and display the MajorVersion, MinorVersion, and MajorBuildNumber.</span></span> <span data-ttu-id="cb094-128">本示例可输入**ServerVersion**值的十六进制值。</span><span class="sxs-lookup"><span data-stu-id="cb094-128">This example enables you to enter a hexadecimal value for the **ServerVersion** value.</span></span> <span data-ttu-id="cb094-129">如果没有**ServerVersion**输入值，使用默认**ServerVersion**值为 738180DA。</span><span class="sxs-lookup"><span data-stu-id="cb094-129">If no **ServerVersion** value is entered, a default **ServerVersion** value of 738180DA is used.</span></span> 
  
```csharp
static void Main(string[] args)
{
    // Convert a ServerVersion value that is returned from an Autodiscover request.
    // The value is a hex value and can be converted to the MajorVersion, MinorVersion,
    // and MajorBuildNumber.
    Console.WriteLine("Enter ServerVersion returned from the Autodiscover (eg. 738180DA) and Enter.");
    Console.WriteLine("To use the default ServerVersion of 738180DA, just hit Enter.");
    // Get the hexadecimal ServerVersion value.
    string serverversionhex = Console.ReadLine();
    // If nothing is entered, use the default server version of "738180DA"
    if (serverversionhex == "")
    {
        serverversionhex = "738180DA";
    }
    Console.WriteLine("ServerVersion (Hex) = " + serverversionhex);
    string serverversionbinary = Convert.ToString(Convert.ToInt32(serverversionhex, 16), 2);
    // The ServerVersion (binary) should be 32 bits in length. If the 
    // server version in binary is a length of 31 characters, the leading
    // zero has been removed in the conversion process. Put the missing zero back.
    if (serverversionbinary.Length == 31)
    {
        serverversionbinary = String.Concat("0", serverversionbinary);
    }
    Console.WriteLine("ServerVersion (bin) = " + serverversionbinary);
    // The first 4 bits represent a number used for comparison against  
    // older version number structures. You can ignore this.
    // The next 6 bits represent the major version number.
    int majorversion = Convert.ToInt32(serverversionbinary.Substring(4, 6), 2);
    Console.WriteLine("MajorVersion: " + majorversion);
    // The next 6 bits represent the minor version number.
    int minorversion = Convert.ToInt32(serverversionbinary.Substring(10, 6), 2);
    Console.WriteLine("MinorVersion: " + minorversion);
    
    // The next bit represent a flag - you can ignore this.
    // The next 15 bits represent the major build number.
    int majorbuild = Convert.ToInt32(serverversionbinary.Substring(17, 15), 2);
    Console.WriteLine("MajorBuildVersion: " + majorbuild);
    Console.WriteLine("\n\nPress any key to continue");
    Console.ReadKey();
}
```

## <a name="see-also"></a><span data-ttu-id="cb094-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="cb094-130">See also</span></span>

- [<span data-ttu-id="cb094-131">Exchange POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="cb094-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

