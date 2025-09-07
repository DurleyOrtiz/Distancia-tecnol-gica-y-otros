# Comparación de Perfiles con Prefijos Tecnológicos (DeTech)

Este proyecto procesa y compara archivos Excel provenientes de dos conjuntos de datos (perfil_1.zip y perfil_2.zip), 
con el objetivo de medir la similitud tecnológica entre ambos.

---

##  Flujo del código

1. **Montaje y extracción**
   - Monta Google Drive en Colab.
   - Extrae los ZIP `Perfil_1.zip` y `perfil_2.zip` en carpetas temporales.

2. **Procesamiento de archivos**
   - Identifica los Excel cuyo nombre comienza con un índice (ej. `123_2002_Univ.xls`).
   - Lee la columna **G** de cada archivo, que contiene códigos tecnológicos.
   - Extrae los **prefijos tecnológicos** (ej. `"C12"`, `"A61"`).
   - Cuenta la frecuencia de cada prefijo en cada archivo.

3. **Generación de comparaciones**
   - Para cada índice `1..348`, compara los archivos de `perfil_1` y `perfil_2`.
   - Produce un archivo `comparacion_i.xlsx` con el conteo de prefijos lado a lado.

4. **Empaquetado**
   - Todos los `comparacion_*.xlsx` se comprimen en `comparaciones.zip`.

5. **Cálculo de DeTech**
   - Calcula la distancia tecnológica `DeTech_ij = 1 - cos(Xi, Xj)` entre los vectores de prefijos.
   - Añade los resultados en una hoja `"DeTech"` dentro de cada Excel de comparación.
   - Genera un archivo maestro `detech_resumen.xlsx` con todos los índices y sus métricas.

---
