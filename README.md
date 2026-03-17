# ⚽ Football Data Science: Player Role & Similarity Analysis

Este proyecto utiliza el dataset **'2022-2023 Football Player Stats'** (Top 5 ligas europeas) para explorar el rendimiento de futbolistas profesionales mediante técnicas avanzadas de **Data Science**. El objetivo es doble: validar roles tácticos y desarrollar una herramienta de búsqueda de "clones" para scouting estratégico.

## 🚀 Descripción del Proyecto

El análisis se centra en transformar más de 120 variables de rendimiento (goles, pases progresivos, acciones defensivas, etc.) en conocimiento accionable. A diferencia de un análisis convencional, este trabajo implementa dos paradigmas de Machine Learning para abordar el fútbol desde una perspectiva de **360 grados**.

## 🧠 Arquitectura de Modelado y Utilidad Práctica

El núcleo del proyecto reside en el uso de dos enfoques complementarios que resuelven necesidades reales en un departamento de análisis deportivo:

### 1. Clasificación Táctica (Random Forest Classifier)
* **Enfoque**: Aprendizaje Supervisado.
* **Utilidad**: Este modelo permite la **Validación de Roles**. El algoritmo aprende las fronteras estadísticas que separan a las posiciones (DF, MF, FW).
* **Aplicación Real**: 
    * Identificar jugadores "polifuncionales" que rinden estadísticamente en una posición distinta a la nominal.
    * Automatizar la categorización de futbolistas en grandes bases de datos.
* **Métrica Clave**: Evaluación mediante **Matriz de Confusión**, identificando los solapamientos naturales entre mediocampistas creativos y atacantes.

### 2. Buscador de "Clones" (K-Nearest Neighbors)
* **Enfoque**: Aprendizaje No Supervisado (Basado en distancias).
* **Utilidad**: Este modelo permite el **Scouting de Precisión**. En lugar de clasificar, mide la distancia matemática entre "vectores de ADN futbolístico". 
* **Aplicación Real**:
    * **Sustitución de Bajas**: Encontrar un reemplazo para un jugador clave basándose exclusivamente en su perfil de juego y no en su fama o valor de mercado.
    * **Detección de "Joyas Ocultas"**: Identificar jugadores en ligas menos competitivas con firmas estadísticas similares a estrellas de élite (ej. encontrar perfiles similares a Lionel Messi o Kevin De Bruyne).
* **Métrica Clave**: Análisis de **Distancia Euclidiana** en un espacio de 12 dimensiones normalizadas.

## 📊 Variables Determinantes (Feature Importance)

El éxito de la predicción radica en las variables que "mueven la aguja" en el fútbol moderno. Tras el análisis, se determinó que las más relevantes son:
1.  **Pases Progresivos (PasProg)**: La métrica reina para distinguir a los organizadores de juego.
2.  **Toques en Área Rival (TouAttPen)**: El predictor más fuerte para identificar la peligrosidad ofensiva.
3.  **Despejes e Intercepciones (Clr/Int)**: La base estadística de la solidez defensiva.

## 🛠️ Stack Tecnológico

* **Lenguaje**: Python 3.x
* **Entorno**: Google Colab
* **Librerías Clave**: 
    * `Pandas` & `NumPy`: Manipulación de datos y limpieza.
    * `Scikit-Learn`: Implementación de modelos (RandomForest, KNN, StandardScaler).
    * `Seaborn` & `Matplotlib`: Visualización de datos estadísticos y matrices de confusión.

## 📈 Resultados y Hallazgos

* El modelo de clasificación demostró que el comportamiento estadístico es un reflejo fiel de la posición nominal.
* El modelo de similitud fue capaz de agrupar a jugadores de élite (como Messi y Neymar) basándose en su alta capacidad de creación y progresión de balón, superando la limitación de las etiquetas fijas.

---
Proyecto desarrollado por **Valentín Cueva Buono** y **Leandro Oficialdegui** como Trabajo Práctico Final de Data Science.
