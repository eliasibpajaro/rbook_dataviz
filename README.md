# R bookdown — EDA de espectros sísmicos

Este repositorio quedó reorganizado para que el libro se centre en:

- Contexto, problema y objetivos
- Marco teórico y metodología del EDA
- Análisis univariado
- Análisis bivariado
- Análisis multivariado
- Conclusiones

## Estructura esperada

- `index.Rmd`: portada y configuración base
- `01-contexto.Rmd`
- `02-marco_metodologia.Rmd`
- `03-univariado.Rmd`
- `04-bivariado.Rmd`
- `05-multivariado.Rmd`
- `06-conclusiones.Rmd`
- `07-referencias.Rmd`
- `data/NGACOL.csv`

## Cómo renderizar localmente

```r
install.packages(c(
  "bookdown", "knitr", "readr", "dplyr", "tidyr", "ggplot2",
  "scales", "stringr", "tibble", "plotly", "car"
))

bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

El resultado se genera en la carpeta `docs/`, que es la que normalmente se publica en GitHub Pages.

## Publicar en GitHub

Después de renderizar:

```bash
git add .
git commit -m "Actualiza R book con EDA y marco teórico"
git push origin main
```

Si GitHub Pages está configurado para publicar desde `main/docs`, la versión nueva del libro quedará lista al terminar el push.
