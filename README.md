# Análisis de desempeño financiero por país con SQL

Análisis del margen de rentabilidad y retorno sobre inversión (ROI) de campañas de marketing en seis países, realizado con **SQL** y presentado como resumen ejecutivo con hallazgos, contexto e implicaciones para el área comercial.

---

## Contexto del problema

La empresa invierte en campañas de marketing en distintos mercados (Estados Unidos, Australia, Reino Unido, Alemania, Francia y Canadá), pero necesitaba entender **no solo cuánto vendía cada país, sino qué tan eficiente era esa inversión**. El objetivo fue calcular el margen de beneficio bruto y el ROI de campañas por país en un mismo periodo, e identificar qué mercados están generando el mejor y el peor retorno por cada dólar invertido.

---

## Herramientas utilizadas

| Herramienta | Uso en el proyecto |
|---|---|
| **SQL** | Consultas para calcular ingresos, costos, beneficio bruto, margen y ROI por país |
| Funciones de agregación (`SUM`, agrupación por país) | Consolidación de ingresos y costos por territorio |
| Cálculo de métricas derivadas | Margen (%) y ROI (%) a partir de ingresos, costos y gasto en campañas |
| Hoja de resumen ejecutivo | Presentación de hallazgos e implicaciones para audiencia no técnica |

---

## Metodología

1. **Consolidación por país.** Se agruparon ingresos, costos operativos y costo de campañas de marketing por país (6 territorios).
2. **Cálculo de métricas.** Para cada país se derivó el **beneficio bruto** (ingresos − costos), el **margen** (beneficio bruto ÷ ingresos) y el **ROI** (beneficio bruto ÷ costo de campañas).
3. **Comparación entre mercados.** Se calculó el promedio de margen y ROI del grupo, y se identificaron los países por encima y por debajo de ese promedio.
4. **Formulación de preguntas de negocio.** En lugar de solo reportar cifras, el análisis se estructuró respondiendo preguntas concretas que anticipan lo que un tomador de decisiones preguntaría, incluyendo un escenario hipotético (qué pasaría con el ROI si aumentara el gasto en campañas un 50%).
5. **Traducción a implicaciones.** Cada hallazgo se acompañó de una recomendación accionable para el área comercial, no solo de la cifra.

---

## Hallazgos principales

| Métrica | Resultado |
|---|---|
| Margen promedio del grupo | **+43%**, con desviación estándar de solo 0.98%, lo que indica rentabilidad uniforme entre países |
| País con mejor ROI | Estados Unidos, **+45% por encima** del promedio del grupo (ROI de 75.75%) |
| Países con menor ROI | Francia (-15.74%) y Canadá (-16.27%) por debajo del promedio |

**¿Por qué el ROI de Estados Unidos es tan alto?** Porque, en proporción a sus ingresos, invierte relativamente menos en campañas que los demás países, obteniendo mayor eficiencia por cada dólar invertido.

**Escenario simulado — ¿qué pasaría si aumentara el gasto en campañas un 50%?** Si el beneficio bruto se mantuviera constante, el ROI de Estados Unidos bajaría de 75.75% a aproximadamente 50.50%, ya que el retorno se diluiría sobre una base de inversión mayor. Antes de decidir un aumento así, se recomienda validar con estudios de demanda si esa inversión adicional generaría ingresos incrementales reales.

### Implicaciones para el negocio

- Evaluar la estrategia de campañas de Estados Unidos (segmentación, canales de marketing, presupuesto y costo de adquisición) para replicarla, cuando sea aplicable, en Francia y Canadá antes de aumentar su inversión.
- Aplicar encuestas de demanda para evaluar la viabilidad de campañas adicionales y evitar comprometer presupuesto de marketing sin evidencia de retorno incremental.

---

## Archivos del repositorio

```
├── data/
│   └── desempeno_financiero_paises.xlsx   # Dashboard con datos, métricas e insights
└── README.md
```

---

## Habilidades demostradas

- Consultas SQL para consolidación y agregación de datos financieros
- Cálculo de métricas de rentabilidad (margen) y eficiencia de inversión (ROI)
- Análisis comparativo entre múltiples segmentos (países)
- Modelado de escenarios hipotéticos para apoyar decisiones de inversión
- Redacción de hallazgos e implicaciones orientadas a un tomador de decisiones no técnico
