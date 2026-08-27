# Movilidad Urbana y Economía en América Latina

## Resumen ejecutivo del proyecto

**Objetivo:** evaluar la relación entre la congestión vehicular y la productividad económica (PIB per cápita) en 15 ciudades de 7 países latinoamericanos durante 2024, para responder una pregunta de negocio: **¿dónde debería priorizarse la inversión en infraestructura de transporte?**

> Este README presenta únicamente los **resultados, visualizaciones e insights**.
> El análisis completo, la limpieza de datos y el código reproducible se encuentran en [`S5_ladb_mobility_economy_project_student_versionGithub.ipynb`](https://github.com/pedrodavidreyes/Movilidad-Urbana-y-Economia/blob/main/S5%20ladb_mobility_economy_project_student_versionGithub.ipynb).

---

## Tabla de contenido

- [Tecnologías utilizadas](#tecnologías-utilizadas)
- [Fuentes de datos](#fuentes-de-datos)
- [Paso 1: Calidad de los datos](#paso-1-calidad-de-los-datos)
- [Paso 2: Congestión vehicular por ciudad](#paso-2-congestión-vehicular-por-ciudad)
- [Paso 3: PIB per cápita y nivel económico](#paso-3-pib-per-cápita-y-nivel-económico)
- [Paso 4: Relación entre congestión y economía](#paso-4-relación-entre-congestión-y-economía)
- [Paso 5: Priorización de inversión](#paso-5-priorización-de-inversión)
- [Conclusión y recomendaciones](#conclusión-y-recomendaciones)

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Tecnologías utilizadas

`Python` · `Jupyter Notebook` · `pandas` · `NumPy` · `Matplotlib` · `Seaborn`

**Técnicas aplicadas:** limpieza y validación de datos, análisis exploratorio (EDA), cálculo de indicadores de congestión, cruce de fuentes económicas y de movilidad, 🔲 *[completar: ¿usaste correlación de Pearson/Spearman? ¿clustering? ¿algún otro método estadístico?]*, y visualización comparativa entre ciudades.

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Fuentes de datos

| Fuente | Contenido | Herramienta |
|---|---|---|
| `tomtom_traffic` | Índice de congestión vehicular (jams_delay y otras métricas) por ciudad | Python |
| `oecd_cities` | PIB per cápita y otros indicadores económicos por ciudad/país | Python |

> ⚠️ **Nota:** el dataset `tomtom_traffic` (>100 MB) aún no está subido al repositorio por límite de tamaño. 🔲 *[actualizar esta nota una vez definas dónde alojarlo — por ejemplo, Git LFS, un enlace externo (Google Drive/Kaggle), o un script de descarga]*.

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Paso 1: Calidad de los datos

**Pregunta del negocio:** ¿podemos confiar en los datos de tráfico y PIB antes de cruzarlos?

Se validaron ambos datasets (`tomtom_traffic`, `oecd_cities`):

- 🔲 *[completar: ¿qué revisaste? Ej. valores nulos, duplicados, homologación de nombres de ciudades entre ambas fuentes, unidades de medida, año de referencia consistente, etc.]*

**Entregable:** 🔲 *[nombre de los archivos limpios, si aplica]*

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Paso 2: Congestión vehicular por ciudad

**Pregunta del negocio:** ¿qué ciudades presentan mayor congestión?

| Ciudad | jams_delay | Posición |
|---|---|---|
| Ciudad de México | **2,833** | 1° (mayor congestión) |
| 🔲 *[ciudad 2]* | 🔲 | 2° |
| 🔲 *[ciudad 3]* | 🔲 | 3° |
| ... | ... | ... |

**Hallazgo:** Ciudad de México presenta el mayor índice de congestión de las 15 ciudades analizadas.

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Paso 3: PIB per cápita y nivel económico

**Pregunta del negocio:** ¿qué ciudades tienen mayor productividad económica?

| Ciudad | PIB per cápita | Congestión (jams_delay) |
|---|---|---|
| Montevideo | 🔲 *[valor]* | Baja (menor tráfico del grupo) |
| 🔲 | 🔲 | 🔲 |

**Hallazgo:** Montevideo combina el mayor PIB per cápita del grupo con uno de los niveles de congestión más bajos.

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Paso 4: Relación entre congestión y economía

**Pregunta del negocio:** ¿a mayor congestión, mayor actividad económica?

🔲 *[completar: ¿calculaste un coeficiente de correlación? Si sí, indica el valor exacto (ej. "r = 0.XX") y qué método usaste. Si el análisis fue solo visual/exploratorio, descríbelo así.]*

**Hallazgo:** no existe una correlación directa entre el nivel de congestión y el nivel económico de una ciudad — hay ciudades con alta congestión y bajo PIB per cápita, y viceversa (ej. Montevideo).

**Insight de negocio:** la congestión por sí sola no es un buen indicador de la salud económica de una ciudad, lo que sugiere que la inversión en transporte no debería priorizarse solo por volumen de tráfico, sino combinando ambos factores.

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Paso 5: Priorización de inversión

**Pregunta del negocio:** ¿dónde debería invertir primero un gobierno o inversor en infraestructura de transporte?

**Ciudades recomendadas:** Bogotá y Lima.

🔲 *[completar: ¿qué criterio usaste para llegar a esta recomendación? Ej. "ciudades con congestión alta Y PIB per cápita medio/alto, donde una mejora en movilidad tendría mayor retorno económico". Sin este criterio explícito, la recomendación pierde fuerza argumentativa.]*

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)

---

## Conclusión y recomendaciones

### Diagnóstico general

El análisis de 15 ciudades latinoamericanas en 2024 muestra que congestión y productividad económica **no están directamente correlacionadas**. Ciudad de México lidera en congestión, mientras que Montevideo combina alto PIB per cápita con bajo tráfico — lo que descarta un vínculo automático entre ambas variables.

### Recomendaciones priorizadas

- **Priorizar inversión en Bogotá y Lima**, 🔲 *[por qué exactamente — ver Paso 5]*.
- 🔲 *[¿alguna otra recomendación de tu notebook? Ej. profundizar el análisis por país, incluir más variables como densidad poblacional, tamaño de flota vehicular, etc.]*

### Consideraciones

Este análisis es exploratorio y se basa en datos de un solo año (2024). 🔲 *[¿mencionas en tu notebook alguna limitación, como tamaño de muestra, calidad de las fuentes, o la necesidad de series de tiempo para conclusiones más sólidas?]*

[↑ Volver al inicio](#movilidad-urbana-y-economía-en-américa-latina)
