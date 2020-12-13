# HMC

This python code represents a simplified version of the c++ code developed by Francisco-Shu Kitaura. 
It permits to sample with Hamiltonian Monte Carlo sampling from a lognormal prior and a Poisson likelihood using the common 2nd order leapfrgo method and the 4th order discretisation scheme.

One can produce mock data with the same lognormal-Poisson model by setting 
inverseCrime=True 

Alternatively one can read the number counts of the halo catalog from the BigMD simulation 
on a 64^3 mesh: nobs64.dat 
or 
on a 128^3 mesh: nobs128.dat 

To run the code one has to make sure to make the power spectrum file available:
Pk.input_zinit_normalized_at_z0.dat

Then one can run the code with second order by setting:
higherorder = False

or with 4th order by setting:
higherorder = True

One can play with a series of parameters, such as:

stepsize = 0.1 # 6e-2 # basic stepsize
Nsteps = 5 #  relevant for 2nd order
nrep = 3 # relevant for 4th order: nrep x forward steps + 1 x backward step + nrep x forward steps

Some diagnostics is shown during the running process.

