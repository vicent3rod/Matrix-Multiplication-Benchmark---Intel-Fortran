# Matrix Multiplication Benchmark - Intel Fortran

### Overview
Program to compare the performances of matrix multiplications (N by N) in three different ways: 
* Triple do-loop (Traditional Parallel processing).
* matmul(a,b) function.
* dgemm routine (INTEL MKL). 

Testing with Intel® Xeon® Processor X5670.


### Tech

* [Intel Fortran Compiler](https://software.intel.com/en-us/fortran-compilers) - Builds high-performance applications with Intel processors.



#### Building for source:
```sh
$ ifort test.f90 -fopenmp -mkl -g -traceback -O3 -xSSE3
```

|Dimensions|Do-Loop                      |matmul|DGEMM                                        |
|----------|-----------------------------|------|---------------------------------------------|
|50        |0.0023                       |0.0007|0.2342                                       |
|100       |0.0026                       |0.0023|0.0159                                       |
|200       |0.0059                       |0.0141|0.057                                        |
|300       |0.007                        |0.0525|0.0231                                       |
|400       |0.0145                       |0.1162|0.0246                                       |
|500       |0.037                        |0.2374|0.0446                                       |
|600       |0.0991                       |0.3719|0.0691                                       |
|700       |0.1488                       |0.6128|0.0624                                       |
|800       |0.1886                       |0.9044|0.1106                                       |
|900       |0.2676                       |1.2445|0.2634                                       |
|1000      |0.3495                       |1.5594|0.0742                                       |
|2000      |3.056                        |2.4477|0.4545                                       |
|3000      |9.1958                       |5.6129|1.4441                                       |
|4000      |24.5081                      |12.2439|4.3943                                       |
|5000      |68.2233                      |23.6146|9.4369                                       |
|6000      |119.7835                     |38.4411|15.9048                                      |
|7000      |188.7068                     |59.4651|25.1005                                      |
|8000      |282.5089                     |95.3954|37.9633                                      |
|9000      |401.2542                     |124.3488|57.2738                                      |
|10000     |556.9635                     |172.0648|79.8223                                      |
|11000     |738.395                      |246.489|98.5934                                      |
|12000     |955.8021                     |294.2676|122.6581                                     |
|13000     |1219.913                     |374.0526|156.4873                                     |
|14000     |1505.828                     |469.4558|201.7539                                     |
|15000     |1875.0114                    |589.8364|299.1275                                     |

## License

MIT

## Acknowledgments

* https://software.intel.com/en-us/forums/intel-fortran-compiler/topic/269726, woshiwuxin
