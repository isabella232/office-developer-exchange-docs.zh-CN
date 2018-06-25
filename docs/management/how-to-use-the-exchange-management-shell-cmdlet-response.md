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
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>使用 Exchange 命令行管理程序 cmdlet 响应

了解如何使用 Exchange 托管应用程序中的 Exchange 命令行管理程序 cmdlet 的响应。
  
**适用于：** Exchange Online |Exchange Server 2013 |Office 365
  
每个 Exchange Management Shell cmdlet 可返回提供一致视图中的 Exchange 命令行管理程序环境的任何对象的一个或多个[PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx)实例。 本文提供有关如何使用**PSObject**实例的属性可返回基础的 Exchange Server 2013 API 对象的属性值的信息。 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>使用 cmdlet 响应的先决条件
<a name="prerequisites_bk"> </a>

若要使用 cmdlet 响应，您需要对**System.Automation.Management**命名空间的引用。 
  
> [!NOTE]
>  当您使用 Visual Studio 创建应用程序时，您必须将 System.Mangagement.Automation.dll 程序集的引用添加到项目中。 您可以在以下位置之一找到该程序集： 
> - 对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell 安装目录 ($PSHOME)。 
> - 对于 Windows 7 和 Windows 8 操作系统，以下文件夹： Windows\assembly\GAC_MSIL\System.Management.Automation。 
  
## <a name="windows-powershell-remote-runspace"></a>Windows PowerShell 远程运行空间
<a name="usingremoterunspace_bk"> </a>

Exchange 命令行管理程序的所有命令，甚至在本地服务器运行的命令使用远程 Windows PowerShell 功能。 因此，从 Exchange 命令行管理程序 cmdlet 的所有响应序列都化的 XML。 这意味着，尽管响应对象指示用于生成响应的 Exchange 对象类型，response 对象无法转换为 Exchange 对象类型;相反，您必须使用公开响应对象以获取从 Exchange 对象类型的值的属性包。
  
响应对象中的属性包中包含的键/值对的每个公共属性或方法中的 Exchange 对象类型。 响应对象包含基础的 Exchange 对象类型; 的名称可以使用此名称以确定，以便您可以提取的相应属性由 response 对象的 Exchange 对象类型。 属性包中的每个值还包括类型信息，以便您可以强制转换为相应的托管类型的属性值。
  
## <a name="use-the-cmdlet-response"></a>使用 cmdlet 响应
<a name="usingPSObject_bk"> </a>

[PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject%28VS.85%29.aspx)类公开以下三个公共属性，包含基础的 Exchange 2013 API 对象的值：[属性](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.properties%28VS.85%29.aspx)、[方法](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.methods%28VS.85%29.aspx)和[成员](http://msdn.microsoft.com/en-us/library/system.management.automation.psobject.members%28VS.85%29.aspx)。 由 Exchange 2013 API 对象公开的每个属性的**属性**和**成员**属性中具有相应的键/值对。 您的应用程序可以按名称检索属性的值的属性的索引的**Properties**集合。 
  
**PSObject**实例的**TypeNames**属性可用于确定封装**PSObject**实例的基础 Exchange 对象的类型。 **TypeNames**属性是类型的字符串，其中包含表示的对象层次结构集合。 可以使用这些名称以确定由**PSObject**实例，以便您可以提取的相应属性的对象。 
  
下面的代码示例使用 cmdlet 响应控制台上打印**PSObject**实例的**Properties**集合的内容。 该代码示例要求对**System.Automation.Management**命名空间的引用。 
  
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
- [使用 Exchange 命令行管理程序中获取邮件用户的列表](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

