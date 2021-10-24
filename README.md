# Project Paper: *Simulation Components for Evaluating a Framework for Multidisciplinary Analyzes*

[[PDF](TeX/EHRMANNTRAUT_SimulationComponentsForEvaluatingAFrameworkForMultidisciplinaryAnalyzes.pdf)]

**Abstract:**
When monolithic approaches to solve multidisciplinary problems are not feasible, single-disciplinary solvers must be coupled. The NASA-developed *Python* framework *OpenMDAO*, which manages the communication between the single-disciplinary solvers, is used to implement various coupling methods (some of which support MPI-parallelism). The feasibility of using *OpenMDAO* on large-scale industrial problems is assessed, based on the experiences made with a small academic problem -- stationary natural convection of a fluid in a square cavity. Two deliberately simple single-disciplinary solvers -- one for the convection-diffusion equation and one for the NAVIER-STOKES equations -- are implemented in *Python*. The solutions returned from *OpenMDAO* match the reference, and the iterative convergence behaviors of the tested coupling methods match their theoretical expectations -- so there is no considerable drawback on convergence when using *OpenMDAO*. *OpenMDAO* allows to quickly test various coupling methods, but it should only be used if the single-disciplinary solvers are fixed and runtime performance is not a major issue.
  
## Content

**`/TeX`**: Contains the project paper

**`/Solvers`**: Contains the single-disciplinary solvers to couple

**`/OpenMDAO`**: Contains the *OpenMDAO*-components and the coupling scripts

**`/Examples`**: Contains various examples/tests

## Authors  
  
Simon Ehrmanntraut  
  
## Acknowledgments  
  
Special thanks go to  
  
* [PD. Dr. Stiller (TU Dresden)](https://tu-dresden.de/ing/maschinenwesen/ism/psm/die-professur/beschaeftigte/pd-dr-ing-habil-joerg-stiller)  
* [Dr. Stück and Mr. Gottfried (DLR)](https://www.dlr.de/sp/en/desktopdefault.aspx/tabid-12176/21361_read-53975/)
