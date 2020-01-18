# Matrix Multiplication Benchmark - Intel Fortran

### Tech

* [Intel Fortran Compiler](https://software.intel.com/en-us/fortran-compilers) - Builds high-performance applications with Intel processors.

#### Building for source:
```sh
$ ifort test.f90 -fopenmp -mkl -g -traceback -O3 -xSSE3
```

## License

MIT

## Acknowledgments

* https://software.intel.com/en-us/forums/intel-fortran-compiler/topic/269726, woshiwuxin
