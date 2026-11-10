# Airline-Ticket-Prediction- ✈️
## 📌 Descripción del proyecto

Este proyecto tiene como objetivo analizar el comportamiento de los precios de boletos de avión en función de diferentes variables, principalmente los días de anticipación a la fecha de salida, la aerolínea, el destino y las características del vuelo.

A través de técnicas de análisis exploratorio de datos, visualización y modelado predictivo, se busca identificar patrones en la variación de los precios y desarrollar modelos capaces de estimar su comportamiento.

El análisis también incorpora una perspectiva social sobre la posible discriminación algorítmica en los sistemas de fijación dinámica de precios de las aerolíneas, explorando cómo estos mecanismos pueden afectar de manera diferenciada a los consumidores.

## 🎯 Objetivos

- Analizar el comportamiento de los precios de boletos de avión según los días de anticipación a la fecha de salida.
- Comparar los precios promedio entre Aeroméxico y VivaAerobus.
- Identificar patrones y relaciones entre las variables del conjunto de datos.
- Implementar y comparar modelos de Machine Learning para la predicción de precios.
- Aplicar una ecuación diferencial logística para modelar el comportamiento de los precios en una ruta específica.
- Explorar las implicaciones sociales de los algoritmos de precios dinámicos.

## 🛠️ Tecnologías y herramientas

| Herramienta | Aplicación |
|---|---|
| Python | Lenguaje principal |
| Pandas | Manipulación y limpieza de datos |
| NumPy | Operaciones numéricas |
| Matplotlib | Visualización de datos |
| Seaborn | Análisis gráfico |
| Scikit-learn | Evaluación y modelado predictivo |
| XGBoost | Modelo de regresión |
| Random Forest | Modelo de regresión |
| SciPy | Ajuste de curvas y modelado logístico |
| Jupyter Notebook | Desarrollo y documentación del análisis |

## 📊 Desarrollo del proyecto

### 1. Limpieza y preparación de datos

Se realizó un proceso de preparación de los conjuntos de datos que incluyó:

- Identificación y eliminación de valores nulos.
- Detección y eliminación de columnas duplicadas.
- Conversión de variables a los tipos de datos correspondientes.
- Transformación de fechas y horarios.
- Estandarización de variables numéricas y categóricas.
- Codificación One-Hot Encoding para variables categóricas.

### 2. Análisis exploratorio y visualización

Se desarrollaron visualizaciones para identificar patrones en los precios de los boletos:

- Precio promedio frente a días de anticipación por destino y aerolínea.
- Comparación de precios promedio entre Aeroméxico y VivaAerobus.
- Identificación de tendencias en los precios según la proximidad de la fecha del vuelo.

### 3. Modelado predictivo con Machine Learning

Se implementaron dos algoritmos de regresión para estimar los precios de los boletos:

**XGBoost Regressor**

Se utilizó para desarrollar modelos de predicción por destino, incorporando variables relacionadas con el horario, la distancia, los días de anticipación, la aerolínea y la ruta.

**Random Forest Regressor**

Se implementó para modelar el comportamiento de los precios por destino y comparar su desempeño predictivo.

La evaluación de los modelos considera las siguientes métricas:

- MAE (Mean Absolute Error).
- RMSE (Root Mean Squared Error).
- R² (Coeficiente de determinación).

También se exploró la importancia de las variables para identificar cuáles tienen mayor influencia dentro de los modelos Random Forest.

### 4. Modelado mediante ecuación logística

Como análisis complementario, se realizó un estudio específico de los precios de vuelos de Aeroméxico con destino a Tuxtla Gutiérrez (TGZ).

Se implementó una función logística para representar la relación entre los días de anticipación y el precio promedio del boleto:

\[
P(t)=\frac{K}{1+Ae^{-rt}}
\]

Donde:

- **K:** precio máximo teórico.
- **r:** tasa de crecimiento.
- **A:** parámetro que determina la forma inicial de la curva.
- **t:** días de anticipación.

Los parámetros fueron estimados mediante `curve_fit` de SciPy.

Se generaron predicciones, comparaciones entre valores reales y estimados, y visualizaciones del comportamiento de la curva logística.

## 📈 Resultados del modelo logístico

De acuerdo con los resultados documentados en el notebook, el modelo logístico obtuvo las siguientes métricas:

| Métrica | Resultado |
|---|---:|
| MAE | 117.49 |
| MSE | 19,894.03 |
| RMSE | 141.05 |
| R² | 0.9256 |
| MAPE | 1.33% |

Estos resultados muestran un ajuste elevado a los datos utilizados para el modelado, con un coeficiente de determinación de 0.9256.

*Nota: estos resultados corresponden al ajuste logístico documentado en el proyecto y no representan una evaluación independiente sobre un conjunto de prueba.*

## 🌎 Análisis e impacto social

Uno de los principales enfoques del proyecto es analizar cómo los sistemas de precios dinámicos pueden generar efectos desiguales entre los consumidores.

Los patrones observados permiten explorar cómo la cercanía de la fecha de salida puede relacionarse con incrementos en los precios de los boletos.

Desde una perspectiva social, esto plantea interrogantes sobre la equidad de los algoritmos de fijación de precios, particularmente para las personas que tienen menor capacidad económica o menos flexibilidad para planificar sus viajes con anticipación.

El proyecto busca mostrar que el análisis de datos y los modelos predictivos también pueden utilizarse para comprender fenómenos económicos y sociales.

## 📂 Estructura del proyecto

```text
ANALISIS-PRECIOS-AEROLINEAS/
│
├── ANALISIS Y MODELADO.ipynb
│
├── data/
│   ├── BasesUnidas.csv
│   └── filtrado_TGZ_Aeromexico.csv
│
└── README.md
```

*Nota: los archivos CSV representan los conjuntos de datos utilizados en el notebook. Deben incorporarse al repositorio o configurarse sus rutas de acceso antes de ejecutar el proyecto.*

## ⚙️ Instalación y ejecución

1. Clonar el repositorio:

```bash
git clone URL_DEL_REPOSITORIO
```

2. Instalar las dependencias:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy jupyter
```

3. Abrir Jupyter Notebook:

```bash
jupyter notebook
```

4. Abrir el archivo `ANALISIS Y MODELADO.ipynb`.

5. Configurar las rutas de acceso a los archivos CSV y ejecutar las celdas en orden.

## 💡 Conclusiones

Este proyecto integra herramientas de análisis de datos y modelado predictivo para estudiar el comportamiento de los precios de boletos de avión.

La combinación de técnicas de Machine Learning y modelado matemático permite explorar diferentes aproximaciones para comprender y estimar la variación de los precios.

Además de su componente técnico, el proyecto incorpora una reflexión sobre las implicaciones sociales de los algoritmos de precios dinámicos y la importancia de considerar sus efectos en distintos sectores de la población.

---

**Categorías:** Data Analysis · Data Science · Machine Learning · Predictive Modeling · Python · Mathematical Modeling
