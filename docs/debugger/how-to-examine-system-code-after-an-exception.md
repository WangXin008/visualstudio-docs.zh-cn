---
title: 在异常发生后检查系统代码 | Microsoft Docs
description: 了解如何检查系统调用中的代码以查找异常的原因。 即使未加载系统代码的符号，该过程也适用。
ms.custom: SEO-VS-2020, seodec18
ms.date: 11/04/2016
ms.topic: how-to
dev_langs:
- CSharp
- VB
- FSharp
- C++
helpviewer_keywords:
- debugging, exceptions
- exceptions, debugging
ms.assetid: a38ad49b-7cf3-483d-91c4-eb3116eba50c
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: eceb9f898b4329940408e4063dc73d81e2a604a4
ms.sourcegitcommit: 620d30c60da8f9805fce524fe4951cf40f28297d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/05/2021
ms.locfileid: "97903450"
---
# <a name="how-to-examine-system-code-after-an-exception"></a>如何：在发生异常后检查系统代码
发生异常时，你可能需要检查系统调用内部的代码，以确定该异常的起因。 如果你没有为系统代码加载符号，或者启用了“仅我的代码”，则下面的步骤说明了如何执行此操作。

### <a name="to-examine-system-code-following-an-exception"></a>在发生异常后检查系统代码

1. 在“调用堆栈”窗口中右键单击，然后单击“显示外部代码” 。

     如果未启用“仅我的代码”，则快捷菜单中不提供此选项，默认情况下显示系统代码。

2. 右键单击此时显示在“调用堆栈”窗口中的外部代码帧。

3. 指向“从其中加载符号”，然后单击“Microsoft 符号服务器” 。

    1. 如果启用了“仅我的代码”，则将显示一个对话框。 它指出“仅我的代码”现在已禁用。 要单步执行系统调用，必须这样做。

    2. “正在下载公共符号”对话框随即出现。 下载完毕后会自动关闭该对话框。

4. 现在即可在“调用堆栈”窗口和其他窗口中检查系统代码。 例如，可以双击调用堆栈帧，在源窗口或“反汇编”窗口中查看代码。

## <a name="see-also"></a>请参阅
- [管理调试器的异常](../debugger/managing-exceptions-with-the-debugger.md)