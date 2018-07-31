---
title: 使用 Exchange 命令行管理程序中获取邮件用户的列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b790dc8-5c4f-4acf-bbe7-63523395fbe7
description: 了解如何使用 Exchange 命令行管理程序 cmdlet 创建一个工具，返回的 Exchange 邮箱用户列表。
ms.openlocfilehash: e9493571e98760e5a11674db9a552111c1ec29b2
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353999"
---
# <a name="get-a-list-of-mail-users-by-using-the-exchange-management-shell"></a>使用 Exchange 命令行管理程序中获取邮件用户的列表

了解如何使用 Exchange 命令行管理程序 cmdlet 创建一个工具，返回的 Exchange 邮箱用户列表。
  
**适用于：** Exchange Online |Exchange Server 2013 |Office 365 
  
从 Exchange Online 中获取用户的列表，Exchange Online 作为 Office 365 的一部分或的开头使用调用 Exchange 命令行管理程序 cmdlet 的管理的工具的 Exchange 2013 的 Exchange 版本是一个两步过程。 首先，建立在 Exchange server; 上的远程运行空间然后，运行此 cmdlet 检索远程运行空间中的用户信息。 

若要连接到远程运行空间，您必须使用满足组织的安全要求的身份验证方案与 Exchange server 身份验证。 

本文提供了可用于设置远程运行空间和运行 Exchange 命令行管理程序 cmdlet 可从 Exchange 服务器获取用户的列表的代码示例。

<a name="bk_prerequisites"> </a>

## <a name="prerequisites-for-getting-a-list-of-mailbox-users"></a>获取列表的邮箱用户的先决条件

若要执行此任务，您需要对以下命名空间的引用：
  
- **System.Collections.ObjectModel**
- **System.Management.Automation**
- **System.Management.Automation.Remoting**
- **System.Management.Automation.Runspaces**
    
> [!NOTE]
>  当您使用 Visual Studio 创建应用程序时，您必须将 System.Management.Automation.dll 程序集的引用添加到项目中。 可以在以下位置之一找到程序集：
> - 对于 Windows XP 和 Windows Vista 操作系统，Windows PowerShell 安装目录 ($PSHOME)。
> - 对于 Windows 7 和 Windows 8 操作系统，以下文件夹： Windows\assembly\GAC_MSIL\System.Management.Automation。 
  
不会加载 Exchange 2013 管理管理单元中运行的应用程序自动执行 Exchange 命令行管理程序 cmdlet 的计算机上运行空间到。 下文中所述，应用程序而是应创建远程运行空间。

<a name="bk_gettinglistmailbox"> </a>

## <a name="connect-to-a-remote-runspace-on-an-exchange-server"></a>连接到 Exchange 服务器上远程运行空间

用于连接到远程运行空间用于 Exchange Management Shell cmdlet 会有所不同，该方法根据您使用的身份验证方案。 本节提供代码示例演示如何使用下表中列出的身份验证方法时，连接到远程运行空间。
  
|**身份验证方法**|**适用于**|**URI**|
|:-----|:-----|:-----|
|[使用基本身份验证连接到 Exchange Online 上远程运行空间](#bk_basic) <br/> |Exchange Online 服务器  <br/> |`https://outlook.office365.com/PowerShell-LiveID`<br/><br/>`https://<server>/PowerShell-LiveID`  <br/> |
|[使用证书身份验证连接到远程运行空间](#bk_cert) <br/> |Exchange Online 和 Exchange 内部部署服务器  <br/> |`https://outlook.office365.com/PowerShell`<br/><br/>`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |
|[使用 Kerberos 身份验证连接到 Exchange 服务器上远程运行空间](#bk_Kerberos) <br/> |Exchange Online 和 Exchange 内部部署服务器  <br/> |`https://<server>/PowerShell`<br/><br/>`http://<server>/PowerShell`  <br/> |

<a name="bk_basic"> </a>

### <a name="connect-to-a-remote-runspace-on-exchange-online-by-using-basic-authentication"></a>使用基本身份验证连接到 Exchange Online 上远程运行空间

下面的代码示例定义**GetUsersUsingBasicAuth**方法，该 Exchange Online 的远程服务器上的 Exchange 命令行管理程序运行空间创建使用基本身份验证方法。 该方法然后调用**GetUserInformation**方法中，在[获取从远程运行空间的邮箱用户的列表](#bk_remote)，请部分定义返回远程服务器上的用户列表。
  
此方法需要以下参数：
  
-  **liveIDConnectionUri**&ndash;一个字符串，包含 Exchange Online 将验证应用程序的服务器的 URI。 Exchange Online 运行 Office 365 中，如果 URI 是`https://outlook.office365.com/PowerShell-LiveID`;否则，URI 是`https://<servername>/PowerShell-LiveID`。 
    
-  **schemaUri**&ndash;一个字符串，包含定义的 Exchange 命令行管理程序架构的架构文档的 URI。 Uri 的架构`http://schemas.microsoft.com/powershell/Microsoft.Exchange`。 
    
-  **凭据**&ndash; [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含正在运行应用程序的用户的凭据。 
    
-  **计数**&ndash;的 Exchange 邮箱用户返回数量。 
    
```cs
public Collection<PSObject> GetUsersUsingBasicAuth(
    string liveIDConnectionUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(liveIDConnectionUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingBasicAuth( _
    ByVal LiveIDConnectionUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(LiveIDConnectionUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Basic
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<a name="bk_cert"> </a>

### <a name="connect-to-a-remote-runspace-by-using-certificate-authentication"></a>使用证书身份验证连接到远程运行空间

下面的代码示例定义**GetUsersUsingCertificate**方法，通过使用证书创建远程服务器的 Exchange 命令行管理程序运行空间。 该方法然后调用**GetUserInformation**方法中，在[获取从远程运行空间的邮箱用户的列表](#bk_remote)，请部分定义返回远程服务器上的用户列表。
  
此方法需要以下参数：
  
-  **指纹**&ndash;一个字符串，包含用于验证应用程序证书的指纹。 
    
-  **certConnectionUri**&ndash;一个字符串，包含将身份验证证书的服务器的 URI。 URI 将其中一种下表中列出。 
    
    **表 1。certConnectionUri Uri**

    |**Server**|**URI**|
    |:-----|:-----|
    |无需使用 SSL 的 Exchange 服务器  <br/> |`http://<servername>/PowerShell`  <br/> |
    |使用 SSL 的 Exchange 服务器  <br/> |`https://<servername>/PowerShell`  <br/> |
    |Exchange Online 作为 Office 365 的一部分  <br/> |`https://outlook.office365.com/PowerShell`  <br/> |
   
- **schemaUri**&ndash;一个字符串，包含定义的 Exchange 命令行管理程序架构的架构文档的 URI。 Uri 的架构http://schemas.microsoft.com/powershell/Microsoft.Exchange。 
    
- **计数**&ndash;的 Exchange 邮箱用户返回数量。 
    
```cs
public Collection<PSObject> GetUsersUsingCertificate(
    string thumbprint, string certConnectionUri, string schemaUri, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(certConnectionUri),
        schemaUri,
        thumbprint)
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```


```vb
  Function GetUsersUsingCertificate( _
    ByVal Thumbprint As String, ByVal CertConnectionUri As String, _
    ByVal SchemaUri As String, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo
    ConnectionInfo = New WSManConnectionInfo(New Uri(CertConnectionUri), SchemaUri, Thumbprint)
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<a name="bk_Kerberos"> </a>

### <a name="connect-to-a-remote-runspace-on-an-exchange-server-by-using-kerberos-authentication"></a>使用 Kerberos 身份验证连接到 Exchange 服务器上远程运行空间

下面的代码示例定义**GetUsersUsingKerberos**方法，该远程服务器上的 Exchange 命令行管理程序运行空间创建使用 Kerberos 身份验证方法。 该方法然后调用**GetUserInformation**方法中，在[获取从远程运行空间的邮箱用户的列表](#bk_remote)，请部分定义返回远程服务器上的用户列表。
  
此方法需要以下参数：
  
- **kerberosUri**&ndash;一个字符串，包含将验证应用程序的 Kerberos 服务器的 URI。 URI 将其中一种下表中列出。 
    
    **表 2。kerberosUri Uri**

    |**Server**|**URI**|
    |:-----|:-----|
    |无需使用 SSL 的 Exchange 服务器  <br/> |`http://<servername>/PowerShell`  <br/> |
    |使用 SSL 的 Exchange 服务器  <br/> |`https://<servername>/PowerShell`  <br/> |
   
- **schemaUri**&ndash;一个字符串，包含定义的 Exchange 命令行管理程序架构的架构文档的 URI。 Uri 的架构http://schemas.microsoft.com/powershell/Microsoft.Exchange。 
    
- **凭据**&ndash; [PSCredential](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx)对象，其中包含正在运行应用程序的用户的凭据。 
    
- **计数**&ndash;的 Exchange 邮箱用户返回数量。 
    
```cs
public Collection<PSObject> GetUsersUsingKerberos(
    string kerberosUri, string schemaUri, PSCredential credentials, int count)
{
    WSManConnectionInfo connectionInfo = new WSManConnectionInfo(
        new Uri(kerberosUri),
        schemaUri, credentials);
    connectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos;
    using (Runspace runspace = RunspaceFactory.CreateRunspace(connectionInfo))
    {
        return GetUserInformation(count, runspace);
    }
}
```

```vb
  Function GetUsersUsingKerberos( _
    ByVal KerberosUri As String, ByVal ScehmaUri As String, _
    ByVal Credentials As PSCredential, ByVal Count As Integer) As Collection(Of PSObject)
    Dim ConnectionInfo As WSManConnectionInfo = _
        New WSManConnectionInfo(New Uri(KerberosUri), ScehmaUri, Credentials)
    ConnectionInfo.AuthenticationMechanism = AuthenticationMechanism.Kerberos
    Dim RemoteRunspace As Runspace
    RemoteRunspace = RunspaceFactory.CreateRunspace(ConnectionInfo)
    Return GetUserInformation(Count, RemoteRunspace)
  End Function

```

<a name="bk_remote"> </a>

## <a name="get-a-list-of-mailbox-users-from-a-remote-runspace"></a>从远程运行空间获取邮箱用户的列表

下面的代码示例定义**GetUserInformation**方法，它返回[PSObject](http://msdn.microsoft.com/en-us/library/system.management.automation.pscredential%28VS.85%29.aspx)实例表示 Exchange 邮箱用户的集合。 调用此方法由**GetUsersUsingBasicAuth**、 **GetUsersUsingCertificate**和**GetUsersUsingKerberos**方法可从远程服务器返回的用户的列表。 
  
此方法需要以下参数：
  
- **计数**&ndash;的 Exchange 邮箱用户返回数量。 
    
- **运行空间**&ndash;的远程 Exchange 服务器建立远程运行空间。 
    
```cs
public Collection<PSObject> GetUserInformation(int count, Runspace runspace)
{
    using (PowerShell powershell = PowerShell.Create())
    {
        powershell.AddCommand("Get-Users");
        powershell.AddParameter("ResultSize", count);
        runspace.Open();
        powershell.Runspace = runspace;
        return powershell.Invoke();
    }
}
```

```vb
Function GetUserInformation(ByVal Count As Integer, ByVal RemoteRunspace As Runspace) As Collection(Of PSObject)
    Dim RemotePowerShell As PowerShell = PowerShell.Create
    RemotePowerShell.AddCommand("Get-Users")
    RemotePowerShell.AddParameter("ResultSize", Count)
    ' Open the remote runspace on the server.
    RemoteRunspace.Open()
    ' Associate the runspace with the Exchange Management Shell.
    RemotePowerShell.Runspace = RemoteRunspace
    ' Invoke the Exchange Management Shell to run the command.
    Return RemotePowerShell.Invoke
End Function

```

**GetUserInformation**方法将返回邮箱用户不能超过_计数_。 若要简化此示例的代码，该方法不筛选或否则限制返回的邮箱用户。 
  
## <a name="see-also"></a>另请参阅

- [创建 Exchange 命令行管理程序工具](create-exchange-management-shell-tools.md)   
- [使用 Exchange 命令行管理程序 cmdlet 响应](how-to-use-the-exchange-management-shell-cmdlet-response.md)
    

