---
title: 不支持的调试方案
description: 了解工作流设计器中不受支持的调试方案，例如，"代码编辑后无法继续执行"。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 6adbe379-41d0-4681-9cd0-b91f187c3c2c
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
author: TerryGLee
ms.openlocfilehash: 4e98e2a75905f4c0a4c007691a99961dbcf1477c
ms.sourcegitcommit: d10f37dfdba5d826e7451260c8370fd1efa2c4e4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/10/2020
ms.locfileid: "96996261"
---
# <a name="unsupported-debugging-scenarios-in-the-workflow-designer"></a>工作流设计器中不受支持的调试方案

工作流设计器不支持以下调试方案：

- 在编辑代码之后不能继续执行。

- 不能从工作流中的任意点继续执行（“设置下一语句”）。

- 只有在到达光标处之后才能继续执行（“运行到光标处”）。

- 不能使用工作流设计器来调试通过代码创建（未使用工作流设计器）的工作流。

- 无法在 .NET Framework 4 或更高版本中调试在早期版本的 Windows Workflow Foundation (WF) 中创建的工作流。

- 不能在两个活动或 <xref:System.Activities.Statements.Flowchart> 节点之间的链接上定义断点。

- 调试期间剪贴板不可用。

- 复制或粘贴活动时不会保留断点。

- 不能在调用堆栈窗口中设置工作流断点。

- 在设计器中创建断点时，不使用 "**新建断点**" 对话框中的 **行** 和 **字符** 设置。

- “断点”窗口或快捷菜单不支持以下用于工作流调试的列或选项：

  - 条件

  - 命中计数

  - 命中条件

  - 函数

  - 数据

  - 过程

  - 转到反汇编
