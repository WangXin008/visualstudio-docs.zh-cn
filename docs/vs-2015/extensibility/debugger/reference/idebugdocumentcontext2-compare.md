---
title: IDebugDocumentContext2::Compare |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IDebugDocumentContext2::Compare
helpviewer_keywords:
- IDebugDocumentContext2::Compare
ms.assetid: 2327b1ba-52d0-42fb-a01e-63cb4b332d2f
caps.latest.revision: 11
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: 2e100fdd8e303bf9a85e9ea8f7f0c77b6b300d8b
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47469650"
---
# <a name="idebugdocumentcontext2compare"></a>IDebugDocumentContext2::Compare
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

本主题的最新版本，请参阅[IDebugDocumentContext2::Compare](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugdocumentcontext2-compare)。  
  
比较此文档上下文到给定数组的文档上下文。  
  
## <a name="syntax"></a>语法  
  
```cpp#  
HRESULT Compare(   
   DOCCONTEXT_COMPARE       compare,  
   IDebugDocumentContext2** rgpDocContextSet,  
   DWORD                    dwDocContextSetLen,  
   DWORD*                   pdwDocContext  
);  
```  
  
```csharp  
int Compare(   
   enum_ DOCCONTEXT_COMPARE compare,  
   IDebugDocumentContext2[] rgpDocContextSet,  
   uint                     dwDocContextSetLen,  
   out uint                 pdwDocContext  
);  
```  
  
#### <a name="parameters"></a>参数  
 `compare`  
 [in]中的值[DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md)枚举，用于指定的比较类型。  
  
 `rgpDocContextSet`  
 [in]一个数组[IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)对象表示要进行比较的文档上下文。  
  
 `dwDocContextSetLen`  
 [in]文档上下文进行比较的数组的长度。  
  
 `pdwDocContext`  
 [out]返回到索引`rgpDocContextSet`满足的比较的第一个文档上下文的数组。  
  
## <a name="return-value"></a>返回值  
 返回`S_OK`如果找到匹配项。 返回`S_FALSE`如果没有找到匹配。 否则，返回错误代码。  
  
## <a name="remarks"></a>备注  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)数组中传递的对象必须由相同的调试引擎实现`IDebugDocumentContext2`对象; 否则为调用该比较不有效。  
  
## <a name="see-also"></a>请参阅  
 [IDebugDocumentContext2](../../../extensibility/debugger/reference/idebugdocumentcontext2.md)   
 [DOCCONTEXT_COMPARE](../../../extensibility/debugger/reference/doccontext-compare.md)
