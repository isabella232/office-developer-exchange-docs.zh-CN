---
title: CChkSGFiles 结构 PAGE_INFO 结构
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 上次修改时间：2013年2月22日
ms.openlocfilehash: 5ec9f4303b26ea95b125adac6943945ae1276439
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456337"
---
# <a name="cchksgfilespage_info-struct"></a>CChkSGFiles 结构 PAGE_INFO 结构

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
保留 Exchange 数据库页面的信息。 此结构与**ErrCheckDbPages**函数一起使用。 
  
```cs
Struct PAGE_INFO  
{
        ULONGulPgno;
        BOOLfPageIsInitialized : 1;
        BOOLfCorrectableError : 1;
        ULONGLONGchecksumActual;
        ULONGLONGchecksumExpected;
        ULONGLONGdbTime;
        ULONGLONGchecksumPageStructure;
        ULONGLONGulFlags;
}

```

## <a name="members"></a>Members

### <a name="ulpgno"></a>ulPgNo
  
无符号长。 要检查的数据库页面的逻辑页面编号。 在调用**ErrCheckDbPages**之前，必须先设置此值。 如果应用程序正在根据文件偏移量读取文件，并且必须将这些文件偏移量映射到逻辑页码，则您将发现**PgnoFromFileOffset**方法对于确定此字段的值很有用。 **ErrCheckDbPages**不会修改此值。 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
布尔. 如果值为 TRUE，则表示数据库页包含数据。 如果值为 FALSE，则表示页面仅包含零。 **ErrCheckDbPages**设置此值。 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
布尔. 值为 TRUE 表示在数据库页面中检测到校验和不匹配，但这是一个可更正的错误。 **ErrCheckDbPages**设置此值。 
    
### <a name="checksumactual"></a>checksumActual
  
无符号64位整数。 指示存储在此逻辑页面的数据库中的校验和值。 **ErrCheckDbPages**设置此值。 
    
### <a name="checksumexpected"></a>checksumExpected
  
无符号64位整数。 这是为数据库页面计算的预期校验和值;它是由**ErrCheckDbPages**设置的。 如果此值不同于存储在数据库页面上的值（即，在**checksumActual**中返回的值），则**ErrCheckDbPages**将指示在此数据库页面上发现了一个错误。 
    
### <a name="dbtime"></a>dbTime
  
无符号64位整数。 **ErrCheckDbPages**将此成员设置为数据库页面上的时间戳。 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
无符号 64-bt 整数。 **ErrCheckDbPages**将此成员设置为页面内容的计算的校验和值，而不需要在确定逻辑页面等效性时不需要的数据。 例如，不需要考虑未使用的数据库页面空间中的数据值。 仅当**checksumActual**和**checksumExpected**值彼此相等时，此成员才有效。 
    
### <a name="ulflags"></a>ulFlags
  
无符号64位整数。 保留供以后使用。 在调用**ErrCheckDbPages**之前，必须将此字段的值设置为0（零）。
    
## <a name="remarks"></a>备注

调用**ErrCheckDbPages**函数时， **RgPageInfo**参数是**页面 \_ 信息**结构的数组。 对于要检查的每个数据库页面，必须有一个**页面 \_ 信息**结构。 
  
应用程序必须将**ulPgno**成员设置为适当的值，并且还必须在调用**ErrCheckDbPages**之前将**ulFlags**成员设置为0（零）。 
  
## <a name="requirements"></a>Requirements

Exchange Server 2013 仅包含64位版本的 CHKSGFILES API。
  
运行应用程序所使用的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

