---
title: Procedimiento Alinear y expandir un Control en un Control TableLayoutPanel
ms.date: 03/30/2017
f1_keywords:
- net.ComponentModel.StyleCollectionEditor.TLP.AlignStretchCtrl
helpviewer_keywords:
- TableLayoutPanel control [Windows Forms], stretching controls
- controls [Windows Forms], stretching
- controls [Windows Forms], aligning
ms.assetid: 7dc1a157-6fee-4995-8ebc-b65bdc0909a8
ms.openlocfilehash: 91464108a6ac4600c14a06b4a7dcea200d7f0254
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54535936"
---
# <a name="how-to-align-and-stretch-a-control-in-a-tablelayoutpanel-control"></a>Procedimiento Alinear y expandir un Control en un Control TableLayoutPanel
Puede alinear y expandir controles en un <xref:System.Windows.Forms.TableLayoutPanel> con el <xref:System.Windows.Forms.Control.Anchor%2A> y <xref:System.Windows.Forms.Control.Dock%2A> propiedades.  
  
> [!NOTE]
>  Los cuadros de diálogo y comandos de menú que se ven pueden diferir de los descritos en la Ayuda, en función de los valores de configuración o de edición activos. Para cambiar la configuración, elija la opción **Importar y exportar configuraciones** del menú **Herramientas** . Para más información, vea [Personalizar el IDE de Visual Studio](/visualstudio/ide/personalizing-the-visual-studio-ide).  
  
### <a name="to-align-and-stretch-a-control"></a>Para alinear y expandir un control  
  
1.  Arrastre un control <xref:System.Windows.Forms.TableLayoutPanel> del **cuadro de herramientas** al formulario.  
  
2.  Arrastre un <xref:System.Windows.Forms.Button> controlar desde la **cuadro de herramientas** en la celda superior izquierda de la <xref:System.Windows.Forms.TableLayoutPanel> control. El <xref:System.Windows.Forms.Button> control está centrado en la celda.  
  
3.  Establezca el valor de la <xref:System.Windows.Forms.Button> del control <xref:System.Windows.Forms.Control.Anchor%2A> propiedad `Left,Right`. El <xref:System.Windows.Forms.Button> control se expande para que coincida con el ancho de la celda.  
  
4.  Establezca el valor de la <xref:System.Windows.Forms.Button> del control <xref:System.Windows.Forms.Control.Anchor%2A> propiedad `Top,Bottom`. El <xref:System.Windows.Forms.Button> control se expande para ajustarse al alto de la celda.  
  
5.  Establezca el valor de la <xref:System.Windows.Forms.Button> del control <xref:System.Windows.Forms.Control.Dock%2A> propiedad <xref:System.Windows.Forms.DockStyle.Fill>. El <xref:System.Windows.Forms.Button> control se expande para rellenar la celda.  
  
6.  Establezca el valor de la <xref:System.Windows.Forms.Button> del control <xref:System.Windows.Forms.Control.Dock%2A> propiedad <xref:System.Windows.Forms.DockStyle.None>. El <xref:System.Windows.Forms.Button> control vuelve a su tamaño original y se mueve a la esquina superior izquierda de la celda. El **Diseñador de Windows Forms** estableció el <xref:System.Windows.Forms.Control.Anchor%2A> propiedad `Top, Left`.  
  
7.  Establezca el valor de la <xref:System.Windows.Forms.Button> del control <xref:System.Windows.Forms.Control.Anchor%2A> propiedad `Bottom,Right`. El <xref:System.Windows.Forms.Button> control se mueve a la esquina inferior derecha de la celda.  
  
8.  Establezca el valor de la <xref:System.Windows.Forms.Button> del control <xref:System.Windows.Forms.Control.Anchor%2A> propiedad <xref:System.Windows.Forms.AnchorStyles.None>. El <xref:System.Windows.Forms.Button> control se desplaza hasta el centro de la celda.  
  
## <a name="see-also"></a>Vea también
- [Control TableLayoutPanel](../../../../docs/framework/winforms/controls/tablelayoutpanel-control-windows-forms.md)
