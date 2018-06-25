---
title: 在 Exchange 存档中的 ews
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 78ae179b-ae4f-4f64-911a-e0c70e0fa314
description: 了解有关在 Exchange 存档中的 ews。
ms.openlocfilehash: bc282a7774bb74e57550bc663512987839324b83
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752697"
---
# <a name="archiving-in-ews-in-exchange"></a><span data-ttu-id="2f68c-103">在 Exchange 存档中的 ews</span><span class="sxs-lookup"><span data-stu-id="2f68c-103">Archiving in EWS in Exchange</span></span>

<span data-ttu-id="2f68c-104">了解有关在 Exchange 存档中的 ews。</span><span class="sxs-lookup"><span data-stu-id="2f68c-104">Learn about archiving in EWS in Exchange.</span></span>
  
<span data-ttu-id="2f68c-105">存档邮箱的第二与用户关联的邮箱。</span><span class="sxs-lookup"><span data-stu-id="2f68c-105">Archive mailboxes are secondary mailboxes that are associated with a user.</span></span> <span data-ttu-id="2f68c-106">存档邮箱通常用于管理电子邮件存储限制。</span><span class="sxs-lookup"><span data-stu-id="2f68c-106">Archive mailboxes are typically used to manage email storage limits.</span></span> <span data-ttu-id="2f68c-107">例如，旧的电子邮件项可能会定期从移收件箱到存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="2f68c-107">For example, older email items might periodically be moved from the Inbox to the archive mailbox.</span></span> 
  
<span data-ttu-id="2f68c-108">Exchange Online、 Exchange Online 作为 Office 365 和 Exchange Server 2013 的一部分介绍可用于存档的一组从主邮箱的邮件项目的两个新的 Exchange Web Services (EWS) 操作。</span><span class="sxs-lookup"><span data-stu-id="2f68c-108">Exchange Online, Exchange Online as part of Office 365, and Exchange Server 2013 introduce two new Exchange Web Services (EWS) operations that you can use to archive a set of mail items from a primary mailbox.</span></span> <span data-ttu-id="2f68c-109">这种方式的收件箱项目存档保留的项目的文件夹层次结构。</span><span class="sxs-lookup"><span data-stu-id="2f68c-109">Archiving Inbox items in this way preserves the folder hierarchy of the items.</span></span> <span data-ttu-id="2f68c-110">此外，现在可以在客户端，本地或是大多数情况下不透明给用户，通过使用文件夹路径指向存档的内容的方式在远程存储存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="2f68c-110">In addition, archive mailboxes can now be stored either locally on a client, or remotely, in a way that is mostly opaque to a user, by using a folder path to point to the contents of the archive.</span></span>
  
## <a name="archiving-operations-in-ews"></a><span data-ttu-id="2f68c-111">存档中的 ews 操作</span><span class="sxs-lookup"><span data-stu-id="2f68c-111">Archiving operations in EWS</span></span>

<span data-ttu-id="2f68c-112">下表列出了 Exchange 2013 中引入的存档操作。</span><span class="sxs-lookup"><span data-stu-id="2f68c-112">The following table lists the archiving operations that were introduced in Exchange 2013.</span></span> 
  
|<span data-ttu-id="2f68c-113">**操作名称**</span><span class="sxs-lookup"><span data-stu-id="2f68c-113">**Operation name**</span></span>|<span data-ttu-id="2f68c-114">**说明**</span><span class="sxs-lookup"><span data-stu-id="2f68c-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2f68c-115">ArchiveItem</span><span class="sxs-lookup"><span data-stu-id="2f68c-115">ArchiveItem</span></span>](http://msdn.microsoft.com/library/1af216b3-13ea-498e-b4fc-23513755d731%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f68c-116">将项目从主邮箱移动到存档邮箱。</span><span class="sxs-lookup"><span data-stu-id="2f68c-116">Moves an item from the primary mailbox to the archive mailbox.</span></span>  <br/> |
|[<span data-ttu-id="2f68c-117">CreateFolderPath</span><span class="sxs-lookup"><span data-stu-id="2f68c-117">CreateFolderPath</span></span>](http://msdn.microsoft.com/library/5a10aa5e-3f25-4ec3-a0b9-284c30918a1f%28Office.15%29.aspx) <br/> |<span data-ttu-id="2f68c-118">创建指向的存档邮箱的存储位置的 URI。</span><span class="sxs-lookup"><span data-stu-id="2f68c-118">Creates a URI that points to the storage location for the archive mailbox.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f68c-119">另请参阅</span><span class="sxs-lookup"><span data-stu-id="2f68c-119">See also</span></span>

- [<span data-ttu-id="2f68c-120">开发 Exchange Web 服务客户端</span><span class="sxs-lookup"><span data-stu-id="2f68c-120">Develop web service clients for Exchange</span></span>](develop-web-service-clients-for-exchange.md)
    
- [<span data-ttu-id="2f68c-121">Start using web services in Exchange</span><span class="sxs-lookup"><span data-stu-id="2f68c-121">Start using web services in Exchange</span></span>](start-using-web-services-in-exchange.md)
    
- [<span data-ttu-id="2f68c-122">Exchange 的 EWS 客户端设计概述</span><span class="sxs-lookup"><span data-stu-id="2f68c-122">EWS client design overview for Exchange</span></span>](ews-client-design-overview-for-exchange.md)
    

