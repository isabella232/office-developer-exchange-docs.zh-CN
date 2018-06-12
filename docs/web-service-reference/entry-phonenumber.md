---
title: 条目 (PhoneNumber)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: Entry 元素表示联系人的电话号码。
ms.openlocfilehash: 3953488fb0b57fcf01c2fb99039478bbe03c7f5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/11/2018
ms.locfileid: "19754143"
---
# <a name="entry-phonenumber"></a>条目 (PhoneNumber)

**Entry**元素表示联系人的电话号码。 
  
```xml
<Entry Key=""/>
```

 **PhoneNumberDictionaryEntryType**
## <a name="attributes-and-elements"></a>属性和元素

如下章节中介绍了属性、子元素和父元素。
  
### <a name="attributes"></a>属性

|**属性**|**说明**|
|:-----|:-----|
|**注册表项** <br/> | 标识电话号码。 Key 属性是类型**PhoneNumberKeyType**。<br/><br/> 以下是该属性可能的值：<br/><br/>-AssistantPhone  <br/>-商务传真  <br/>-BusinessPhone  <br/>-BusinessPhone2  <br/>-回调  <br/>-CarPhone  <br/>-CompanyMainPhone  <br/>-HomeFax  <br/>-住宅电话  <br/>-HomePhone2  <br/>Isdn  <br/>-MobilePhone  <br/>-OtherFax  <br/>-OtherTelephone  <br/>-寻呼机  <br/>-PrimaryPhone  <br/>-RadioPhone  <br/>-电报  <br/>-TtyTddPhone  <br/> |
   
### <a name="child-elements"></a>子元素

无。
  
### <a name="parent-elements"></a>父元素

|**元素**|**说明**|
|:-----|:-----|
|[PhoneNumbers](phonenumbers.md) <br/> |表示联系人的电话号码的集合。  <br/> |
   
## <a name="text-value"></a>文本值

如果使用此元素，则需要一个表示电话号码的文本值。
  
## <a name="remarks"></a>备注

描述此元素的架构位于正在运行 MicrosoftExchange Server 2007 的计算机（已安装客户端访问服务器角色）的 EWS 虚拟目录中。
  
## <a name="element-information"></a>元素信息

|||
|:-----|:-----|
|命名空间  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|架构名称  <br/> |类型架构  <br/> |
|验证文件  <br/> |Types.xsd  <br/> |
|可以为空  <br/> |False  <br/> |
   
## <a name="see-also"></a>另请参阅

- [在交换 EWS XML 元素](ews-xml-elements-in-exchange.md)
- [Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [更新联系人](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [删除联系人](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

