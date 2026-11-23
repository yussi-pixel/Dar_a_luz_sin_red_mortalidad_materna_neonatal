# Dar a luz sin red: mortalidad materna y neonatal, natalidad y pobreza en el mundo

Seminario de la asignatura **Fuentes de Datos Biomédicos y Web Semántica**
(Grado en Ingeniería de la Salud, Universidad de Burgos, curso 2026-2027).

**Autora:** Yousra El Jarjini

## ¿De qué trata?

Analizamos, a escala de país, cómo se relacionan las muertes de madres y de recién nacidos con la fecundidad, la pobreza, la atención sanitaria en el parto y la contaminación del aire. Usamos datos públicos del Banco Mundial (*World Development Indicators*) y trabajamos con R y RMarkdown.

## Objetivos

1. **Descripción espacial:** países donde se concentran las muertes maternas y neonatales.
2. **Descripción temporal:** evolución entre 2000 y 2023 según el nivel de ingreso del país.
3. **Fecundidad:** relación entre la fecundidad y la mortalidad materna y neonatal.
4. **Pobreza, atención sanitaria y ambiente:** relación de la mortalidad con la pobreza, los partos atendidos por personal cualificado y la contaminación del aire.

## Contenido del repositorio

```
.
├── README.md                     Esta página
├── Dar_a_luz_sin_red_mortalidad_materna_neonatal.Rmd      Cuaderno de R: texto y código del seminario
├── Dar_a_luz_sin_red_mortalidad_materna_neonatal.html     Seminario renderizado (descargar y abrir en el navegador)
├── Data/                         Archivos CSV descargados del Banco Mundial
└── OUTPUT/                       Tablas generadas por el código (CSV y JSON)
```

> GitHub no muestra los archivos `.html` como página web. Para verlo bien, hay que **descargar** `Dar_a_luz_sin_red_mortalidad_materna_neonatal.html` y abrirlo en el navegador.

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

## Cómo reproducir el análisis

1. Descargar el repositorio completo (**Code → Download ZIP**) y descomprimirlo.
2. Abrir `Dar_a_luz_sin_red_mortalidad_materna_neonatal.Rmd` en RStudio.
3. Instalar, si hace falta, los paquetes: `tidyverse`, `sf`, `giscoR`, `scales`, `knitr`, `broom` y `jsonlite`.
4. Pulsar **Knit**. La carpeta `Data` debe estar junto al archivo `.Rmd`.

## Fuentes principales

- World Bank. *World Development Indicators*. https://data.worldbank.org/
- Gunja, M. Z., Gumas, E. D., Masitha, R., & Zephyrin, L. C. (2024). *Insights into the U.S. maternal mortality crisis: An international comparison*. Commonwealth Fund.
