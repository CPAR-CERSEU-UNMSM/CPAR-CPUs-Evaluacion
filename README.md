# CPAR-CPUs-Evaluacion de Marzo 2024

Esta evaluación examina algunos conocimientos teóricos y habilidades en la paralelización y/o vectorizacion en CPUs.

## Puntaje

| Ejercicio | Puntaje  |
|:-------|:--------:|
| 1       | 1 |
| 2       | 1 |
| 3       | 8 |
| 4       | 4 |
| 5       | 4 |
| 6       | 2 |
| 7       | 2 |
| ======= |======  |
| Total   | 20 |

## Ejercicios

### Ejercicio 1
Clonar el siguiente repositorio:

https://github.com/essentialsofparallelcomputing/EssentialsOfParallelComputing.git

- **Pregunta 1.1.** Listar el/los comando(s) utilizado(s) y su salida correspondiente en la consola

### Ejercicio 2

Moverse al directorio `Chapter 6`. Estando en ese directorio, clonar el submodulo `Chapter 6` usando el comando `git submodule update --init Chapter6`

- **Pregunta 2.1.** Listar el/los comando(s) utilizado(s) y su salida correspondiente en la consola

### Ejercicio 3
Moverse al directorio `mass_sum`. 

- **Pregunta 3.1.** Listar los archivos presentes en tal directorio
- **Pregunta 3.2.** Analizar el archivo `CMakeLists.txt` e indicar todas las opciones especificadas para el compilador GCC
- **Pregunta 3.3.** De las opciones del compilador de la pregunta 3.2, indicar aquella(s) que _habilita(n)_/_facilita(n)_/_informa(n) sobre_ la vectorización
- **Pregunta 3.4.** De las opciones del compilador de la pregunta 3.2, indicar aquella(s) que especifique(n) el ancho preferido del vector


### Ejercicio 4
Permancecer en el directorio `mass_sum`. 

- **Pregunta 4.1.** Indicar el pragma utilizado en alguno(s) de sus archivos fuente. 
- **Pregunta 4.2.** Compilar el proyecto usando `cmake` y `make`.  Listar el/los comando(s) utilizado(s) y su salida correspondiente en la consola
- **Pregunta 4.3.** Indicar que bucles (_"for loops"_) han sido vectorizados. Indicar el archivo y la línea correspondiente
- **Pregunta 4.4.** Ejecutar el programa e indicar el tiempo de ejecución usando `time ./mass_sum`

### Ejercicio 5
Permancecer en el directorio `mass_sum`. Compilar el proyecto usando `cmake` y `make`.

- **Pregunta 5.1.** Explicar usando máximo tres oraciones como podría **deshabilitar** de manera _explícita_ la vectorización del programa
- **Pregunta 5.2.** Una vez deshabilitada la vectorización, compile y ejecute nuevamente el programa. Indique si hay diferencia con respecto al tiempo de ejecución del ejercicio anterior

### Ejercicio 6
Contestar las siguientes preguntas de teoría.

- **Pregunta 6.1.** ¿Cuáles son las locaciones de git?
- **Pregunta 6.3.** Mencione dos técnicas de vectorización

### Ejercicio 7
Crear un repositorio en GitHub para guardar sus respuestas de este examen.

- **Pregunta 7.1.** Proporcionar el link del repositorio creado y enviarlo por email a los docentes
