---
title: CreateManagedFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateManagedFolder
api_type:
- schema
ms.assetid: cfdf01a9-0191-47c7-a7ad-5254d8bdee4a
description: CreateManagedFolder元素定义添加到邮箱托管自定义文件夹的请求。
ms.openlocfilehash: 4acc931de2a8665db092c3b309d914f0a3c67558
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19753676"
---
# <a name="createmanagedfolder"></a>CreateManagedFolder

本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 **CreateManagedFolder**元素定义添加到邮箱托管自定义文件夹的请求。 
  
```xml
<CreateManagedFolder>
   <FolderNames/>
   <Mailbox/>
</CreateManagedFolder>
```

 **CreateManagedFolderRequestType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

无。
  
### <a name="child-elements"></a>子元素

|**元素**|**说明**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |包含一数组的已命名托管文件夹添加到邮箱。  <br/> |
|[Mailbox](mailbox.md) <br/> |标识已启用邮件的Active Directory目录服务对象。  <br/> |
   
### <a name="parent-elements"></a>父元素

无。
  
## <a name="remarks"></a>备注

发出请求的用户帐户必须具有在其中创建托管的文件夹邮箱 FullAccess 权限。您可以使用与 Exchange 管理外壳 **Add-MailboxPermission** cmdlet  _ -AccessRights _参数分配 FullAccess 权限。 
  
尽管可以使用 Exchange Web 服务添加到邮箱的托管的文件夹，不能使用 Exchange Web 服务来访问可用的托管文件夹的列表。要获取可用的托管文件夹的列表，请使用 **get-managedfolder** Exchange 管理外壳 cmdlet。 **get-managedfolder cmdlet** 返回的列表将包含托管自定义文件夹和托管的默认文件夹。通过使用 CreateManagedFolder 操作可以只将类型为 **managedcustomfolder**的文件夹添加到邮箱。 
  
> [!NOTE]
> [!注释] 此外可以使用 DirectoryServices Microsoft.NET Framework 的 API 的托管文件夹的列表。 
  
您可以使用[FindFolder Operation](findfolder-operation.md)查找邮箱中的托管的文件夹。可以通过将[BaseShape](baseshape.md)元素设置为AllProperties ，在请求中区分托管的文件夹。响应将包含要区分从 Exchange 存储文件夹的托管的文件夹的 [ManagedFolderInformation](managedfolderinformation.md)元素。以同样的方式删除其他文件夹类型，您可以删除托管的文件夹。 
  
描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|架构名称  <br/> |消息架构  <br/> |
|验证文件  <br/> |Messages.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅



[CreateManagedFolder 操作](createmanagedfolder-operation.md)
  
[FindFolder Operation](findfolder-operation.md)


[Finding Folders](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adding Managed Folders](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

