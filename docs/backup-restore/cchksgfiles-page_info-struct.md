---
title: CChkSGFiles.PAGE_INFO 结构
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
description: 上次修改时间： 2013 年 2 月 22 日
ms.openlocfilehash: fa66d253b4fc6bd5c29a39c5323f59bf323a906f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2018
ms.locfileid: "19753627"
---
# <a name="cchksgfilespageinfo-struct"></a>CChkSGFiles.PAGE_INFO 结构

**适用于：** Exchange Server 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013
  
包含一个 Exchange 数据库页的信息。 该结构用于**ErrCheckDbPages**函数。 
  
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

## <a name="members"></a>成员

### <a name="ulpgno"></a>ulPgNo
  
无符号长。 逻辑页的数据库页上，要检查的数。 调用**ErrCheckDbPages**之前，必须设置此值。 如果应用程序阅读基于文件偏移量的文件，因此必须将这些文件偏移映射到逻辑页码，您将发现**PgnoFromFileOffset**方法可用来确定该字段的值。 **ErrCheckDbPages**不修改此值。 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
布尔值。 值为 TRUE 指示数据库页包含数据。 值为 FALSE 指示页包含仅零。 **ErrCheckDbPages**设置此值。 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
布尔值。 值为 TRUE 指示出现在数据库页中检测到校验和不匹配，但它是可纠正错误。 **ErrCheckDbPages**设置此值。 
    
### <a name="checksumactual"></a>checksumActual
  
无符号的 64 位整数。 指示此逻辑页数据库中存储的校验和值。 **ErrCheckDbPages**设置此值。 
    
### <a name="checksumexpected"></a>checksumExpected
  
无符号的 64 位整数。 这是数据库页中; 计算预期的校验和值由**ErrCheckDbPages**设置。 如果此值是不同于存储在数据库页上的 （即，返回的值在**checksumActual**）， **ErrCheckDbPages**将指示此数据库页上找到错误。 
    
### <a name="dbtime"></a>dbTime
  
无符号的 64 位整数。 **ErrCheckDbPages**数据库页上设置为时间戳的此成员。 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
无符号的 64 bt 整数。 **ErrCheckDbPages**将此成员设置为不包括这是不必要时确定逻辑页等价数据页上的内容的计算校验和值。 例如，不需要考虑未使用的数据库页空间中的数据值。 此成员才如果**checksumActual**和**checksumExpected**值等于每个其他有效。 
    
### <a name="ulflags"></a>ulFlags
  
无符号的 64 位整数。 保留以备今后使用。 此字段的值必须调用**ErrCheckDbPages**之前设置为 0 （零）。
    
## <a name="remarks"></a>注解

调用**ErrCheckDbPages**函数的**rgPageInfo**参数是一个数组**页\_INFO**结构。 必须有一个**页\_INFO**要检查每个数据库页的结构。 
  
应用程序必须设置为适当值， **ulPgno**成员，还必须将**ulFlags**成员为 0 （零） 调用**ErrCheckDbPages**之前。 
  
## <a name="requirements"></a>要求

Exchange Server 2013 只包括 CHKSGFILES API 的 64 位版本。
  
下运行该应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

