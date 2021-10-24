## Results from the BOUSSINESQ Problem
File names: 
- `BoussinesqGS` (GAUSS-SEIDEL): *Re*, *Ra*, *Pr* ~ *P*, *N*_e ~ *mtol* ~ *mtol*\_internal
- `BoussinesqNJ` (NEWTON-block-JACOBI): *Re*, *Ra*, *Pr* ~ *P*, *N*_e ~ *mtol*, AG *maxiter*, AG *rho*, AG *c* ~ *mtol*\_internal
- `BoussinesqNJ` (block-JACOBI preconditioned NEWTON-KRYLOV): *Re*, *Ra*, *Pr* ~ *P*, *N*\_e ~ *mtol* ~ *mtol*\_lin, GMRES *restart* ~ *mtol*\_internal

Extensions:
- `.log`: console output from OpenMDAO
- `.hitory`: reformat from `.log`; nonlinear iteration, absolute nonlinear euclidean residual, absolute nonlinear euclidean residual before backtracking, absolute nonlinear mean root square residual, absolute nonlinear mean root square residual before backtracking
- `.gmres`: reformat from `.log` (only for JNK); NEWTON iteration, GMRES iteration, linear absolute euclidian residual, linear mean root square residual