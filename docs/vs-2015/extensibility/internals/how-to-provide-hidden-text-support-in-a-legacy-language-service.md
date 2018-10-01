---
title: 如何： 提供旧版语言服务中的隐藏的文本支持 |Microsoft Docs
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- hidden text, supporting
- editors [Visual Studio SDK], hidden text
- language services, implementing hidden text regions
ms.assetid: 1c1dce9f-bbe2-4fc3-a736-5f78a237f4cc
caps.latest.revision: 22
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: b689bdfff45f12bc85f79b3cba8581e728c89728
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/22/2018
ms.locfileid: "47476856"
---
# <a name="how-to-provide-hidden-text-support-in-a-legacy-language-service"></a>如何： 提供旧版语言服务中的隐藏的文本支持
[!INCLUDE[vs2017banner](../../includes/vs2017banner.md)]

本主题的最新版本，请参阅[如何： 提供旧版语言服务中隐藏的文本支持](https://docs.microsoft.com/visualstudio/extensibility/internals/how-to-provide-hidden-text-support-in-a-legacy-language-service)。  
  
你可以创建大纲区域除了隐藏的文本区域。 隐藏的文本区域可以是客户端控制或编辑器控制和用于完全隐藏的文本区域。 编辑器为水平线条显示隐藏的区域。 出现这种是在 HTML 编辑器中的仅限脚本视图。  
  
## <a name="procedure"></a>过程  
  
#### <a name="to-implement-a-hidden-text-region"></a>若要实现隐藏的文本区域  
  
1.  调用`QueryService`为<xref:Microsoft.VisualStudio.TextManager.Interop.SVsTextManager>。  
  
     这将返回一个指向<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager>。  
  
2.  调用<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.GetHiddenTextSession%2A>、 传入针对给定的文本缓冲区的指针。 这将确定是否隐藏的文本已存在的会话的缓冲区。  
  
3.  如果已存在，则不需要创建一个，一个指向现有<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession>返回对象。 使用此指针来枚举和创建隐藏的文本区域。 否则，调用<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextManager.CreateHiddenTextSession%2A>创建隐藏的文本，会话的缓冲区。  
  
     一个指向<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession>返回对象。  
  
    > [!NOTE]
    >  当您调用`CreateHiddenTextSession`，可以指定一个隐藏的文本，客户端 (即， <xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextClient>)。 隐藏的文本或大纲显示展开或折叠的用户时，隐藏的文本，客户端将通知你。  
  
4.  调用<xref:Microsoft.VisualStudio.TextManager.Interop.IVsHiddenTextSession.AddHiddenRegions%2A>以添加一个或其他新大纲区域时，指定以下信息在`reHidReg`(<xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion>) 参数：  
  
    1.  指定的值`hrtConcealed`中`iType`的成员<xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion>结构，以指示要创建一个隐藏的区域，而不是大纲区域。  
  
        > [!NOTE]
        >  隐藏的区域处于隐藏状态，编辑器将自动显示要指明其状态的隐藏区域周围的线。  
  
    2.  指定区域是否受客户端管理，或以编辑器控制`dwBehavior`的成员<xref:Microsoft.VisualStudio.TextManager.Interop.NewHiddenRegion>结构。 智能的大纲显示实现可以包含多个编辑器和客户端控制大纲和隐藏的文本区域。
