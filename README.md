# 📉 Análisis de Cancelación de Clientes

Este proyecto tiene como objetivo analizar los factores que más influyen en la **cancelación de clientes** utilizando modelos de Machine Learning. A partir de un conjunto de datos simulados con variables demográficas, de comportamiento y de transacción, se evaluaron varios algoritmos y se identificaron las variables clave asociadas a la cancelación.

## 📁 Estructura del Proyecto

analisis_cancelacion_clientes/
│
├── informe.md # Informe detallado con análisis y conclusiones
├── resultados_modelos.ipynb # Notebook con el desarrollo del análisis
├── graficos/ # Imágenes de métricas y visualizaciones
├── data/ # Dataset utilizado (opcional)
└── README.md # Este archivo



---

## 🧪 Modelos Evaluados

Se entrenaron y compararon múltiples modelos supervisados para clasificar si un cliente cancela o no su contrato:

| Modelo                 | Accuracy | Precision (Clase 1) | Recall (Clase 1) | F1-Score (Clase 1) |
|------------------------|----------|----------------------|------------------|--------------------|
| Regresión Logística    | 0.82     | 0.50                 | 0.10             | 0.17               |
| Random Forest          | 0.68     | 0.18                 | 0.18             | 0.18               |

📌 *Nota:* Aunque la Regresión Logística tiene mayor accuracy, ambos modelos presentan un bajo desempeño en la clase "cancelado" (1), lo cual sugiere un problema de **desbalance de clases**.

---

## 📊 Visualizaciones

### Matriz de Confusión - Regresión Logística
![Matriz Modelo 1](graficos/matriz_confusion_modelo1.png)

### Matriz de Confusión - Random Forest
![Matriz Modelo 2](graficos/matriz_confusion_modelo2.png)

### Importancia de Variables - Random Forest
![Importancia Variables](graficos/importancia_variables.png)

---

## 🔍 Variables Más Relevantes

### Regresión Logística
| Variable                              | Impacto |
|---------------------------------------|---------|
| Lugar de Compra_Medellín              | 0.15    |
| Producto: Electrodomésticos           | 0.12    |
| Gasto_Total_log (negativo)            | -0.12   |
| Método de pago: Tarjeta de crédito    | 0.11    |
| Calificación                          | 0.09    |

### Random Forest
| Variable              | Importancia |
|-----------------------|-------------|
| Costo_log             | 0.197       |
| Precio                | 0.181       |
| Gasto_Total_log       | 0.134       |
| Gasto_total           | 0.129       |
| Calificación          | 0.053       |

---

## 📌 Conclusiones

- El **Gasto total** y el **costo del producto** son los factores más relevantes para predecir cancelación.
- Las ciudades de compra también influyen, especialmente **Medellín** y **Bogotá**.
- Métodos de pago como **tarjeta de crédito** y plataformas digitales (Nequi) presentan patrones distintos de comportamiento.

---

## 🧩 Recomendaciones de Retención

- 💳 **Incentivar el uso de métodos de pago asociados a baja cancelación** mediante promociones.
- 💡 **Segmentar campañas por ciudad**, enfocando esfuerzos en ciudades con mayor riesgo.
- 📞 Implementar estrategias de fidelización en categorías con mayor índice de cancelación, como **Electrodomésticos** y **Electrónicos**.

---

## 🧠 Herramientas Utilizadas

- Python 3.11
- Scikit-learn
- Matplotlib & Seaborn
- Pandas & NumPy

---

## 👨‍💻 Autor

**Manuel Morales**  
Estudiante de Ingeniería de Sistemas  
GitHub: [@mmoralesos](https://github.com/mmoralesos)

---

