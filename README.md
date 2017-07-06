---
date: "2017-07-06"
title: "Ejemplo de flujo de trabajo"
author: "Joshua Haase"
---

El objetivo de este proyecto es mostrar
cómo se genera y se utiliza un flujo de trabajo en mk.

# Ejecución

El módulo de `analysis/001` genera redes de aracne y opcionalmente genera SIF.

Es conveniente ejecutar las redes en paralelo usando condor
y la generación del SIF localmente en castillo.

```
# generar las redes
cd analysis/001
condor submit
# al terminar, generar el SIF
bin/targets-sif | xargs mk
```

El módulo de `analysis/002` es el que recién solicitó el revisor 2.
Un compañero lo publicó en [github](https://github.com/CSB-IG/midist.git )

El reporte que se va a entregar se encuentra en `reporte/`
y se puede generar desde esa carpeta usando mk:

```
cd reporte
mk -f reporte.pdf
```

El reporte requiere que las imágenes existan en `analysis/002/results`.

Las redes para generar los análisis se encuentran en `/labs/taller/pipeline/data`

# Ejercicio

Tenemos un paper en revisión en la carpeta ` `.

Revisor 1 dice:

> Corregir ortografía.

Revisor 2 dice:

> Requerimos gráficas de la distribución de la Información Mutua para las redes de aracne en sus datos.

Hay que descargar el módulo para el segundo análisis
y ejecutarlo de acuerdo a las instrucciones.

# Flujo de trabajo

La información acerca del análisis se encuentra en `analysis/README.md`.


