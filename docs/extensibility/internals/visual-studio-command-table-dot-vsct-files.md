---
title: Visual Studio 命令表 (。.Vsct) 文件 |Microsoft Docs
description: 了解命令表配置文件，这些文件是描述 VSPackage 包含的命令集的文本文件。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT files, overview
- Visual Studio command table configuration files (VSCT), overview
ms.assetid: 1313adb4-add4-4e74-90e2-f4be522f5259
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 377bae52f506c1cb9ac0f6b2d4136faaab0b50ad
ms.sourcegitcommit: 19061b61759ce8e3b083a0e01a858e5435580b3e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "97488032"
---
# <a name="visual-studio-command-table-vsct-files"></a>Visual Studio 命令表格 (.Vsct) 文件
命令表配置文件是一个文本文件，用于描述 VSPackage 包含的一组命令。 [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)]命令表 (.vsct) 编译器将基于 XML 的配置文件 () 到二进制命令表输出 ( cto) 文件。 生成的 cto 文件与使用命令表创建的文件相同， (.CTC) 编译器编译 .ctc 配置文件。 但是，.vsct 文件有一些优点，例如 XML 编辑器和 XML IntelliSense。

 若要了解有关 .vsct 文件语法和语义的详细信息，请参阅 [设计 XML 命令表 (。.Vsct) 文件](../../extensibility/internals/designing-xml-command-table-dot-vsct-files.md)

## <a name="in-this-section"></a>本节内容
 [设计 XML 命令表格 (.Vsct) 文件](../../extensibility/internals/designing-xml-command-table-dot-vsct-files.md)

 描述如何设计 .vsct 文件。

 [如何：创建 .Vsct 文件](../../extensibility/internals/how-to-create-a-dot-vsct-file.md)

 比较用于创建 .vsct 文件的方法。 介绍手动创建 .vsct 文件的过程。

## <a name="related-sections"></a>相关章节
 [VSCT XML 架构参考](../../extensibility/vsct-xml-schema-reference.md)

 提供有关命令表 XML 配置文件的每个部分的详细信息。

 [命令表配置 (。.Ctc) 文件](/previous-versions/bb165153(v=vs.100)) 提供了 .ctc 文件格式的概述。

 [VSPackage 如何添加用户界面元素](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)

 描述命令表格式规范。

 [VSPackage 中的资源](../../extensibility/internals/resources-in-vspackages.md)

 介绍如何在托管 Vspackage 中使用托管资源和非托管资源。

 [命令、菜单和工具栏](../../extensibility/internals/commands-menus-and-toolbars.md)

 说明如何创建包含菜单、工具栏和命令组合框的 UI。