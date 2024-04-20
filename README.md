# Higgs boson equation in de Sitter spacetime, numerical simulations

Python CUDA code using the CuPy library, and a faster Fortran CUDA code, both with visualization. 
The computations were done on Centos and Ubuntu workstations using CUDA v. 11.4 with Nvidia Tesla K-80 GPUs. The Python code also runs on Google Colaboratory. Both codes output binary files that can be postprocessed for visualization using ParaView. The Python code can also visualize line plot over the diagonal of the three-dimensional cube which is the computational domain. 


## Related publication:
["High-performance implementation of a Runge–Kutta finite-difference scheme for the Higgs boson equation in the de Sitter spacetime](https://andrasbalogh.github.io/assets/pubs/higgs-boson-desitter.pdf), <i> Communications in Nonlinear Science and Numerical Simulation,</i> Volume 68, March 2019, Pages 15-30, with J. Banda and K. Yagdjian.

* one_bubble.cuf - CUDA Fortran source file.
  * Under Ubuntu OS with NVIDIA HPC SDK installed compile from command prompt with command: nvfortran -fast -o one_bubble one_bubble.cuf
  * Execute: ./one_bubble
  * It will create 151 binary data files with the results out000.vtk - out150.vtk
  *  one_bubble.pvsm - ParaView "state" file. Use it with paraview to read the vtk files and to create visualization of the bubble formation.
  * one_bubble.mp4, one_bubble.ogv - animation in different formats
 
  * two_bubbles.cuf - CUDA Fortran source file.
  * Under Ubuntu OS with NVIDIA HPC SDK installed compile from command prompt with command: nvfortran -fast -o two_bubble two_bubble.cuf
  * Execute: ./two_bubble
  * It will create 301 binary data files with the results out000.vtk - out300.vtk
  *  two_bubbles.pvsm - ParaView "state" file. Use it with paraview to read the vtk files and to create visualization of the bubble formation.
  * two_bubbles.mp4, two_bubbles.flv, two_bubbles.ogv - animation in various formats
