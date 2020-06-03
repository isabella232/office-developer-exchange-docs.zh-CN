---
title: 使用 Exchange 命令行管理程序 cmdlet 响应
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dac8e526-11c6-4c2e-b9a2-f016b1fc738a
description: 了解如何在 Exchange 托管应用程序中使用来自 Exchange 命令行管理程序 cmdlet 的响应。
ms.openlocfilehash: c1b81356ab5dc288ab08287d47581871c36beb05
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44435700"
---
# <a name="use-the-exchange-management-shell-cmdlet-response"></a>使用 Exchange 命令行管理程序 cmdlet 响应

了解如何在 Exchange 托管应用程序中使用来自 Exchange 命令行管理程序 cmdlet 的响应。
  
**适用于：** Exchange Online |Exchange Server 2013 |Office 365
  
每个 Exchange 命令行管理程序 cmdlet 返回一个或多个[PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx)实例，这些实例提供了对 Exchange 命令行管理程序环境中的任何对象的一致视图。 本文提供有关如何使用**PSObject**实例的属性返回基础 Exchange SERVER 2013 API 对象的属性值的信息。 
  
## <a name="prerequisites-for-using-cmdlet-responses"></a>使用 cmdlet 响应的先决条件
<a name="prerequisites_bk"> </a>

若要使用 cmdlet 响应，您需要一个对**System. Automation. Management** namespace 的引用。 
  
> [!NOTE]
>  使用 Visual Studio 创建应用程序时，必须将对 Mangagement 程序集的引用添加到项目中。 您可以在以下位置之一找到程序集： 
> - 对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell 安装目录（$PSHOME）。 
> - 对于 Windows 7 和 Windows 8 操作系统，以下文件夹： Windows\assembly\ GAC_MSIL \System.Management.Automation。 
  
## <a name="windows-powershell-remote-runspace"></a>Windows PowerShell 远程运行空间
<a name="usingremoterunspace_bk"> </a>

Exchange 命令行管理程序对所有命令（甚至在本地服务器上运行的命令）使用远程 Windows PowerShell 功能。 因此，来自 Exchange 命令行管理程序 cmdlet 的所有响应都是序列化的 XML。 这意味着，尽管 response 对象指示用于生成响应的 Exchange 对象类型，但 response 对象无法转换为 Exchange 对象类型;相反，您必须使用由 response 对象公开的属性包来获取 Exchange 对象类型的值。
  
Response 对象中的属性包包含 Exchange 对象类型中的每个公共属性或方法的键/值对。 Response 对象包含基础 Exchange 对象类型的名称;您可以使用此名称来确定由 response 对象表示的 Exchange 对象类型，以便您可以提取相应的属性。 属性包中的每个值还包括类型信息，以便您可以将属性值转换为适当的托管类型。
  
## <a name="use-the-cmdlet-response"></a>使用 cmdlet 响应
<a name="usingPSObject_bk"> </a>

[PSObject](https://msdn.microsoft.com/library/system.management.automation.psobject%28VS.85%29.aspx)类公开以下三个公共属性，其中包含基础 EXCHANGE 2013 API 对象的值：[属性](https://msdn.microsoft.com/library/system.management.automation.psobject.properties%28VS.85%29.aspx)、[方法](https://msdn.microsoft.com/library/system.management.automation.psobject.methods%28VS.85%29.aspx)和[成员](https://msdn.microsoft.com/library/system.management.automation.psobject.members%28VS.85%29.aspx)。 Exchange 2013 API 对象公开的每个属性在 "**属性**" 和 "**成员**" 属性中都有对应的键/值对。 您的应用程序可以**按属性名称为属性集合编制**索引，以检索属性的值。 
  
可以使用**psobject**实例的**TypeNames**属性来确定由**PSObject**实例封装的基础 Exchange 对象的类型。 **TypeNames**属性是包含所表示类型的对象层次结构的字符串的集合。 您可以使用这些名称来确定由**PSObject**实例表示的对象，以便您可以提取相应的属性。 
  
下面的代码示例使用 cmdlet 响应在控制台上打印**PSObject**实例的**Properties**集合的内容。 此代码示例需要一个对**system.web**命名空间的引用。 
  
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
- [使用 Exchange 命令行管理程序获取邮件用户列表](how-to-get-a-list-of-mail-users-by-using-the-exchange-management-shell.md)
    

