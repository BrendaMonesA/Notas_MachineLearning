# Notas_MachineLearning
Curso de MICD ML Primavera 2026
---
#  Panorama General — Machine Learning

Actualmente es clave en la ciencia de datos.

##  Aplicaciones

* Reconocimiento óptico
* Filtros de spam

Estos sistemas tienen la capacidad de **aprender patrones** y **automatizar decisiones**.

##  Definición clásica

> Campo de estudio que da a los ordenadores la capacidad de aprender.

---

##  Componentes clave

* **Datos de entrenamiento (E)** → Instancias o muestras
* **Modelo**
* **Tarea (T)**
* **Medida de rendimiento (P)**

El Machine Learning es fundamental en problemas donde **no existen algoritmos explícitos escalables**.

---

##  Tipos de supervisión

### 🔵 Aprendizaje Supervisado

Utiliza datos etiquetados para aprender una función que mapea entradas y salidas.

### 🟢 Aprendizaje No Supervisado

Trabaja con datos sin etiquetas; busca estructuras, patrones o representaciones latentes.

### 🟡 Aprendizaje Auto-supervisado

Genera señales de supervisión a partir de los datos.

### 🟠 Aprendizaje Semi-supervisado

Combina pocos datos etiquetados con grandes volúmenes de datos no etiquetados.

### 🔴 Aprendizaje por Refuerzo

Entrena agentes que aprenden a tomar decisiones mediante interacción con un entorno y recompensas.

---

##  Aprendizaje Supervisado (detalle)

También se conoce como **aprendizaje estadístico**.

### Tareas comunes

* Clasificación de noticias
* Filtro de spam
* Identificación de partículas
* Clasificación de eventos en rayos cósmicos

### Métricas típicas

* Error cuadrático medio (MSE)
* Raíz del error (RMSE)

**Nota:** *Etiqueta* y *Objetivo* suelen usarse como sinónimos.

---

##  Aprendizaje No Supervisado

* Explora la estructura interna de los datos
* Detecta patrones y clusters
* Reducción de dimensionalidad
* Detección de anomalías

---

##  Ejemplo de código

````markdown
```python
from pathlib import Path
import urllib.request

datapath = Path("datasets") / "lifesat"
datapath.mkdir(parents=True, exist_ok=True)

data_root = "https://raw.githubusercontent.com/enrique-varela/ml/main/datasets/lifesat/"

for filename in ("oecd_bli.csv", "gdp_per_capita.csv"):
    file_path = datapath / filename
    if not file_path.is_file():
        print("Downloading", filename)
        url = data_root + filename
        urllib.request.urlretrieve(url, file_path)
    else:
        print(filename, "already exists")
```
````

