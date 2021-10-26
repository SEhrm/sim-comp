Small changes must be made to `openmdao` for the couplers to work:

 1. For nonlinear block-GAUSS-SEIDEL to work on parallel groups, [these](https://github.com/OpenMDAO/OpenMDAO/blob/03f542bb92c81be88fbf0ed368ae1adf6fc8c8c8/openmdao/solvers/nonlinear/nonlinear_block_gs.py#L54-L56) lines must be removed. Of course, the method can not run in parallel, though in different processes.
 2. For linear block-JACOBI to be zero-initialized, [this](https://github.com/OpenMDAO/OpenMDAO/blob/03f542bb92c81be88fbf0ed368ae1adf6fc8c8c8/openmdao/solvers/linear/linear_block_jac.py#L30) line must be replaced by
	```python import numpy as np  
	b_vec *= -1.0 if self._iter_count != 0 else 0.
