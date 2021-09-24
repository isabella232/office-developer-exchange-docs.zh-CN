---
title: 使用 Exchange 命令行管理程序 cmdlet 响应
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: 了解如何在托管应用程序中使用来自 Exchange 命令行管理程序 cmdlet Exchange响应。
ms.openlocfilehash: be66be31e435be1553eba16d8f367a79317618f2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520961"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>使用 Exchange 命令行管理程序 cmdlet 响应

了解如何在托管应用程序中使用来自 Exchange 命令行管理程序 cmdlet Exchange响应。
  
**适用于：Exchange Online |** Exchange Server 2013 |Office 365
  
每个Exchange命令行管理程序 cmdlet 返回一个或多个[PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx)实例，这些实例提供命令行管理程序环境中任何对象的Exchange视图。 本文提供有关如何使用 **PSObject** 实例的属性返回基础 Exchange Server 2013 API 对象的属性的信息。 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>使用 cmdlet 响应的先决条件
<a name="prerequisites_bk"> </a>

若要使用 cmdlet 响应，您需要对 **System.Automation.Management** 命名空间的引用。 
  
> [!NOTE]
>  当您使用 Visual Studio创建应用程序时，您必须向项目添加对System.Mangagement.Automation.dll程序集的引用。 您可以在以下位置之一找到程序集： 
> - 对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell安装目录 ($PSHOME) 。 
> - 对于 Windows 7 和 Windows 8 操作系统，以下文件夹：Windows\assembly\GAC_MSIL\System.Management.Automation。 
  
## <a name="windows-powershell-remote-runspace"></a>Windows PowerShell远程运行空间
<a name="usingremoterunspace_bk"> </a>

命令行Exchange命令行管理程序Windows PowerShell所有命令（甚至是在本地服务器上运行的命令）使用远程命令行管理程序功能。 因此，来自命令行管理程序 cmdlet Exchange响应都为序列化 XML。 这意味着，虽然响应对象指示Exchange 对象类型响应的子对象，但无法将响应对象强制转换到Exchange 对象类型;相反，必须使用响应对象公开的属性包从响应对象Exchange 对象类型。
  
响应对象中的属性包包含每个公共属性或方法的键/值对Exchange 对象类型。 response 对象包含基础对象Exchange 对象类型;可以使用此名称来确定Exchange 对象类型对象所代表的属性，以便提取相应的属性。 属性包中的每个值还包括类型信息，以便可以将属性值强制转换到适当的托管类型。
  
## <a name="use-the-cmdlet-response"></a>使用 cmdlet 响应
<a name="usingPSObject_bk"> </a>

[PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx)类公开以下三个公共属性，其中包含基础 Exchange 2013 API 对象的值[：Properties、Methods](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx)和[](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx) [Members](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx)。 由 2013 API Exchange公开的每个属性在 **Properties** 和 Members 属性中都有一个对应的键/**值** 对。 应用程序可以按属性的名称对 **Properties** 集合编制索引，以检索该属性的值。 
  
可以使用 **PSObject** 实例的 **TypeNames** 属性来确定 **PSObject** 实例封装的基础 Exchange 对象的类型。 **TypeNames** 属性是字符串的集合，其中包含表示的类型的对象层次结构。 可以使用这些名称来确定 **PSObject** 实例表示的对象，以便提取相应的属性。 
  
以下代码示例使用 cmdlet 响应在控制台上打印 **PSObject** 实例的 **Properties** 集合的内容。 该代码示例需要一个对 **System.Automation.Management 命名空间** 的引用。 
  
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

## <a name="see-also"></a>另请参阅

- [创建 Exchange 命令行管理程序工具](create-exchange-management-shell-tools.md)   
- [使用命令行管理程序获取邮件Exchange列表](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

