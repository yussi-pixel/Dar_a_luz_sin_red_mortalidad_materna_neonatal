# Dar a luz sin red: mortalidad materna y neonatal, natalidad y pobreza en el mundo

Seminario de la asignatura **Fuentes de Datos Biomédicos y Web Semántica**
(Grado en Ingeniería de la Salud, Universidad de Burgos, curso 2026-2027).

**Autora:** Yousra El Jarjini

## Acerca de este proyecto

Este trabajo estudia, a escala mundial, por qué en unos países las mujeres embarazadas y los recién nacidos mueren con mucha más frecuencia que en otros. Comparamos los países del mundo con datos disponibles usando datos públicos del Banco Mundial (*World Development Indicators*), y relacionamos las muertes maternas y neonatales con cuatro factores: la **fecundidad**, la **pobreza**, la **atención sanitaria en el parto** y la **contaminación del aire**.

Todo el análisis está hecho en **R y RMarkdown**: se importan los datos desde archivos CSV, se limpian y se unen con *joins*, se guardan también en formato JSON, y se representan con mapas, gráficos, correlaciones de Spearman y un modelo de regresión lineal. El documento final se genera en HTML y contiene el texto, el código y sus resultados.

El seminario completo está en el archivo `.html` de este repositorio: descárgalo y ábrelo en el navegador para verlo bien.

## Introducción

Cada año mueren muchas mujeres por causas relacionadas con el embarazo y el parto, y muchos recién nacidos mueren durante su primer mes de vida. La mayoría de estas muertes se deben a causas conocidas y evitables: hemorragias, infecciones y problemas de tensión arterial en las madres; y prematuridad, falta de oxígeno al nacer e infecciones en los bebés. Casi siempre se pueden evitar con personal cualificado, medicamentos y un centro de salud al que llegar a tiempo.

Sin embargo, el lugar donde nace una persona sigue marcando enormemente sus probabilidades de sobrevivir. Con este trabajo queremos ver, con datos, cómo se reparten estas muertes en el mundo, cómo han cambiado desde el año 2000, y qué factores aparecen asociados a ellas. También analizamos el caso de Estados Unidos, un país rico con la mortalidad materna más alta entre los países de ingresos altos, para comprobar que la riqueza media de un país no basta para garantizar un parto seguro.

## Objetivos

1. **Descripción espacial:** países donde se concentran las muertes maternas y neonatales.
2. **Descripción temporal:** evolución entre 2000 y 2023 según el nivel de ingreso del país.
3. **Fecundidad:** relación entre la fecundidad y la mortalidad materna y neonatal.
4. **Pobreza, atención sanitaria y ambiente:** relación de la mortalidad con la pobreza, los partos atendidos por personal cualificado y la contaminación del aire.

## Datos

Los indicadores proceden del Banco Mundial (https://data.worldbank.org/). Cada archivo de la carpeta `Data` corresponde a un indicador:

| Código | Indicador |
|---|---|
| SH.STA.MMRT | Razón de mortalidad materna |
| SH.DYN.NMRT | Mortalidad neonatal |
| SH.DYN.MORT | Mortalidad de menores de 5 años |
| SP.DYN.TFRT.IN | Fecundidad |
| SH.STA.BRTC.ZS | Partos atendidos por personal cualificado |
| NY.GDP.PCAP.PP.CD | PIB per cápita (PPA) |
| SI.POV.DDAY | Pobreza extrema |
| EN.ATM.PM25.MC.M3 | Exposición a PM2.5 |
| EG.CFT.ACCS.ZS | Acceso a combustibles limpios para cocinar |

El archivo `Metadata_Country...csv` contiene el nombre, la región y el grupo de ingreso de cada país.

## Fuentes principales

- World Bank. *World Development Indicators*. https://data.worldbank.org/
- Gunja, M. Z., Gumas, E. D., Masitha, R., & Zephyrin, L. C. (2024). *Insights into the U.S. maternal mortality crisis: An international comparison*. Commonwealth Fund.
