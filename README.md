<h1>Challenge 2  ALURA-LATAM </h1>
<h2>          
Telecom X
  
Elaborado por: Mario Fco. Monzón 
</h2>

---

## Introducción

<p>La empresa Telecom X enfrenta una alta tasa de cancelaciones y necesita comprender los factores que llevan a la pérdida de clientes. 

Esta evasión de clientes representa un problema relevante para el negocio, ya que impacta directamente en la estabilidad y en los ingresos. A través del análisis de datos, se busca generar información que sirva como base para futuras estrategias de retención y modelos predictivos.

El objetivo principal, utilizando Python y sus principales bibliotecas para extraer información, se centra en analizar el fenómeno de Evasión de Clientes **(churn)** en Telecom X, con el objetivo de identificar patrones y factores asociados a la cancelación del servicio.
</p>

---

<h2>Entorno de desarrollo</h2>
<p>Google Colab.</p>


---

##  Tecnología utilizada y Librerías
El proyecto fue desarrollado íntegramente en **Python**, utilizando las siguientes librerías especializadas para cada etapa del proceso:

* **`requests`**: Extracción de datos. Se utilizó para conectar con la API fuente y descargar la información cruda en formato JSON.
* **`pandas`**: Núcleo del análisis. Utilizada para la normalización del JSON (aplanamiento de diccionarios), limpieza de datos nulos, transformación de tipos de variables y manipulación tabular (DataFrames).
* **`numpy`**: Soporte matemático. Implementada para el manejo eficiente de valores numéricos y tratamiento de vectores.
* **`matplotlib.pyplot`**: Visualización base. Utilizada para la configuración de lienzos (`figure`, `subplots`) y personalización fina de los gráficos.
* **`seaborn`**: Visualización estadística. Empleada para generar gráficos avanzados (Countplots, Boxplots) que permitieron identificar patrones complejos y correlaciones visuales de manera estética y clara.

---

<h2>Notebook de análisis</h2>
<p>El notebook con los análisis de los datos se encuentras en el archivo: TelecomX_LATAM.ipynb</p>

---

## Objetivos del análisis

- Analizar la distribución del churn entre los clientes.
- Identificar variables categóricas asociadas a la evasión.
- Comparar variables numéricas entre clientes que cancelan y los que no.
- Explorar relaciones entre variables mediante análisis de correlación.
- Generar informe final para la toma de decisiones.

---


## Lo que se pondrá en práctica:
1. Importación y manipulación de datos desde una API de manera eficiente.
2. Aplicar los conceptos de ETL (Extracción, Transformación y Carga) en la preparación de los datos.
3. Crear visualizaciones estratégicas para identificar patrones y tendencias.
4. Realizar un Análisis Exploratorio de Datos (EDA) y generar un informe final con recomendaciones.

---


##  Metodología del Proyecto

### 1. Extracción y Transformación (ETL)
* **Normalización:** Se procesó un archivo JSON anidado proveniente de una API, reestructurando diccionarios complejos para obtener un dataset tabular limpio de **7,032 registros** y **21 columnas**.
* **Limpieza:** Se identificaron y eliminaron registros con valores vacíos en variables críticas (`Churn`, `TotalCharges`) y se estandarizaron los tipos de datos (conversión de `Object` a `Float` en cargos mensuales).

### 2. Análisis Exploratorio de Datos (EDA)
Se realizaron análisis univariados y bivariados para detectar "puntos de dolor" en la experiencia del cliente:
* **Análisis Categórico:** Evaluación de fugas por tipo de contrato, método de pago y servicios contratados.
* **Análisis Numérico:** Estudio de distribuciones de cargos mensuales, totales y antigüedad (*Tenure*) mediante Boxplots.

---

##  Principales Hallazgos (Insights)

El análisis reveló patrones claros que explican la fuga de clientes:

1.  **Vulnerabilidad Contractual:** Los clientes con contratos **"Mes a Mes"** presentan una tasa de abandono drásticamente superior a los de contratos anuales (fidelidad >90%).
2.  **Método de en Pago:** El método de pago **"Electronic Check"** es un factor crítico de riesgo; los usuarios que lo utilizan tienen una probabilidad de fuga significativamente mayor que aquellos con pagos automatizados.
3.  **Desempeño del servicio:** Los usuarios de **Fibra Óptica** (servicio de mayor costo) muestran mayores índices de cancelación que los de DSL, sugiriendo una insatisfacción con la relación calidad-precio.

---

##  Conclusiones y Recomendaciones
________________________________________
Conclusiones e Insights
________________________________________
-	El abandono de clientes se concentra principalmente en los primeros meses de permanencia.
-	La tasa de evasión general es del 26.6%, lo cual es un porcentaje bastante crítico.
-	La antigüedad del cliente (tenure) mantiene una relación inversa con la evasión. Los clientes que abandonan el servicio tienden a concentrarse en los primeros meses, mientras que aquellos con mayor permanencia presentan una probabilidad significativamente menor de churn
-	Las cancelaciones se concentran en el servicio de Internet por fibra óptica, en aquellos contratos que son mensuales. Puede ser que los clientes prueban el servicio de Internet por 1 mes y posteriormente cancelan el servicio.
-	Los medios de pago no automáticos están asociados a una mayor probabilidad de evasión.
-	El churn no se distribuye de manera uniforme, sino que se concentra en perfiles específicos: clientes recientes, con contratos mensuales y mayores cargos.
-	Los clientes que no usan los servicios de seguridad_online, backup_online y protección_dispositivo, presentan un alto registro de cancelaciones
-	Desde el punto de vista económico, los clientes que cancelan suelen registrar cargos mensuales y diarios más elevados, lo que indica que el costo del servicio puede influir en la decisión de abandono. Este patrón se observa tanto en los análisis gráficos como en el análisis de correlación
 
________________________________________
Recomendaciones
________________________________________

1)  A los clientes con contratos mensuales, tratar de incentivarlos para que cambien de contrato mensual hacia contratos de mayor duración mediante incentivos tempranos.

2)  Mejorar la percepción del servicio de fibra óptica a través de mejoras técnicas o campañas de satisfacción.

3)  Promover más los métodos de pago automáticos.  Incentivar el cambio de usuarios de "Electronic Check" hacia débitos automáticos,

4)  Hacer un estudio o una evaluación para tratar de rebajar más las tarifas.

5)  Implementar estrategias de retención enfocadas en clientes con baja antigüedad, haciendo énfasis a los primeros meses de relación con la empresa.
6)  Mejorar condiciones comerciales para nuevos clientes que opten por servicios anuales o bianuales, y así asegurar su permanencia.
7)  Desarrollar un modelo predictivo del parámetro ‘churn’.
