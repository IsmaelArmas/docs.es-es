---
title: Esta matriz es fija o está bloqueada temporalmente (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vbrID10
ms.assetid: de6713a6-51d7-4edb-8515-d5fb544e2091
ms.openlocfilehash: f70b984fc493e79d7a83b33236615a3220405786
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54516998"
---
# <a name="this-array-is-fixed-or-temporarily-locked-visual-basic"></a>Esta matriz es fija o está bloqueada temporalmente (Visual Basic)
Este error tiene las siguientes causas posibles:  
  
-   Uso de `ReDim` para cambiar el número de elementos de una matriz de tamaño fijo.  
  
-   Cambiar el tamaño de una matriz dinámica de nivel de módulo, en el que se ha pasado un elemento como un argumento a un procedimiento. Si se pasa un elemento, la matriz está bloqueada para evitar la desasignación de memoria para el parámetro de referencia dentro del procedimiento.  
  
-   Al intentar asignar un valor a un `Variant` variable que contiene una matriz, pero la `Variant` está bloqueada actualmente.  
  
## <a name="to-correct-this-error"></a>Para corregir este error  
  
1.  Convertir la matriz original dinámico en lugar de fija declarándola con `ReDim` (si la matriz se declara dentro de un procedimiento,) o declarando sin especificar el número de elementos (si la matriz se declara en el nivel de módulo.  
  
2.  Determinar si realmente necesita pasar el elemento, ya que es visible dentro de todos los procedimientos en el módulo.  
  
3.  Determinar la causa del bloqueo del `Variant` y soluciónelo.  
  
## <a name="see-also"></a>Vea también
- [Matrices](../../../visual-basic/programming-guide/language-features/arrays/index.md)
