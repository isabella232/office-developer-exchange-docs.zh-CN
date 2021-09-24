---
title: CChkSGFiles.PAGE_INFO 结构
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PAGE_INFO
api_type:
- dllExport
ms.assetid: 408335e1-6977-441f-bfad-ede791d1630c
description: 上次修改时间：2013 年 2 月 22 日
ms.openlocfilehash: f324ec9aca6f94911041c227ce039139292a10aa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516256"
---
# <a name="cchksgfilespage_info-struct"></a>CChkSGFiles.PAGE_INFO 结构

**适用于：Exchange Server** 2003 |Exchange Server 2007 |Exchange Server 2010 |Exchange Server 2013 年
  
保存数据库Exchange的信息。 此结构与 **ErrCheckDbPages 函数** 一同使用。 
  
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
  
无符号长 。 要检查的数据库页的逻辑页码。 在调用 **ErrCheckDbPages 之前，必须设置此值**。 如果应用程序基于文件偏移读取文件，因此必须将文件偏移映射到逻辑页码，则您将发现 **PgnoFromFileOffset** 方法对于确定此字段的值非常有用。 **ErrCheckDbPages** 不会修改此值。 
    
### <a name="fpageisinitialized"></a>fPageIsInitialized 
  
Boolean。 TRUE 值表示数据库页包含数据。 FALSE 值表示页面仅包含零。 **ErrCheckDbPages** 设置此值。 
    
### <a name="fcorrectableerror"></a>fCorrectableError
  
Boolean。 TRUE 值表示在数据库页中检测到校验和不匹配，但这是一个可更正的错误。 **ErrCheckDbPages** 设置此值。 
    
### <a name="checksumactual"></a>checksumActual
  
无符号 64 位整数。 指示数据库中为此逻辑页存储的校验和值。 **ErrCheckDbPages** 设置此值。 
    
### <a name="checksumexpected"></a>checksumExpected
  
无符号 64 位整数。 这是为数据库页计算的预期校验和值;它由 **ErrCheckDbPages 设置**。 如果此值与数据库页上存储的值不同 (即 **，在 checksumActual**) 中返回的值 **，ErrCheckDbPages** 将指示在此数据库页上发现了错误。 
    
### <a name="dbtime"></a>dbTime
  
无符号 64 位整数。 **ErrCheckDbPages** 将此成员设置数据库页上的时间戳。 
    
### <a name="checksumpagestructure"></a>checksumPageStructure 
  
无符号 64 bt 整数。 **ErrCheckDbPages** 将此成员设置为页面内容的计算校验和值，不包括确定逻辑页面等效时不必要的数据。 例如，不需要考虑未使用的数据库页面空间的数据值。 此成员仅在 **校验和Actual**  和  **checksumExpected**  值相等时有效。 
    
### <a name="ulflags"></a>ulFlags
  
无符号 64 位整数。 保留供以后使用。 在调用 **ErrCheckDbPages** 之前，此字段的值必须设置为 0 (0) 0。
    
## <a name="remarks"></a>注解

调用 **ErrCheckDbPages** 函数时 **，rgPageInfo**  参数是 **PAGE \_ INFO** 结构的数组。 对于每个要检查 **的数据库页 \_** ，必须存在一个页面 INFO 结构。 
  
应用程序必须将 **ulPgno** 成员设置为正确的值，并且还必须在调用 **ErrCheckDbPages** 之前将 **ulFlags** 成员设置为 0 (0) 0。 
  
## <a name="requirements"></a>Requirements

Exchange Server 2013 仅包括 64 位版本的 CHKSGFILES API。
  
运行应用程序的帐户必须具有对要检查的数据库和日志文件的读取访问权限。
  

