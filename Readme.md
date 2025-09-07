# Excel ZIP Sorter

Este script organiza automáticamente un archivo `.zip` que contiene múltiples archivos de Excel.  
El resultado final es un nuevo `.zip` con todos los Excel **ordenados, renombrados y procesados**.

---

## ¿Qué hace el script?

1. **Descomprime** un archivo ZIP que contiene hojas de cálculo Excel.
2. **Procesa cada archivo Excel**:
   - Elimina la primera fila (generalmente títulos o encabezados).
   - Ordena el contenido alfabéticamente según la primera columna.
   - Renombra el archivo eliminando el prefijo `resultados_`.
3. **Ordena los archivos** según el número presente en el nombre (ejemplo: `3.xlsx` va antes de `10.xlsx`).
4. **Genera un nuevo ZIP** con todos los archivos ya organizados.

---
