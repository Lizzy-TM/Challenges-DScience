# **📊 Análisis de TelecomX para la evasión(Churn) de clientes**

**1. Contexto del Proyecto**

Durante este proyecto,analizaremos los datos en Telecom X del proyecto "Churn de Clientes" (Evasión de Clientes). La empresa enfrenta una alta tasa de cancelaciones y necesita comprender los factores que llevan a la pérdida de clientes.
Empezaremos a recopilar, procesar y analizar los datos, utilizando Python y sus principales bibliotecas para extraer información valiosa. A partir de tu análisis, el equipo de Data Science podrá avanzar en modelos predictivos y desarrollar estrategias para reducir la evasión.

**2. Objetivos**

•	Preparar los datos para el modelado (tratamiento, codificación, normalización).

•	Realizar análisis de correlación y selección de variables.

•	Entrenar dos o más modelos de clasificación.

•	Evaluar el rendimiento de los modelos con métricas.

•	Interpretar los resultados, incluyendo la importancia de las variables.

•	Crear una conclusión estratégica señalando los principales factores que influyen en la cancelación.

**3. Datos Utilizados**

Archivos disponibles en formato JSON y contienen información esencial sobre los clientes, incluyendo datos demográficos, tipo de servicio contratado y estado de evasión.

📌 Enlace de la API:

- [Repositorio completo del proyecto](https://github.com/ingridcristh/challenge2-data-science-LATAM)
- 
- [Dataset TelecomX (vista en GitHub)](https://github.com/ingridcristh/challenge2-data-science-LATAM/blob/main/TelecomX_Data.json)
-  
- [Dataset TelecomX (descarga directa)](https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/main/TelecomX_Data.json)
  

Algunas palabras clave del Diccionario dentro de los archivos de github:

    customerID: número de identificación único de cada cliente
    
    Churn: si el cliente dejó o no la empresa
    
    gender: género (masculino y femenino)
    
    SeniorCitizen: información sobre si un cliente tiene o no una edad igual o mayor a 65 años
    
    Contract: tipo de contrato
    
    PaperlessBilling: si el cliente prefiere recibir la factura en línea
    
    PaymentMethod: forma de pago
    
    Charges.Monthly: total de todos los servicios del cliente por mes
    
    Charges.Total: total gastado por el cliente


**4. 💡 Metodología**

**Extracción:**

Aquí documentamos cómo y desde dónde obtienes los datos.

Fuente: URL del archivo JSON de TelecomX (mencionar si es pública, interna, API, etc.).

Herramientas: requests, pandas, json.

Los datos se extrajeron desde el repositorio público de GitHub usando la librería requests. Se obtuvo un archivo JSON con información de clientes de TelecomX, incluyendo datos demográficos, tipo de servicio y estado de evasión.

📌 Acción:
Se descargó el JSON desde GitHub usando la URL RAW.

Verificar que la descarga fue correcta (vista previa).

Guardar copia local (opcional).

**Transformación:**

Aquí se deja todo listo para el análisis.

Normalizar el JSON a un DataFrame plano (pd.json_normalize). (En caso se tengan columnas anidadas)

Manejar columnas anidadas o listas internas.

Renombrar columnas para que sean legibles.

Corregir tipos de datos (int, float, datetime).


Eliminar duplicados.

Tratar valores nulos (relleno, eliminación o imputación).

📌 Acción:

Se normalizó la estructura JSON a un DataFrame, renombrando columnas con nombres claros y planos.

Se corrigieron tipos de datos, se eliminaron registros duplicados y se imputaron valores nulos en las columnas de ingresos y edad.

Además, se creó una variable “número_servicios” contando cuántos servicios contrató cada cliente.


Visualizaciones:

Gráfico de distribución de Churn (Evasión).

Gráficos de barras para ver relación con variables categóricas.

Boxplots para comparar numéricas según Churn(Evasión).

Mapa de correlaciones para variables numéricas.


**5. 💡 Principales Resultados**

**Introducción**

El objetivo de este análisis fue comprender cómo las variables numéricas clave se relacionan con la evasión de clientes (Churn) en una empresa de telecomunicaciones. Utilizando un mapa de calor de correlaciones, se buscó identificar patrones que indiquen posibles factores de riesgo para la pérdida de clientes.

**Resultados**

Mayor tiempo de permanencia (tenure) reduce el riesgo de evasión.

Cargos mensuales elevados (monthly_charges) tienen una ligera asociación con mayor evasión, aunque su impacto no es tan fuerte.

Cargos totales acumulados (total_charges) muestran que clientes con mayor historial de facturación tienden a ser más leales.

Las variables tenure y total_charges están fuertemente relacionadas, lo que implica que en el modelado predictivo podría evaluarse evitar usar ambas simultáneamente para prevenir multicolinealidad.

**6. 📌 Recomendación**

Con base en los datos:

La retención debería enfocarse especialmente en clientes nuevos (bajo tenure)

Programas de fidelización podrían ser efectivos para reducir la evasión temprana.

**Justificación:**

Los cliente nuevos (bajo tenure) son más propensos a abandonar, se puede presentar un programa de beneficios en lugar de solo descuentos

Los clientes con mayor permanencia son menos propensos a abandonar.

**7. 💡 Ejecución del Código**

Este análisis fue realizado en Google Colab utilizando Python y librerías como pandas, matplotlib, numpy y seaborn.

