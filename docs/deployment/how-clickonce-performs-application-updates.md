---
title: ClickOnce 如何执行应用程序更新 |Microsoft Docs
description: 了解 ClickOnce 如何使用文件版本信息来决定是否更新应用程序。 ClickOnce 使用文件修补来避免下载冗余。
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- updates, ClickOnce
- ClickOnce deployment, updates
- deploying applications [ClickOnce], application updates
ms.assetid: d54313c2-cf0c-420d-b151-99953a95f0bb
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: e0177f199f0178e9fe0221a4cb6daa58d36a6f87
ms.sourcegitcommit: 0893244403aae9187c9375ecf0e5c221c32c225b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/09/2020
ms.locfileid: "94382662"
---
# <a name="how-clickonce-performs-application-updates"></a>ClickOnce 如何执行应用程序更新
ClickOnce 使用在应用程序的部署清单中指定的文件版本信息来决定是否更新应用程序的文件。 开始更新后，ClickOnce 使用称为 " *文件修补* " 的技术，以避免应用程序文件的多余下载。

## <a name="file-patching"></a>文件修补
 更新应用程序时，ClickOnce 不会下载新版本的应用程序的所有文件，除非这些文件已更改。 相反，它会将当前应用程序的应用程序清单中指定的文件的哈希签名与新版本的清单中的签名进行比较。 如果文件的签名不同，则 ClickOnce 会下载新版本。 如果签名匹配，则文件未从一个版本更改为下一个版本。 在这种情况下，ClickOnce 将复制现有文件，并在新版本的应用程序中使用它。 此方法可防止 ClickOnce 再次下载整个应用程序，即使只有一个或两个文件发生了更改。

 文件修补还适用于按需使用和方法下载的程序 <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroup%2A> 集 <xref:System.Deployment.Application.ApplicationDeployment.DownloadFileGroupAsync%2A> 。

 如果你使用 Visual Studio 编译你的应用程序，则在你重新生成整个项目时，它将为所有文件生成新的哈希签名。 在这种情况下，所有程序集都将被下载到客户端，但只有几个程序集可能已更改。

 文件修补不适用于标记为数据并存储在数据目录中的文件。 无论文件的哈希签名如何，都将始终下载这些文件。 有关数据目录的详细信息，请参阅 [在 ClickOnce 应用程序中访问本地数据和远程数据](../deployment/accessing-local-and-remote-data-in-clickonce-applications.md)。

## <a name="see-also"></a>请参阅
- [选择 ClickOnce 更新策略](../deployment/choosing-a-clickonce-update-strategy.md)
- [选择 ClickOnce 部署策略](../deployment/choosing-a-clickonce-deployment-strategy.md)