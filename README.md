# imtool

## Description

Imtool is an image processing tool designed to work with PPM format images. Developed as part of the Computer Architecture course at Universidad Carlos III de Madrid, this project focuses on optimizing image transformations using C++20. It explores two different data organization strategies to evaluate their impact on performance and energy efficiency.

The project features two implementations:

- **imtool-soa**: Uses the Structure of Arrays (SOA) approach.
- **imtool-aos**: Uses the Array of Structures (AOS) approach.

By comparing these two implementations, the project provides insights into memory access patterns and computational efficiency in image processing tasks.

## Features

The application allows performing the following operations on PPM images:

- **info**: Retrieve image metadata.
- **maxlevel**: Scale the number of intensity levels.
- **resize**: Resize the image using bilinear interpolation.
- **cutfreq**: Remove the least frequent colors from the image.
- **compress**: Compress the image using a fictitious CPPM format.

## Project Structure

The project is divided into several folders to improve modularity and organization:

- **common/**: Contains code shared by both implementations.
- **imgsoa/**: Code specific to the SOA version.
- **imgaos/**: Code specific to the AOS version.
- **utest-common/**: Unit tests for the common library.
- **utest-imgsoa/**: Unit tests for the SOA library.
- **utest-imgaos/**: Unit tests for the AOS library.
- **ftest-soa/**: Functional tests for imtool-soa.
- **ftest-aos/**: Functional tests for imtool-aos.
- **imagesPPM/**: Contains test images.

## Compilation and Installation

The project uses CMake for compilation. To compile, run the following commands from the project root:

```sh
mkdir build
cd build
cmake ..
make
```

This will generate the `imtool-soa` and `imtool-aos` executables.

## Usage

To execute the application, use the following format:

```sh
./imtool-<soa|aos> <input.ppm> <output.ppm> <operation> [parameters]
```
Example usage:

```sh
./imtool-aos input.ppm output.ppm resize 200 150
```

## Performance and Energy Evaluation

Performance and energy consumption tests have been conducted on the Avignon cluster using the `perf` tool.

## Project Members

- **Alberto Sánchez del Álamo**
- **Amina Errami Maslaoui**
- **Martín Portugal González**
- **George Jose Hallak Pita**
