# Python y R

Instalación de paquetes en **directorios de usuario**.

```{warning}
Documentación en construcción.
```

## Instalación de paquetes R

Creamos un nuevo directorio donde irán los paquetes de nuestro proyecto:

```console
   $ mkdir ~/mi_nuevo_proyectoen_R
   $ cd ~/mi_nuevo_proyectoen_R
```

Cargamos el módulo de R que vayamos a usar, por ejemplo:

```console
    $ module load r-3.5.1-gcc-8.2.0-lnyyu4a
    $ R
```

Instalamos por ejemplo **CDFt**

```python
   > install.packages("CDFt", lib="~/mi_nuevo_proyectoen_R/")
```

Y para usarlo:

```python
   > library("CDFt", lib="~/mi_nuevo_proyectoen_R/")
```
[Más info](https://cran.r-project.org/doc/manuals/r-release/R-admin.html)

## Instalación de paquetes python

Creamos un nuevo directorio donde irán los paquetes de nuestro proyecto:

```console
   $ mkdir ~/mi_nuevo_proyectoen_py
   $ cd ~/mi_nuevo_proyectoen_py
```

Cargamos el módulo de python que vayamos a usar, por ejemplo:

```console
    $ module load python-3.7.0-gcc-8.3.0-3gbn5jk
```

Creamos un nuevo *environment* y lo activamos cada vez que hagamos uso del mismo:

```console
    $ python -m venv .
    $ source bin/activate
```

Ya podemos instalar paquetes en este *environment*, por ejemplo con *pip*:

```console
    $ pip install keras
```

[Más info](https://docs.python.org/3/library/venv.html)
