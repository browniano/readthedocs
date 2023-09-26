# Python y R

Instalación de paquetes en **directorios de usuario**.

```{warning}
Documentación en construcción.
```

## Instalación de paquetes R

Creamos entornos virtuales para cada uno de nuestros proyectos en directorios específicos.

```{code-block}
$ mkdir mi_nuevo_proyectoen_R
$ cd mi_nuevo_proyectoen_R
$ module load R
$ R
```

```{eval-rst}
.. highlight:: R

Instalamos el paquete renv::

    > install.packages("renv")
    Warning in install.packages("renv") :
    'lib = "/mnt/lustre/localsoft/R-v3.6.0/rlib/R/library"' is not writable
    Would you like to use a personal library instead? (yes/No/cancel) yes
    Would you like to create a personal library
    ‘~/R/x86_64-pc-linux-gnu-library/3.6’
    to install packages into? (yes/No/cancel) yes
    --- Please select a CRAN mirror for use in this session ---
    Secure CRAN mirrors
    Selection: 60
    trying URL 'https://cran.rediris.es/src/contrib/renv_1.0.2.tar.gz'
    Content type 'application/x-gzip' length 1135957 bytes (1.1 MB)
    ==================================================
    downloaded 1.1 MB

    * installing *source* package ‘renv’ ...
    ** package ‘renv’ successfully unpacked and MD5 sums checked
    ** using staged installation
    ** R
    ** inst
    ** byte-compile and prepare package for lazy loading
    ** help
    *** installing help indices
    *** copying figures
    ** building package indices
    ** installing vignettes
    ** testing if installed package can be loaded from temporary location
    ** testing if installed package can be loaded from final location
    ** testing if installed package keeps a record of temporary installation path
    * DONE (renv)

    The downloaded source packages are in
        ‘/tmp/Rtmpyi8JG0/downloaded_packages’
    >

Y activamos el entorno::

    > library(renv)
    > renv::init()
    The following package(s) will be updated in the lockfile:
    # CRAN -----------------------------------------------------------------------
    - renv   [* -> 1.0.2]
    The version of R recorded in the lockfile will be updated:
    - R      [* -> 3.6.0]
    - Lockfile written to "~/Pruebas/R_tests/renv.lock".
    - renv activated -- please restart the R session.


```

```R
   library(renv)
   renv::init()
```
