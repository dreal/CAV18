Title:   Artifact evaluation
Author:  Soonho Kong
Date:    15 Apr 2018
CSS: css/tufte.css

Artifact evaluation of the following paper.

```
Delta-Decision Procedures for Exists-Forall Problems over the Reals
Soonho Kong, Armando Solar-Lezama, and Sicun Gao
In CAV (International Conference on Computer Aided Verification) 2018
```

Virtual Machine
---------------

 - Image File: [http://www.cs.cmu.edu/~soonhok/CAV18_Paper248_AE.ova](http://www.cs.cmu.edu/~soonhok/CAV18_Paper248_AE.ova)
 - OS: ubuntu-16.04.4-desktop-amd64
 - Account (ID/Password): cav / ae
 - Host Platform: 2017 Macbook Pro with 2.9 GHz Intel Core i7
   (QuadCore) and 16 GB RAM running MacOS 10.13.4
   

Coverage
--------

 - Section 5.1 Nonlinear Global Optimization
    - Table 1.
 - Section 5.2 Synthesizing Lyapunov Function for Dynamical System
    - Normalized Pendulum
    - Damped Mathieu System

Instructions
------------

Log in the provided VM (ID: `cav`, PASSWORD: `ae`). Open a terminal
and execute the following instructions.

 - Table 1 in Section 5.1 (Expected Running Time <= 5min) 
    ```
    ./dreal4/bazel-bin/dreal/api/cav18_benchmark
    ./dreal4/bazel-bin/dreal/api/cav18_benchmark --local-optimization
    ```
    [[Source Code]](https://github.com/dreal/dreal4/blob/c37dfdbb64c2bb15c8f9d7250d20e98c53b948e5/dreal/api/test/cav18_benchmark.py)
	
 - Normalized Pendulum in Section 5.2 (Expected Running Time <= 1min)
    ```
    ./dreal4/bazel-bin/dreal/examples/synthesize_lyapunov_normalized_pendulum
    ```
    [[Source Code]](https://github.com/dreal/dreal4/blob/master/dreal/examples/synthesize_lyapunov_normalized_pendulum.cc)
	
 - Damped Mathieu System in Section 5.2 (Expected Running Time <= 1min)
    ```
    ./dreal4/bazel-bin/dreal/examples/synthesize_lyapunov_damped_mathieu
    ```
    [[Source Code]](https://github.com/dreal/dreal4/blob/master/dreal/examples/synthesize_lyapunov_damped_mathieu.cc)

Quality
-------

 - Source code of the implementation, dReal4, is available at
   [https://github.com/dreal/dreal4/tree/cav18](https://github.com/dreal/dreal4/tree/cav18).
 - Its
   [README.md](https://github.com/dreal/dreal4/blob/master/README.md)
   file provides build and install instructions.
 - Source code is documented using Doxygen. Documentation webpage is
   at
   [https://dreal.github.io/dreal4](https://dreal.github.io/dreal4).
 - We provide a comprehensive set of unittests, which can be executed by running
	"`bazel test //...`".
 - We provide packages for macOS (via homebrew) and Debian/Ubuntu
   Linux. The instructions are in the
   [README.md](https://github.com/dreal/dreal4/blob/master/README.md).
