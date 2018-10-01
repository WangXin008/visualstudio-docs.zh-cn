---
title: ResolveManifestFiles 任务 | Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- ResolveManifestFiles task [MSBuild]
- MSBuild, ResolveManifestFiles task
ms.assetid: e1e14f67-9b69-433f-94d4-a783a68676b2
caps.latest.revision: 8
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: b459ef08b9375fc246d51a161601879a26b61afa
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47479724"
---
# <a name="resolvemanifestfiles-task"></a>ResolveManifestFiles 任务
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

本主题的最新版本，请参阅[ResolveManifestFiles 任务](https://docs.microsoft.com/visualstudio/msbuild/resolvemanifestfiles-task)。  
  
  
在生成过程中，将以下各项解析为文件以便生成清单：生成项、依赖项、附属项、内容、调试符号和文档。  
  
## <a name="parameters"></a>参数  
 下表描述了 `ResolveManifestFiles` 任务的参数。  
  
|参数|描述|  
|---------------|-----------------|  
|`DeploymentManifestEntryPoint`|可选 <xref:Microsoft.Build.Framework.ITaskItem> 参数。<br /><br /> 指定部署清单的名称。|  
|`EntryPoint`|可选 <xref:Microsoft.Build.Framework.ITaskItem> 参数。<br /><br /> 指定作为清单入口点的托管程序集或 ClickOnce 清单引用。|  
|`ExtraFiles`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定额外文件。|  
|`ManagedAssemblies`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定托管程序集。|  
|`NativeAssemblies`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定本机程序集。|  
|`OutputAssemblies`|可选的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 输出参数。<br /><br /> 指定所生成的程序集。|  
|`OutputDeploymentManifestEntryPoint`|可选 <xref:Microsoft.Build.Framework.ITaskItem> 输出参数。<br /><br /> 指定输出部署清单入口点。|  
|`OutputEntryPoint`|可选 <xref:Microsoft.Build.Framework.ITaskItem> 输出参数。<br /><br /> 指定输出入口点。|  
|`OutputFiles`|可选的 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 输出参数。<br /><br /> 指定输出文件。|  
|`PublishFiles`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定发布文件。|  
|`SatelliteAssemblies`|可选 <xref:Microsoft.Build.Framework.ITaskItem>`[]` 参数。<br /><br /> 指定附属程序集。|  
|`SigningManifests`|可选 `Boolean` 参数。<br /><br /> 如果为 `true`，则清单已签名。|  
|`TargetCulture`|可选 `String` 参数。<br /><br /> 指定附属程序集的目标区域性。|  
|`TargetFrameworkVersion`|可选 `String` 参数。<br /><br /> 指定目标 .NET Framework 的版本。|  
  
## <a name="remarks"></a>备注  
 除了具有表中列出的参数外，此任务还将从本身继承自 <xref:Microsoft.Build.Utilities.Task> 类的 <xref:Microsoft.Build.Tasks.TaskExtension> 类继承参数。 有关这些其他参数的列表及其说明的信息，请参阅 [TaskExtension Base Class](../msbuild/taskextension-base-class.md)。  
  
## <a name="see-also"></a>请参阅  
 [任务](../msbuild/msbuild-tasks.md)   
 [任务参考](../msbuild/msbuild-task-reference.md)


