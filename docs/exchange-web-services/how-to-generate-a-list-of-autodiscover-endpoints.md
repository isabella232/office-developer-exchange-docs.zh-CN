---
title: 生成自动发现终结点列表
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 82394d3c-9fc7-4b3c-b48d-1fe983c198f7
description: 了解如何生成自动发现终结点的按优先级排序的列表。
localization_priority: Priority
ms.openlocfilehash: db888c8d562f57bd46edc251f4917e9e03d85d95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528096"
---
# <a name="generate-a-list-of-autodiscover-endpoints"></a>生成自动发现终结点列表

了解如何生成自动发现终结点的按优先级排序的列表。
  
[自动发现过程](autodiscover-for-exchange.md)中的第一个任务是为您的应用程序生成要尝试的自动发现终结点的列表。 这些自动发现终结点可以来自[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)，也可以从用户的电子邮件地址派生。 最后，您可以最终使用大量终结点。 我们来看看如何按优先级对其进行组织。 
  
## <a name="start-with-scp-lookup"></a>从 SCP 查找开始
<a name="bk_StartWithScp"> </a>

来自[SCP 查找](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)的自动发现终结点应具有列表中的最高优先级。 管理员可以将 SCP 对象配置为将客户端路由到最接近或最高效的自动发现终结点，因此最好从这些终结点开始。 由于 SCP 查找过程具有其自己的优先顺序方案，因此 SCP 查找的结果已进行了优先级划分，如下所示： 
  
1. 从作用域到客户端计算机所属的 Active Directory 站点的 SCP 对象的自动发现终结点。
    
2. 来自不限于任何 Active Directory 站点的 SCP 对象的自动发现终结点。
    
3. 来自 SCP 对象的自动发现终结点位于与客户端计算机所属的站点不同的 Active Directory 站点范围内。
    
获得 SCP 查找过程的结果后，可以添加从用户的电子邮件地址派生的终结点。 这些项可用作一组默认的终结点和回退，以防没有 SCP 结果或从 SCP 查找返回的终结点不足。
  
## <a name="add-endpoints-derived-from-the-users-email-address"></a>添加从用户的电子邮件地址派生的终结点
<a name="bk_AddDerivedEndpoints"> </a>

当 SCP 查找不起作用，或者 SCP 查找返回的终结点不返回成功响应时，可以从用户的电子邮件地址派生一组默认的自动发现终结点。 这些终结点的优先级应低于来自 SCP 查找的优先级，但如果 SCP 查找不成功，则可能需要这些终结点。
  
### <a name="to-derive-autodiscover-endpoints"></a>派生自动发现终结点

1. 从用户的电子邮件地址中提取域名。 例如，如果用户的电子邮件地址为 Sadie.Daniels@contoso.com，则域名将为 contoso.com。
    
2. 构造不带文件扩展名的终结点 Url，格式如下：
    
  - "https://" + domain + "/autodiscover/autodiscover"
    
  - "https://autodiscover." + domain + "/autodiscover/autodiscover"
    
编译从 SCP 查找和用户的电子邮件地址派生的终结点的列表后，可能需要在这些 Url 中修改文件扩展名，具体取决于您使用的是[SOAP 自动发现 web 服务](https://msdn.microsoft.com/library/61c21ea9-7fea-4f56-8ada-bf80e1e6b074%28Office.15%29.aspx)还是[POX 自动发现 web 服务](https://msdn.microsoft.com/library/877152f0-f4b1-4f63-b2ce-924f4bdf2d20%28Office.15%29.aspx)。
  
## <a name="add-or-replace-file-name-extensions-in-endpoint-urls"></a>在终结点 Url 中添加或替换文件扩展名
<a name="bk_FileExtensions"> </a>

您可以使用 SOAP 自动发现 web 服务或 POX 自动发现 web 服务来访问自动发现服务。 每个服务使用类似的终结点 Url，唯一的区别是文件扩展名。 SOAP 自动发现 web 服务使用 ".svc" 文件扩展名，POX 自动发现 web 服务使用 ".xml" 文件扩展名。
  
默认情况下，从 SCP 查找返回的自动发现终结点 Url 是 POX Url。 但是，如果您使用的是 SOAP 自动发现，则只需将文件扩展名从 ".xml" 更改为 ".svc"，然后尝试 SOAP 请求即可。
  
对于派生的自动发现终结点 Url，将省略文件扩展名。 在尝试 URL 之前，为要使用的自动发现 web 服务添加适当的文件扩展名。
  
## <a name="example-generating-a-list-of-autodiscover-endpoints"></a>示例：生成自动发现终结点列表
<a name="bk_Example"> </a>

我们来看一个示例。 Sadie Daniels （Sadie.Daniels@contoso.com）是首次使用 Exchange Web 服务（EWS）应用程序。 应用程序使用自动发现来配置自身。 Sadie 的计算机已加入 contoso.com 域，位于 Redmond Active Directory 站点中。 应用程序将生成图1中所示的自动发现终结点的列表。
  
**图1：自动发现终结点的示例列表**

![自动发现终结点的示例列表，显示从 SCP 查找获得的终结点，具有比派生终结点更高的优先级。](media/Ex15_Autodiscover_GenerateList_Example.png)
  
此示例中的 EWS 应用程序优先于 SOAP 自动发现 web 服务，因此在向其发送 SOAP 请求之前，它会将 SCP 结果的文件扩展名更改为 ".svc"。
  
## <a name="next-steps"></a>后续步骤
<a name="bk_NextSteps"> </a>

生成自动发现终结点的列表后，通过[向这些终结点发送请求来](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)尝试这些终结点。
  
## <a name="see-also"></a>另请参阅


- [Exchange 自动发现](autodiscover-for-exchange.md)
    
- [通过使用 Exchange 中的 SCP 查找来找到自动发现终结点](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [处理自动发现错误消息](handling-autodiscover-error-messages.md)
    

