---
title: Visual Studio 的建模 SDK 的 API 参考 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-tfs-dev14
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 590c9a69-4e22-4841-bb23-f32e80ec1e76
caps.latest.revision: 10
author: gewarren
ms.author: gewarren
manager: douge
ms.openlocfilehash: 65f8fffbe86bfb80916aa62d3f148795a3c279d5
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47471121"
---
# <a name="api-reference-for-modeling-sdk-for-visual-studio"></a>Visual Studio 的建模 SDK 的 API 参考
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[Visual Studio 的建模 SDK 的 API 参考](https://docs.microsoft.com/visualstudio/modeling/api-reference-for-modeling-sdk-for-visual-studio)。  
  
Visual Studio 可视化和建模 SDK 提供了你的域特定语言 (DSL) 和 UML 工具生成的平台。  
  
> [!NOTE]
>  有关 UML 建模 API 的信息，请参阅[UML 建模扩展性的 API 参考](../modeling/api-reference-for-uml-modeling-extensibility.md)。 有关文本转换的信息，请参阅[自定义 T4 文本转换](../modeling/customizing-t4-text-transformation.md)。  
  
 本部分包含具有以"Microsoft.VisualStudio.Modeling"开头的名称的命名空间的参考资料。  
  
|命名空间|内容|  
|---------------|-------------|  
|<xref:Microsoft.VisualStudio.Modeling?displayProperty=fullName>|如 ModelElement，是在 DSL 中定义的所有域类的基类的类。|  
|<xref:Microsoft.VisualStudio.Modeling.Design?displayProperty=fullName>|形成 DSL 定义的一部分的类。|  
|<xref:Microsoft.VisualStudio.Modeling.Diagnostics?displayProperty=fullName>|模型存储查看器和性能的评定工具。|  
|<xref:Microsoft.VisualStudio.Modeling.Diagrams?displayProperty=fullName>|如 ShapeElement，是在 DSL 中定义的所有形状的基类的类。|  
|<xref:Microsoft.VisualStudio.Modeling.Diagrams.ExtensionEnablement?displayProperty=fullName>|手势和选择的方法。|  
|<xref:Microsoft.VisualStudio.Modeling.DslDefinition?displayProperty=fullName>|DSL 定义设计器的 API。|  
|<xref:Microsoft.VisualStudio.Modeling.DslDefinition.Design?displayProperty=fullName>|在 DSL 定义设计器的内部类。|  
|<xref:Microsoft.VisualStudio.Modeling.DslDefinition.ExtensionEnablement?displayProperty=fullName>|使你可以扩展 DSL 设计器具有命令、 笔势和验证的属性。|  
|<xref:Microsoft.VisualStudio.Modeling.Extensibility?displayProperty=fullName>|实现 DSL 可扩展性的扩展方法的模型元素。|  
|<xref:Microsoft.VisualStudio.Modeling.ExtensionEnablement?displayProperty=fullName>|扩展属性|  
|<xref:Microsoft.VisualStudio.Modeling.Immutability?displayProperty=fullName>|能让你的模型部分只读的。|  
|<xref:Microsoft.VisualStudio.Modeling.Integration?displayProperty=fullName>|Modelbus API，它可以帮助您将集成不同的模型。|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Picker?displayProperty=fullName>|对话框中，可让用户导航到的模型和元素来创建 Modelbus 引用。|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Picker.Hosting?displayProperty=fullName>|选取器服务中。|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Shell?displayProperty=fullName>|Modelbus 适配器框架，用于[!INCLUDE[vsprvs](../includes/vsprvs-md.md)]。|  
|<xref:Microsoft.VisualStudio.Modeling.Integration.Shell.Picker?displayProperty=fullName>|选取器对话框中，可让用户导航到的模型和元素来创建 Modelbus 引用。|  
|<xref:Microsoft.VisualStudio.Modeling.Shell?displayProperty=fullName>|Dsl 之间的接口和[!INCLUDE[vsprvs](../includes/vsprvs-md.md)]。|  
|<xref:Microsoft.VisualStudio.Modeling.Shell.ExtensionEnablement?displayProperty=fullName>|你可以定义快捷 （上下文） 菜单命令。|  
|<xref:Microsoft.VisualStudio.Modeling.Validation?displayProperty=fullName>|你可以定义验证约束。|  
  
## <a name="see-also"></a>请参阅  
 [UML 建模扩展性的 API 参考](../modeling/api-reference-for-uml-modeling-extensibility.md)   
 [自定义 T4 文本转换](../modeling/customizing-t4-text-transformation.md)


