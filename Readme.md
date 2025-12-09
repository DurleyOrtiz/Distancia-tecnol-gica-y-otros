# 📂 Repositorio de  Perfiles Tecnológicos

Este repositorio se hizo con el propósito de que futuros ingenieros que quieran abordar este tema puedan guiarse de los códigos aquí presentados.  
Cada script resuelve una parte del flujo de trabajo relacionado con la **organización, procesamiento y comparación de archivos Excel** que contienen información tecnológica.  

---

## Códigos incluidos

### 1) `excel_zip_sorter.py`
Organiza un archivo `.zip` que contiene múltiples Excel.  
- Descomprime los archivos.  
- Elimina la primera fila de cada Excel y ordena la primera columna alfabéticamente.  
- Renombra quitando el prefijo `resultados_`.  
- Ordena los archivos por número y genera un nuevo ZIP con los resultados.  

---

### 2) `comparar_prefijos.py`
Compara dos conjuntos de perfiles almacenados en ZIP.  
- Extrae los archivos Excel de cada ZIP.  
- Identifica los archivos por índice (ej. `23_2002_Univ.xls`).  
- Lee la columna **G** y extrae los prefijos tecnológicos.  
- Genera comparaciones `comparacion_i.xlsx` mostrando los conteos de prefijos en ambos perfiles.  
- Empaqueta todos los resultados en un ZIP.  

---

### 3) `calcular_detech.py`
Calcula la métrica **DeTech_ij** (distancia tecnológica) a partir de las comparaciones generadas.  
- Recorre los `comparacion_*.xlsx`.  
- Calcula `DeTech_ij = 1 - cos(Xi, Xj)` usando los vectores de frecuencias.  
- Inserta los resultados en una hoja `"DeTech"` dentro de cada Excel.  
- Genera un archivo resumen `detech_resumen.xlsx` con todas las métricas consolidadas.  

---

## Futuras adiciones
Este repositorio está en crecimiento.  
Aquí se irán agregando nuevos códigos relacionados con:  
- Procesamiento automatizado de datos tecnológicos.  
- Nuevas métricas de comparación.  
- Visualizaciones y reportes avanzados.  

---

## ⚙️ Dependencias generales
Los scripts usan principalmente:  
- `pandas`  
- `numpy`  
- `openpyxl`  
- `xlrd`  
- Librerías estándar de Python (`os`, `re`, `glob`, `zipfile`, `shutil`, `math`)  
