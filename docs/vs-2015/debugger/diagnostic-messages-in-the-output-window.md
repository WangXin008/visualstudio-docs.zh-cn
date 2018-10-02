---
title: 输出窗口中的诊断消息 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.output
dev_langs:
- FSharp
- VB
- CSharp
- C++
helpviewer_keywords:
- diagnostic messages [C#]
- System.Diagnostics.Debug class, Output window
- messages, diagnostic
- Debug.Print replacements
- diagnosis
- Output window, diagnostic messages
- System.Diagnostics.Trace class, Output window
- Trace class, diagnostic messages
- diagnostics
- debugger, Output window
- debugging [Visual Studio], diagnostic messages in Output window
- Debug class
ms.assetid: 386e9524-be17-4573-83fb-4f7c5cae0be0
caps.latest.revision: 19
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: f0a9e0bb4fa34133937e39b310cb05360e66a443
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47482813"
---
# <a name="diagnostic-messages-in-the-output-window"></a>“输出”窗口中的诊断消息
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[输出窗口中的诊断消息](https://docs.microsoft.com/visualstudio/debugger/diagnostic-messages-in-the-output-window)。  
  
可以使用 Debug 类或 Trace 类（属于 <xref:System.Diagnostics> 类库）将运行时消息写到“输出”窗口。 如果只在程序的调试版本中输出，则使用 Debug 类。 如果要同时在调试版本和发布版本中输出，则使用 Trace 类。  
  
## <a name="output-methods"></a>输出方法  
 <xref:System.Diagnostics.Trace> 和 <xref:System.Diagnostics.Debug> 类提供下列输出方法：  
  
-   在不中断执行情况下输出信息的各种 `Write` 方法。 这些方法取代了在 Visual Basic 早期版本中使用的 `Debug.Print` 方法。  
  
-   <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=fullName> 和 <xref:System.Diagnostics.Trace.Assert%2A?displayProperty=fullName> 方法，如果指定的条件失败，这些方法将中断执行并输出信息。 默认情况下，`Assert` 方法显示对话框中的信息。 有关详细信息，请参阅[托管代码中的断言](../debugger/assertions-in-managed-code.md)。  
  
-   <xref:System.Diagnostics.Debug.Fail%2A?displayProperty=fullName> 和 <xref:System.Diagnostics.Trace.Fail%2A?displayProperty=fullName> 方法，它们总是中断执行并输出信息。 默认情况下，`Fail` 方法在对话框中显示信息。  
  
 扩展程序从应用程序中，除了**输出**窗口可以显示下列信息：  
  
-   调试器已经加载或卸载的模块。  
  
-   引发的异常。  
  
-   退出的进程。  
  
-   退出的线程。  
  
## <a name="see-also"></a>请参阅  
 [调试器安全](../debugger/debugger-security.md)   
 [“输出”窗口](../ide/reference/output-window.md)   
 [跟踪应用程序和在应用程序中插入检测点](http://msdn.microsoft.com/library/773b6fc4-9013-4322-b728-5dec7a72e743)   
 [检测和跟踪简介](http://msdn.microsoft.com/en-us/e924e57c-33cf-4b0e-9e7f-a45d13e38f2c)   
 [C#、F#、和 Visual Basic 项目类型](../debugger/debugging-preparation-csharp-f-hash-and-visual-basic-project-types.md)   
 [调试托管代码](../debugger/debugging-managed-code.md)


