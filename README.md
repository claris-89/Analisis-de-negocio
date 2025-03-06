# Analisis-de-negocio

### Descripción del Proyecto
Este proyecto tiene como objetivo analizar el comportamiento de los usuarios, las ventas y los gastos de marketing de Showz, una plataforma de comercio electrónico, para optimizar las inversiones publicitarias y mejorar la rentabilidad. Usando registros detallados de visitas al sitio, pedidos y gastos de marketing, este análisis busca responder preguntas clave sobre el uso del servicio, el aporte económico de los clientes y la recuperación de los costos de adquisición.

### Objetivos
1. Comprender el comportamiento del cliente:
    - Analizar cómo los usuarios interactúan con la plataforma (frecuencia de uso, duración de sesiones, retorno).
    - Evaluar la transición de usuarios a clientes (tiempo hasta la primera compra).

2. Cuantificar el aporte económico:
    - Determinar el valor de vida del cliente (LTV).
    - Identificar patrones en el tamaño y frecuencia de las compras.

3. Optimizar los gastos de marketing:
    - Calcular el costo de adquisición de clientes (CAC) por fuente publicitaria.
    - Evaluar la rentabilidad de las inversiones publicitarias (ROMI).

4. Recomendar estrategias publicitarias:
   - Identificar las plataformas más rentables y recomendar enfoques específicos.
  
### Descripción de los Datos
El proyecto utiliza tres conjuntos de datos clave:

1. Datos de Visitas (visits)
Registra la interacción de usuarios con el sitio web:
- Uid: Identificador único de usuario.
- Device: Dispositivo usado por el cliente.
- Start Ts, End Ts: Fechas y horas de inicio/fin de la sesión.
- Source Id: Fuente de adquisición del usuario (campaña publicitaria).

2. Datos de Pedidos (orders)
Incluye información sobre las ventas:
- Uid: Identificador único del cliente.
- Buy Ts: Fecha y hora de la compra.
- Revenue: Ingreso generado por el pedido.

3. Gastos de Marketing (costs)
Detalla los costos de las campañas publicitarias:
- source_id: Identificador de la fuente de adquisición.
- dt: Fecha del gasto.
- costs: Monto gastado en publicidad.

Metodología
Paso 1: Preparación de los Datos
- Importar y limpiar los datasets.
- Verificar y ajustar los tipos de datos (e.g., convertir fechas a formato datetime).
- Eliminar valores duplicados y ausentes.

Paso 2: Cálculo de Métricas
Visitas:
- Usuarios únicos diarios, semanales y mensuales.
- Número y duración promedio de sesiones por usuario y dispositivo.
- Tasa de retorno de usuarios.

Ventas:
- Tiempo entre registro y primera compra (categorías Conversion 0d, 1d, etc.).
- Frecuencia y tamaño promedio de pedidos.
- LTV (valor de vida del cliente): $$\text{LTV} = \frac{\text{Ingresos totales por cliente}}{\text{Duración de su relación con la compañía}}$$

Marketing:
- Gastos totales y desglose por fuente publicitaria.
- Costo de Adquisición de Clientes (CAC): $$\text{CAC} = \frac{\text{Gasto total en publicidad por fuente}}{\text{Nuevos clientes adquiridos por esa fuente}}$$
- Retorno de Inversión en Marketing (ROMI): $$\text{ROMI} = \frac{\text{Ingresos generados por la fuente} - \text{Costo en publicidad}}{\text{Costo en publicidad}} \times 100\%$$

Paso 3: Análisis Visual
- Gráficos que comparen métricas clave entre dispositivos, fuentes y períodos.
- Tendencias temporales en visitas, ventas y ROMI.

Paso 4: Conclusiones y Recomendaciones
- Identificación de fuentes publicitarias más eficaces basadas en CAC y ROMI.
- Análisis de cohortes para entender qué campañas convierten mejor a clientes.
- Estrategias para maximizar el valor de vida del cliente.

### Conclusión 
En conclusión, el análisis de marketing es un proceso crucial para cualquier empresa que desee desarrollar una estrategia de marketing efectiva y alcanzar el éxito en el mercado.  Al hacer este análisis se facilita la toma de decisiones lo que permite a los inversionistas saber que fuentes generan mejores ingresos que les permitan maximizar sus ganancias.

De acuerdo a los resultados de analisis se hacen las siguientes sugerencias para las inversiones. Se debe priorizar la inversión en las fuentes con los ROMI más altos, como las fuentes 1, 5 y 4, para maximizar el retorno de las inversiones de marketing. Fuentes con ROMI bajo deben ser reevaluadas para determinar si vale la pena mantener la inversión.

Fuentes con mayor ROMI en las que se sugiere invertir:

Fuente 1: Tiene un ROMI bastante  alto, lo que sugiere que por cada unidad monetaria invertida, se generan aproximadamente 2,095,740 en ingresos. Esta fuente es la más eficiente y debería recibir la mayor parte de la inversión de marketing.
Fuente 5: También muestra un ROMI muy alto, lo que indica una excelente rentabilidad. Es una fuente muy eficiente y una inversión adicional sería recomendable.
Fuente 4: Igualmente es otra fuente altamente rentable que merece atención.

Reducir o Reconsiderar Inversiones en Fuentes con Menor ROMI:

Fuente 10 y Fuente 9: Aunque son rentables, generan mucho menos retorno comparado con las fuentes principales. Se recomienda evaluar si el costo de oportunidad de invertir en estas fuentes justifica su rendimiento.
