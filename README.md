# Trabajo Final – Natalia Re – Vinos 🍷

Este repositorio está siendo utilizado como parte del **Trabajo Final** del curso de **Data Science** de **Coderhouse (2025)**.

Contiene los archivos, notebooks y análisis desarrollados durante el proyecto.

# 📊 Diagnóstico Comercial y Análisis Estratégico de Ventas (Base_SANA)

## 🧾 Descripción General
Este repositorio contiene el trabajo de *Primera Entrega* del proyecto final de Data Science.  
El objetivo es realizar un *diagnóstico integral del rendimiento comercial* de la empresa utilizando el dataset *Base_SANA*, validando la estrategia actual a partir de indicadores operativos y de valor.

El análisis se enfoca en:
- *Eficiencia operativa: discrepancia entre *cajas entregadas y cajas facturadas.
- *Valor estratégico: tendencias de crecimiento por **familias de producto* en los últimos 3 años.
- *Concentración de ingresos: identificación de clientes clave y comportamiento por **canal de distribución*.

---

## 🎯 Objetivos del Proyecto
✅ Diagnosticar eficiencia operativa con métricas de volumen (entregado vs vendido)  
✅ Formular preguntas e hipótesis de negocio basadas en datos reales  
✅ Explorar el dataset (estructura, tipos, valores faltantes, estadísticos)  
✅ Construir visualizaciones para validar hipótesis (univariadas, bivariadas y multivariadas)  
✅ Interpretar resultados y cerrar con conclusiones accionables para estrategia comercial  

---

## 📦 Dataset
| Característica | Detalle |
|---|---|
| Fuente | Base interna (Excel) |
| Registros | 94.511 filas |
| Columnas | 38 variables |
| Período | 2023–2025 |
| Nivel | Cliente • Producto • Canal • Zona/Provincia • Vendedor |
| Métricas clave | Ventas, Cajas Entregadas, Factu1, Factu2, Botellas entregadas |

---

## 🔑 Variables clave utilizadas
| Variable | Descripción |
|---|---|
| Anio, Mes | Dimensión temporal |
| Cod. Cliente, Razon Social, Nombre de Fantasia | Identificación del cliente |
| Canal, Desc.Canal | Segmentación comercial |
| Desc.Familia, Desc.Linea, Producto | Producto y jerarquía |
| Ventas | Cajas vendidas (con cargo) |
| Cajas Entregadas | Cajas despachadas |
| Factu2 | Facturación (variable principal de ingresos) |

---

## ❓ Preguntas e Hipótesis
| Hipótesis | Qué busca probar |
|---|---|
| H1: Ventas sin cargo > 20% del total entregado | Si el desvío entre entregado y vendido es crítico |
| H2: Familias top mantienen crecimiento en 3 años | Si el portfolio líder sostiene tendencia |
| H3: Canal con más volumen ≠ canal más rentable | Si rentabilidad y volumen van por caminos distintos |

---

## 📊 Visualizaciones realizadas
| Tipo de gráfico | Contenido | Variables |
|---|---|---|
| Comparativo | Entregado vs vendido + umbral 20% | Cajas Entregadas, Ventas |
| Temporal | Evolución de volumen por familia (Top 5) | Anio, Desc.Familia, Cajas Entregadas |
| Temporal | Evolución de facturación por familia (Top 5) | Anio, Desc.Familia, Factu2 |
| Multivariado | Relación volumen vs facturación por canal | Cajas Entregadas, Factu2, Canal |
| Resumen | Rentabilidad promedio por canal | Factu2, Canal |

---

## 🧪 Técnicas utilizadas
- 🐼 *Pandas*: carga, limpieza, agregaciones (groupby, sum, reset_index)
- 🔎 *EDA*: info(), describe(), análisis de distribuciones y consistencia
- 📈 *Matplotlib / Seaborn*: gráficos de tendencia y análisis multivariado
- 🧹 Normalización: conversión de tipos, tratamiento de nulos y outliers básicos

---

## ✅ Resultados principales
### 🔸 Hipótesis 1 (Entregado vs Vendido)
- Ventas sin cargo: *8,26%*  
- Total sin facturar: *50.820 cajas*  
📌 Conclusión: *Hipótesis rechazada* (no supera 20%), aunque el volumen es relevante.

### 🔸 Hipótesis 2 (Tendencia por familia)
📌 Se observa crecimiento/declive interanual en familias top.  
⚠️ Importante: *2025 está incompleto* (hasta mes 07), por lo que los totales pueden subestimar el año.

### 🔸 Hipótesis 3 (Volumen vs Rentabilidad por canal)
📌 El canal con más volumen no necesariamente es el de mayor facturación promedio.  
✅ Conclusión: *Hipótesis confirmada* → rentabilidad ≠ volumen.

---

## 🧩 Conclusión Final
- La empresa muestra *buena eficiencia operativa* (entregas sin facturar por debajo del umbral crítico).
- La facturación presenta *concentración elevada en pocos clientes/pedidos*, lo cual implica riesgo.
- La estrategia recomendada debería priorizar *clientes de alto valor y canales más rentables*, no solo aumentar volumen operativo.
