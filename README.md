# JENUI 2024: Estrategias de control y seguimiento de proyectos de desarrollo de software

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://nbviewer.org/github/matey97/jenui2024/)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/matey97/jenui2024/v1.0.0)

Este repositorio contiene contiene los datos utilizados y los análisis efectuados para el artículo _"Estrategias de control y seguimiento de proyectos de desarrollo de software"_, presentado en las **XXX Jornadas sobre la Enseñanza Universitaria de la Informática (JENUI 2024)**.

> Matey Sanz, M., Granell Canut, C. , Mollineda Cárdenas, R. A. (2024). Estrategias de control y seguimiento activo de proyectos de desarrollo de software. Actas de las Jenui, 9, 165-172.

## Reproducibilidad 

### Reproducir online

Haga click en la insignia "Binder" para abir un entorno interactivo de Jupyter con todo el software necesario instalado.

### Reproducir localmente
Instale Python 3.9, descargue el repositorio, inicie una linea de comandos en la raíz del directorio e instale las dependencias requeridas mediante la execución del siguiente comando:

```bash
pip install -r requirements.txt
```

### Reproducir localmente con Docker
Instalar [Docker](https://www.docker.com) para construir una imagen basada en el `Dockerfile` con un entorno Jupyter y ejecutar un conteneder basado en la imagen.

Descargue el repositorio, abra una linea de comandos en la raíz del directorio y ejecute:

1. Construya la imagen:

```bash
docker build . --tag jenui24
```

2. Ejecute la imagen:

```bash
docker run -it -p 8888:8888 jenui24
```

3. Haga click en el link de login (o copie y pegue en el navegador) que se muestra en la consola para acceder al entorno de Jupyter.

### Reproduzca el análisis
Abra el notebook `01_analysis.ipynb`. Dicho fichero contiene el código empleado para realizar los análisis y obtener los resultados mostrados en el artículo. Puede ejecutar el código para reproducir los resultados mostrados.  


## Estructura del repositorio

- `01_notas`: contiene los datos de entrada y los resultados de los análisis de las notas y entregas.
  - `01_entrada`: directorio que contiene los siguientes ficheros empleados en los análisis:
    - [`entregas_23-24.csv`](./01_notas/01_entrada/entregas_23-24.csv): resultados de las entregas parciales del curso 2023/2024.
    - [`notas_23-24.csv`](./01_notas/01_entrada/notas_23-24.csv): notas del curso 2023/2024.
    - [`notas_22-23.csv`](./01_notas/01_entrada/notas_22-23.csv): notas del curso 2022/2023.
    - [`notas_21-22.csv`](./01_notas/01_entrada/notas_21-22.csv): notas del curso 2021/2022.
  - `02_resultados`: directorio que contiene los resultados obtenidos en los análisis:
    - [`evolucion.pdf`](./01_notas/02_resultados/evolucion.pdf): gráfico que muestra la evolución de los equipos en las entregas y el proyecto final durante el curso 2023/2024.
- `02_encuesta-conocimientos`: contiene los datos de entrada y los resultados de los análisis de las encuestas de conocimiento.
  - `01_respuestas`: directorio que contiene los siguientes ficheros empleados en los análisis:
    - [`00_items.csv`](./02_encuesta-conocimientos/01_respuestas/00_items.csv): descripción de los items de la encuesta.
    - [`01_encuestas-pre.csv`](./02_encuesta-conocimientos/01_respuestas/01_encuestas-pre.csv): respuestas a las encuestas pre del curso 2023/2024.
    - [`02_encuestas-post.csv`](./02_encuesta-conocimientos/01_respuestas/02_encuestas-post.csv): respuestas a las encuestas post del curso 2023/2024.
    - [`03_resultados_21-22.csv`](./02_encuesta-conocimientos/01_respuestas/03_resultados_21-22.csv): resultados de las encuestas del curso 2021/2022.
  - `02_resultados`: directorio que contiene los resultados obtenidos en los análisis:
    - [`01_inc-relativo.pdf`](./02_encuesta-conocimientos/02_resultados/01_inc-relativo.pdf): incremento relativo porcentual de conocimientos.
    - [`02_inc-abs-perc.pdf`](./02_encuesta-conocimientos/02_resultados/02_inc-abs-perc.pdf): incremento absoluto porcentual de conocimientos.
    - [`02_inc-abs.pdf`](./02_encuesta-conocimientos/02_resultados/02_inc-abs.pdf): incremento absoluto de conocimientos.
    - [`03_comparativa-incrementos.pdf`](./02_encuesta-conocimientos/02_resultados/03_comparativa-incrementos.pdf): comparativa de incrementos medidos entre el curso 2023/2024 y el curso 2021/2022.
- `03_encuesta-satisfaccion`: contiene los datos de entrada y los resultados de los análisis de la encuesta de satisfacción.
  - `01_respuestas`: directorio que contiene los siguientes ficheros empleados en los análisis:
    - [`00_items.csv`](./03_encuesta-satisfaccion/01_respuestas/00_items.csv): descripción de los items de la encuesta.
    - [`01_respuestas-freetext.csv`](./03_encuesta-satisfaccion/01_respuestas/01_respuestas-freetext.csv): respuestas de texto libre del curso 2023/2024.
    - [`01_respuestas-likert.csv`](./03_encuesta-satisfaccion/01_respuestas/01_respuestas-likert.csv): respuestas de los items de satisfacción likert del curso 2023/2024.
    - [`02_resultados_21-22.csv`](./03_encuesta-satisfaccion/01_respuestas/02_resultados_21-22.csv): resultados de las encuestas del curso 2021/2022.
  - `02_resultados`: directorio que contiene los resultados obtenidos en los análisis:
    - [`01_comparativa-satisfaccion.pdf`](./03_encuesta-satisfaccion/02_resultados/01_comparativa-satisfaccion.pdf): comparativa de resultados de satisfacción media entre los cursos 2023/2024 y 2021/2022.
    - [`02_comparativa-medias-satisfaccion.csv`](./03_encuesta-satisfaccion/02_resultados/02_comparativa-medias-satisfaccion.csv): comparativa de resultados de satisfacción media agregada por categorías entre los cursos 2023/2024 y 2021/2022.
- [`04_ponencia`](./04_ponencia): directorio que contiene la presentación en PowerPoint (`.pptx`) y PDF empleada durante la ponencia.
- [`01_analisis.ipynb`](./01_analisis.ipynb): notebook que contiene todos los análisis ejecutados.
- [`requirements.txt`](./requirements.txt): dependencias utilizadas para ejecutar los análisis en Python 3.9.


## Licencia

Este repositorio esta licenciado bajo [Apache License 2.0](./LICENSE)
