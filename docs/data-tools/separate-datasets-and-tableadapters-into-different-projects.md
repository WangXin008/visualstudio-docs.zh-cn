---
title: 使用单独的项目错误
description: 了解如何将数据集和 Tableadapter 分隔到不同的项目中，以便你可以快速地分离应用程序层并生成 N 层数据应用程序。
ms.date: 11/04/2016
ms.topic: how-to
ms.custom: SEO-VS-2020
helpviewer_keywords:
- TableAdapters, n-tier applications
- n-tier applications, separating Datasets and TableAdapters
ms.assetid: f66a3940-6227-46af-a930-9177f425f4fd
author: ghogen
ms.author: ghogen
manager: jillfra
ms.workload:
- data-storage
ms.openlocfilehash: f039dc445acd9032a5fe6862e78e5c28ec67bf5d
ms.sourcegitcommit: ed26b6e313b766c4d92764c303954e2385c6693e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/10/2020
ms.locfileid: "94435998"
---
# <a name="separate-datasets-and-tableadapters-into-different-projects"></a>将数据集和 TableAdapter 分离到不同的项目中
已对类型化的数据集进行了增强，以便可以将 [tableadapter](create-and-configure-tableadapters.md) 和 dataset 类生成到单独的项目中。 这使你能够快速分离应用程序层并生成 n 层数据应用程序。

下面的过程介绍使用 **数据集设计器** 将数据集代码生成到与包含生成的 TableAdapter 代码的项目不同的项目中的过程。

## <a name="separate-datasets-and-tableadapters"></a>单独的数据集和 Tableadapter
将数据集代码与 TableAdapter 代码分离时，包含数据集代码的项目必须位于当前解决方案中。 如果此项目不在当前解决方案中，则它将不会出现在 " **属性** " 窗口的 " **数据集项目** " 列表中。

[!INCLUDE[note_settings_general](../data-tools/includes/note_settings_general_md.md)]

#### <a name="to-separate-the-dataset-into-a-different-project"></a>将数据集分隔到不同的项目中

1. 打开包含数据集 ( *.xsd* 文件) 的解决方案。

    > [!NOTE]
    > 如果解决方案不包含要将数据集代码分离到其中的项目，请创建项目，或者将现有项目添加到解决方案中。

2. 双击 **解决方案资源管理器** 中)  ( *.xsd* 文件的类型化数据集，以便在 **数据集设计器** 中打开数据集。

3. 选择 **数据集设计器** 的空白区域。

4. 在 " **属性** " 窗口中，找到 " **数据集项目** " 节点。

5. 在 " **数据集项目** " 列表中，选择要在其中生成数据集代码的项目的名称。

     选择要在其中生成数据集代码的项目后，将使用默认文件名填充 " **数据集文件** " 属性。 如果需要，可以更改此名称。 此外，如果想要将数据集代码生成到特定目录中，则可以将 " **项目文件夹** " 属性设置为文件夹的名称。

    > [!NOTE]
    > 通过将 **数据集项目** 属性)  (分离数据集和 tableadapter 时，项目中的现有部分数据集类将不会自动移动。 必须将现有部分数据集类手动移动到数据集项目。

6. 保存数据集。

     数据集代码生成到 **数据集项目** 属性中的选定项目，并且 **TableAdapter** 代码生成到当前项目中。

默认情况下，在分离数据集和 TableAdapter 代码后，结果是每个项目中的离散类文件。 原始项目包含一个名为 *DatasetName* 的文件 (或包含 TableAdapter 代码的 *DatasetName.Designer.cs* ) 。 **数据集项目** 属性中指定的项目包含一个名为 *DatasetName* 的文件 (或包含数据集代码的 *DatasetName.DataSet.Designer.cs* ) 。

> [!NOTE]
> 若要查看生成的类文件，请选择数据集或 TableAdapter 项目。 然后，在 **解决方案资源管理器** 中，选择 " **显示所有文件** "。

## <a name="see-also"></a>另请参阅

- [N 层数据应用程序概述](../data-tools/n-tier-data-applications-overview.md)
- [演练：创建 N 层数据应用程序](../data-tools/walkthrough-creating-an-n-tier-data-application.md)
- [分层更新](../data-tools/hierarchical-update.md)
- [在 Visual Studio 中访问数据](../data-tools/accessing-data-in-visual-studio.md)
- [ADO.NET](/dotnet/framework/data/adonet/index)
