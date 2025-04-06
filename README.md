# Instrucciones

Resuelve los siguientes ejercicios en Python y responde a los planteamientos indicados en cada uno. Incluye en tu reporte las salidas de tus programas, y una **conclusión breve** para esta actividad sobre la efectividad de los métodos probados.

---

## Ejercicio 1 (25 puntos)

1. Carga la base de datos **Iris** y grafica las observaciones incluídas en este conjunto de datos utilizando pares de variables predictoras. Representa la clase de cada observación con un color distinto.
2. **Preguntas**:
   - ¿Qué representan las variables incluidas en la base de datos?
   - ¿Consideras que las variables predictoras tienen información suficiente para determinar la clase de cada uno de los tipos de datos?
3. Entrena un clasificador **SVM lineal** con todos los datos.
   - Asegúrate de usar el parámetro `kernel='linear'`.
4. Inventa **10 nuevas observaciones**, y verifica el resultado obtenido al evaluar el clasificador con estos nuevos datos.
5. Evalúa el modelo de clasificación con **k-fold cross validation** (k = 10).
   - Calcula:
     - **Exactitud** del clasificador (accuracy),
     - **Precisión** y
     - **Recall** para cada clase.
   - Puedes utilizar la **matriz de confusión** calculada con `sklearn`.

---

## Ejercicio 2 (25 puntos)

1. Carga la base de datos **Wine** y muestra las variables predictoras de este conjunto de datos.
2. **Preguntas**:
   - ¿Cuántas variables y observaciones por clase hay en este conjunto de datos?
   - ¿Qué representan los predictores?
3. Calcula la exactitud de los siguientes modelos de clasificación con **k-fold cross validation (k = 5)** para la base de datos Wine:
   - **SVM lineal** (`kernel='linear'`)
   - **SVM con base radial** (`kernel='rbf'`)
   - **k-NN** (para `k = 3`)
   - **Árbol de decisión**
   - Cualquier otro clasificador que esté implementado en `sklearn`
4. Indica **con qué clasificador se obtuvieron los mejores resultados**.

---

## Ejercicio 3 (25 puntos)

Con este **conjunto de datos misteriosos** (con tres clases):

1. Encuentra el mejor valor del parámetro `k` del clasificador **k-NN** utilizando validación cruzada. Para ello:
   - Grafica el rendimiento obtenido con validación cruzada para diferentes valores del parámetro `k`. Se recomienda: `k = 1, 2, 3, ..., 40`.
   - Selecciona el **mejor valor de k** con los resultados del punto anterior.
   - Evalúa con **validación cruzada anidada** el rendimiento del modelo incluyendo **selección de hiperparámetros**.

2. Repite lo anterior, pero para un clasificador **SVM lineal** usando diferentes valores del factor de regularización:  
   `C = 0.000001, 0.000002, 0.000003, ..., 0.0001`

3. Repite el punto 1, pero con un clasificador **SVM de base radial**, para diferentes valores del parámetro del kernel:  
   `gamma = 0.000001, 0.000002, 0.000003, ..., 0.0002`

> 📌 En el archivo de datos de este ejercicio, la **primera columna corresponde a la etiqueta o clase (1, 2 o 3)**, y el resto de las columnas son variables o predictores.

---

## Problema 4 (25 puntos)

Con otro **conjunto de datos misteriosos** (con 4 clases):

1. Seleccionen un modelo de clasificación **(que no sea SVM)** y utilicen el método **filter** para reducir el número de características. Prueben limitando el número de características a:  
   `10, 20, 30, 40, ..., 100`

2. Utilicen el método de **selección de características secuencial (Wrapper)** para reducir el número de características. Prueben con los siguientes límites:  
   `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`

3. Utilicen el método de **selección de características recursivo (Filter-Wrapper)** para reducir el número de características. Prueben con los siguientes límites:  
   `1, 2, 3, 4, 5, 6, 7, 8, 9, 10`

---

### Preguntas finales:

- ¿Qué método les permitió obtener un menor número de características?
- ¿Cuál método consideras que es más rápido para encontrar una solución?
