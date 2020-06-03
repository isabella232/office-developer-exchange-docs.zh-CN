---
title: 在 Exchange 中 EWS 存档
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: 了解 Exchange 中 EWS 的存档。
ms.openlocfilehash: b433b9f88905ee255720e8b341d560fa0e464975
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456211"
---
# <a name="archiving-in-ews-in-exchange"></a><span data-ttu-id="5335d-103">在 Exchange 中 EWS 存档</span><span class="sxs-lookup"><span data-stu-id="5335d-103">Archiving in EWS in Exchange</span></span>

<span data-ttu-id="5335d-104">了解 Exchange 中 EWS 的存档。</span><span class="sxs-lookup"><span data-stu-id="5335d-104">Learn about archiving in EWS in Exchange.</span></span>
  
<span data-ttu-id="5335d-105">存档邮箱是与用户相关联的辅助邮箱。</span><span class="sxs-lookup"><span data-stu-id="5335d-105">Archive mailboxes are secondary mailboxes that are associated with a user.</span></span> <span data-ttu-id="5335d-106">存档邮箱通常用于管理电子邮件存储限制。</span><span class="sxs-lookup"><span data-stu-id="5335d-106">Archive mailboxes are typically used to manage email storage limits.</span></span> <span data-ttu-id="5335d-107">例如，较旧的电子邮件项目可能会定期从收件箱移动到存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="5335d-107">For example, older email items might periodically be moved from the Inbox to the archive mailbox.</span></span> 
  
<span data-ttu-id="5335d-108">Exchange Online，Exchange Online 作为 Office 365 的一部分，Exchange Server 2013 介绍了两种新的 Exchange Web 服务（EWS）操作，可用于存档主邮箱中的一组邮件项目。</span><span class="sxs-lookup"><span data-stu-id="5335d-108">Exchange Online, Exchange Online as part of Office 365, and Exchange Server 2013 introduce two new Exchange Web Services (EWS) operations that you can use to archive a set of mail items from a primary mailbox.</span></span> <span data-ttu-id="5335d-109">以这种方式存档收件箱项目可保留项目的文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="5335d-109">Archiving Inbox items in this way preserves the folder hierarchy of the items.</span></span> <span data-ttu-id="5335d-110">此外，存档邮箱现在可以本地存储在客户端上，也可以远程存储为用户对用户不透明的方式，方法是使用文件夹路径指向存档的内容。</span><span class="sxs-lookup"><span data-stu-id="5335d-110">In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.</span></span>
  
## <a name="archiving-operations-in-ews"></a><span data-ttu-id="5335d-111">在 EWS 中存档操作</span><span class="sxs-lookup"><span data-stu-id="5335d-111">Archiving operations in EWS</span></span>

<span data-ttu-id="5335d-112">下表列出了在 Exchange 2013 中引入的存档操作。</span><span class="sxs-lookup"><span data-stu-id="5335d-112">The following table lists the archiving operations that were introduced in Exchange 2013.</span></span> 
  
|<span data-ttu-id="5335d-113">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="5335d-113">**Operation name**</span></span>|<span data-ttu-id="5335d-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="5335d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5335d-115">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="5335d-115">ArchiveItem</span></span>](https://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |<span data-ttu-id="5335d-116">将项目从主邮箱移动到存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="5335d-116">Moves an item from the primary mailbox to the archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="5335d-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="5335d-117">CreateFolderPath</span></span>](https://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |<span data-ttu-id="5335d-118">创建指向存档邮箱的存储位置的 URI。</span><span class="sxs-lookup"><span data-stu-id="5335d-118">Creates a URI that points to the storage location for the archive mailbox.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5335d-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="5335d-119">See also</span></span>

- [<span data-ttu-id="5335d-120">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="5335d-120">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="5335d-121">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="5335d-121">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="5335d-122">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="5335d-122">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

