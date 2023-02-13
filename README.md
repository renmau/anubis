ANUBIS is an extension of RAMSES including massive neutrino particles.

cosmo_neutrinos.nml shows an example for a run file with massive neutrinos and an extarnal hubble
function file. 

The input files are in gadget format and separate for the cdm and neutrinos. 

Changes have been made in the files:
- pm/move_fine.f90
- pm/synchro_fine.f90
- pm/init_part.f90
- pm/rho_fine.f90
- amr/amr_parameters.f90
- amr/read_params.f90
- hydro/read_hydro_params.f90

No changes have currently been implemented in the time-stepping method. 

The code was compiled with
- Intel_parallel_studio/2019/3.062
- gcc/8.3.1
- python/2.7

For multiple nodes and cpus and a log-file it can be run like:
mpirun -np 144 -perhost 16 -hostfile hostfile.txt ./ramses3d cosmo.nml | tee -a log.txt

--------------------------------------------------------------------------------------------

RAMSES README:
RAMSES version 3.10

Copyright Romain Teyssier and CEA from 1997 to 2007

Copyright Romain Teyssier and the University of Zurich from 2008 to 2013

romain.teyssier@gmail.com

This software is  an open source computer program whose  purpose is to
perform  simulations of  self-gravitating  fluids  with Adaptive  Mesh
Refinement on massively parallel computers. It is based on the Fortran
90 language and the MPI communication library.

When using the RAMSES code, please cite the following paper for proper
credit:

Teyssier, R., "Cosmological hydrodynamics with adaptive mesh refinement.
A new high resolution code called RAMSES", 2002, A&A, 385, 337

The code is available for download and documentation in
https://bitbucket.org/rteyssie/ramses

You can quickly test your installation by executing:
$ cd bin
$ make
$ cd ..
$ bin/ramses1d namelist/tube1d.nml

Enjoy !


