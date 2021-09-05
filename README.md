# algebraic-multigrid- РУМБА v.0.14

code realese: https://github.com/kirill7785/AliceFlow

## Classical Algebraic Multigrid Method (CAMG)

The rate of convergence of many matrix inversion methods can be significantly increased by using a technique called "multigrid". The multigrid process involves performing early iterations on a fine grid, and later, iterations on nested more coarse “virtual” grids.

The results are then transferred back from the coarse grids to the original fine grid, more detailed. From a numerical point of view, the multigrid approach offers a significant advantage. For a given grid of a specific finite size, iterative methods are effective only at reducing errors, which have a wavelength of the order of a grid step (a tetrahedron edge in tetra meshes, a hexahedron edge in hexa dominant meshes). Thus, while shorter wavelengths errors disappear rather quickly, errors with a longer wavelength (on the order of the size of the computational domain) disappear very slowly (catastrophically slowly). The Multigrid method avoids this problem by using a number of coarse grids (they are nested in the original detailed grid as matrioshka) so that the available components of the error vector with a long wavelength are short-wave (easily suppressed by the usual iterative smoother method) on coarse grids from the nesting hierarchy. In order to avoid the need for coarse-mesh meshing of geometry using a number of different grid steps, we use the Algebraic multigrid method.

nvidia CUSP 0.5.1 smoothed aggregation amg memory usage comparison:

![alt text](https://github.com/kirill7785/algebraic-multigrid-method/blob/master/picture/Comparison-of-operator-complexity-SAMG-versus-AMG1R5_ru.png)

![alt text](https://github.com/kirill7785/algebraic-multigrid-method/blob/master/picture/Comparison-of-operator-complexity-RUMBAv0-14-versus-amg1r5.png)

![alt text](https://github.com/kirill7785/algebraic-multigrid-method/blob/master/picture/RS%20coarsening.png)

![alt text](https://github.com/kirill7785/algebraic-multigrid-method/blob/master/picture/RS2.png)


