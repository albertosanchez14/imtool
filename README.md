# imtool

## Descripción

Este proyecto forma parte de la asignatura de Arquitectura de Computadores de la Universidad Carlos III de Madrid. Consiste en el desarrollo de una aplicación de procesamiento de imágenes en formato PPM, optimizada para rendimiento en C++20.

Se han desarrollado dos versiones de la aplicación:

- **imtool-soa**: Implementación basada en Structure of Arrays (SOA).
- **imtool-aos**: Implementación basada en Array of Structures (AOS).

## Funcionalidades

La aplicación permite realizar las siguientes operaciones sobre imágenes PPM:

- **info**: Obtener metadatos de una imagen.
- **maxlevel**: Escalar el número de niveles de intensidad de color.
- **resize**: Escalar el tamaño de la imagen usando interpolación bilineal.
- **cutfreq**: Eliminar los colores menos frecuentes de la imagen.
- **compress**: Comprimir la imagen usando un formato ficticio CPPM.

## Estructura del Proyecto

El proyecto está dividido en varias carpetas para mejorar la modularidad y organización:

- **common/**: Contiene código compartido por ambas implementaciones.
- **imgsoa/**: Código específico de la versión SOA.
- **imgaos/**: Código específico de la versión AOS.
- **utest-common/**: Pruebas unitarias para la biblioteca común.
- **utest-imgsoa/**: Pruebas unitarias para la biblioteca SOA.
- **utest-imgaos/**: Pruebas unitarias para la biblioteca AOS.
- **ftest-soa/**: Pruebas funcionales de imtool-soa.
- **ftest-aos/**: Pruebas funcionales de imtool-aos.
- **imagesPPM/**: Contiene imágenes de prueba.

## Compilación e Instalación

El proyecto utiliza CMake para su compilación. Para compilarlo, ejecuta los siguientes comandos en la raíz del proyecto:

```sh
mkdir build
cd build
cmake ..
make
```

Esto generará los ejecutables `imtool-soa` y `imtool-aos`.

## Uso

Para ejecutar la aplicación, usa el siguiente formato:

```sh
./imtool-<soa|aos> <input.ppm> <output.ppm> <operación> [parámetros]
```

Ejemplo de uso:

```sh
./imtool-aos input.ppm output.ppm resize 200 150
```

## Evaluación de Rendimiento y Energía

Se han realizado pruebas de rendimiento y consumo energético en el clúster Avignon, utilizando la herramienta `perf`.

## Integrantes del Proyecto

- **Amina Errami Maslaoui**
- **Alberto Sánchez del Álamo**
- **Martín Portugal González**
- **George Jose Hallak Pita**