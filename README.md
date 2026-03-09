# Telecom-X---Parte-2

## Propósito del Proyecto
El objetivo principal de este análisis es predecir la cancelación de clientes (Churn) utilizando técnicas de Machine Learning. Se busca identificar los factores críticos que influyen en la fuga de usuarios para proponer estrategias de retención basadas en datos.

## Estructura del Proyecto
- `Cuaderno Principal`: Contiene el flujo completo desde la carga de datos hasta la evaluación de modelos.
- `datos_tratados.cvs`: Conjunto de datos procesado utilizado para el entrenamiento.
- `Visualizaciones`: Gráficos generados (Boxplots, Heatmaps, Scatter plots) integrados en el cuaderno.

## Preparación de los Datos
1.  **Clasificación de Variables**: Identificación de variables numéricas (cargos) y categóricas (contratos, métodos de pago).
2.  **Codificación (Encoding)**: Aplicación de One-Hot Encoding a variables categóricas para compatibilidad con algoritmos.
3.  **Normalización**: Escalado de variables numéricas continuas mediante `StandardScaler` para modelos lineales.
4.  **División de Datos**: Separación en conjuntos de Entrenamiento (80%) y Prueba (20%) con estratificación para mantener el balance de clases.

## Modelización y Justificación
- **Regresión Logística**: Elegida por su interpretabilidad y buen desempeño en problemas binarios (80% Accuracy).
- **Random Forest**: Utilizado para capturar relaciones no lineales y evaluar importancia de características mediante impureza de Gini.

## Insights del EDA
- Los clientes con contratos **mes a mes** tienen una tasa de cancelación del 41.3%, comparado con solo el 2.7% en contratos de dos años.
- Cargos mensuales altos correlacionan con una mayor probabilidad de abandono, especialmente en clientes nuevos.

## Instrucciones de Ejecución
1. Asegúrate de tener instalado: `pandas`, `scikit-learn`, `matplotlib`, `seaborn`.
2. Carga el archivo `datos_tratados.cvs` en el directorio `/content/`.
3. Ejecuta las celdas en orden secuencial.
"""

with open('README.md', 'w') as f:
    f.write(readme_content)

print("Archivo README.md generado exitosamente.")
