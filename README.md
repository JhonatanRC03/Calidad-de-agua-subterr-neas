# 💧 **AGUAS SUBTERRANEAS - LAMBAYEQUE** 💧
El estudio proporciona un enfoque efectivo usando Machine Learning para la evaluación de la calidad del agua subterránea, con implicaciones significativas para la gestión y conservación de este recurso vital en Lambayeque.
## <font color='orange'>🟠 **Problema de Negocio: Gestión Sostenible de Cuencas y Pozos Acuíferos en Lambayeque** </font>
Para el departamento de Lambayeque en gran crecimiento que depende en gran medida de las aguas subterráneas para satisfacer las necesidades de agua potable. Sin embargo, debido al aumento de la población y la expansión urbana, la sobreexplotación de los recursos hídricos subterráneos se ha convertido en un problema crítico. Esto ha llevado a la disminución del nivel freático, la intrusión salina en acuíferos y la degradación de la calidad del agua.

## <font color='orange'>🟠 **Datos** </font>

El desafío radica en encontrar soluciones para garantizar una gestión sostenible de las aguas subterráneas, equilibrando la demanda creciente con la necesidad de conservar y proteger este recurso vital.
 **Los datos están en formato xlsx en donde cada línea representa un atributo:**
  - `CLAVE`: Identificador único para una ubicación o muestra específica.
  - `SITIO`: Indica el lugar donde se recogió la muestra.
  - `ORGANISMO_DE_CUENCA`: Se refiere a la organización de la cuenca asociada al sitio.
  - `ESTADO`: Indica el estado en el que se encuentra el sitio.
  - `MUNICIPIO`: Especifica el municipio de la ubicación del sitio.
  - `ACUIFERO`: Se refiere al acuífero asociado o cercano al sitio.
  - `SUBTIPO`: Proporciona información adicional de clasificación o subtipo sobre el tipo de agua subterranea donde se recogio la muestra.
  - `LONGITUD/LATITUD`: Coordenadas geográficas que especifican la ubicación exacta del sitio/muestra.
  - `PH`: Mide la acidez/alcalinidad del agua en una escala de 0-14, donde 7 es neutro, <7 ácido, >7 alcalino.
  - `Hardness`: Se mide en miligramos por litro (mg/L), que indica la concentración de iones de calcio y magnesio en el agua.
  - `Solids`: Se mide en miligramos por litro (mg/L) y representa la cantidad total de partículas disueltas en el agua, incluyendo minerales, sales, metales, etc.
  - `Sulfate`: Se mide en miligramos por litro (mg/L) es un anión común en el agua que puede influir en su sabor y puede tener efectos adversos en la salud humana en concentraciones elevadas.
  - `Conductivity`: Se mide en microsiemens por centímetro (µS/cm) y representa la capacidad del agua para conducir la corriente eléctrica.
  - `Organic_carbon`: Se mide en miligramos por litro (mg/L) y refleja la cantidad de carbono orgánico presente en el agua.
  - `Trihalomethanes`: Se mide en microgramos por litro (µg/L) y representa la concentración de trihalometanos en el agua.
  - `Turbidity`: Mide la turbidez o claridad del agua en unidades de nefelometría turbia (NTU).
  - `Potability`: Indica si el agua es potable o no (1: potable, 0: no potable).

Los datos que te ha enviado la compañía están en el archivo `Aguas-Subterraneas.xlsx`.

## <font color='orange'>🟠 **Agrupando Métricas - Comparando los modelos** </font>

![image](https://github.com/JhonatanRC03/Calidad-de-agua-subterrneas/assets/132719375/c1d9a555-186c-46bd-9897-f36c0ab153d8)


Gráfico de Barras:
![image](https://github.com/JhonatanRC03/Calidad-de-agua-subterrneas/assets/132719375/a6317805-50d2-44da-9377-30b00e927acf)


## <font color='orange'>🟠 **Optimizando nuestro modelo con Hiperparámetros (LightGBM)** </font> <font color='orange'>
![image](https://github.com/JhonatanRC03/Calidad-de-agua-subterrneas/assets/132719375/7329abc7-af9a-47b2-a5c1-ea54b818b145)
Curva ROC:
![image](https://github.com/JhonatanRC03/Calidad-de-agua-subterrneas/assets/132719375/510326b9-fb6f-4f31-a7db-00999abd252c)


## <font color='orange'>🟠 **Conclusión** </font> <font color='orange'>

**Después de optimizar los modelos usando Grid Search nos quedamos con el modelo LightGBM**

**Se logró mejorar la métrica AUC-ROC a 85.33%, lo que indica un buen rendimiento del modelo en términos de discriminación entre clases. Esta métrica es especialmente útil para evaluar modelos en problemas de clasificación binaria como la calidad del agua subterránea, donde es crucial identificar correctamente las muestras positivas (agua de calidad inaceptable).**

**La métrica AUC-ROC se basa en la tasa de verdaderos positivos (recall) y la tasa de falsos positivos. En este caso, un valor de 0.851 sugiere que el modelo es capaz de clasificar correctamente el 85.33% de los casos positivos (agua de buena calidad). Esto indica una buena capacidad del modelo para distinguir entre las dos clases.**

**Además, se seleccionó el modelo LGBMClassifier como el mejor para predecir la calidad del agua subterránea, lo que sugiere que este algoritmo es efectivo en este contexto. Esto podría atribuirse a su capacidad para manejar grandes conjuntos de datos y su eficiencia en términos de tiempo de procesamiento.**

**En conclusión, con un modelo optimizado y una métrica AUC-ROC mejorada, se puede confiar en las predicciones del modelo LGBMClassifier para identificar la calidad del agua subterránea de manera efectiva, lo que puede ser fundamental para la toma de decisiones en la gestión y conservación de los recursos hídricos.**




