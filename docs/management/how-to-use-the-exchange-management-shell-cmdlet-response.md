---
title: 使用 Exchange 命令行管理程序 cmdlet 响应
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: 了解如何使用 Exchange 托管应用程序中的 Exchange 命令行管理程序 cmdlet 的响应。
ms.openlocfilehash: 5edf75afd556f67e815bc519c87586f2f62f057b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753020"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a><span data-ttu-id="acaf5-103">使用 Exchange 命令行管理程序 cmdlet 响应</span><span class="sxs-lookup"><span data-stu-id="acaf5-103">Use the Exchange Management Shell cmdlet response</span></span>

<span data-ttu-id="acaf5-104">了解如何使用 Exchange 托管应用程序中的 Exchange 命令行管理程序 cmdlet 的响应。</span><span class="sxs-lookup"><span data-stu-id="acaf5-104">Learn how to use the response from an Exchange Management Shell cmdlet in your Exchange managed application.</span></span>
  
<span data-ttu-id="acaf5-105">**适用于：** Exchange Online |Exchange Server 2013 |Office 365</span><span class="sxs-lookup"><span data-stu-id="acaf5-105">**Applies to:** Exchange Online | Exchange Server 2013 | Office 365</span></span>
  
<span data-ttu-id="acaf5-106">每个 Exchange Management Shell cmdlet 可返回提供一致视图中的 Exchange 命令行管理程序环境的任何对象的一个或多个[PSObject](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject%28VS.85%29.aspx)实例。</span><span class="sxs-lookup"><span data-stu-id="acaf5-106">Each Exchange Management Shell cmdlet returns one or more [PSObject](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject%28VS.85%29.aspx) instances that provide a consistent view of any object in the Exchange Management Shell environment.</span></span> <span data-ttu-id="acaf5-107">本文提供有关如何使用**PSObject**实例的属性可返回基础的 Exchange Server 2013 API 对象的属性值的信息。</span><span class="sxs-lookup"><span data-stu-id="acaf5-107">This article provides information about how to use the properties of a **PSObject** instance to return the property values of the underlying Exchange Server 2013 API object.</span></span> 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a><span data-ttu-id="acaf5-108">使用 cmdlet 响应的先决条件</span><span class="sxs-lookup"><span data-stu-id="acaf5-108">Prerequisites for using cmdlet responses</span></span>
<span data-ttu-id="acaf5-109"><a name="prerequisites_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="acaf5-109"></span></span>

<span data-ttu-id="acaf5-110">若要使用 cmdlet 响应，您需要对**System.Automation.Management**命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="acaf5-110">To use cmdlet responses, you need a reference to the **System.Automation.Management** namespace.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="acaf5-111">当您使用 Visual Studio 创建应用程序时，您必须将 System.Mangagement.Automation.dll 程序集的引用添加到项目中。</span><span class="sxs-lookup"><span data-stu-id="acaf5-111">When you are using Visual Studio to create an application, you must add a reference to the System.Mangagement.Automation.dll assembly to the project.</span></span> <span data-ttu-id="acaf5-112">您可以在以下位置之一找到该程序集：</span><span class="sxs-lookup"><span data-stu-id="acaf5-112">You can find the assembly in one of the following locations:</span></span> 
> - <span data-ttu-id="acaf5-113">对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell 安装目录 ($PSHOME)。</span><span class="sxs-lookup"><span data-stu-id="acaf5-113">For Windows XP and Windows Vista operating systems, the Windows PowerShell installation directory ($PSHOME).</span></span> 
> - <span data-ttu-id="acaf5-114">对于 Windows 7 和 Windows 8 操作系统，以下文件夹： Windows\assembly\GAC_MSIL\System.Management.Automation。</span><span class="sxs-lookup"><span data-stu-id="acaf5-114">For the Windows 7 and Windows 8 operating systems, the following folder: Windows\assembly\GAC_MSIL\System.Management.Automation.</span></span> 
  
## <a name="windows-powershell-remote-runspace"></a><span data-ttu-id="acaf5-115">Windows PowerShell 远程运行空间</span><span class="sxs-lookup"><span data-stu-id="acaf5-115">Windows PowerShell remote runspace</span></span>
<span data-ttu-id="acaf5-116"><a name="usingremoterunspace_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="acaf5-116"></span></span>

<span data-ttu-id="acaf5-117">Exchange 命令行管理程序的所有命令，甚至在本地服务器运行的命令使用远程 Windows PowerShell 功能。</span><span class="sxs-lookup"><span data-stu-id="acaf5-117">The Exchange Management Shell uses remote Windows PowerShell features for all commands, even commands that are run on the local server.</span></span> <span data-ttu-id="acaf5-118">因此，从 Exchange 命令行管理程序 cmdlet 的所有响应序列都化的 XML。</span><span class="sxs-lookup"><span data-stu-id="acaf5-118">As a result, all responses from Exchange Management Shell cmdlets are serialized XML.</span></span> <span data-ttu-id="acaf5-119">这意味着，尽管响应对象指示用于生成响应的 Exchange 对象类型，response 对象无法转换为 Exchange 对象类型;相反，您必须使用公开响应对象以获取从 Exchange 对象类型的值的属性包。</span><span class="sxs-lookup"><span data-stu-id="acaf5-119">This means that although the response object indicates the Exchange object type that was used to generate the response, the response object cannot be cast to the Exchange object type; instead, you must use the property bag that is exposed by the response object to obtain the values from the Exchange object type.</span></span>
  
<span data-ttu-id="acaf5-120">响应对象中的属性包中包含的键/值对的每个公共属性或方法中的 Exchange 对象类型。</span><span class="sxs-lookup"><span data-stu-id="acaf5-120">The property bag in the response object contains a key/value pair for each public property or method in the Exchange object type.</span></span> <span data-ttu-id="acaf5-121">响应对象包含基础的 Exchange 对象类型; 的名称可以使用此名称以确定，以便您可以提取的相应属性由 response 对象的 Exchange 对象类型。</span><span class="sxs-lookup"><span data-stu-id="acaf5-121">The response object contains the name of the underlying Exchange object type; you can use this name to determine the Exchange object type that is represented by the response object so that you can extract the appropriate property.</span></span> <span data-ttu-id="acaf5-122">属性包中的每个值还包括类型信息，以便您可以强制转换为相应的托管类型的属性值。</span><span class="sxs-lookup"><span data-stu-id="acaf5-122">Each value in the property bag also includes type information so that you can cast the property value to the appropriate managed type.</span></span>
  
## <a name="use-the-cmdlet-response"></a><span data-ttu-id="acaf5-123">使用 cmdlet 响应</span><span class="sxs-lookup"><span data-stu-id="acaf5-123">Use the cmdlet response</span></span>
<span data-ttu-id="acaf5-124"><a name="usingPSObject_bk"> </a></span><span class="sxs-lookup"><span data-stu-id="acaf5-124"></span></span>

<span data-ttu-id="acaf5-125">[PSObject](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject%28VS.85%29.aspx)类公开以下三个公共属性，包含基础的 Exchange 2013 API 对象的值：[属性](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject.properties%28VS.85%29.aspx)、[方法](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject.methods%28VS.85%29.aspx)和[成员](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject.members%28VS.85%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="acaf5-125">The [PSObject](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject%28VS.85%29.aspx) class exposes the following three public properties that contain the values of the underlying Exchange 2013 API object: [Properties](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject.properties%28VS.85%29.aspx), [Methods](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject.methods%28VS.85%29.aspx), and [Members](http://msdn.microsoft.com/zh-cn/library/system.management.automation.psobject.members%28VS.85%29.aspx).</span></span> <span data-ttu-id="acaf5-126">由 Exchange 2013 API 对象公开的每个属性的**属性**和**成员**属性中具有相应的键/值对。</span><span class="sxs-lookup"><span data-stu-id="acaf5-126">Each property that is exposed by the Exchange 2013 API object has a corresponding key/value pair in the **Properties** and **Members** properties.</span></span> <span data-ttu-id="acaf5-127">您的应用程序可以按名称检索属性的值的属性的索引的**Properties**集合。</span><span class="sxs-lookup"><span data-stu-id="acaf5-127">Your application can index the **Properties** collection by the name of a property to retrieve the value of the property.</span></span> 
  
<span data-ttu-id="acaf5-128">**PSObject**实例的**TypeNames**属性可用于确定封装**PSObject**实例的基础 Exchange 对象的类型。</span><span class="sxs-lookup"><span data-stu-id="acaf5-128">You can use the **TypeNames** property of the **PSObject** instance to determine the type of the underlying Exchange object that is encapsulated by the **PSObject** instance.</span></span> <span data-ttu-id="acaf5-129">**TypeNames**属性是类型的字符串，其中包含表示的对象层次结构集合。</span><span class="sxs-lookup"><span data-stu-id="acaf5-129">The **TypeNames** property is a collection of strings that contains the object hierarchy of the represented type.</span></span> <span data-ttu-id="acaf5-130">可以使用这些名称以确定由**PSObject**实例，以便您可以提取的相应属性的对象。</span><span class="sxs-lookup"><span data-stu-id="acaf5-130">You can use these names to determine the object that is represented by the **PSObject** instance so that you can extract the appropriate property.</span></span> 
  
<span data-ttu-id="acaf5-131">下面的代码示例使用 cmdlet 响应控制台上打印**PSObject**实例的**Properties**集合的内容。</span><span class="sxs-lookup"><span data-stu-id="acaf5-131">The following code example uses the cmdlet response to print the contents of the **Properties** collection of a **PSObject** instance on the console.</span></span> <span data-ttu-id="acaf5-132">该代码示例要求对**System.Automation.Management**命名空间的引用。</span><span class="sxs-lookup"><span data-stu-id="acaf5-132">The code example requires a reference to the **System.Automation.Management** namespace.</span></span> 
  
```cs
foreach (PSPropertyInfo propertyInfo in psObject.Properties)
{
    Console.WriteLine(string.Format("{0}: {1}",
        propertyInfo.Name, propertyInfo.Value);
}
```

<br/>

```vb
For Each PropertyInfo As PSProperty In ObjectInfo.Properties
    Console.WriteLine(String.Format("{0}: {1}", PropertyInfo.Name, PropertyInfo.Value))
Next

```

## <a name="see-also"></a><span data-ttu-id="acaf5-133">另请参阅</span><span class="sxs-lookup"><span data-stu-id="acaf5-133">See also</span></span>

- [<span data-ttu-id="acaf5-134">创建 Exchange 命令行管理程序工具</span><span class="sxs-lookup"><span data-stu-id="acaf5-134">Create Exchange Management Shell tools</span></span>](create-exchange-management-shell-tools.md)   
- [<span data-ttu-id="acaf5-135">使用 Exchange 命令行管理程序中获取邮件用户的列表</span><span class="sxs-lookup"><span data-stu-id="acaf5-135">Get a list of mail users by using the Exchange Management Shell</span></span>](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

