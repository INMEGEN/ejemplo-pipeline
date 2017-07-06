# Reporte para taller de supercómputo

Para generar el archivo, usar el comando:

```
mk -a reporte.pdf
```

# Requisitos

En la carpeta de estilos `$HOME/texmf/tex/latex`,
se requiere instaler el archivo `algorithm2e.sty`.

```
DIR="$HOME/texmf/tex/latex"
mkdir -p $DIR
cd $DIR
curl -LO https://github.com/SDN-Survey/latex/raw/master/algorithm2e.sty
```
