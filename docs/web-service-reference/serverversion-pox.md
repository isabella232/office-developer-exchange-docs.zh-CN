---
title: ServerVersion （POX）
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2c0bc41c-2452-4fc8-a19c-0e85f9fdbc4a
description: ServerVersion 元素表示运行 Microsoft Exchange Server 的计算机的版本号。
ms.openlocfilehash: 3ef531a69d2dd00ee9784c9eb191684ce517e842
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461966"
---
# <a name="serverversion-pox"></a><span data-ttu-id="bee8c-103">ServerVersion （POX）</span><span class="sxs-lookup"><span data-stu-id="bee8c-103">ServerVersion (POX)</span></span>

<span data-ttu-id="bee8c-104">**ServerVersion**元素表示运行 Microsoft Exchange Server 的计算机的版本号。</span><span class="sxs-lookup"><span data-stu-id="bee8c-104">The **ServerVersion** element represents the version number of the computer that is running Microsoft Exchange Server.</span></span> 
  
- [<span data-ttu-id="bee8c-105">自动发现（POX）</span><span class="sxs-lookup"><span data-stu-id="bee8c-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md) 
- [<span data-ttu-id="bee8c-106">响应（POX）</span><span class="sxs-lookup"><span data-stu-id="bee8c-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="bee8c-107">帐户（POX）</span><span class="sxs-lookup"><span data-stu-id="bee8c-107">Account (POX)</span></span>](account-pox.md)
- [<span data-ttu-id="bee8c-108">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="bee8c-108">Protocol (POX)</span></span>](protocol-pox.md)
- [<span data-ttu-id="bee8c-109">ServerVersion （POX）</span><span class="sxs-lookup"><span data-stu-id="bee8c-109">ServerVersion (POX)</span></span>](serverversion-pox.md)
  
```xml
<ServerVersion/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="bee8c-110">属性和元素</span><span class="sxs-lookup"><span data-stu-id="bee8c-110">Attributes and elements</span></span>

<span data-ttu-id="bee8c-111">下面各部分介绍了属性、子元素和父元素。</span><span class="sxs-lookup"><span data-stu-id="bee8c-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bee8c-112">Attributes</span><span class="sxs-lookup"><span data-stu-id="bee8c-112">Attributes</span></span>

<span data-ttu-id="bee8c-113">无。</span><span class="sxs-lookup"><span data-stu-id="bee8c-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bee8c-114">子元素</span><span class="sxs-lookup"><span data-stu-id="bee8c-114">Child elements</span></span>

<span data-ttu-id="bee8c-115">无。</span><span class="sxs-lookup"><span data-stu-id="bee8c-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="bee8c-116">父元素</span><span class="sxs-lookup"><span data-stu-id="bee8c-116">Parent elements</span></span>

|<span data-ttu-id="bee8c-117">**元素**</span><span class="sxs-lookup"><span data-stu-id="bee8c-117">**Element**</span></span>|<span data-ttu-id="bee8c-118">**说明**</span><span class="sxs-lookup"><span data-stu-id="bee8c-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bee8c-119">协议（POX）</span><span class="sxs-lookup"><span data-stu-id="bee8c-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="bee8c-120">包含将客户端连接到运行 Microsoft Exchange 且安装了客户端访问服务器角色的计算机的规范。</span><span class="sxs-lookup"><span data-stu-id="bee8c-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="bee8c-121">文本值</span><span class="sxs-lookup"><span data-stu-id="bee8c-121">Text value</span></span>

<span data-ttu-id="bee8c-122">该文本值代表 Exchange 服务器版本号。</span><span class="sxs-lookup"><span data-stu-id="bee8c-122">The text value represents the Exchange server version number.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bee8c-123">备注</span><span class="sxs-lookup"><span data-stu-id="bee8c-123">Remarks</span></span>

<span data-ttu-id="bee8c-124">仅当[Type （POX）](type-pox.md)元素等于 EXCH 或 EXPR 时， **ServerVersion**值才有效。</span><span class="sxs-lookup"><span data-stu-id="bee8c-124">The **ServerVersion** value is only valid if the [Type (POX)](type-pox.md) element is equal to EXCH or EXPR.</span></span> <span data-ttu-id="bee8c-125">**ServerVersion**值是一个十六进制数，包含服务器的 MajorVersion、MinorVersion 和 MajorBuildNumber。</span><span class="sxs-lookup"><span data-stu-id="bee8c-125">The **ServerVersion** value is a hexadecimal number that contains the MajorVersion, MinorVersion, and MajorBuildNumber of the server.</span></span> 
  
## <a name="example"></a><span data-ttu-id="bee8c-126">示例</span><span class="sxs-lookup"><span data-stu-id="bee8c-126">Example</span></span>

<span data-ttu-id="bee8c-127">下面的示例 coverts 在自动发现响应中返回的**ServerVersion**值，以获取并显示 MajorVersion、MinorVersion 和 MajorBuildNumber。</span><span class="sxs-lookup"><span data-stu-id="bee8c-127">The following example coverts a **ServerVersion** value that is returned in an Autodiscover response to obtain and display the MajorVersion, MinorVersion, and MajorBuildNumber.</span></span> <span data-ttu-id="bee8c-128">本示例使您能够为**ServerVersion**值输入十六进制值。</span><span class="sxs-lookup"><span data-stu-id="bee8c-128">This example enables you to enter a hexadecimal value for the **ServerVersion** value.</span></span> <span data-ttu-id="bee8c-129">如果未输入**ServerVersion**值，则使用默认的**ServerVersion**值738180DA。</span><span class="sxs-lookup"><span data-stu-id="bee8c-129">If no **ServerVersion** value is entered, a default **ServerVersion** value of 738180DA is used.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="bee8c-130">另请参阅</span><span class="sxs-lookup"><span data-stu-id="bee8c-130">See also</span></span>

- [<span data-ttu-id="bee8c-131">Exchange 的 POX 自动发现 XML 元素</span><span class="sxs-lookup"><span data-stu-id="bee8c-131">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

