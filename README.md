# Anemia infantil en el Perú — ENDES 2025

Este proyecto analiza los factores asociados con la anemia en niños de 6 a 35 meses en el Perú utilizando información de la **Encuesta Demográfica y de Salud Familiar (ENDES) 2025**.

A partir de los módulos de hogares, características de sus miembros y mediciones de hemoglobina, se construye un indicador de anemia ajustado por altitud siguiendo la **RM 363-2022-MINSA**. Posteriormente, se estima un Modelo de Probabilidad Lineal incorporando el diseño muestral complejo de la ENDES.

## Principales resultados

- La prevalencia estimada de anemia infantil es cercana al **43 %**.
- La anemia se concentra principalmente en los primeros meses de vida.
- Un mayor nivel de riqueza del hogar se asocia con una menor probabilidad de anemia.
- El acceso a fuentes seguras de agua y saneamiento presenta una relación significativa con el estado nutricional infantil.
- Las diferencias observadas entre áreas rurales y urbanas están estrechamente relacionadas con las condiciones socioeconómicas y de infraestructura.

## Herramientas utilizadas

- Stata
- ENDES 2025
- Modelo de Probabilidad Lineal
- Regresión MCO
- Análisis con ponderadores y diseño muestral complejo

## Ejecución del código

El archivo `Anemia_Infantil_MCO.do` contiene todo el flujo de procesamiento y análisis en Stata: integración de los módulos de la ENDES, construcción del indicador de anemia, elaboración de gráficos y estimación de modelos econométricos.

### Requisitos

Para ejecutar el proyecto se necesita:

- Stata 16 o una versión posterior.
- Microdatos de la ENDES 2025 descargados del portal del INEI.
- Shapefile departamental del Perú para generar el mapa.
- Paquetes de Stata:
  - `estout`
  - `spmap`

El código instala automáticamente estos paquetes cuando no se encuentran disponibles.

### Archivos necesarios

Los siguientes archivos `.dta` deben colocarse en la carpeta principal del proyecto:

```text
RECH0_2025.dta
RECH1_2025.dta
RECH4_2025.dta
RECH6_2025.dta
RECH23_2025.dta
REC0111_2025.dta

