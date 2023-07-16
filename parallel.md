## Getting Started: Parallel Programming
### Parallel Programming

The compass lab is often used by students for tasks related to parallel programming. Students can use the computers to write programs in different languages, test them run them for upto 4 processors and for more computation power they can use the terminal to access and use the Stromboli IT cluster. As this documentation is only related to the compass lab, only a short introduction of how to run parallel programs using compass computers will be given.

#### Parallel Computing

Parallel computing is an approach to solving complex computational problems by dividing them into smaller tasks that can be executed simultaneously. It involves running multiple computations concurrently, either on multiple processors or across a network of interconnected computers. Parallel programming refers to the techniques and methods used to design and implement programs that can effectively utilize these parallel resources, improving performance and enabling faster execution of computationally intensive tasks.

To impliment parallel computing in real life we write computer programs and in your courses you will focus mainly on **Message Passing Interface (MPI)** and **OpenMP**.


#### Introduction to MPI (Message Passing Interface):

MPI is a widely-used standard for writing parallel programs that can run on multiple processors or computers. It allows for efficient communication and coordination between processes, enabling distributed computing. MPI programs are written in languages like C, C++, or Fortran and can be used for solving computationally intensive problems, such as simulations or large-scale data processing.

#### Introduction to OpenMP:

OpenMP is a programming interface that supports shared-memory parallelism in C, C++, and Fortran. It allows developers to parallelize their code by adding directives (pragmas) to the source code, specifying which parts of the code should be executed in parallel. OpenMP is useful for exploiting multiple cores on a single machine, making it suitable for parallelizing loops, tasks, and sections of code.

#### Running MPI and OpenMP Programs:

MPI and OpenMP are already installed in the compass computers. In your courses you will mostly use C programming for MPI and openMP so some examples on how to run such programs using the terminal will be given.

First you must write a parallel computing program  then you use the terminal to compile the program and finally run the program using MPI and OpenMP.

### MPI

### 1. Compiling MPI Programs:

* Save your MPI program with a "**.c**" extension (e.g., **mpi_program.c**).

* Compile the program using an MPI-aware compiler. For example:

````````
$ mpicc mpi_program.c -o mpi_program

`````````

* This generates an executable file (**mpi_program**) that can be run on the terminal.


### 2. Running MPI Programs:

* Execute the compiled MPI program using the mpiexec or mpirun command, followed by the desired number of processes. For example:

````````
$ mpiexec -n 4 ./mpi_program

````````
* This command runs the MPI program with 4 processes, utilizing parallelism.

### OpenMP

### 1. Compiling OpenMP Programs:

* Save your OpenMP program with a "**.c**" extension (e.g., **openmp_program.c**).

* Compile the program using an OpenMP-enabled compiler. For example:

````````
$ gcc -fopenmp openmp_program.c -o openmp_program

````````

* The "**-fopenmp**" flag enables OpenMP support during compilation.

### 2. Running OpenMP Programs:


* Run the compiled OpenMP program as a regular executable file. For example:

````````

$ ./openmp_program

````````

* OpenMP automatically distributes the workload across available threads, utilizing parallelism.

### Additional Information

If you would like more information, we suggest visiting the [HPC Wiki](https://hpc-wiki.info/hpc/OpenMP_in_Small_Bites).

