
## Ctypes & PAPI

This repository contains an implementation of molecular dynamics simulation by connecting python, and c, using c types. Ability to connect python to a faster programming language such as C is crucial in today's world. Where most of the machine learning problems are being solved in python, it is essential to write C modules and call it, just the way numpy works! 

#### Ctypes

Ctypes is a library for Python which provides C compatible data types, and allows calling functions in shared libraries. 
*To create shared library, [geekstuff](https://www.thegeekstuff.com/2012/06/linux-shared-libraries/) gives a good introduction.* 
The c module exposed as a shared object can be called from python and he best part is, we can pass arguments by reference. This feature makes the computation at ease. In the example code repository, a simulation example can be found. One examining closely, you can see that simulation is run in python and the updations are made in C.
 
#### PAPI 

PAPI modules are used to take the performance measure from the Hardware Performance Counters.

 > Use #include <papi.h> to include/import papi module   

With PAPI, we can read various informations such as the Cache misses, hits, Store misses and many more. A detailed list of suppoerted counters for various architecture can be found [here](http://icl.cs.utk.edu/projects/papi/presets.html).  PAPI error handling mechanism throws error if particular attribute is not supported by system. A detailed description of errors can be seen [here](http://icl.cs.utk.edu/projects/papi/wiki/Error_Handling) 
