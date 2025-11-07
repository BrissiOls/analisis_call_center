# 📊 Análisis de Desempeño Operacional: Proyecto CallMeMaybe

## 📝 Contexto del Proyecto

El objetivo de este proyecto fue desarrollar una funcionalidad dentro del servicio de telefonía virtual **CallMeMaybe** para **identificar a los operadores menos eficaces** del centro de llamadas.

Mi rol consistió en el **análisis exploratorio y estadístico** de los datos operacionales, definiendo y aplicando métricas clave basadas en estándares de la industria para establecer umbrales de ineficacia y validar los hallazgos.

### Criterios para Operadores Ineficaces

Se considera un operador ineficaz si cumple con alguno de los siguientes criterios:
* Alta cantidad de **llamadas entrantes perdidas**.
* **Tiempo de espera prolongado** para las llamadas entrantes.
* **Número reducido de llamadas salientes** (operadores por debajo del primer cuartil).

## 🛠️ Herramientas y Técnicas Utilizadas

| Categoría | Herramientas/Librerías | Aplicación |
| :--- | :--- | :--- |
| **Lenguaje y Data** | `Python` (`pandas`, `numpy`) | Manipulación, limpieza y cálculo de métricas. |
| **Visualización** | `matplotlib.pyplot`, `seaborn` | Gráficos de tendencias (*boxplots*) para identificar *outliers* y variabilidad. |
| **Estadística** | `scipy.stats` | Prueba de hipótesis para validar la significancia estadística de los hallazgos. |
| **Metodología** | Benchmarks (ICMI, NAQC) | Definición de umbrales de desempeño ($\text{Tasa de Abandono} \le 5-8\%$, $\text{ASA} \le 20\text{ segundos}$). |

## 📈 Análisis y Resultados Clave

El análisis arrojó hallazgos críticos que impactan tanto en la gestión individual como en la capacidad operativa del servicio:

* **⚠️ Problema de Servicio Crítico:** El **44% de las llamadas no son atendidas** (Tasa de Abandono), lo que indica un problema sistémico grave de capacidad o distribución, afectando directamente la satisfacción del cliente y la potencial pérdida de ingresos.
* **🚨 Retrasos Generalizados en la Atención:** El **39% de los operadores** no cumplen con el nivel de servicio deseado, registrando tiempos de espera superiores a 20 segundos para la mayoría de sus llamadas.
* **🎯 Identificación de Críticos:** Se identificó que un **5% de los operadores** cumplen con los tres criterios establecidos para ser catalogados como ineficaces.

## ✅ Conclusiones

Los resultados confirman la necesidad de una doble intervención:

1.  **Intervención Focalizada:** Gestionar y aplicar medidas correctivas inmediatas (capacitación, *coaching*) al **5% de los operadores** ineficaces identificados.
2.  **Estrategia Táctica de Capacidad:** La alta tasa de llamadas perdidas exige un análisis de capacidad y una **revisión de la planificación de turnos** para alinear la plantilla con la demanda real.

### Limitación Crítica
La **falta de información temporal (hora de las llamadas)** es una limitación clave. Se recomienda encarecidamente incorporarla para identificar los picos de demanda y optimizar la distribución de recursos.
