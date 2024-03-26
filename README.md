# CPAR-CPUs-Evaluacion de Marzo 2024

Esta evaluación examina algunos conocimientos teóricos y habilidades en la paralelización y/o vectorizacion en CPUs.

## Puntaje

| Ejercicio | Puntaje  |
|:-------|:--------:|
| 1       | 1 |
| 2       | 1 |
| 3       | 1 |
| 4       | 3 |
| 5       | 4 |
| 6       | 3 |
| 7       | 4 |
| 8       | 3 |
| ======= |======  |
| Total   | 20 |

## Ejercicios

### Ejercicio 1
Clonar el siguiente repositorio:

https://github.com/essentialsofparallelcomputing/EssentialsOfParallelComputing.git

- **Pregunta 1.1.** Listar el/los comando(s) utilizado(s) y su salida correspondiente en la consola

### Ejercicio 2

Moverse al directorio `Chapter 6`, y desde ese directorio clonar el submodulo `Chapter 6` usando el siguiente comando:

`git submodule update --init Chapter6`

- **Pregunta 2.1.** Listar el/los comando(s) utilizado(s) y su salida correspondiente en la consola

### Ejercicio 3
Moverse al directorio del `matrix_mul`. La ruta es: `oneAPI-samples/DirectProgramming/C++SYCL/DenseLinearAlgebra/matrix_mul`.

- **Pregunta 3.1.** Listar el/los comando(s) utilizado(s) y su salida correspondiente en la consola

### Ejercicio 4
Comentar las siguientes líneas en el archivo fuente `src/matrix_mul_omp.cpp` (dentro de la función `main()`): 

```
//  MatrixMulOpenMpGpuOffloading();
//  cout << "Result of matrix multiplication using GPU offloading: ";
//  Result2 = VerifyResult(c);
```

Guardar los cambios en el archivo fuente. Luego ejecutar `git diff`.

- **Pregunta 4.1.** Listar la salida correspondiente en consola del comando `git diff`
- **Pregunta 4.2.** Interpretar y explicar el funcionamiento de `git diff`

### Ejercicio 5
Ejecutar el comando `make build_omp` en la terminal.

- **Pregunta 5.1.** Listar la/las salida correspondiente en la consola. 
- **Pregunta 5.1.** Indicar (usando máximo dos oraciones) que es lo que realiza el comando anterior
- **Pregunta 5.2.** Se ha ejecutado satisfactoriamente el comando anterior? Justifique su respuesta  (usando máximo dos oraciones)

Modificar el archivo `Makefile` en el modo siguiente:

```
#CXX = icpx
CXX = g++
```

```
#OMP_CXXFLAGS = -fiopenmp -fopenmp-targets=spir64 -D__STRICT_ANSI__ -g -o
OMP_CXXFLAGS = -fopenmp -D__STRICT_ANSI__ -g -o
````

Modificar el archivo `matrix_mul_omp.cpp` en el modo siguiente:

```
 #pragma omp target teams distribute parallel for map(to : a, b) \
   map(tofrom : c) thread_limit(128)
//{
     for (i = 0; i < M; i++) {
       for (k = 0; k < N; k++) {
         // Each element of the product is just the sum 1+2+...+n
          ...
         }
       }
     }
//}
```

Ejecutar nuevamente el comando `make build_omp` en la terminal.

- **Pregunta 5.1.** Listar la/las salida correspondiente en la consola. 
- **Pregunta 5.2.** Se ha ejecutado satisfactoriamente el comando anterior? Justifique su respuesta  (usando máximo dos oraciones)

### Ejercicio 6
Ejecutar el programa usando los siguientes comandos:

```
./matrix_mul_omp
```

- **Pregunta 6.1.** Listar la/las salida correspondiente en la consola

### Ejercicio 7
Contestar las siguientes preguntas de teoría. Guardar las respuestas en un archivo texto o en un markdown. 

- **Pregunta 7.1.** ¿Cuáles son las locaciones de git?
- **Pregunta 7.2.** ¿Qué es el speedup y cómo se calcula?
- **Pregunta 7.3.** Mencione dos técnicas de paralelización
- **Pregunta 7.4.** ¿Cuáles son las dos leyes fundamentales de la computación paralela?

### Ejercicio 8
Crear un repositorio (en GitHub ó GitLab) para guardar el repositorio `oneAPI-samples` y sus cambios efectuados en este ejercicio (ejm. usando `git push`).

- **Pregunta 8.1.** Listar todos los comandos `git` utilizados
- **Pregunta 8.2.** Proporcionar el link del repositorio creado (en GitHub ó GitLab) en este [Ejercicio 8](#ejercicio-8)
