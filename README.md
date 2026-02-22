# Recomendación de Planes Móviles - Megaline 📱

## Descripción del Proyecto
La compañía móvil **Megaline** busca optimizar sus recomendaciones de planes para clientes que aún utilizan planes heredados. El objetivo de este proyecto es desarrollar un modelo de Machine Learning capaz de analizar el comportamiento de los clientes y recomendarles uno de los nuevos planes: **Smart** o **Ultra**.

Se trata de un problema de **clasificación binaria** donde la exactitud (accuracy) mínima requerida es de 0.75.

## Datos
El dataset contiene información sobre el comportamiento mensual de los suscriptores:
- **calls**: Número de llamadas.
- **minutes**: Duración total de llamadas en minutos.
- **messages**: Número de mensajes de texto.
- **mb_used**: Tráfico de internet utilizado en MB.
- **is_ultra**: Plan actual (1 para Ultra, 0 para Smart).

## Metodología
1. **Preprocesamiento**: Carga de datos y verificación de integridad.
2. **Segmentación**: División de datos en conjuntos de Entrenamiento (60%), Validación (20%) y Prueba (20%).
3. **Modelado**: Se probaron y ajustaron tres algoritmos:
   - Árbol de Decisión (Decision Tree)
   - Bosque Aleatorio (Random Forest)
   - Regresión Logística (Logistic Regression)
4. **Evaluación**: Selección del mejor modelo basado en métricas de validación y prueba final.

## Resultados
El modelo seleccionado fue el **Bosque Aleatorio (Random Forest)** con la siguiente configuración:
- `n_estimators`: 50
- `max_depth`: 10

**Métricas Finales:**
- **Exactitud en Prueba:** ~79.9%
- **Prueba de Cordura:** El modelo superó la línea base del 69% (predicción de clase mayoritaria).

## Tecnologías Utilizadas
- Python 3.x
- Pandas
- Scikit-learn
- Jupyter Notebook

## Cómo ejecutar este proyecto
1. Clona el repositorio:
   ```bash
   git clone [https://github.com/joseariasduran/megaline-plan-recommendation.git]
