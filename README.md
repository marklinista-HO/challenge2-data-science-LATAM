<h1>Challenge 2  ALURA-LATAM </h1>
<h2>          
Telecom X
  
Elaborado por: Mario Fco. Monzón 
</h2>


## Introducción


<p>La empresa Telecom X enfrenta una alta tasa de cancelaciones y necesita comprender los factores que llevan a la pérdida de clientes. El desafío es recopilar, procesar y analizar los datos, utilizando Python y sus principales bibliotecas para extraer información.</p>

La evasión de clientes representa un problema relevante para el negocio, ya que impacta directamente en la estabilidad y los ingresos. A través del análisis de datos, se busca generar información que sirva como base para futuras estrategias de retención y modelos predictivos.

El objetivo principal se centra en analizar el fenómeno de Evasión de Clientes **(churn)** en Telecom X, con el objetivo de identificar patrones y factores asociados a la cancelación del servicio.


<br>
<h2>Entorno de desarrollo</h2>
<p>Google Colab.</p>
<br>

---

##  Tecnología utilizada y Librerías
El proyecto fue desarrollado íntegramente en **Python**, utilizando las siguientes librerías especializadas para cada etapa del proceso:

* **`requests`**: Extracción de datos. Se utilizó para conectar con la API fuente y descargar la información cruda en formato JSON.
* **`pandas`**: Núcleo del análisis. Utilizada para la normalización del JSON (aplanamiento de diccionarios), limpieza de datos nulos, transformación de tipos de variables y manipulación tabular (DataFrames).
* **`numpy`**: Soporte matemático. Implementada para el manejo eficiente de valores numéricos y tratamiento de vectores.
* **`matplotlib.pyplot`**: Visualización base. Utilizada para la configuración de lienzos (`figure`, `subplots`) y personalización fina de los gráficos.
* **`seaborn`**: Visualización estadística. Empleada para generar gráficos avanzados (Countplots, Boxplots) que permitieron identificar patrones complejos y correlaciones visuales de manera estética y clara.

---

<br>
<h2>Notebook de análisis</h2>
<p>El notebook con los análisis de los datos se encuentras en el archivo: TelecomX_LATAM.ipynb</p>
<br>


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
* **Ingeniería de Características:** Binarización de variables categóricas clave para facilitar el análisis estadístico.

### 2. Análisis Exploratorio de Datos (EDA)
Se realizaron análisis univariados y bivariados para detectar "puntos de dolor" en la experiencia del cliente:
* **Análisis Categórico:** Evaluación de fugas por tipo de contrato, método de pago y servicios contratados.
* **Análisis Numérico:** Estudio de distribuciones de cargos mensuales, totales y antigüedad (*Tenure*) mediante Boxplots.

---

##  Principales Hallazgos (Insights)

El análisis reveló patrones claros que explican la fuga de clientes:

1.  **Vulnerabilidad Contractual:** Los clientes con contratos **"Mes a Mes"** presentan una tasa de abandono drásticamente superior a los de contratos anuales (fidelidad >90%).
2.  **Fricción en Pagos:** El método de pago **"Electronic Check"** es un factor crítico de riesgo; los usuarios que lo utilizan tienen una probabilidad de fuga significativamente mayor que aquellos con pagos automatizados.
3.  **Problema en el Segmento Premium:** Los usuarios de **Fibra Óptica** (servicio de mayor costo) muestran mayores índices de cancelación que los de DSL, sugiriendo una insatisfacción con la relación calidad-precio.
4.  **Curva de Permanencia:** El riesgo de pérdida es crítico durante los primeros **12 meses**. Superado el primer año, la fidelidad del cliente se estabiliza.

---

##  Conclusiones y Recomendaciones
Para mitigar la tasa de Churn, se sugieren las siguientes estrategias basadas en datos:
* Implementar un programa de **Onboarding y Fidelización** agresivo durante el primer año de vida del cliente.
* Incentivar la migración de pagos manuales a **Débito Automático** mediante descuentos porcentuales.
* Revisar la competitividad y calidad técnica del servicio de **Fibra Óptica**.
* Promover contratos de largo plazo (1-2 años) ofreciendo beneficios exclusivos para reducir la volatilidad del segmento "Mes a Mes".

---



##  Autor
 *Junior Software Developer & Data Analyst* ```










