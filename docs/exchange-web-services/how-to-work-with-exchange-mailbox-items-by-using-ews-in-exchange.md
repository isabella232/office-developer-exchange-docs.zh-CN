---
title: 通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 721deb84-f85d-45d0-84c1-0ed55f359969
description: 本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除项目。
ms.openlocfilehash: e70ac499da57faa60b4bcb6082648b23d1a7e791
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19752908"
---
# <a name="work-with-exchange-mailbox-items-by-using-ews-in-exchange"></a><span data-ttu-id="7c4bc-103">通过在 Exchange 使用 EWS 来处理 Exchange 邮箱项目</span><span class="sxs-lookup"><span data-stu-id="7c4bc-103">Work with Exchange mailbox items by using EWS in Exchange</span></span>

<span data-ttu-id="7c4bc-104">本文档可能包含与预发布功能或产品相关的内容，这些功能或产品在最终商业发布之前可能会有重大变化。本文档按"原样"提供，仅供参考，Microsoft 不在本文档中作出任何明示或暗示担保。 了解如何通过使用 Exchange 中的 EWS 托管 API 或 EWS 创建、获取、更新和删除项目。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-104">Learn how to create, get, update, and delete items by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="7c4bc-105">您可以使用 EWS 托管 API 或 EWS 处理邮箱中的项目。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-105">You can use the EWS Managed API or EWS to work with items in a mailbox.</span></span> <span data-ttu-id="7c4bc-106">可以使用泛型项  EWS 托管 API [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 对象或 EWS [Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) 类型  来执行一些操作（获取某项或使用项的标识符删除项）；但是，大多数情况下您需要使用 [强类型项](folders-and-items-in-ews-in-exchange.md#bk_item)执行获取或更新操作，因为您将需要访问特定于强类型项的属性。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-106">You can use generic items — EWS Managed API [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) objects or EWS [Item](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) types — to perform some operations (getting an item or deleting an item by using the item's identifier); however, most of the time you'll have to use a [strongly typed item](folders-and-items-in-ews-in-exchange.md#bk_item) to perform a get or update operation because you'll need access to the properties that are specific to the strongly typed item.</span></span> 

<span data-ttu-id="7c4bc-107">例如，您无法使用泛型项检索某个项包含开始日期和结束日期的项 - 您需要一个 EWS 托管 API [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) 对象或 EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) 类型来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-107">For example, you can't use a generic item to retrieve an item that contains a start and end date - you need an EWS Managed API [Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) object or an EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) type to do that.</span></span> <span data-ttu-id="7c4bc-108">如果您正在使用 EWS 托管 API，您总是需要创建强类型项，因为泛型 **Item** 类没有构造函数。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-108">And if you're using the EWS Managed API, you always have to create strongly typed items, because the generic **Item** class does not have a constructor.</span></span> <span data-ttu-id="7c4bc-109">如果您正在处理非强类型项，您始终可以使用基 **Item** 类来处理该项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-109">If you're working with an item that is not strongly typed, you can always use the base **Item** class to work with the item.</span></span> 
  
<span data-ttu-id="7c4bc-110">**表 1. 用于处理项的 EWS 托管 API 方法和 EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="7c4bc-110">**Table 1. EWS Managed API methods and EWS operations for working with items**</span></span>

|<span data-ttu-id="7c4bc-111">**若要...**</span><span class="sxs-lookup"><span data-stu-id="7c4bc-111">**In order to…**</span></span>|<span data-ttu-id="7c4bc-112">**EWS 托管的 API 方法**</span><span class="sxs-lookup"><span data-stu-id="7c4bc-112">**EWS Managed API method**</span></span>|<span data-ttu-id="7c4bc-113">**EWS 操作**</span><span class="sxs-lookup"><span data-stu-id="7c4bc-113">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7c4bc-114">创建泛型项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-114">Create a generic item</span></span>  <br/> |<span data-ttu-id="7c4bc-p103">无。您只能通过使用 EWS 托管 API 创建特定项类型；不能创建泛型项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p103">None. You can only create specific item types by using the EWS Managed API; you cannot create generic items.</span></span>  <br/> |[<span data-ttu-id="7c4bc-117">CreateItem</span><span class="sxs-lookup"><span data-stu-id="7c4bc-117">CreateItem</span></span>](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="7c4bc-118">获取项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-118">Get an item</span></span>  <br/> |[<span data-ttu-id="7c4bc-119">Item.Bind</span><span class="sxs-lookup"><span data-stu-id="7c4bc-119">Item.Bind</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="7c4bc-120">GetItem</span><span class="sxs-lookup"><span data-stu-id="7c4bc-120">GetItem</span></span>](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="7c4bc-121">更新项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-121">Update an item</span></span>  <br/> |[<span data-ttu-id="7c4bc-122">Item.Update</span><span class="sxs-lookup"><span data-stu-id="7c4bc-122">Item.Update</span></span>](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="7c4bc-123">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="7c4bc-123">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="7c4bc-124">删除项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-124">Delete an item</span></span>  <br/> |[<span data-ttu-id="7c4bc-125">Item.Delete</span><span class="sxs-lookup"><span data-stu-id="7c4bc-125">Item.Delete</span></span>](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="7c4bc-126">删除项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-126">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="7c4bc-p104">在本文中，您将了解到何时可以使用泛型基类以及何时需要使用强类型项来完成您的任务。代码示例将演示如何使用基类，以及不能使用基类或它不符合您需求时应该怎么做。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p104">In this article, you'll learn when you can use the generic base class and when you need to use a strongly typed item to complete your task. The code examples will show you how to use the base class, and what to do when you can't use the base class or it doesn't fit your needs.</span></span>
  
## <a name="create-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="7c4bc-129">使用 EWS 托管 API 创建项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-129">Create an item by using the EWS Managed API</span></span>
<span data-ttu-id="7c4bc-130"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-130"></span></span>

<span data-ttu-id="7c4bc-p105">EWS 托管 API 没有公共构造函数用于 [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 类，因此您必须使用您想要创建的特定项类型的构造函数来创建项。例如，使用 [EmailMessage 类构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx)来创建新的电子邮件，以及使用 [Contact 类构造函数](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx)创建新联系人。同样，服务器从不在响应中返回泛型 **Item** 对象；所有泛型项作为 **EmailMessage** 对象返回。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p105">The EWS Managed API does not have a publicly available constructor for the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) class, so you must use the constructor for the specific item type you want to create in order to create an item. For example, use the [EmailMessage class constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.emailmessage%28v=exchg.80%29.aspx) to create a new email message, and the [Contact class constructor](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) to create a new contact. Likewise, the server never returns generic **Item** objects in responses; all generic items are returned as **EmailMessage** objects.</span></span> 
  
<span data-ttu-id="7c4bc-p106">当您确定要创建的项的类型时，您只需几个步骤便可完成任务。所有项类型的步骤类似：</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p106">When you know the type of item to create, you can complete the task in just a few steps. The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="7c4bc-136">初始化其中一个 [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 类的新实例，使用 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象作为参数。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-136">Initialize a new instance of one of the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) classes with the [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object as a parameter.</span></span> 
    
2. <span data-ttu-id="7c4bc-p107">设置项上的属性。架构对于每个项类型不同，所以不同的项可用的属性不同。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p107">Set properties on the item. The schemas are different for each item type, so different properties are available for different items.</span></span>
    
3. <span data-ttu-id="7c4bc-139">保存该项，或保存并发送该项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-139">Save the item, or save and send the item.</span></span>
    
<span data-ttu-id="7c4bc-140">例如，您可以创建 [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 对象，设置 [Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx)、[Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx) 和 [ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) 属性，然后通过使用 [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法发送它。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-140">For example, you can create an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object, set the [Subject](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.subject%28v=exchg.80%29.aspx), [Body](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.body%28v=exchg.80%29.aspx), and [ToRecipients](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.torecipients%28v=exchg.80%29.aspx) properties, and then send it by using the [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
```

<span data-ttu-id="7c4bc-141">若要了解如何使用 EWS 托管 API 创建会议或约会项目，请参阅[创建约会和会议使用 EWS 在 Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-141">To learn how to create a meeting or appointment item by using the EWS Managed API, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="create-an-item-by-using-ews"></a><span data-ttu-id="7c4bc-142">使用 EWS 创建项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-142">Create an item by using EWS</span></span>
<span data-ttu-id="7c4bc-143"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-143"></span></span>

<span data-ttu-id="7c4bc-p108">可以通过使用 EWS 创建泛型项或强类型项。所有项类型的步骤类似：</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p108">You can create a generic item or a strongly typed item by using EWS. The steps are similar for all item types:</span></span>
  
1. <span data-ttu-id="7c4bc-146">使用 [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) 操作在 Exchange 存储中创建项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-146">Use the [CreateItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) operation to create an item in the Exchange store.</span></span> 
    
2. <span data-ttu-id="7c4bc-147">使用 [Items](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) 元素包含要创建的一个或多个项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-147">Use the [Items](http://msdn.microsoft.com/library/0811a73e-bf1f-4889-9219-73902dd47639%28Office.15%29.aspx) element to contain one or more items to create.</span></span> 
    
3. <span data-ttu-id="7c4bc-148">设置项上的属性。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-148">Set properties on the item.</span></span>
    
<span data-ttu-id="7c4bc-p109">例如，您可以创建电子邮件并通过在下面的示例中使用代码来发送电子邮件。这也是在您调用 [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) 方法时 EWS 托管 API 发送的 XML 请求。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p109">For example, you can create an email message and send it by using the code in the following example. This is also the XML request that the EWS Managed API sends when you call the [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7c4bc-151">服务器使用 **CreateItemResponse** 邮件响应 [CreateItem](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) 请求，其中包括 [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) 值 **NoError**（表示电子邮件创建成功）和新创建邮件的 [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-151">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
<span data-ttu-id="7c4bc-152">若要了解如何使用 EWS 创建会议或约会项目，请参阅[创建约会和会议使用 EWS 在 Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-152">To learn how to create a meeting or appointment item by using EWS, see [Create appointments and meetings by using EWS in Exchange 2013](how-to-create-appointments-and-meetings-by-using-ews-in-exchange-2013.md).</span></span>
  
## <a name="get-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="7c4bc-153">使用 EWS 托管 API 获取项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-153">Get an item by using the EWS Managed API</span></span>
<span data-ttu-id="7c4bc-154"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-154"></span></span>

<span data-ttu-id="7c4bc-p110">若要使用 EWS 托管 API 来获取项目，如果您知道要检索的项的 [Item.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) ，您只需调用该项上的一个 [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 方法，则会检索到该项。最佳做法是建议您限制仅返回所需的属性。此示例返回项 **Id** 属性和 **Subject** 属性。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p110">To use the EWS Managed API to get an item if you know the [Item.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to retrieve, you simply call one of the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) methods on the item, and the item is retrieved. As a best practice, we recommend that you limit the properties returned to only those that are required. This example returns the item **Id** property and the **Subject** property.</span></span> 
  
<span data-ttu-id="7c4bc-p111">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。本地变量  *itemId*  是要更新的项的 [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p111">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// As a best practice, limit the properties returned to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.Subject);
// Bind to the existing item by using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId, propSet);

```

<span data-ttu-id="7c4bc-160">如果您正在搜索满足特定条件的项，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7c4bc-160">If you're searching for an item that meets specific criteria, do the following:</span></span>
  
1. <span data-ttu-id="7c4bc-161">绑定到包含要获取的项的文件夹。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-161">Bind to the folder that contains the items to get.</span></span>
    
2. <span data-ttu-id="7c4bc-162">实例化 [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) 或 [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) 过滤要返回的项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-162">Instantiate a [SearchFilter.SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) or a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) to filter the items to return.</span></span> 
    
3. <span data-ttu-id="7c4bc-163">实例化 [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) 或 [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) 对象指定要返回的项数。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-163">Instantiate an [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) object to specify the number of items to return.</span></span> 
    
4. <span data-ttu-id="7c4bc-164">调用 [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) 或 [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) 方法。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-164">Call the [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [ExchangeService.FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="7c4bc-p112">例如，如果您想要检索收件箱中未读的电子邮件，请在下面的示例中使用代码。此示例使用 **SearchFilterCollection** 将 **FindItems** 方法的结果限制为未读邮件，并限制 **ItemView** 以将结果限制为一个项。此特定代码仅适用于 [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) 对象，因为 [EmailMessageSchema.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) 值属于 **SearchFilter** 。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p112">For example, if you want to retrieve unread email messages in the Inbox, use the code in the following example. This example uses a **SearchFilterCollection** to limit the results of the **FindItems** method to unread messages, and limits the **ItemView** to limit results to one item. This particular code only works on [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects because the [EmailMessageSchema.IsRead](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessageschema.isread%28v=exchg.80%29.aspx) value is part of the **SearchFilter**.</span></span> 
  
```cs
// Bind the Inbox folder to the service object.
Folder inbox = Folder.Bind(service, WellKnownFolderName.Inbox);
// The search filter to get unread email.
SearchFilter sf = new SearchFilter.SearchFilterCollection(LogicalOperator.And, new SearchFilter.IsEqualTo(EmailMessageSchema.IsRead, false));
ItemView view = new ItemView(1);
// Fire the query for the unread items.
// This method call results in a FindItem call to EWS.
FindItemsResults<Item> findResults = service.FindItems(WellKnownFolderName.Inbox, sf, view);
```

<span data-ttu-id="7c4bc-p113">或者，您可以使用 [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 限制搜索结果，如以下代码示例中所示。此示例使用 [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) 方法来检索在接下来的 30 天中发生的最多五个约会。当然，此代码仅适用于日历项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p113">Alternatively, you can use a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) to limit the results of the search as shown in the following code example. This example uses the [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to retrieve up to five appointments that occur in the next 30 days. This code of course only works on calendar items.</span></span> 
  
```cs
// Initialize values for the start and end times, and the number of appointments to retrieve.
DateTime startDate = DateTime.Now;
DateTime endDate = startDate.AddDays(30);
const int NUM_APPTS = 5;
// Bind the Calendar folder to the service object.
// This method call results in a GetFolder call to EWS.
CalendarFolder calendar = CalendarFolder.Bind(service, WellKnownFolderName.Calendar, new PropertySet());
// Set the start and end time and number of appointments to retrieve.
CalendarView cView = new CalendarView(startDate, endDate, NUM_APPTS);
// Limit the properties returned to the appointment's subject, start time, and end time.
cView.PropertySet = new PropertySet(AppointmentSchema.Subject, AppointmentSchema.Start, AppointmentSchema.End);
// Retrieve a collection of appointments by using the calendar view.
// This method call results in a FindAppointments call to EWS.
FindItemsResults<Appointment> appointments = calendar.FindAppointments(cView);
```

<span data-ttu-id="7c4bc-p114">请注意，服务器在 **Bind** 方法响应中返回的信息不同于服务器为 **FindItem** 或 **FindAppointment** 方法响应返回的信息。 **Bind** 方法可返回所有架构化属性，而 **FindItem** 和 **FindAppointment** 方法不会返回所有架构化属性。所以如果需要完全访问项，您将需要使用 **Bind** 方法。如果您不具备要检索的项的项 **Id** ，请使用 **FindItem** 或 **FindAppointment** 方法来检索 ID，然后使用 **Bind** 方法来检索所需的属性。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p114">Note that the information the server returns in the **Bind** method response is different than the information that the server returns for a **FindItem** or **FindAppointment** method response. The **Bind** method can return all the schematized properties, whereas the **FindItem** and **FindAppointment** methods do not return all the schematized properties. So if you need full access to the item, you'll have to use the **Bind** method. If you don't have the item **Id** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** methods to retrieve the Id, and then use the **Bind** method to retrieve the properties you need.</span></span> 
  
<span data-ttu-id="7c4bc-175">若要了解如何使用 EWS 托管 API 获取会议或约会项目，请参阅[获取约会和会议使用 EWS 在 Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-175">To learn how to get a meeting or appointment item by using the EWS Managed API, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="get-an-item-by-using-ews"></a><span data-ttu-id="7c4bc-176">使用 EWS 获取项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-176">Get an item by using EWS</span></span>
<span data-ttu-id="7c4bc-177"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-177"></span></span>

<span data-ttu-id="7c4bc-178">如果您知道要检索的项的 [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx)，您可以通过使用 [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) 操作获取项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-178">If you know the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the item to retrieve, you can get the item by using the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation.</span></span> 
  
<span data-ttu-id="7c4bc-p115">下面的示例演示 XML 请求通过特定 [ItemId](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) 获取某项的 **"主题"**。这也是当在 [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 上调用 **Bind** 方法时 EWS 托管 API 发送的 XML 请求。为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p115">The following example shows the XML request to get the [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) of an item with a specific **ItemId**. This is also the XML request that the EWS Managed API sends when calling the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method on an **ItemId**. The values of some attributes and elements have been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="GJc/NAAA=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7c4bc-p116">以下示例显示了服务器在处理 **GetItem** 操作后返回的 XML 响应。该响应指示项已成功检索。为了方便读取，已缩短某些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p116">The following example shows the XML response that the server returns after it processes the **GetItem** operation. The response indicates the item was retrieved successfully. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" 
                         MinorVersion="0" 
                         MajorBuildNumber="815" 
                         MinorBuildNumber="6" 
                         Version="V2_7" 
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="GJc/NAAA=" ChangeKey="CQAAABYAAAAPxolXAHv3TaHUnjW8wWqXAAAGJd9Z"/>
              <t:Subject>Company Soccer Team</t:Subject>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="7c4bc-p117">如果您不知道要检索的项的 **ItemId**，您可以使用 [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) 操作来查找该项。为了使用 **FindItem** 操作，必须首先标识要搜索的文件夹。您可以通过使用其 **DistinguinguishedFolderName** 或使用 [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) 标识该文件夹。您可以使用 [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) 或 [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) 操作来获取您需要的 **FolderId**。然后使用 **FindItem** 操作来搜索该文件夹中与搜索筛选器匹配的结果。与 EWS 托管 API 不同，EWS 不提供单独的约会查找操作。 **FindItem** 操作会检索所有类型的项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p117">If you do not know the **ItemId** of the item you want to retrieve, you can use the [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) operation to find the item. In order to use the **FindItem** operation, you must first identify the folder that you're searching. You can identify the folder by using its **DistinguinguishedFolderName** or by using the [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx). You can use either the [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) or [SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) operations to get the **FolderId** you need. Then use the **FindItem** operation to search that folder for results that match the search filter. Unlike the EWS Managed API, EWS does not provide a separate find operation for appointments. The **FindItem** operation retrieves items of all types.</span></span> 
  
<span data-ttu-id="7c4bc-p118">下面的示例演示 XML **FindItem** 操作请求发送到服务器以查找在接下来的 30 天内出现的日历文件夹中的约会。为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p118">The following example shows the XML **FindItem** operation request that is sent to the server to find appointments in the Calendar folder that occur in the next 30 days. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="calendar:Start" />
          <t:FieldURI FieldURI="calendar:End" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:CalendarView MaxEntriesReturned="5" StartDate="2013-10-16T17:04:28.722Z" EndDate="2013-11-15T18:04:28.722Z" />
      <m:ParentFolderIds>
        <t:FolderId Id="AAAEOAAA=" ChangeKey="AgAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAAAA3" />
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7c4bc-p119">服务器通过包含 **NoError** 的 [ResponseCode](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) 值的 [ FindItemResponse ](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) 消息响应 **FindItem** 请求，该值指示操作已成功完成。如果任意日历项符合过滤条件，则它们将会包括在响应中。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p119">The server responds to the **FindItem** request with a [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) message that includes the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the operation completed successfully. If any calendar items meet the filtering criteria, they are included in the response.</span></span>
  
<span data-ttu-id="7c4bc-p120">请注意，服务器在 **GetItem** 操作响应中返回的信息不同于服务器在 **FindItem** 或 **FindAppointment** 操作响应中返回的信息。 **GetItem** 方法可返回所有架构化属性，而 **FindItem** 和 **FindAppointment** 操作不会返回所有架构化属性。所以，如果您需要对项进行完全访问，您将需要使用 **GetItem** 操作。如果您不具备要检索的项的 **ItemId**，请使用 **FindItem** 或 **FindAppointment** 操作来检索 **ItemId**，然后使用 **GetItem** 操作来检索所需的元素。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p120">Note that the information the server returns in the **GetItem** operation response is different than the information the server returns in a **FindItem** or **FindAppointment** operation response. The **GetItem** operation can return all the schematized properties, whereas the **FindItem** and **FindAppointment** operations do not return all the schematized properties. So if you need full access to the item, you'll have to use the **GetItem** operation. If you don't have the **ItemId** of the item you'd like to retrieve, use the **FindItem** or **FindAppointment** operations to retrieve the **ItemId**, and then use the **GetItem** operation to retrieve the elements you need.</span></span> 
  
<span data-ttu-id="7c4bc-200">若要了解如何使用 EWS 获取会议或约会项目，请参阅[获取约会和会议使用 EWS 在 Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-200">To learn how to get a meeting or appointment item by using EWS, see [Get appointments and meetings by using EWS in Exchange](how-to-get-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="7c4bc-201">使用 EWS 托管 API 更新项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-201">Update an item by using the EWS Managed API</span></span>
<span data-ttu-id="7c4bc-202"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-202"></span></span>

<span data-ttu-id="7c4bc-p121">通过 EWS 托管 API 更新项的步骤对于所有项类型是相似的；但是，项属性对于每种项类型是不同的，[Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) 方法具有许多可选择的过载方法。要更新项，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p121">The steps to update an item by using the EWS Managed API are similar for all item types; however, the item properties are different for each item type, and the [Update](http://msdn.microsoft.com/en-us/library/office/dd635915%28v=exchg.80%29.aspx) method has many overloaded methods to choose from. To update an item:</span></span> 
  
1. <span data-ttu-id="7c4bc-p122">使用 [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) 方法获取最新版本的项，除非已经拥有该项。若要更新特定于某个强类型项的属性，您需要绑定到该项类型。若要更新可用的泛型项类型上可用的属性，您可以绑定到 [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) 对象。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p122">Use the [Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) method to get the latest version of the item, unless you already have it. To update properties specific to a strongly typed item, you'll have to bind to that item type. To update properties available on the generic item type, you can bind to the [Item](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) object.</span></span> 
    
2. <span data-ttu-id="7c4bc-208">更新项上的属性。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-208">Update the properties on the item.</span></span>
    
3. <span data-ttu-id="7c4bc-209">调用 **Update** 方法。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-209">Call the **Update** method.</span></span> 
    
<span data-ttu-id="7c4bc-210">例如，可以使用泛型项类型更新某个电子邮件的主题，如下面的示例代码中所示。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-210">For example, you can update the subject of an email by using the generic item type, as shown in the code in the following example.</span></span>
  
<span data-ttu-id="7c4bc-p123">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。本地变量  *itemId*  是要更新的项的 [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p123">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Update the Subject of the email.
item.Subject = "New subject";
// Save the updated email.
// This method call results in an UpdateItem call to EWS.
item.Update(ConflictResolutionMode.AlwaysOverwrite);
```

<span data-ttu-id="7c4bc-213">若要了解如何使用 EWS 托管 API 更新会议或约会项目，请参阅[更新约会和会议使用 EWS 在 Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-213">To learn how to update a meeting or appointment item by using the EWS Managed API, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="update-an-item-by-using-ews"></a><span data-ttu-id="7c4bc-214">使用 EWS 更新项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-214">Update an item by using EWS</span></span>
<span data-ttu-id="7c4bc-215"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-215"></span></span>

<span data-ttu-id="7c4bc-216">要通过 EWS 更新某项，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7c4bc-216">To update an item by using EWS, do the following:</span></span>
  
1. <span data-ttu-id="7c4bc-217">使用 [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) 操作获取最新版本的项，除非已拥有该项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-217">Use the [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) operation to get the latest version of the item, unless you already have it.</span></span> 
    
2. <span data-ttu-id="7c4bc-218">使用 [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) 操作来指定字段，以更新并将新值分配给这些字段。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-218">Use the [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) operation to specify fields to update and assign new values to those fields.</span></span> 
    
<span data-ttu-id="7c4bc-p124">下面的示例显示了发送给服务器以更新电子邮件 **"主题"** 值的 XML [UpdateItem](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) 操作请求。为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p124">The following example shows the XML **UpdateItem** operation request that is sent to the server to update the [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) value of the email message. The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateItem MessageDisposition="SaveOnly" ConflictResolution="AlwaysOverwrite">
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAAAPdgr" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>New subject</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7c4bc-221">服务器使用 **UpdateItemResponse** 邮件响应 [UpdateItem](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) 请求，该邮件中包括 [NoError](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) 的 **ResponseCode** 值，该值表示项更新成功。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-221">The server responds to the **UpdateItem** request with a [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item update was successful.</span></span>
  
<span data-ttu-id="7c4bc-222">若要了解如何使用 EWS 更新会议或约会项目，请参阅[更新约会和会议使用 EWS 在 Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-222">To learn how to update a meeting or appointment item by using EWS, see [Update appointments and meetings by using EWS in Exchange](how-to-update-appointments-and-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-the-ews-managed-api"></a><span data-ttu-id="7c4bc-223">使用 EWS 托管 API 删除项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-223">Delete an item by using the EWS Managed API</span></span>
<span data-ttu-id="7c4bc-224"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-224"></span></span>

<span data-ttu-id="7c4bc-p125">您可以通过将项移动到已删除项文件夹或垃圾站来删除项。如果您知道要删除的项的 [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)，只需调用该项的 [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) 方法。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p125">You can delete items by moving them to the Deleted Items folder or to the dumpster. If you know the [ItemId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to delete, just call the [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) method on the item.</span></span> 
  
<span data-ttu-id="7c4bc-227">如果您需要在删除项之前找到它，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7c4bc-227">If you need to find the item before deleting it, do the following:</span></span>
  
1. <span data-ttu-id="7c4bc-228">调用 [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) 或 [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) 方法找到要删除的项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-228">Call the [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) or [FindAppointments](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findappointments%28v=exchg.80%29.aspx) method to find the item to delete.</span></span> 
    
1. <span data-ttu-id="7c4bc-229">实例化 [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) 并将其限制为要返回的属性，或者使用 [SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) 查找特定项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-229">Instantiate a [PropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) and limit it to the properties to return, or use a [SearchFilterCollection](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfilter.searchfiltercollection%28v=exchg.80%29.aspx) to find specific items.</span></span> 
    
2. <span data-ttu-id="7c4bc-230">实例化 [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) 或 [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) 指定要返回的项数。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-230">Instantiate an [ItemView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemview%28v=EXCHG.80%29.aspx) or [CalendarView](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) to specify the number of items to return.</span></span> 
    
2. <span data-ttu-id="7c4bc-231">调用 [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) 方法。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-231">Call the [Delete](http://msdn.microsoft.com/en-us/library/office/dd635072%28v=exchg.80%29.aspx) method.</span></span> 
    
<span data-ttu-id="7c4bc-232">例如，下面的代码演示如何将电子邮件移动到已删除项文件夹。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-232">For example, the following code shows how to move an email message to the Deleted Items folder.</span></span>
  
<span data-ttu-id="7c4bc-p126">此示例假定 **service** 是有效的 [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) 对象，并且已向 Exchange 服务器对该用户进行身份验证。本地变量  *itemId*  是要更新的项的 [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p126">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server. The local variable  *itemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to update.</span></span> 
  
```cs
// Bind to the existing item, using the ItemId.
// This method call results in a GetItem call to EWS.
Item item = Item.Bind(service, itemId);
// Delete the item by moving it to the Deleted Items folder.
// This method call results in a DeleteItem call to EWS.
item.Delete(DeleteMode.MoveToDeletedItems);
```

<span data-ttu-id="7c4bc-235">有关删除项的更多详细信息，请参阅[通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-235">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="7c4bc-236">若要了解如何使用 EWS 托管 API 删除会议或约会项目，请参阅[删除约会和取消在 Exchange 使用 EWS 的会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-236">To learn how to delete a meeting or appointment item by using the EWS Managed API, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="delete-an-item-by-using-ews"></a><span data-ttu-id="7c4bc-237">使用 EWS 删除项</span><span class="sxs-lookup"><span data-stu-id="7c4bc-237">Delete an item by using EWS</span></span>
<span data-ttu-id="7c4bc-238"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-238"></span></span>

<span data-ttu-id="7c4bc-239">您可以通过使用 [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) 操作删除项。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-239">You can delete an item by using the [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) operation.</span></span> 
  
<span data-ttu-id="7c4bc-p128">下面的示例显示了发送给服务器以将电子邮件移动到已删除项文件夹的 XML 请求。为了方便读取，已缩短一些属性和元素的值。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p128">The following example shows the XML request that is sent to the server to move the email message to the Deleted Items folder. The values of some attributes and elements have been shortened for readability.</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010_SP1" />
  </soap:Header>
  <soap:Body>
    <m:DeleteItem DeleteType="MoveToDeletedItems">
      <m:ItemIds>
        <t:ItemId Id="APdZjAAA=" ChangeKey="CQAAABYAAAAqRr3mNdNMSasqx/o9J13UAAANIFzC" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="7c4bc-242">服务器使用 **DeleteItemResponse** 邮件响应 [DeleteItem](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) 请求，该邮件中包括 [NoError](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) 的 **ResponseCode** 值，该值表示项删除成功。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-242">The server responds to the **DeleteItem** request with a [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes the a [ResponseCode](http://msdn.microsoft.com/en-us/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the item deletion was successful.</span></span>
  
<span data-ttu-id="7c4bc-243">有关删除项的更多详细信息，请参阅[通过在 Exchange 使用 EWS 中删除项目](deleting-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-243">For more details about deleting items, see [Deleting items by using EWS in Exchange](deleting-items-by-using-ews-in-exchange.md).</span></span> <span data-ttu-id="7c4bc-244">若要了解如何使用 EWS 删除会议或约会项目，请参阅[删除约会和取消在 Exchange 使用 EWS 的会议](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-244">To learn how to delete a meeting or appointment item by using EWS, see [Delete appointments and cancel meetings by using EWS in Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md).</span></span>
  
## <a name="move-or-copy-items-to-another-mailbox"></a><span data-ttu-id="7c4bc-245">将项移动或复制到另一个邮箱</span><span class="sxs-lookup"><span data-stu-id="7c4bc-245">Move or copy items to another mailbox</span></span>
<span data-ttu-id="7c4bc-246"><a name="bk_movecopybtnmailboxes"> </a></span><span class="sxs-lookup"><span data-stu-id="7c4bc-246"></span></span>

<span data-ttu-id="7c4bc-p130">您可以使用 [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) 和 [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) 操作在邮件之间移动或复制项。若要了解更多信息，请参阅 [导出和导入 Exchange 中使用 EWS 的项目](exporting-and-importing-items-by-using-ews-in-exchange.md)。</span><span class="sxs-lookup"><span data-stu-id="7c4bc-p130">You can move or copy items between mailboxes by using the [ExportItems](http://msdn.microsoft.com/library/e2846abb-0b16-4732-bbd8-038a674672f6%28Office.15%29.aspx) and [UploadItems](http://msdn.microsoft.com/library/a88cbe99-7968-454d-a545-4f92c330909f%28Office.15%29.aspx) operations. To learn more, see [Exporting and importing items by using EWS in Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7c4bc-249">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7c4bc-249">See also</span></span>

- [<span data-ttu-id="7c4bc-250">文件夹和交换中的 EWS 中的项目</span><span class="sxs-lookup"><span data-stu-id="7c4bc-250">Folders and items in EWS in Exchange</span></span>](folders-and-items-in-ews-in-exchange.md)    
- [<span data-ttu-id="7c4bc-251">在 Exchange 使用 EWS 使用文件夹</span><span class="sxs-lookup"><span data-stu-id="7c4bc-251">Work with folders by using EWS in Exchange</span></span>](how-to-work-with-folders-by-using-ews-in-exchange.md)    
- [<span data-ttu-id="7c4bc-252">通过在 Exchange 使用 EWS 中删除项目</span><span class="sxs-lookup"><span data-stu-id="7c4bc-252">Deleting items by using EWS in Exchange</span></span>](deleting-items-by-using-ews-in-exchange.md)
    

