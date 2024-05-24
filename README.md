# server-simulation-24th-may-2024
myc-max A and B chains simulation



user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ module load gromacs-2023 
Loading gromacs-2023
  Loading requirement: openmpi-5.0.0 plumed2-2.9.0 fftw-3.3.10
user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx grompp -f step4.0_minimization.mdp -c step3_input.gro -r step3_input.gro -p topol.top -n index.ndx -o em.tpr
                :-) GROMACS - gmx grompp, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx grompp -f step4.0_minimization.mdp -c step3_input.gro -r step3_input.gro -p topol.top -n index.ndx -o em.tpr

Setting the LD random seed to -413205507

Generated 700 of the 703 non-bonded parameter combinations
Generating 1-4 interactions: fudge = 1

Generated 378 of the 703 1-4 parameter combinations

Excluding 3 bonded neighbours molecule type 'PROA'

turning H bonds into constraints...

Excluding 3 bonded neighbours molecule type 'PROB'

turning H bonds into constraints...

Excluding 1 bonded neighbours molecule type 'POT'

turning H bonds into constraints...

Excluding 1 bonded neighbours molecule type 'CLA'

turning H bonds into constraints...

Excluding 2 bonded neighbours molecule type 'TIP3'

turning H bonds into constraints...
Number of degrees of freedom in T-Coupling group rest is 369887.00
The integrator does not provide a ensemble temperature, there is no system ensemble temperature

The largest distance between excluded atoms is 0.395 nm between atom 382 and 393

NOTE 1 [file step4.0_minimization.mdp]:
  Removing center of mass motion in the presence of position restraints
  might cause artifacts. When you are using position restraints to
  equilibrate a macro-molecule, the artifacts are usually negligible.

Calculating fourier grid dimensions for X Y Z
Using a fourier grid of 108x108x108, spacing 0.116 0.116 0.116

Estimate for the relative computational load of the PME mesh part: 0.23

This run will generate roughly 14 Mb of data

There was 1 NOTE

GROMACS reminds you: ""What are the biological implications of your research?" - "Well, I simulate water." " (Petter Johansson)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx mdrun -v -deffnm em -nb gpu
                 :-) GROMACS - gmx mdrun, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx mdrun -v -deffnm em -nb gpu

Reading file em.tpr, VERSION 2023-plumed_2.9.0 (single precision)
On host user 1 GPU selected for this run.
Mapping of GPU IDs to the 4 GPU tasks in the 4 ranks on this node:
  PP:0,PP:0,PP:0,PP:0
PP tasks will do (non-perturbed) short-ranged interactions on the GPU
PP task will update and constrain coordinates on the CPU
Using 4 MPI threads
Using 28 OpenMP threads per tMPI thread


Steepest Descents:
   Tolerance (Fmax)   =  1.00000e+03
   Number of steps    =         5000
Step=    0, Dmax= 1.0e-02 nm, Epot= -2.88610e+06 Fmax= 8.78425e+03, atom= 1350
Step=    1, Dmax= 1.0e-02 nm, Epot= -2.88757e+06 Fmax= 4.48169e+03, atom= 1349
Step=    2, Dmax= 1.2e-02 nm, Epot= -2.88960e+06 Fmax= 9.22400e+03, atom= 1349
Step=    3, Dmax= 1.4e-02 nm, Epot= -2.89066e+06 Fmax= 1.08955e+04, atom= 1349
Step=    4, Dmax= 1.7e-02 nm, Epot= -2.89167e+06 Fmax= 1.17714e+04, atom= 1349
Step=    5, Dmax= 2.1e-02 nm, Epot= -2.89265e+06 Fmax= 1.62929e+04, atom= 1349
Step=    6, Dmax= 2.5e-02 nm, Epot= -2.89359e+06 Fmax= 1.63665e+04, atom= 1349
Step=    7, Dmax= 3.0e-02 nm, Epot= -2.89437e+06 Fmax= 2.35540e+04, atom= 1349
Step=    8, Dmax= 3.6e-02 nm, Epot= -2.89527e+06 Fmax= 2.33628e+04, atom= 1349
Step=    9, Dmax= 4.3e-02 nm, Epot= -2.89574e+06 Fmax= 3.37697e+04, atom= 1349
Step=   10, Dmax= 5.2e-02 nm, Epot= -2.89661e+06 Fmax= 3.35446e+04, atom= 1349
Step=   12, Dmax= 3.1e-02 nm, Epot= -2.89818e+06 Fmax= 6.89492e+03, atom= 1349
Step=   13, Dmax= 3.7e-02 nm, Epot= -2.89939e+06 Fmax= 4.24253e+04, atom= 1349
Step=   14, Dmax= 4.5e-02 nm, Epot= -2.90137e+06 Fmax= 1.68853e+04, atom= 1349
Step=   16, Dmax= 2.7e-02 nm, Epot= -2.90213e+06 Fmax= 1.80838e+04, atom= 1349
Step=   17, Dmax= 3.2e-02 nm, Epot= -2.90281e+06 Fmax= 2.39782e+04, atom= 1349
Step=   18, Dmax= 3.9e-02 nm, Epot= -2.90350e+06 Fmax= 2.61211e+04, atom= 1349
Step=   19, Dmax= 4.6e-02 nm, Epot= -2.90395e+06 Fmax= 3.46688e+04, atom= 1349
Step=   20, Dmax= 5.5e-02 nm, Epot= -2.90455e+06 Fmax= 3.72799e+04, atom= 1349
Step=   22, Dmax= 3.3e-02 nm, Epot= -2.90607e+06 Fmax= 5.86923e+03, atom= 1349
Step=   23, Dmax= 4.0e-02 nm, Epot= -2.90744e+06 Fmax= 4.70060e+04, atom= 1349
Step=   24, Dmax= 4.8e-02 nm, Epot= -2.90948e+06 Fmax= 1.63344e+04, atom= 1349
Step=   26, Dmax= 2.9e-02 nm, Epot= -2.91012e+06 Fmax= 2.10116e+04, atom= 1349
Step=   27, Dmax= 3.5e-02 nm, Epot= -2.91073e+06 Fmax= 2.41285e+04, atom= 1349
Step=   28, Dmax= 4.1e-02 nm, Epot= -2.91125e+06 Fmax= 2.95482e+04, atom= 1349
Step=   29, Dmax= 5.0e-02 nm, Epot= -2.91170e+06 Fmax= 3.55995e+04, atom= 1349
Step=   30, Dmax= 6.0e-02 nm, Epot= -2.91203e+06 Fmax= 4.15197e+04, atom= 1349
Step=   31, Dmax= 7.2e-02 nm, Epot= -2.91206e+06 Fmax= 5.23010e+04, atom= 1349
Step=   32, Dmax= 8.6e-02 nm, Epot= -2.91216e+06 Fmax= 5.84792e+04, atom= 1349
Step=   34, Dmax= 5.2e-02 nm, Epot= -2.91504e+06 Fmax= 7.58304e+03, atom= 1349
Step=   36, Dmax= 3.1e-02 nm, Epot= -2.91588e+06 Fmax= 3.38785e+04, atom= 1349
Step=   37, Dmax= 3.7e-02 nm, Epot= -2.91703e+06 Fmax= 1.45278e+04, atom= 1349
Step=   39, Dmax= 2.2e-02 nm, Epot= -2.91764e+06 Fmax= 1.43505e+04, atom= 1349
Step=   40, Dmax= 2.7e-02 nm, Epot= -2.91821e+06 Fmax= 2.04732e+04, atom= 1349
Step=   41, Dmax= 3.2e-02 nm, Epot= -2.91880e+06 Fmax= 2.10799e+04, atom= 1349
Step=   42, Dmax= 3.8e-02 nm, Epot= -2.91921e+06 Fmax= 2.92075e+04, atom= 1349
Step=   43, Dmax= 4.6e-02 nm, Epot= -2.91974e+06 Fmax= 3.05405e+04, atom= 1349
Step=   44, Dmax= 5.5e-02 nm, Epot= -2.91984e+06 Fmax= 4.19854e+04, atom= 1349
Step=   45, Dmax= 6.6e-02 nm, Epot= -2.92027e+06 Fmax= 4.38333e+04, atom= 1349
Step=   47, Dmax= 4.0e-02 nm, Epot= -2.92201e+06 Fmax= 7.48999e+03, atom= 1349
Step=   48, Dmax= 4.8e-02 nm, Epot= -2.92201e+06 Fmax= 5.55906e+04, atom= 1349
Step=   49, Dmax= 5.7e-02 nm, Epot= -2.92448e+06 Fmax= 1.96743e+04, atom= 1349
Step=   51, Dmax= 3.4e-02 nm, Epot= -2.92493e+06 Fmax= 2.49103e+04, atom= 1349
Step=   52, Dmax= 4.1e-02 nm, Epot= -2.92536e+06 Fmax= 2.89543e+04, atom= 1349
Step=   53, Dmax= 5.0e-02 nm, Epot= -2.92565e+06 Fmax= 3.51468e+04, atom= 1349
Step=   54, Dmax= 6.0e-02 nm, Epot= -2.92584e+06 Fmax= 4.26457e+04, atom= 1349
Step=   55, Dmax= 7.1e-02 nm, Epot= -2.92588e+06 Fmax= 4.94034e+04, atom= 1349
Step=   57, Dmax= 4.3e-02 nm, Epot= -2.92801e+06 Fmax= 5.62208e+03, atom= 1349
Step=   59, Dmax= 2.6e-02 nm, Epot= -2.92895e+06 Fmax= 2.87150e+04, atom= 1349
Step=   60, Dmax= 3.1e-02 nm, Epot= -2.92986e+06 Fmax= 1.15527e+04, atom= 1349
Step=   61, Dmax= 3.7e-02 nm, Epot= -2.93000e+06 Fmax= 3.60606e+04, atom= 1349
Step=   62, Dmax= 4.4e-02 nm, Epot= -2.93106e+06 Fmax= 2.17691e+04, atom= 1349
Step=   64, Dmax= 2.7e-02 nm, Epot= -2.93170e+06 Fmax= 1.29501e+04, atom= 1349
Step=   65, Dmax= 3.2e-02 nm, Epot= -2.93200e+06 Fmax= 2.87269e+04, atom= 1349
Step=   66, Dmax= 3.8e-02 nm, Epot= -2.93271e+06 Fmax= 2.11024e+04, atom= 1349
Step=   68, Dmax= 2.3e-02 nm, Epot= -2.93335e+06 Fmax= 8.73427e+03, atom= 1349
Step=   69, Dmax= 2.8e-02 nm, Epot= -2.93383e+06 Fmax= 2.71593e+04, atom= 1349
Step=   70, Dmax= 3.3e-02 nm, Epot= -2.93459e+06 Fmax= 1.60479e+04, atom= 1349
Step=   72, Dmax= 2.0e-02 nm, Epot= -2.93511e+06 Fmax= 9.87014e+03, atom= 1349
Step=   73, Dmax= 2.4e-02 nm, Epot= -2.93558e+06 Fmax= 2.12622e+04, atom= 1349
Step=   74, Dmax= 2.9e-02 nm, Epot= -2.93615e+06 Fmax= 1.59646e+04, atom= 1349
Step=   75, Dmax= 3.4e-02 nm, Epot= -2.93635e+06 Fmax= 2.90489e+04, atom= 1349
Step=   76, Dmax= 4.1e-02 nm, Epot= -2.93696e+06 Fmax= 2.44765e+04, atom= 1349
Step=   78, Dmax= 2.5e-02 nm, Epot= -2.93770e+06 Fmax= 7.59757e+03, atom= 1349
Step=   79, Dmax= 3.0e-02 nm, Epot= -2.93813e+06 Fmax= 3.10408e+04, atom= 1349
Step=   80, Dmax= 3.6e-02 nm, Epot= -2.93907e+06 Fmax= 1.54558e+04, atom= 1349
Step=   82, Dmax= 2.1e-02 nm, Epot= -2.93954e+06 Fmax= 1.23835e+04, atom= 1349
Step=   83, Dmax= 2.6e-02 nm, Epot= -2.93992e+06 Fmax= 2.11053e+04, atom= 1349
Step=   84, Dmax= 3.1e-02 nm, Epot= -2.94041e+06 Fmax= 1.88830e+04, atom= 1349
Step=   85, Dmax= 3.7e-02 nm, Epot= -2.94056e+06 Fmax= 2.94906e+04, atom= 1349
Step=   86, Dmax= 4.4e-02 nm, Epot= -2.94105e+06 Fmax= 2.79920e+04, atom= 1349
Step=   88, Dmax= 2.7e-02 nm, Epot= -2.94194e+06 Fmax= 6.45563e+03, atom= 1349
Step=   89, Dmax= 3.2e-02 nm, Epot= -2.94231e+06 Fmax= 3.51965e+04, atom= 1349
Step=   90, Dmax= 3.8e-02 nm, Epot= -2.94349e+06 Fmax= 1.48402e+04, atom= 1349
Step=   92, Dmax= 2.3e-02 nm, Epot= -2.94392e+06 Fmax= 1.50453e+04, atom= 1349
Step=   93, Dmax= 2.8e-02 nm, Epot= -2.94425e+06 Fmax= 2.09589e+04, atom= 1349
Step=   94, Dmax= 3.3e-02 nm, Epot= -2.94464e+06 Fmax= 2.19838e+04, atom= 1349
Step=   95, Dmax= 4.0e-02 nm, Epot= -2.94479e+06 Fmax= 2.99888e+04, atom= 1349
Step=   96, Dmax= 4.8e-02 nm, Epot= -2.94510e+06 Fmax= 3.17311e+04, atom= 1349
Step=   98, Dmax= 2.9e-02 nm, Epot= -2.94620e+06 Fmax= 5.25692e+03, atom= 1349
Step=   99, Dmax= 3.4e-02 nm, Epot= -2.94652e+06 Fmax= 3.97532e+04, atom= 1349
Step=  100, Dmax= 4.1e-02 nm, Epot= -2.94807e+06 Fmax= 1.41503e+04, atom= 1349
Step=  102, Dmax= 2.5e-02 nm, Epot= -2.94841e+06 Fmax= 1.78989e+04, atom= 1349
Step=  103, Dmax= 3.0e-02 nm, Epot= -2.94875e+06 Fmax= 2.08091e+04, atom= 1349
Step=  104, Dmax= 3.6e-02 nm, Epot= -2.94899e+06 Fmax= 2.52959e+04, atom= 1349
Step=  105, Dmax= 4.3e-02 nm, Epot= -2.94916e+06 Fmax= 3.05445e+04, atom= 1349
Step=  106, Dmax= 5.1e-02 nm, Epot= -2.94925e+06 Fmax= 3.57155e+04, atom= 1349
Step=  108, Dmax= 3.1e-02 nm, Epot= -2.95065e+06 Fmax= 3.99859e+03, atom= 1349
Step=  109, Dmax= 3.7e-02 nm, Epot= -2.95093e+06 Fmax= 4.48886e+04, atom= 1349
Step=  110, Dmax= 4.4e-02 nm, Epot= -2.95306e+06 Fmax= 1.33455e+04, atom= 1349
Step=  112, Dmax= 2.7e-02 nm, Epot= -2.95328e+06 Fmax= 2.09455e+04, atom= 1349
Step=  113, Dmax= 3.2e-02 nm, Epot= -2.95367e+06 Fmax= 2.06790e+04, atom= 1349
Step=  114, Dmax= 3.8e-02 nm, Epot= -2.95369e+06 Fmax= 2.88087e+04, atom= 1349
Step=  115, Dmax= 4.6e-02 nm, Epot= -2.95394e+06 Fmax= 3.11954e+04, atom= 1349
Step=  117, Dmax= 2.8e-02 nm, Epot= -2.95512e+06 Fmax= 4.84038e+03, atom= 1349
Step=  118, Dmax= 3.3e-02 nm, Epot= -2.95535e+06 Fmax= 3.78625e+04, atom= 1349
Step=  119, Dmax= 4.0e-02 nm, Epot= -2.95682e+06 Fmax= 1.38697e+04, atom= 1349
Step=  121, Dmax= 2.4e-02 nm, Epot= -2.95712e+06 Fmax= 1.72994e+04, atom= 1349
Step=  122, Dmax= 2.9e-02 nm, Epot= -2.95740e+06 Fmax= 1.97355e+04, atom= 1349
Step=  123, Dmax= 3.4e-02 nm, Epot= -2.95756e+06 Fmax= 2.50971e+04, atom= 1349
Step=  124, Dmax= 4.1e-02 nm, Epot= -2.95774e+06 Fmax= 2.81754e+04, atom= 1349
Step=  126, Dmax= 2.5e-02 nm, Epot= -2.95876e+06 Fmax= 3.77806e+03, atom= 1349
Step=  127, Dmax= 3.0e-02 nm, Epot= -2.95915e+06 Fmax= 3.51546e+04, atom= 1349
Step=  128, Dmax= 3.6e-02 nm, Epot= -2.96065e+06 Fmax= 1.14053e+04, atom= 1349
Step=  130, Dmax= 2.1e-02 nm, Epot= -2.96090e+06 Fmax= 1.62153e+04, atom= 1349
Step=  131, Dmax= 2.6e-02 nm, Epot= -2.96122e+06 Fmax= 1.71997e+04, atom= 1349
Step=  132, Dmax= 3.1e-02 nm, Epot= -2.96135e+06 Fmax= 2.25889e+04, atom= 1349
Step=  133, Dmax= 3.7e-02 nm, Epot= -2.96155e+06 Fmax= 2.55858e+04, atom= 1349
Step=  135, Dmax= 2.2e-02 nm, Epot= -2.96248e+06 Fmax= 3.32451e+03, atom= 1349
Step=  136, Dmax= 2.7e-02 nm, Epot= -2.96314e+06 Fmax= 3.09454e+04, atom= 1349
Step=  137, Dmax= 3.2e-02 nm, Epot= -2.96431e+06 Fmax= 1.05332e+04, atom= 1349
Step=  139, Dmax= 1.9e-02 nm, Epot= -2.96458e+06 Fmax= 1.45338e+04, atom= 1349
Step=  140, Dmax= 2.3e-02 nm, Epot= -2.96488e+06 Fmax= 1.52091e+04, atom= 1349
Step=  141, Dmax= 2.8e-02 nm, Epot= -2.96503e+06 Fmax= 2.07984e+04, atom= 1349
Step=  142, Dmax= 3.3e-02 nm, Epot= -2.96529e+06 Fmax= 2.20133e+04, atom= 1349
Step=  144, Dmax= 2.0e-02 nm, Epot= -2.96604e+06 Fmax= 3.69267e+03, atom= 1349
Step=  145, Dmax= 2.4e-02 nm, Epot= -2.96643e+06 Fmax= 2.73665e+04, atom= 1349
Step=  146, Dmax= 2.9e-02 nm, Epot= -2.96748e+06 Fmax= 9.94040e+03, atom= 1349
Step=  148, Dmax= 1.7e-02 nm, Epot= -2.96776e+06 Fmax= 1.22809e+04, atom= 1349
Step=  149, Dmax= 2.1e-02 nm, Epot= -2.96800e+06 Fmax= 1.45501e+04, atom= 1349
Step=  150, Dmax= 2.5e-02 nm, Epot= -2.96823e+06 Fmax= 1.74268e+04, atom= 1349
Step=  151, Dmax= 3.0e-02 nm, Epot= -2.96838e+06 Fmax= 2.12572e+04, atom= 1349
Step=  152, Dmax= 3.5e-02 nm, Epot= -2.96848e+06 Fmax= 2.47325e+04, atom= 1349
Step=  154, Dmax= 2.1e-02 nm, Epot= -2.96947e+06 Fmax= 2.88410e+03, atom= 1349
Step=  155, Dmax= 2.6e-02 nm, Epot= -2.96982e+06 Fmax= 3.07119e+04, atom= 1349
Step=  156, Dmax= 3.1e-02 nm, Epot= -2.97129e+06 Fmax= 9.51931e+03, atom= 1349
Step=  158, Dmax= 1.8e-02 nm, Epot= -2.97149e+06 Fmax= 1.43313e+04, atom= 2656
Step=  159, Dmax= 2.2e-02 nm, Epot= -2.97178e+06 Fmax= 1.44909e+04, atom= 1349
Step=  160, Dmax= 2.6e-02 nm, Epot= -2.97184e+06 Fmax= 2.02990e+04, atom= 2656
Step=  161, Dmax= 3.2e-02 nm, Epot= -2.97208e+06 Fmax= 2.11399e+04, atom= 2656
Step=  163, Dmax= 1.9e-02 nm, Epot= -2.97290e+06 Fmax= 3.72029e+03, atom= 1349
Step=  164, Dmax= 2.3e-02 nm, Epot= -2.97305e+06 Fmax= 2.60567e+04, atom= 1349
Step=  165, Dmax= 2.7e-02 nm, Epot= -2.97414e+06 Fmax= 9.73487e+03, atom= 2656
Step=  167, Dmax= 1.6e-02 nm, Epot= -2.97438e+06 Fmax= 1.17957e+04, atom= 1349
Step=  168, Dmax= 2.0e-02 nm, Epot= -2.97460e+06 Fmax= 1.41101e+04, atom= 2656
Step=  169, Dmax= 2.4e-02 nm, Epot= -2.97479e+06 Fmax= 1.68390e+04, atom= 2656
Step=  170, Dmax= 2.8e-02 nm, Epot= -2.97490e+06 Fmax= 2.05401e+04, atom= 2656
Step=  171, Dmax= 3.4e-02 nm, Epot= -2.97497e+06 Fmax= 2.39544e+04, atom= 2656
Step=  173, Dmax= 2.1e-02 nm, Epot= -2.97598e+06 Fmax= 2.79961e+03, atom= 1349
Step=  174, Dmax= 2.5e-02 nm, Epot= -2.97631e+06 Fmax= 2.90309e+04, atom= 1349
Step=  175, Dmax= 3.0e-02 nm, Epot= -2.97764e+06 Fmax= 9.43077e+03, atom= 1349
Step=  177, Dmax= 1.8e-02 nm, Epot= -2.97782e+06 Fmax= 1.38682e+04, atom= 1349
Step=  178, Dmax= 2.1e-02 nm, Epot= -2.97808e+06 Fmax= 1.37282e+04, atom= 1349
Step=  179, Dmax= 2.6e-02 nm, Epot= -2.97811e+06 Fmax= 1.97065e+04, atom= 1349
Step=  180, Dmax= 3.1e-02 nm, Epot= -2.97836e+06 Fmax= 2.00238e+04, atom= 1349
Step=  182, Dmax= 1.8e-02 nm, Epot= -2.97911e+06 Fmax= 4.11444e+03, atom= 2656
Step=  183, Dmax= 2.2e-02 nm, Epot= -2.97919e+06 Fmax= 2.47315e+04, atom= 2656
Step=  184, Dmax= 2.6e-02 nm, Epot= -2.98013e+06 Fmax= 9.93121e+03, atom= 2656
Step=  186, Dmax= 1.6e-02 nm, Epot= -2.98038e+06 Fmax= 1.08362e+04, atom= 2656
Step=  187, Dmax= 1.9e-02 nm, Epot= -2.98056e+06 Fmax= 1.40184e+04, atom= 2656
Step=  188, Dmax= 2.3e-02 nm, Epot= -2.98077e+06 Fmax= 1.59323e+04, atom= 2656
Step=  189, Dmax= 2.7e-02 nm, Epot= -2.98086e+06 Fmax= 1.98014e+04, atom= 2656
Step=  190, Dmax= 3.3e-02 nm, Epot= -2.98094e+06 Fmax= 2.33896e+04, atom= 2656
Step=  192, Dmax= 2.0e-02 nm, Epot= -2.98184e+06 Fmax= 2.61808e+03, atom= 2656
Step=  193, Dmax= 2.4e-02 nm, Epot= -2.98240e+06 Fmax= 2.81423e+04, atom= 2656
Step=  194, Dmax= 2.8e-02 nm, Epot= -2.98344e+06 Fmax= 9.12647e+03, atom= 2656
Step=  196, Dmax= 1.7e-02 nm, Epot= -2.98363e+06 Fmax= 1.33094e+04, atom= 2656
Step=  197, Dmax= 2.0e-02 nm, Epot= -2.98389e+06 Fmax= 1.34031e+04, atom= 2656
Step=  198, Dmax= 2.5e-02 nm, Epot= -2.98399e+06 Fmax= 1.88460e+04, atom= 2656
Step=  199, Dmax= 2.9e-02 nm, Epot= -2.98420e+06 Fmax= 1.95888e+04, atom= 2656
Step=  201, Dmax= 1.8e-02 nm, Epot= -2.98480e+06 Fmax= 3.39971e+03, atom= 2656
Step=  202, Dmax= 2.1e-02 nm, Epot= -2.98509e+06 Fmax= 2.44075e+04, atom= 2656
Step=  203, Dmax= 2.5e-02 nm, Epot= -2.98591e+06 Fmax= 8.85678e+03, atom= 2656
Step=  205, Dmax= 1.5e-02 nm, Epot= -2.98612e+06 Fmax= 1.10984e+04, atom= 2656
Step=  206, Dmax= 1.8e-02 nm, Epot= -2.98634e+06 Fmax= 1.29194e+04, atom= 2656
Step=  207, Dmax= 2.2e-02 nm, Epot= -2.98650e+06 Fmax= 1.57858e+04, atom= 2656
Step=  208, Dmax= 2.6e-02 nm, Epot= -2.98665e+06 Fmax= 1.88441e+04, atom= 2656
Step=  209, Dmax= 3.2e-02 nm, Epot= -2.98672e+06 Fmax= 2.24248e+04, atom= 2656
Step=  211, Dmax= 1.9e-02 nm, Epot= -2.98748e+06 Fmax= 2.25136e+03, atom= 2656
Step=  212, Dmax= 2.3e-02 nm, Epot= -2.98805e+06 Fmax= 2.78814e+04, atom= 2656
Step=  213, Dmax= 2.7e-02 nm, Epot= -2.98915e+06 Fmax= 7.91890e+03, atom= 2656
Step=  215, Dmax= 1.6e-02 nm, Epot= -2.98931e+06 Fmax= 1.34187e+04, atom= 2656
Step=  216, Dmax= 2.0e-02 nm, Epot= -2.98958e+06 Fmax= 1.24036e+04, atom= 2656
Step=  217, Dmax= 2.4e-02 nm, Epot= -2.98962e+06 Fmax= 1.84032e+04, atom= 2656
Step=  218, Dmax= 2.8e-02 nm, Epot= -2.98984e+06 Fmax= 1.88050e+04, atom= 2656
Step=  220, Dmax= 1.7e-02 nm, Epot= -2.99043e+06 Fmax= 3.58796e+03, atom= 2656
Step=  221, Dmax= 2.0e-02 nm, Epot= -2.99064e+06 Fmax= 2.31139e+04, atom= 2656
Step=  222, Dmax= 2.5e-02 nm, Epot= -2.99137e+06 Fmax= 9.02328e+03, atom= 2656
Step=  224, Dmax= 1.5e-02 nm, Epot= -2.99158e+06 Fmax= 1.02321e+04, atom= 2656
Step=  225, Dmax= 1.8e-02 nm, Epot= -2.99177e+06 Fmax= 1.28221e+04, atom= 2656
Step=  226, Dmax= 2.1e-02 nm, Epot= -2.99195e+06 Fmax= 1.49405e+04, atom= 2656
Step=  227, Dmax= 2.5e-02 nm, Epot= -2.99206e+06 Fmax= 1.82093e+04, atom= 2656
Step=  228, Dmax= 3.1e-02 nm, Epot= -2.99215e+06 Fmax= 2.18234e+04, atom= 2656
Step=  229, Dmax= 3.7e-02 nm, Epot= -2.99215e+06 Fmax= 2.58246e+04, atom= 2656
Step=  231, Dmax= 2.2e-02 nm, Epot= -2.99308e+06 Fmax= 2.65407e+03, atom= 2656
Step=  232, Dmax= 2.6e-02 nm, Epot= -2.99317e+06 Fmax= 3.21844e+04, atom= 2656
Step=  233, Dmax= 3.2e-02 nm, Epot= -2.99459e+06 Fmax= 9.17953e+03, atom= 2656
Step=  235, Dmax= 1.9e-02 nm, Epot= -2.99467e+06 Fmax= 1.54560e+04, atom= 2656
Step=  236, Dmax= 2.3e-02 nm, Epot= -2.99494e+06 Fmax= 1.43844e+04, atom= 2656
Step=  238, Dmax= 1.4e-02 nm, Epot= -2.99534e+06 Fmax= 3.55696e+03, atom= 2656
Step=  239, Dmax= 1.6e-02 nm, Epot= -2.99560e+06 Fmax= 1.78950e+04, atom= 2656
Step=  240, Dmax= 2.0e-02 nm, Epot= -2.99609e+06 Fmax= 7.88322e+03, atom= 2656
Step=  242, Dmax= 1.2e-02 nm, Epot= -2.99630e+06 Fmax= 7.54063e+03, atom= 2656
Step=  243, Dmax= 1.4e-02 nm, Epot= -2.99649e+06 Fmax= 1.09741e+04, atom= 2656
Step=  244, Dmax= 1.7e-02 nm, Epot= -2.99670e+06 Fmax= 1.12764e+04, atom= 2656
Step=  245, Dmax= 2.0e-02 nm, Epot= -2.99682e+06 Fmax= 1.53400e+04, atom= 2656
Step=  246, Dmax= 2.4e-02 nm, Epot= -2.99699e+06 Fmax= 1.67433e+04, atom= 2656
Step=  247, Dmax= 2.9e-02 nm, Epot= -2.99700e+06 Fmax= 2.15226e+04, atom= 2656
Step=  248, Dmax= 3.5e-02 nm, Epot= -2.99704e+06 Fmax= 2.47447e+04, atom= 2656
Step=  250, Dmax= 2.1e-02 nm, Epot= -2.99792e+06 Fmax= 3.12600e+03, atom= 2656
Step=  251, Dmax= 2.5e-02 nm, Epot= -2.99803e+06 Fmax= 2.98611e+04, atom= 2656
Step=  252, Dmax= 3.0e-02 nm, Epot= -2.99909e+06 Fmax= 1.00795e+04, atom= 2656
Step=  254, Dmax= 1.8e-02 nm, Epot= -2.99923e+06 Fmax= 1.39254e+04, atom= 2656
Step=  255, Dmax= 2.2e-02 nm, Epot= -2.99942e+06 Fmax= 1.46914e+04, atom= 2656
Step=  256, Dmax= 2.6e-02 nm, Epot= -2.99946e+06 Fmax= 1.98435e+04, atom= 2656
Step=  257, Dmax= 3.2e-02 nm, Epot= -2.99960e+06 Fmax= 2.13191e+04, atom= 2656
Step=  259, Dmax= 1.9e-02 nm, Epot= -3.00023e+06 Fmax= 3.28589e+03, atom= 2656
Step=  260, Dmax= 2.3e-02 nm, Epot= -3.00031e+06 Fmax= 2.65748e+04, atom= 2656
Step=  261, Dmax= 2.7e-02 nm, Epot= -3.00122e+06 Fmax= 9.05667e+03, atom= 2656
Step=  263, Dmax= 1.6e-02 nm, Epot= -3.00137e+06 Fmax= 1.23076e+04, atom= 2656
Step=  264, Dmax= 2.0e-02 nm, Epot= -3.00155e+06 Fmax= 1.34166e+04, atom= 2656
Step=  265, Dmax= 2.4e-02 nm, Epot= -3.00164e+06 Fmax= 1.73249e+04, atom= 2656
Step=  266, Dmax= 2.8e-02 nm, Epot= -3.00175e+06 Fmax= 1.97645e+04, atom= 2656
Step=  268, Dmax= 1.7e-02 nm, Epot= -3.00232e+06 Fmax= 2.57264e+03, atom= 2656
Step=  269, Dmax= 2.0e-02 nm, Epot= -3.00274e+06 Fmax= 2.38903e+04, atom= 2656
Step=  270, Dmax= 2.4e-02 nm, Epot= -3.00343e+06 Fmax= 8.14274e+03, atom= 2656
Step=  272, Dmax= 1.5e-02 nm, Epot= -3.00361e+06 Fmax= 1.10908e+04, atom= 2656
Step=  273, Dmax= 1.8e-02 nm, Epot= -3.00379e+06 Fmax= 1.18915e+04, atom= 2656
Step=  274, Dmax= 2.1e-02 nm, Epot= -3.00390e+06 Fmax= 1.57942e+04, atom= 2656
Step=  275, Dmax= 2.5e-02 nm, Epot= -3.00405e+06 Fmax= 1.72669e+04, atom= 2656
Step=  277, Dmax= 1.5e-02 nm, Epot= -3.00449e+06 Fmax= 2.50217e+03, atom= 2656
Step=  278, Dmax= 1.8e-02 nm, Epot= -3.00490e+06 Fmax= 2.14860e+04, atom= 2656
Step=  279, Dmax= 2.2e-02 nm, Epot= -3.00550e+06 Fmax= 7.11315e+03, atom= 2656
Step=  281, Dmax= 1.3e-02 nm, Epot= -3.00568e+06 Fmax= 1.00396e+04, atom= 2656
Step=  282, Dmax= 1.6e-02 nm, Epot= -3.00586e+06 Fmax= 1.05956e+04, atom= 2656
Step=  283, Dmax= 1.9e-02 nm, Epot= -3.00598e+06 Fmax= 1.40926e+04, atom= 2656
Step=  284, Dmax= 2.3e-02 nm, Epot= -3.00614e+06 Fmax= 1.56524e+04, atom= 2656
Step=  285, Dmax= 2.7e-02 nm, Epot= -3.00618e+06 Fmax= 1.98481e+04, atom= 2656
Step=  286, Dmax= 3.3e-02 nm, Epot= -3.00624e+06 Fmax= 2.30435e+04, atom= 2656
Step=  288, Dmax= 2.0e-02 nm, Epot= -3.00695e+06 Fmax= 2.79043e+03, atom= 2656
Step=  289, Dmax= 2.4e-02 nm, Epot= -3.00718e+06 Fmax= 2.77723e+04, atom= 2656
Step=  290, Dmax= 2.8e-02 nm, Epot= -3.00804e+06 Fmax= 9.25439e+03, atom= 2656
Step=  292, Dmax= 1.7e-02 nm, Epot= -3.00817e+06 Fmax= 1.30028e+04, atom= 2656
Step=  293, Dmax= 2.0e-02 nm, Epot= -3.00835e+06 Fmax= 1.35411e+04, atom= 2656
Step=  294, Dmax= 2.4e-02 nm, Epot= -3.00840e+06 Fmax= 1.84749e+04, atom= 2656
Step=  295, Dmax= 2.9e-02 nm, Epot= -3.00854e+06 Fmax= 1.97100e+04, atom= 2656
Step=  297, Dmax= 1.8e-02 nm, Epot= -3.00906e+06 Fmax= 3.11814e+03, atom= 2656
Step=  298, Dmax= 2.1e-02 nm, Epot= -3.00921e+06 Fmax= 2.45677e+04, atom= 2656
Step=  299, Dmax= 2.5e-02 nm, Epot= -3.00993e+06 Fmax= 8.47268e+03, atom= 2656
Step=  301, Dmax= 1.5e-02 nm, Epot= -3.01009e+06 Fmax= 1.13485e+04, atom= 2656
Step=  302, Dmax= 1.8e-02 nm, Epot= -3.01025e+06 Fmax= 1.25005e+04, atom= 2656
Step=  303, Dmax= 2.2e-02 nm, Epot= -3.01034e+06 Fmax= 1.60177e+04, atom= 2656
Step=  304, Dmax= 2.6e-02 nm, Epot= -3.01045e+06 Fmax= 1.83680e+04, atom= 2656
Step=  305, Dmax= 3.1e-02 nm, Epot= -3.01045e+06 Fmax= 2.26298e+04, atom= 2656
Step=  307, Dmax= 1.9e-02 nm, Epot= -3.01112e+06 Fmax= 1.87621e+03, atom= 2656
Step=  308, Dmax= 2.3e-02 nm, Epot= -3.01157e+06 Fmax= 2.82350e+04, atom= 2656
Step=  309, Dmax= 2.7e-02 nm, Epot= -3.01260e+06 Fmax= 7.35360e+03, atom= 2656
Step=  311, Dmax= 1.6e-02 nm, Epot= -3.01268e+06 Fmax= 1.37958e+04, atom= 2656
Step=  312, Dmax= 2.0e-02 nm, Epot= -3.01292e+06 Fmax= 1.18493e+04, atom= 2656
Step=  314, Dmax= 1.2e-02 nm, Epot= -3.01319e+06 Fmax= 3.56585e+03, atom= 2656
Step=  315, Dmax= 1.4e-02 nm, Epot= -3.01339e+06 Fmax= 1.48832e+04, atom= 2656
Step=  316, Dmax= 1.7e-02 nm, Epot= -3.01373e+06 Fmax= 7.27619e+03, atom= 2656
Step=  318, Dmax= 1.0e-02 nm, Epot= -3.01391e+06 Fmax= 5.97684e+03, atom= 2656
Step=  319, Dmax= 1.2e-02 nm, Epot= -3.01406e+06 Fmax= 9.95268e+03, atom= 2656
Step=  320, Dmax= 1.5e-02 nm, Epot= -3.01425e+06 Fmax= 9.16696e+03, atom= 2656
Step=  321, Dmax= 1.8e-02 nm, Epot= -3.01434e+06 Fmax= 1.37289e+04, atom= 2656
Step=  322, Dmax= 2.1e-02 nm, Epot= -3.01451e+06 Fmax= 1.38371e+04, atom= 2656
Step=  324, Dmax= 1.3e-02 nm, Epot= -3.01484e+06 Fmax= 2.75549e+03, atom= 2656
Step=  325, Dmax= 1.5e-02 nm, Epot= -3.01513e+06 Fmax= 1.70164e+04, atom= 2656
Step=  326, Dmax= 1.8e-02 nm, Epot= -3.01554e+06 Fmax= 6.81159e+03, atom= 2656
Step=  328, Dmax= 1.1e-02 nm, Epot= -3.01571e+06 Fmax= 7.45669e+03, atom= 2656
Step=  329, Dmax= 1.3e-02 nm, Epot= -3.01586e+06 Fmax= 9.66049e+03, atom= 2656
Step=  330, Dmax= 1.6e-02 nm, Epot= -3.01601e+06 Fmax= 1.09109e+04, atom= 2656
Step=  331, Dmax= 1.9e-02 nm, Epot= -3.01612e+06 Fmax= 1.37062e+04, atom= 2656
Step=  332, Dmax= 2.3e-02 nm, Epot= -3.01622e+06 Fmax= 1.59524e+04, atom= 2656
Step=  333, Dmax= 2.7e-02 nm, Epot= -3.01626e+06 Fmax= 1.94440e+04, atom= 2656
Step=  334, Dmax= 3.3e-02 nm, Epot= -3.01626e+06 Fmax= 2.33232e+04, atom= 2656
Step=  336, Dmax= 2.0e-02 nm, Epot= -3.01698e+06 Fmax= 2.43471e+03, atom= 2656
Step=  337, Dmax= 2.3e-02 nm, Epot= -3.01721e+06 Fmax= 2.79541e+04, atom= 2656
Step=  338, Dmax= 2.8e-02 nm, Epot= -3.01807e+06 Fmax= 8.94976e+03, atom= 2656
Step=  340, Dmax= 1.7e-02 nm, Epot= -3.01817e+06 Fmax= 1.32729e+04, atom= 2656
Step=  341, Dmax= 2.0e-02 nm, Epot= -3.01833e+06 Fmax= 1.31857e+04, atom= 2656
Step=  342, Dmax= 2.4e-02 nm, Epot= -3.01835e+06 Fmax= 1.87420e+04, atom= 2656
Step=  343, Dmax= 2.9e-02 nm, Epot= -3.01848e+06 Fmax= 1.93295e+04, atom= 2656
Step=  345, Dmax= 1.8e-02 nm, Epot= -3.01898e+06 Fmax= 3.43345e+03, atom= 2656
Step=  346, Dmax= 2.1e-02 nm, Epot= -3.01898e+06 Fmax= 2.41265e+04, atom= 2656
Step=  347, Dmax= 2.5e-02 nm, Epot= -3.01967e+06 Fmax= 8.80815e+03, atom= 2656
Step=  349, Dmax= 1.5e-02 nm, Epot= -3.01980e+06 Fmax= 1.09652e+04, atom= 2656
Step=  350, Dmax= 1.8e-02 nm, Epot= -3.01993e+06 Fmax= 1.28092e+04, atom= 2656
Step=  351, Dmax= 2.2e-02 nm, Epot= -3.02001e+06 Fmax= 1.56270e+04, atom= 2656
Step=  352, Dmax= 2.6e-02 nm, Epot= -3.02008e+06 Fmax= 1.86559e+04, atom= 2656
Step=  354, Dmax= 1.6e-02 nm, Epot= -3.02056e+06 Fmax= 1.98935e+03, atom= 2656
Step=  355, Dmax= 1.9e-02 nm, Epot= -3.02102e+06 Fmax= 2.23900e+04, atom= 2656
Step=  356, Dmax= 2.3e-02 nm, Epot= -3.02160e+06 Fmax= 7.20981e+03, atom= 2656
Step=  358, Dmax= 1.4e-02 nm, Epot= -3.02173e+06 Fmax= 1.05925e+04, atom= 2656
Step=  359, Dmax= 1.6e-02 nm, Epot= -3.02189e+06 Fmax= 1.06551e+04, atom= 2656
Step=  360, Dmax= 2.0e-02 nm, Epot= -3.02196e+06 Fmax= 1.49414e+04, atom= 2656
Step=  361, Dmax= 2.3e-02 nm, Epot= -3.02209e+06 Fmax= 1.56340e+04, atom= 2656
Step=  363, Dmax= 1.4e-02 nm, Epot= -3.02244e+06 Fmax= 2.65294e+03, atom= 2656
Step=  364, Dmax= 1.7e-02 nm, Epot= -3.02268e+06 Fmax= 1.94854e+04, atom= 2656
Step=  365, Dmax= 2.0e-02 nm, Epot= -3.02315e+06 Fmax= 6.95015e+03, atom= 2656
Step=  367, Dmax= 1.2e-02 nm, Epot= -3.02329e+06 Fmax= 8.92373e+03, atom= 2656
Step=  368, Dmax= 1.5e-02 nm, Epot= -3.02344e+06 Fmax= 1.01480e+04, atom= 2656
Step=  369, Dmax= 1.7e-02 nm, Epot= -3.02354e+06 Fmax= 1.26872e+04, atom= 2656
Step=  370, Dmax= 2.1e-02 nm, Epot= -3.02364e+06 Fmax= 1.48083e+04, atom= 2656
Step=  371, Dmax= 2.5e-02 nm, Epot= -3.02370e+06 Fmax= 1.80280e+04, atom= 2656
Step=  372, Dmax= 3.0e-02 nm, Epot= -3.02371e+06 Fmax= 2.16189e+04, atom= 2656
Step=  374, Dmax= 1.8e-02 nm, Epot= -3.02431e+06 Fmax= 2.25610e+03, atom= 2656
Step=  375, Dmax= 2.2e-02 nm, Epot= -3.02458e+06 Fmax= 2.59237e+04, atom= 2656
Step=  376, Dmax= 2.6e-02 nm, Epot= -3.02530e+06 Fmax= 8.29020e+03, atom= 2656
Step=  378, Dmax= 1.6e-02 nm, Epot= -3.02540e+06 Fmax= 1.23076e+04, atom= 2656
Step=  379, Dmax= 1.9e-02 nm, Epot= -3.02555e+06 Fmax= 1.22345e+04, atom= 2656
Step=  380, Dmax= 2.3e-02 nm, Epot= -3.02557e+06 Fmax= 1.73646e+04, atom= 2656
Step=  381, Dmax= 2.7e-02 nm, Epot= -3.02570e+06 Fmax= 1.79503e+04, atom= 2656
Step=  383, Dmax= 1.6e-02 nm, Epot= -3.02612e+06 Fmax= 3.16856e+03, atom= 2656
Step=  384, Dmax= 1.9e-02 nm, Epot= -3.02618e+06 Fmax= 2.23943e+04, atom= 2656
Step=  385, Dmax= 2.3e-02 nm, Epot= -3.02676e+06 Fmax= 8.15146e+03, atom= 2656
Step=  387, Dmax= 1.4e-02 nm, Epot= -3.02688e+06 Fmax= 1.01881e+04, atom= 2656
Step=  388, Dmax= 1.7e-02 nm, Epot= -3.02700e+06 Fmax= 1.18564e+04, atom= 2656
Step=  389, Dmax= 2.0e-02 nm, Epot= -3.02709e+06 Fmax= 1.45204e+04, atom= 2656
Step=  390, Dmax= 2.4e-02 nm, Epot= -3.02716e+06 Fmax= 1.72661e+04, atom= 2656
Step=  391, Dmax= 2.9e-02 nm, Epot= -3.02718e+06 Fmax= 2.06562e+04, atom= 2656
Step=  393, Dmax= 1.7e-02 nm, Epot= -3.02772e+06 Fmax= 2.01657e+03, atom= 2656
Step=  394, Dmax= 2.1e-02 nm, Epot= -3.02793e+06 Fmax= 2.57064e+04, atom= 2656
Step=  395, Dmax= 2.5e-02 nm, Epot= -3.02874e+06 Fmax= 7.17159e+03, atom= 2656
Step=  397, Dmax= 1.5e-02 nm, Epot= -3.02881e+06 Fmax= 1.24387e+04, atom= 2656
Step=  398, Dmax= 1.8e-02 nm, Epot= -3.02899e+06 Fmax= 1.12657e+04, atom= 2656
Step=  400, Dmax= 1.1e-02 nm, Epot= -3.02922e+06 Fmax= 2.98674e+03, atom= 2656
Step=  401, Dmax= 1.3e-02 nm, Epot= -3.02941e+06 Fmax= 1.40495e+04, atom= 2656
Step=  402, Dmax= 1.6e-02 nm, Epot= -3.02969e+06 Fmax= 6.43688e+03, atom= 2656
Step=  404, Dmax= 9.4e-03 nm, Epot= -3.02983e+06 Fmax= 5.81844e+03, atom= 2656
Step=  405, Dmax= 1.1e-02 nm, Epot= -3.02996e+06 Fmax= 8.90980e+03, atom= 2656
Step=  406, Dmax= 1.4e-02 nm, Epot= -3.03010e+06 Fmax= 8.76707e+03, atom= 2656
Step=  407, Dmax= 1.6e-02 nm, Epot= -3.03018e+06 Fmax= 1.24073e+04, atom= 2656
Step=  408, Dmax= 1.9e-02 nm, Epot= -3.03031e+06 Fmax= 1.30782e+04, atom= 2656
Step=  409, Dmax= 2.3e-02 nm, Epot= -3.03032e+06 Fmax= 1.73701e+04, atom= 2656
Step=  410, Dmax= 2.8e-02 nm, Epot= -3.03039e+06 Fmax= 1.93757e+04, atom= 2656
Step=  412, Dmax= 1.7e-02 nm, Epot= -3.03089e+06 Fmax= 2.74562e+03, atom= 2656
Step=  413, Dmax= 2.0e-02 nm, Epot= -3.03096e+06 Fmax= 2.35166e+04, atom= 2656
Step=  414, Dmax= 2.4e-02 nm, Epot= -3.03159e+06 Fmax= 8.21255e+03, atom= 2656
Step=  416, Dmax= 1.5e-02 nm, Epot= -3.03169e+06 Fmax= 1.08329e+04, atom= 2656
Step=  417, Dmax= 1.7e-02 nm, Epot= -3.03181e+06 Fmax= 1.19325e+04, atom= 2656
Step=  418, Dmax= 2.1e-02 nm, Epot= -3.03187e+06 Fmax= 1.54923e+04, atom= 2656
Step=  419, Dmax= 2.5e-02 nm, Epot= -3.03194e+06 Fmax= 1.72553e+04, atom= 2656
Step=  421, Dmax= 1.5e-02 nm, Epot= -3.03235e+06 Fmax= 2.33002e+03, atom= 2656
Step=  422, Dmax= 1.8e-02 nm, Epot= -3.03251e+06 Fmax= 2.14515e+04, atom= 2656
Step=  423, Dmax= 2.2e-02 nm, Epot= -3.03308e+06 Fmax= 6.88802e+03, atom= 2656
Step=  425, Dmax= 1.3e-02 nm, Epot= -3.03318e+06 Fmax= 1.00946e+04, atom= 2656
Step=  426, Dmax= 1.6e-02 nm, Epot= -3.03332e+06 Fmax= 1.03490e+04, atom= 2656
Step=  427, Dmax= 1.9e-02 nm, Epot= -3.03337e+06 Fmax= 1.41040e+04, atom= 2656
Step=  428, Dmax= 2.2e-02 nm, Epot= -3.03347e+06 Fmax= 1.53624e+04, atom= 2656
Step=  430, Dmax= 1.3e-02 nm, Epot= -3.03382e+06 Fmax= 2.37117e+03, atom= 2656
Step=  431, Dmax= 1.6e-02 nm, Epot= -3.03403e+06 Fmax= 1.87158e+04, atom= 2656
Step=  432, Dmax= 1.9e-02 nm, Epot= -3.03446e+06 Fmax= 6.73915e+03, atom= 2656
Step=  434, Dmax= 1.2e-02 nm, Epot= -3.03458e+06 Fmax= 8.52491e+03, atom= 2656
Step=  435, Dmax= 1.4e-02 nm, Epot= -3.03469e+06 Fmax= 9.75601e+03, atom= 2656
Step=  436, Dmax= 1.7e-02 nm, Epot= -3.03478e+06 Fmax= 1.22351e+04, atom= 2656
Step=  437, Dmax= 2.0e-02 nm, Epot= -3.03487e+06 Fmax= 1.40623e+04, atom= 2656
Step=  438, Dmax= 2.4e-02 nm, Epot= -3.03489e+06 Fmax= 1.76418e+04, atom= 2656
Step=  439, Dmax= 2.9e-02 nm, Epot= -3.03491e+06 Fmax= 2.01710e+04, atom= 2656
Step=  441, Dmax= 1.7e-02 nm, Epot= -3.03544e+06 Fmax= 2.44171e+03, atom= 2656
Step=  443, Dmax= 1.0e-02 nm, Epot= -3.03567e+06 Fmax= 1.13995e+04, atom= 2656
Step=  444, Dmax= 1.3e-02 nm, Epot= -3.03589e+06 Fmax= 4.98367e+03, atom= 2656
Step=  445, Dmax= 1.5e-02 nm, Epot= -3.03592e+06 Fmax= 1.46068e+04, atom= 2656
Step=  446, Dmax= 1.8e-02 nm, Epot= -3.03618e+06 Fmax= 8.97833e+03, atom= 2656
Step=  448, Dmax= 1.1e-02 nm, Epot= -3.03635e+06 Fmax= 5.21745e+03, atom= 2656
Step=  449, Dmax= 1.3e-02 nm, Epot= -3.03643e+06 Fmax= 1.17800e+04, atom= 2656
Step=  450, Dmax= 1.6e-02 nm, Epot= -3.03661e+06 Fmax= 8.62014e+03, atom= 2656
Step=  452, Dmax= 9.4e-03 nm, Epot= -3.03678e+06 Fmax= 3.57951e+03, atom= 2656
Step=  453, Dmax= 1.1e-02 nm, Epot= -3.03691e+06 Fmax= 1.11156e+04, atom= 2656
Step=  454, Dmax= 1.3e-02 nm, Epot= -3.03711e+06 Fmax= 6.48945e+03, atom= 2656
Step=  456, Dmax= 8.1e-03 nm, Epot= -3.03724e+06 Fmax= 4.10605e+03, atom= 2656
Step=  457, Dmax= 9.7e-03 nm, Epot= -3.03738e+06 Fmax= 8.57384e+03, atom= 2656
Step=  458, Dmax= 1.2e-02 nm, Epot= -3.03752e+06 Fmax= 6.65834e+03, atom= 2656
Step=  459, Dmax= 1.4e-02 nm, Epot= -3.03759e+06 Fmax= 1.16422e+04, atom= 2656
Step=  460, Dmax= 1.7e-02 nm, Epot= -3.03775e+06 Fmax= 1.02695e+04, atom= 2656
Step=  462, Dmax= 1.0e-02 nm, Epot= -3.03794e+06 Fmax= 2.84072e+03, atom= 2656
Step=  463, Dmax= 1.2e-02 nm, Epot= -3.03810e+06 Fmax= 1.29636e+04, atom= 2656
Step=  464, Dmax= 1.4e-02 nm, Epot= -3.03835e+06 Fmax= 5.95964e+03, atom= 2656
Step=  466, Dmax= 8.7e-03 nm, Epot= -3.03848e+06 Fmax= 5.42043e+03, atom= 2656
Step=  467, Dmax= 1.0e-02 nm, Epot= -3.03859e+06 Fmax= 8.22042e+03, atom= 2656
Step=  468, Dmax= 1.3e-02 nm, Epot= -3.03872e+06 Fmax= 8.14271e+03, atom= 2656
Step=  469, Dmax= 1.5e-02 nm, Epot= -3.03879e+06 Fmax= 1.15291e+04, atom= 2656
Step=  470, Dmax= 1.8e-02 nm, Epot= -3.03890e+06 Fmax= 1.20074e+04, atom= 2656
Step=  471, Dmax= 2.2e-02 nm, Epot= -3.03891e+06 Fmax= 1.63534e+04, atom= 2656
Step=  472, Dmax= 2.6e-02 nm, Epot= -3.03898e+06 Fmax= 1.74947e+04, atom= 2656
Step=  474, Dmax= 1.6e-02 nm, Epot= -3.03942e+06 Fmax= 2.75412e+03, atom= 2656
Step=  476, Dmax= 9.3e-03 nm, Epot= -3.03959e+06 Fmax= 9.57338e+03, atom= 2656
Step=  477, Dmax= 1.1e-02 nm, Epot= -3.03976e+06 Fmax= 5.07531e+03, atom= 2656
Step=  478, Dmax= 1.3e-02 nm, Epot= -3.03981e+06 Fmax= 1.24775e+04, atom= 2656
Step=  479, Dmax= 1.6e-02 nm, Epot= -3.04003e+06 Fmax= 8.62857e+03, atom= 2656
Step=  481, Dmax= 9.7e-03 nm, Epot= -3.04019e+06 Fmax= 4.07061e+03, atom= 2656
Step=  482, Dmax= 1.2e-02 nm, Epot= -3.04028e+06 Fmax= 1.11293e+04, atom= 2656
Step=  483, Dmax= 1.4e-02 nm, Epot= -3.04047e+06 Fmax= 7.12325e+03, atom= 2656
Step=  485, Dmax= 8.4e-03 nm, Epot= -3.04061e+06 Fmax= 3.79647e+03, atom= 2656
Step=  486, Dmax= 1.0e-02 nm, Epot= -3.04073e+06 Fmax= 9.34196e+03, atom= 2656
Step=  487, Dmax= 1.2e-02 nm, Epot= -3.04089e+06 Fmax= 6.41047e+03, atom= 2656
Step=  488, Dmax= 1.4e-02 nm, Epot= -3.04093e+06 Fmax= 1.24611e+04, atom= 2656
Step=  489, Dmax= 1.7e-02 nm, Epot= -3.04110e+06 Fmax= 1.02448e+04, atom= 2656
Step=  491, Dmax= 1.0e-02 nm, Epot= -3.04130e+06 Fmax= 3.41345e+03, atom= 2656
Step=  492, Dmax= 1.2e-02 nm, Epot= -3.04139e+06 Fmax= 1.29243e+04, atom= 2656
Step=  493, Dmax= 1.5e-02 nm, Epot= -3.04164e+06 Fmax= 6.70374e+03, atom= 2656
Step=  495, Dmax= 9.0e-03 nm, Epot= -3.04177e+06 Fmax= 5.04366e+03, atom= 2656
Step=  496, Dmax= 1.1e-02 nm, Epot= -3.04187e+06 Fmax= 9.07047e+03, atom= 2656
Step=  497, Dmax= 1.3e-02 nm, Epot= -3.04200e+06 Fmax= 7.87363e+03, atom= 2656
Step=  498, Dmax= 1.6e-02 nm, Epot= -3.04204e+06 Fmax= 1.24153e+04, atom= 2656
Step=  499, Dmax= 1.9e-02 nm, Epot= -3.04217e+06 Fmax= 1.20102e+04, atom= 2656
Step=  501, Dmax= 1.1e-02 nm, Epot= -3.04241e+06 Fmax= 2.68249e+03, atom= 2656
Step=  502, Dmax= 1.3e-02 nm, Epot= -3.04255e+06 Fmax= 1.48608e+04, atom= 2656
Step=  503, Dmax= 1.6e-02 nm, Epot= -3.04285e+06 Fmax= 6.24585e+03, atom= 2656
Step=  505, Dmax= 9.7e-03 nm, Epot= -3.04297e+06 Fmax= 6.39700e+03, atom= 2656
Step=  506, Dmax= 1.2e-02 nm, Epot= -3.04306e+06 Fmax= 8.77040e+03, atom= 2656
Step=  507, Dmax= 1.4e-02 nm, Epot= -3.04317e+06 Fmax= 9.45781e+03, atom= 2656
Step=  508, Dmax= 1.7e-02 nm, Epot= -3.04323e+06 Fmax= 1.23565e+04, atom= 2656
Step=  509, Dmax= 2.0e-02 nm, Epot= -3.04331e+06 Fmax= 1.39204e+04, atom= 2656
Step=  511, Dmax= 1.2e-02 nm, Epot= -3.04360e+06 Fmax= 1.88646e+03, atom= 2656
Step=  512, Dmax= 1.4e-02 nm, Epot= -3.04386e+06 Fmax= 1.69097e+04, atom= 2656
Step=  513, Dmax= 1.7e-02 nm, Epot= -3.04424e+06 Fmax= 5.78088e+03, atom= 2656
Step=  515, Dmax= 1.0e-02 nm, Epot= -3.04433e+06 Fmax= 7.84168e+03, atom= 2656
Step=  516, Dmax= 1.2e-02 nm, Epot= -3.04444e+06 Fmax= 8.45892e+03, atom= 2656
Step=  517, Dmax= 1.5e-02 nm, Epot= -3.04452e+06 Fmax= 1.11556e+04, atom= 2656
Step=  518, Dmax= 1.8e-02 nm, Epot= -3.04461e+06 Fmax= 1.23002e+04, atom= 2656
Step=  519, Dmax= 2.2e-02 nm, Epot= -3.04462e+06 Fmax= 1.59710e+04, atom= 2656
Step=  520, Dmax= 2.6e-02 nm, Epot= -3.04467e+06 Fmax= 1.77633e+04, atom= 2656
Step=  522, Dmax= 1.6e-02 nm, Epot= -3.04510e+06 Fmax= 2.42126e+03, atom= 2656
Step=  524, Dmax= 9.3e-03 nm, Epot= -3.04528e+06 Fmax= 9.88234e+03, atom= 2656
Step=  525, Dmax= 1.1e-02 nm, Epot= -3.04545e+06 Fmax= 4.72596e+03, atom= 2656
Step=  526, Dmax= 1.3e-02 nm, Epot= -3.04549e+06 Fmax= 1.27587e+04, atom= 2656
Step=  527, Dmax= 1.6e-02 nm, Epot= -3.04570e+06 Fmax= 8.28049e+03, atom= 2656
Step=  529, Dmax= 9.6e-03 nm, Epot= -3.04585e+06 Fmax= 4.37576e+03, atom= 2656
Step=  530, Dmax= 1.2e-02 nm, Epot= -3.04593e+06 Fmax= 1.07825e+04, atom= 2656
Step=  531, Dmax= 1.4e-02 nm, Epot= -3.04610e+06 Fmax= 7.40873e+03, atom= 2656
Step=  533, Dmax= 8.3e-03 nm, Epot= -3.04623e+06 Fmax= 3.47675e+03, atom= 2656
Step=  534, Dmax= 1.0e-02 nm, Epot= -3.04634e+06 Fmax= 9.62035e+03, atom= 2656
Step=  535, Dmax= 1.2e-02 nm, Epot= -3.04650e+06 Fmax= 6.08318e+03, atom= 2656
Step=  536, Dmax= 1.4e-02 nm, Epot= -3.04652e+06 Fmax= 1.27242e+04, atom= 2656
Step=  537, Dmax= 1.7e-02 nm, Epot= -3.04670e+06 Fmax= 9.90956e+03, atom= 2656
Step=  539, Dmax= 1.0e-02 nm, Epot= -3.04688e+06 Fmax= 3.70249e+03, atom= 2656
Step=  540, Dmax= 1.2e-02 nm, Epot= -3.04696e+06 Fmax= 1.25924e+04, atom= 2656
Step=  541, Dmax= 1.5e-02 nm, Epot= -3.04717e+06 Fmax= 6.97071e+03, atom= 2656
Step=  543, Dmax= 9.0e-03 nm, Epot= -3.04730e+06 Fmax= 4.73878e+03, atom= 2656
Step=  544, Dmax= 1.1e-02 nm, Epot= -3.04738e+06 Fmax= 9.33000e+03, atom= 2656
Step=  545, Dmax= 1.3e-02 nm, Epot= -3.04752e+06 Fmax= 7.56057e+03, atom= 2656
Step=  546, Dmax= 1.5e-02 nm, Epot= -3.04754e+06 Fmax= 1.26608e+04, atom= 2656
Step=  547, Dmax= 1.9e-02 nm, Epot= -3.04768e+06 Fmax= 1.16865e+04, atom= 2656
Step=  549, Dmax= 1.1e-02 nm, Epot= -3.04790e+06 Fmax= 2.95674e+03, atom= 2656
Step=  550, Dmax= 1.3e-02 nm, Epot= -3.04799e+06 Fmax= 1.45457e+04, atom= 2656
Step=  551, Dmax= 1.6e-02 nm, Epot= -3.04827e+06 Fmax= 6.49237e+03, atom= 2656
Step=  553, Dmax= 9.6e-03 nm, Epot= -3.04838e+06 Fmax= 6.10773e+03, atom= 2656
Step=  554, Dmax= 1.2e-02 nm, Epot= -3.04847e+06 Fmax= 9.01119e+03, atom= 2656
Step=  555, Dmax= 1.4e-02 nm, Epot= -3.04857e+06 Fmax= 9.15883e+03, atom= 2656
Step=  556, Dmax= 1.7e-02 nm, Epot= -3.04861e+06 Fmax= 1.25834e+04, atom= 2656
Step=  557, Dmax= 2.0e-02 nm, Epot= -3.04869e+06 Fmax= 1.36087e+04, atom= 2656
Step=  559, Dmax= 1.2e-02 nm, Epot= -3.04897e+06 Fmax= 2.14495e+03, atom= 2656
Step=  560, Dmax= 1.4e-02 nm, Epot= -3.04914e+06 Fmax= 1.66227e+04, atom= 2656
Step=  561, Dmax= 1.7e-02 nm, Epot= -3.04948e+06 Fmax= 5.99671e+03, atom= 2656
Step=  563, Dmax= 1.0e-02 nm, Epot= -3.04959e+06 Fmax= 7.57379e+03, atom= 2656
Step=  564, Dmax= 1.2e-02 nm, Epot= -3.04968e+06 Fmax= 8.67511e+03, atom= 2656
Step=  565, Dmax= 1.5e-02 nm, Epot= -3.04975e+06 Fmax= 1.08747e+04, atom= 2656
Step=  566, Dmax= 1.8e-02 nm, Epot= -3.04982e+06 Fmax= 1.25037e+04, atom= 2656
Step=  567, Dmax= 2.1e-02 nm, Epot= -3.04985e+06 Fmax= 1.56759e+04, atom= 2656
Step=  568, Dmax= 2.6e-02 nm, Epot= -3.04987e+06 Fmax= 1.79473e+04, atom= 2656
Step=  570, Dmax= 1.5e-02 nm, Epot= -3.05030e+06 Fmax= 2.17319e+03, atom= 2656
Step=  571, Dmax= 1.9e-02 nm, Epot= -3.05030e+06 Fmax= 2.22560e+04, atom= 2656
Step=  572, Dmax= 2.2e-02 nm, Epot= -3.05090e+06 Fmax= 6.87394e+03, atom= 2656
Step=  574, Dmax= 1.3e-02 nm, Epot= -3.05096e+06 Fmax= 1.05466e+04, atom= 2656
Step=  575, Dmax= 1.6e-02 nm, Epot= -3.05107e+06 Fmax= 1.04634e+04, atom= 2656
Step=  577, Dmax= 9.6e-03 nm, Epot= -3.05126e+06 Fmax= 2.16481e+03, atom= 2656
Step=  578, Dmax= 1.2e-02 nm, Epot= -3.05143e+06 Fmax= 1.29219e+04, atom= 2656
Step=  579, Dmax= 1.4e-02 nm, Epot= -3.05167e+06 Fmax= 5.22812e+03, atom= 2656
Step=  581, Dmax= 8.3e-03 nm, Epot= -3.05177e+06 Fmax= 5.64491e+03, atom= 2656
Step=  582, Dmax= 1.0e-02 nm, Epot= -3.05187e+06 Fmax= 7.40193e+03, atom= 2656
Step=  583, Dmax= 1.2e-02 nm, Epot= -3.05196e+06 Fmax= 8.27253e+03, atom= 2656
Step=  584, Dmax= 1.4e-02 nm, Epot= -3.05203e+06 Fmax= 1.04949e+04, atom= 2656
Step=  585, Dmax= 1.7e-02 nm, Epot= -3.05210e+06 Fmax= 1.20986e+04, atom= 2656
Step=  586, Dmax= 2.1e-02 nm, Epot= -3.05212e+06 Fmax= 1.48971e+04, atom= 2656
Step=  587, Dmax= 2.5e-02 nm, Epot= -3.05214e+06 Fmax= 1.76736e+04, atom= 2656
Step=  589, Dmax= 1.5e-02 nm, Epot= -3.05255e+06 Fmax= 1.92052e+03, atom= 2656
Step=  590, Dmax= 1.8e-02 nm, Epot= -3.05268e+06 Fmax= 2.13029e+04, atom= 2656
Step=  591, Dmax= 2.1e-02 nm, Epot= -3.05319e+06 Fmax= 6.79558e+03, atom= 2656
Step=  593, Dmax= 1.3e-02 nm, Epot= -3.05326e+06 Fmax= 1.01177e+04, atom= 2656
Step=  594, Dmax= 1.5e-02 nm, Epot= -3.05336e+06 Fmax= 1.00551e+04, atom= 2656
Step=  595, Dmax= 1.9e-02 nm, Epot= -3.05337e+06 Fmax= 1.42612e+04, atom= 2656
Step=  596, Dmax= 2.2e-02 nm, Epot= -3.05346e+06 Fmax= 1.47709e+04, atom= 2656
Step=  598, Dmax= 1.3e-02 nm, Epot= -3.05375e+06 Fmax= 2.60755e+03, atom= 2656
Step=  599, Dmax= 1.6e-02 nm, Epot= -3.05378e+06 Fmax= 1.83837e+04, atom= 2656
Step=  600, Dmax= 1.9e-02 nm, Epot= -3.05419e+06 Fmax= 6.73301e+03, atom= 2656
Step=  602, Dmax= 1.2e-02 nm, Epot= -3.05427e+06 Fmax= 8.33774e+03, atom= 2656
Step=  603, Dmax= 1.4e-02 nm, Epot= -3.05435e+06 Fmax= 9.78105e+03, atom= 2656
Step=  604, Dmax= 1.7e-02 nm, Epot= -3.05441e+06 Fmax= 1.19003e+04, atom= 2656
Step=  605, Dmax= 2.0e-02 nm, Epot= -3.05445e+06 Fmax= 1.42193e+04, atom= 2656
Step=  606, Dmax= 2.4e-02 nm, Epot= -3.05446e+06 Fmax= 1.69635e+04, atom= 2656
Step=  608, Dmax= 1.4e-02 nm, Epot= -3.05484e+06 Fmax= 1.69833e+03, atom= 2656
Step=  609, Dmax= 1.7e-02 nm, Epot= -3.05496e+06 Fmax= 2.10171e+04, atom= 2656
Step=  610, Dmax= 2.1e-02 nm, Epot= -3.05552e+06 Fmax= 6.00953e+03, atom= 2656
Step=  612, Dmax= 1.2e-02 nm, Epot= -3.05558e+06 Fmax= 1.01234e+04, atom= 2656
Step=  613, Dmax= 1.5e-02 nm, Epot= -3.05569e+06 Fmax= 9.35928e+03, atom= 2656
Step=  615, Dmax= 8.9e-03 nm, Epot= -3.05585e+06 Fmax= 2.34555e+03, atom= 2656
Step=  616, Dmax= 1.1e-02 nm, Epot= -3.05599e+06 Fmax= 1.16622e+04, atom= 2656
Step=  617, Dmax= 1.3e-02 nm, Epot= -3.05618e+06 Fmax= 5.16653e+03, atom= 2656
Step=  619, Dmax= 7.7e-03 nm, Epot= -3.05628e+06 Fmax= 4.91247e+03, atom= 2656
Step=  620, Dmax= 9.2e-03 nm, Epot= -3.05637e+06 Fmax= 7.18750e+03, atom= 2656
Step=  621, Dmax= 1.1e-02 nm, Epot= -3.05647e+06 Fmax= 7.34459e+03, atom= 2656
Step=  622, Dmax= 1.3e-02 nm, Epot= -3.05653e+06 Fmax= 1.00591e+04, atom= 2656
Step=  623, Dmax= 1.6e-02 nm, Epot= -3.05660e+06 Fmax= 1.08868e+04, atom= 2656
Step=  624, Dmax= 1.9e-02 nm, Epot= -3.05662e+06 Fmax= 1.41477e+04, atom= 2656
Step=  625, Dmax= 2.3e-02 nm, Epot= -3.05666e+06 Fmax= 1.60464e+04, atom= 2656
Step=  627, Dmax= 1.4e-02 nm, Epot= -3.05701e+06 Fmax= 2.11297e+03, atom= 2656
Step=  628, Dmax= 1.7e-02 nm, Epot= -3.05708e+06 Fmax= 1.94828e+04, atom= 2656
Step=  629, Dmax= 2.0e-02 nm, Epot= -3.05752e+06 Fmax= 6.57464e+03, atom= 2656
Step=  631, Dmax= 1.2e-02 nm, Epot= -3.05760e+06 Fmax= 9.08348e+03, atom= 2656
Step=  632, Dmax= 1.4e-02 nm, Epot= -3.05768e+06 Fmax= 9.62685e+03, atom= 2656
Step=  633, Dmax= 1.7e-02 nm, Epot= -3.05771e+06 Fmax= 1.29114e+04, atom= 2656
Step=  634, Dmax= 2.1e-02 nm, Epot= -3.05777e+06 Fmax= 1.40115e+04, atom= 2656
Step=  636, Dmax= 1.2e-02 nm, Epot= -3.05804e+06 Fmax= 2.10669e+03, atom= 2656
Step=  637, Dmax= 1.5e-02 nm, Epot= -3.05814e+06 Fmax= 1.73840e+04, atom= 2656
Step=  638, Dmax= 1.8e-02 nm, Epot= -3.05851e+06 Fmax= 5.91337e+03, atom= 2656
Step=  640, Dmax= 1.1e-02 nm, Epot= -3.05858e+06 Fmax= 8.05263e+03, atom= 2656
Step=  641, Dmax= 1.3e-02 nm, Epot= -3.05867e+06 Fmax= 8.75046e+03, atom= 2656
Step=  642, Dmax= 1.5e-02 nm, Epot= -3.05871e+06 Fmax= 1.13532e+04, atom= 2656
Step=  643, Dmax= 1.8e-02 nm, Epot= -3.05877e+06 Fmax= 1.28631e+04, atom= 2656
Step=  645, Dmax= 1.1e-02 nm, Epot= -3.05901e+06 Fmax= 1.69791e+03, atom= 2656
Step=  646, Dmax= 1.3e-02 nm, Epot= -3.05922e+06 Fmax= 1.56324e+04, atom= 2656
Step=  647, Dmax= 1.6e-02 nm, Epot= -3.05953e+06 Fmax= 5.27356e+03, atom= 2656
Step=  649, Dmax= 9.6e-03 nm, Epot= -3.05961e+06 Fmax= 7.28284e+03, atom= 2656
Step=  650, Dmax= 1.1e-02 nm, Epot= -3.05970e+06 Fmax= 7.73856e+03, atom= 2656
Step=  651, Dmax= 1.4e-02 nm, Epot= -3.05975e+06 Fmax= 1.03386e+04, atom= 2656
Step=  652, Dmax= 1.7e-02 nm, Epot= -3.05983e+06 Fmax= 1.12783e+04, atom= 2656
Step=  653, Dmax= 2.0e-02 nm, Epot= -3.05983e+06 Fmax= 1.47749e+04, atom= 2656
Step=  654, Dmax= 2.4e-02 nm, Epot= -3.05987e+06 Fmax= 1.63197e+04, atom= 2656
Step=  656, Dmax= 1.4e-02 nm, Epot= -3.06022e+06 Fmax= 2.29384e+03, atom= 2656
Step=  658, Dmax= 8.6e-03 nm, Epot= -3.06035e+06 Fmax= 9.02966e+03, atom= 2656
Step=  659, Dmax= 1.0e-02 nm, Epot= -3.06049e+06 Fmax= 4.43567e+03, atom= 2656
Step=  660, Dmax= 1.2e-02 nm, Epot= -3.06052e+06 Fmax= 1.16804e+04, atom= 2656
Step=  661, Dmax= 1.5e-02 nm, Epot= -3.06069e+06 Fmax= 7.71321e+03, atom= 2656
Step=  663, Dmax= 8.9e-03 nm, Epot= -3.06081e+06 Fmax= 3.94729e+03, atom= 2656
Step=  664, Dmax= 1.1e-02 nm, Epot= -3.06087e+06 Fmax= 1.00253e+04, atom= 2656
Step=  665, Dmax= 1.3e-02 nm, Epot= -3.06101e+06 Fmax= 6.73750e+03, atom= 2656
Step=  667, Dmax= 7.7e-03 nm, Epot= -3.06112e+06 Fmax= 3.29863e+03, atom= 2656
Step=  668, Dmax= 9.2e-03 nm, Epot= -3.06121e+06 Fmax= 8.76645e+03, atom= 2656
Step=  669, Dmax= 1.1e-02 nm, Epot= -3.06133e+06 Fmax= 5.70922e+03, atom= 2656
Step=  670, Dmax= 1.3e-02 nm, Epot= -3.06136e+06 Fmax= 1.16245e+04, atom= 2656
Step=  671, Dmax= 1.6e-02 nm, Epot= -3.06149e+06 Fmax= 9.23802e+03, atom= 2656
Step=  673, Dmax= 9.6e-03 nm, Epot= -3.06164e+06 Fmax= 3.30316e+03, atom= 2656
Step=  674, Dmax= 1.1e-02 nm, Epot= -3.06170e+06 Fmax= 1.17170e+04, atom= 2656
Step=  675, Dmax= 1.4e-02 nm, Epot= -3.06188e+06 Fmax= 6.30960e+03, atom= 2656
Step=  677, Dmax= 8.3e-03 nm, Epot= -3.06198e+06 Fmax= 4.48640e+03, atom= 2656
Step=  678, Dmax= 9.9e-03 nm, Epot= -3.06205e+06 Fmax= 8.47619e+03, atom= 2656
Step=  679, Dmax= 1.2e-02 nm, Epot= -3.06215e+06 Fmax= 7.09340e+03, atom= 2656
Step=  680, Dmax= 1.4e-02 nm, Epot= -3.06218e+06 Fmax= 1.15436e+04, atom= 2656
Step=  681, Dmax= 1.7e-02 nm, Epot= -3.06228e+06 Fmax= 1.08978e+04, atom= 2656
Step=  683, Dmax= 1.0e-02 nm, Epot= -3.06246e+06 Fmax= 2.59264e+03, atom= 2656
Step=  684, Dmax= 1.2e-02 nm, Epot= -3.06254e+06 Fmax= 1.35403e+04, atom= 2656
Step=  685, Dmax= 1.5e-02 nm, Epot= -3.06277e+06 Fmax= 5.84445e+03, atom= 2656
Step=  687, Dmax= 8.9e-03 nm, Epot= -3.06286e+06 Fmax= 5.77245e+03, atom= 2656
Step=  688, Dmax= 1.1e-02 nm, Epot= -3.06292e+06 Fmax= 8.15852e+03, atom= 2656
Step=  689, Dmax= 1.3e-02 nm, Epot= -3.06300e+06 Fmax= 8.58986e+03, atom= 2656
Step=  690, Dmax= 1.5e-02 nm, Epot= -3.06305e+06 Fmax= 1.14488e+04, atom= 2656
Step=  691, Dmax= 1.8e-02 nm, Epot= -3.06311e+06 Fmax= 1.26919e+04, atom= 2656
Step=  693, Dmax= 1.1e-02 nm, Epot= -3.06333e+06 Fmax= 1.82128e+03, atom= 2656
Step=  694, Dmax= 1.3e-02 nm, Epot= -3.06350e+06 Fmax= 1.54757e+04, atom= 2656
Step=  695, Dmax= 1.6e-02 nm, Epot= -3.06378e+06 Fmax= 5.36387e+03, atom= 2656
Step=  697, Dmax= 9.5e-03 nm, Epot= -3.06386e+06 Fmax= 7.15024e+03, atom= 2656
Step=  698, Dmax= 1.1e-02 nm, Epot= -3.06394e+06 Fmax= 7.82246e+03, atom= 2656
Step=  699, Dmax= 1.4e-02 nm, Epot= -3.06399e+06 Fmax= 1.01978e+04, atom= 2656
Step=  700, Dmax= 1.6e-02 nm, Epot= -3.06405e+06 Fmax= 1.13491e+04, atom= 2656
Step=  701, Dmax= 2.0e-02 nm, Epot= -3.06406e+06 Fmax= 1.46224e+04, atom= 2656
Step=  702, Dmax= 2.4e-02 nm, Epot= -3.06410e+06 Fmax= 1.63715e+04, atom= 2656
Step=  704, Dmax= 1.4e-02 nm, Epot= -3.06443e+06 Fmax= 2.18406e+03, atom= 2656
Step=  706, Dmax= 8.5e-03 nm, Epot= -3.06456e+06 Fmax= 9.10688e+03, atom= 2656
Step=  707, Dmax= 1.0e-02 nm, Epot= -3.06469e+06 Fmax= 4.31868e+03, atom= 2656
Step=  708, Dmax= 1.2e-02 nm, Epot= -3.06472e+06 Fmax= 1.17411e+04, atom= 2656
Step=  709, Dmax= 1.5e-02 nm, Epot= -3.06488e+06 Fmax= 7.59179e+03, atom= 2656
Step=  711, Dmax= 8.9e-03 nm, Epot= -3.06499e+06 Fmax= 4.03070e+03, atom= 2656
Step=  712, Dmax= 1.1e-02 nm, Epot= -3.06505e+06 Fmax= 9.90003e+03, atom= 2656
Step=  713, Dmax= 1.3e-02 nm, Epot= -3.06518e+06 Fmax= 6.80842e+03, atom= 2656
Step=  715, Dmax= 7.7e-03 nm, Epot= -3.06528e+06 Fmax= 3.19651e+03, atom= 2656
Step=  716, Dmax= 9.2e-03 nm, Epot= -3.06536e+06 Fmax= 8.82967e+03, atom= 2656
Step=  717, Dmax= 1.1e-02 nm, Epot= -3.06548e+06 Fmax= 5.60081e+03, atom= 2656
Step=  718, Dmax= 1.3e-02 nm, Epot= -3.06550e+06 Fmax= 1.16759e+04, atom= 2656
Step=  719, Dmax= 1.6e-02 nm, Epot= -3.06564e+06 Fmax= 9.12112e+03, atom= 2656
Step=  721, Dmax= 9.5e-03 nm, Epot= -3.06577e+06 Fmax= 3.37935e+03, atom= 2656
Step=  722, Dmax= 1.1e-02 nm, Epot= -3.06582e+06 Fmax= 1.15962e+04, atom= 2656
Step=  723, Dmax= 1.4e-02 nm, Epot= -3.06599e+06 Fmax= 6.37197e+03, atom= 2656
Step=  725, Dmax= 8.2e-03 nm, Epot= -3.06608e+06 Fmax= 4.39007e+03, atom= 2656
Step=  726, Dmax= 9.9e-03 nm, Epot= -3.06615e+06 Fmax= 8.53049e+03, atom= 2656
Step=  727, Dmax= 1.2e-02 nm, Epot= -3.06625e+06 Fmax= 6.99023e+03, atom= 2656
Step=  728, Dmax= 1.4e-02 nm, Epot= -3.06627e+06 Fmax= 1.15863e+04, atom= 2656
Step=  729, Dmax= 1.7e-02 nm, Epot= -3.06637e+06 Fmax= 1.07843e+04, atom= 2656
Step=  731, Dmax= 1.0e-02 nm, Epot= -3.06654e+06 Fmax= 2.66274e+03, atom= 2656
Step=  732, Dmax= 1.2e-02 nm, Epot= -3.06661e+06 Fmax= 1.34234e+04, atom= 2656
Step=  733, Dmax= 1.5e-02 nm, Epot= -3.06682e+06 Fmax= 5.89876e+03, atom= 2656
Step=  735, Dmax= 8.8e-03 nm, Epot= -3.06690e+06 Fmax= 5.68103e+03, atom= 2656
Step=  736, Dmax= 1.1e-02 nm, Epot= -3.06697e+06 Fmax= 8.20552e+03, atom= 2656
Step=  737, Dmax= 1.3e-02 nm, Epot= -3.06704e+06 Fmax= 8.48997e+03, atom= 2656
Step=  738, Dmax= 1.5e-02 nm, Epot= -3.06708e+06 Fmax= 1.14845e+04, atom= 2656
Step=  739, Dmax= 1.8e-02 nm, Epot= -3.06714e+06 Fmax= 1.25796e+04, atom= 2656
Step=  741, Dmax= 1.1e-02 nm, Epot= -3.06735e+06 Fmax= 1.88611e+03, atom= 2656
Step=  742, Dmax= 1.3e-02 nm, Epot= -3.06749e+06 Fmax= 1.53642e+04, atom= 2656
Step=  743, Dmax= 1.6e-02 nm, Epot= -3.06775e+06 Fmax= 5.40963e+03, atom= 2656
Step=  745, Dmax= 9.5e-03 nm, Epot= -3.06782e+06 Fmax= 7.06272e+03, atom= 2656
Step=  746, Dmax= 1.1e-02 nm, Epot= -3.06790e+06 Fmax= 7.86265e+03, atom= 2656
Step=  747, Dmax= 1.4e-02 nm, Epot= -3.06795e+06 Fmax= 1.00998e+04, atom= 2656
Step=  748, Dmax= 1.6e-02 nm, Epot= -3.06801e+06 Fmax= 1.13780e+04, atom= 2656
Step=  749, Dmax= 2.0e-02 nm, Epot= -3.06802e+06 Fmax= 1.45104e+04, atom= 2656
Step=  750, Dmax= 2.4e-02 nm, Epot= -3.06805e+06 Fmax= 1.63840e+04, atom= 2656
Step=  752, Dmax= 1.4e-02 nm, Epot= -3.06836e+06 Fmax= 2.11288e+03, atom= 2656
Step=  753, Dmax= 1.7e-02 nm, Epot= -3.06836e+06 Fmax= 2.02923e+04, atom= 2656
Step=  754, Dmax= 2.0e-02 nm, Epot= -3.06880e+06 Fmax= 6.47134e+03, atom= 2656
Step=  756, Dmax= 1.2e-02 nm, Epot= -3.06885e+06 Fmax= 9.54068e+03, atom= 2656
Step=  757, Dmax= 1.5e-02 nm, Epot= -3.06893e+06 Fmax= 9.76210e+03, atom= 2656
Step=  758, Dmax= 1.8e-02 nm, Epot= -3.06893e+06 Fmax= 1.33049e+04, atom= 2656
Step=  759, Dmax= 2.1e-02 nm, Epot= -3.06898e+06 Fmax= 1.45110e+04, atom= 2656
Step=  761, Dmax= 1.3e-02 nm, Epot= -3.06924e+06 Fmax= 2.21264e+03, atom= 2656
Step=  762, Dmax= 1.5e-02 nm, Epot= -3.06929e+06 Fmax= 1.77191e+04, atom= 2656
Step=  763, Dmax= 1.8e-02 nm, Epot= -3.06962e+06 Fmax= 6.28942e+03, atom= 2656
Step=  765, Dmax= 1.1e-02 nm, Epot= -3.06968e+06 Fmax= 8.12455e+03, atom= 2656
Step=  766, Dmax= 1.3e-02 nm, Epot= -3.06975e+06 Fmax= 9.11862e+03, atom= 2656
Step=  767, Dmax= 1.6e-02 nm, Epot= -3.06979e+06 Fmax= 1.16420e+04, atom= 2656
Step=  768, Dmax= 1.9e-02 nm, Epot= -3.06983e+06 Fmax= 1.31678e+04, atom= 2656
Step=  770, Dmax= 1.1e-02 nm, Epot= -3.07005e+06 Fmax= 1.68876e+03, atom= 2656
Step=  771, Dmax= 1.4e-02 nm, Epot= -3.07020e+06 Fmax= 1.62925e+04, atom= 2656
Step=  772, Dmax= 1.6e-02 nm, Epot= -3.07049e+06 Fmax= 5.18308e+03, atom= 2656
Step=  774, Dmax= 9.8e-03 nm, Epot= -3.07056e+06 Fmax= 7.67637e+03, atom= 2656
Step=  775, Dmax= 1.2e-02 nm, Epot= -3.07063e+06 Fmax= 7.80806e+03, atom= 2656
Step=  776, Dmax= 1.4e-02 nm, Epot= -3.07067e+06 Fmax= 1.07149e+04, atom= 2656
Step=  777, Dmax= 1.7e-02 nm, Epot= -3.07073e+06 Fmax= 1.15966e+04, atom= 2656
Step=  779, Dmax= 1.0e-02 nm, Epot= -3.07091e+06 Fmax= 1.81401e+03, atom= 2656
Step=  780, Dmax= 1.2e-02 nm, Epot= -3.07106e+06 Fmax= 1.41865e+04, atom= 2656
Step=  781, Dmax= 1.5e-02 nm, Epot= -3.07128e+06 Fmax= 5.07626e+03, atom= 2656
Step=  783, Dmax= 8.8e-03 nm, Epot= -3.07135e+06 Fmax= 6.48508e+03, atom= 2656
Step=  784, Dmax= 1.1e-02 nm, Epot= -3.07142e+06 Fmax= 7.35754e+03, atom= 2656
Step=  785, Dmax= 1.3e-02 nm, Epot= -3.07148e+06 Fmax= 9.29607e+03, atom= 2656
Step=  786, Dmax= 1.5e-02 nm, Epot= -3.07154e+06 Fmax= 1.06232e+04, atom= 2656
Step=  787, Dmax= 1.8e-02 nm, Epot= -3.07156e+06 Fmax= 1.33777e+04, atom= 2656
Step=  788, Dmax= 2.2e-02 nm, Epot= -3.07158e+06 Fmax= 1.52769e+04, atom= 2656
Step=  790, Dmax= 1.3e-02 nm, Epot= -3.07186e+06 Fmax= 1.88128e+03, atom= 2656
Step=  791, Dmax= 1.6e-02 nm, Epot= -3.07191e+06 Fmax= 1.89022e+04, atom= 2656
Step=  792, Dmax= 1.9e-02 nm, Epot= -3.07229e+06 Fmax= 5.91870e+03, atom= 2656
Step=  794, Dmax= 1.1e-02 nm, Epot= -3.07234e+06 Fmax= 8.92859e+03, atom= 2656
Step=  795, Dmax= 1.4e-02 nm, Epot= -3.07242e+06 Fmax= 8.96989e+03, atom= 2656
Step=  796, Dmax= 1.6e-02 nm, Epot= -3.07243e+06 Fmax= 1.24236e+04, atom= 2656
Step=  797, Dmax= 2.0e-02 nm, Epot= -3.07248e+06 Fmax= 1.33663e+04, atom= 2656
Step=  799, Dmax= 1.2e-02 nm, Epot= -3.07271e+06 Fmax= 2.13685e+03, atom= 2656
Step=  800, Dmax= 1.4e-02 nm, Epot= -3.07278e+06 Fmax= 1.63564e+04, atom= 2656
Step=  801, Dmax= 1.7e-02 nm, Epot= -3.07305e+06 Fmax= 5.90547e+03, atom= 2656
Step=  803, Dmax= 1.0e-02 nm, Epot= -3.07312e+06 Fmax= 7.45627e+03, atom= 2656
Step=  804, Dmax= 1.2e-02 nm, Epot= -3.07319e+06 Fmax= 8.53530e+03, atom= 2656
Step=  805, Dmax= 1.5e-02 nm, Epot= -3.07323e+06 Fmax= 1.07131e+04, atom= 2656
Step=  806, Dmax= 1.8e-02 nm, Epot= -3.07327e+06 Fmax= 1.22966e+04, atom= 2656
Step=  808, Dmax= 1.1e-02 nm, Epot= -3.07346e+06 Fmax= 1.48417e+03, atom= 2656
Step=  809, Dmax= 1.3e-02 nm, Epot= -3.07364e+06 Fmax= 1.51944e+04, atom= 2656
Step=  810, Dmax= 1.5e-02 nm, Epot= -3.07390e+06 Fmax= 4.72352e+03, atom= 2656
Step=  812, Dmax= 9.1e-03 nm, Epot= -3.07396e+06 Fmax= 7.19916e+03, atom= 2656
Step=  813, Dmax= 1.1e-02 nm, Epot= -3.07404e+06 Fmax= 7.15989e+03, atom= 2656
Step=  814, Dmax= 1.3e-02 nm, Epot= -3.07408e+06 Fmax= 1.00179e+04, atom= 2656
Step=  815, Dmax= 1.6e-02 nm, Epot= -3.07414e+06 Fmax= 1.06698e+04, atom= 2656
Step=  817, Dmax= 9.5e-03 nm, Epot= -3.07429e+06 Fmax= 1.76233e+03, atom= 2656
Step=  818, Dmax= 1.1e-02 nm, Epot= -3.07444e+06 Fmax= 1.30849e+04, atom= 2656
Step=  819, Dmax= 1.4e-02 nm, Epot= -3.07464e+06 Fmax= 4.77637e+03, atom= 2656
Step=  821, Dmax= 8.2e-03 nm, Epot= -3.07471e+06 Fmax= 5.94232e+03, atom= 2656
Step=  822, Dmax= 9.8e-03 nm, Epot= -3.07477e+06 Fmax= 6.89478e+03, atom= 2656
Step=  823, Dmax= 1.2e-02 nm, Epot= -3.07483e+06 Fmax= 8.54658e+03, atom= 2656
Step=  824, Dmax= 1.4e-02 nm, Epot= -3.07488e+06 Fmax= 9.92696e+03, atom= 2656
Step=  825, Dmax= 1.7e-02 nm, Epot= -3.07491e+06 Fmax= 1.23261e+04, atom= 2656
Step=  826, Dmax= 2.0e-02 nm, Epot= -3.07494e+06 Fmax= 1.42502e+04, atom= 2656
Step=  828, Dmax= 1.2e-02 nm, Epot= -3.07518e+06 Fmax= 1.66684e+03, atom= 2656
Step=  829, Dmax= 1.5e-02 nm, Epot= -3.07528e+06 Fmax= 1.76080e+04, atom= 2656
Step=  830, Dmax= 1.8e-02 nm, Epot= -3.07561e+06 Fmax= 5.41181e+03, atom= 2656
Step=  832, Dmax= 1.1e-02 nm, Epot= -3.07566e+06 Fmax= 8.35479e+03, atom= 2656
Step=  833, Dmax= 1.3e-02 nm, Epot= -3.07574e+06 Fmax= 8.24275e+03, atom= 2656
Step=  834, Dmax= 1.5e-02 nm, Epot= -3.07575e+06 Fmax= 1.15981e+04, atom= 2656
Step=  835, Dmax= 1.8e-02 nm, Epot= -3.07581e+06 Fmax= 1.23149e+04, atom= 2656
Step=  837, Dmax= 1.1e-02 nm, Epot= -3.07600e+06 Fmax= 2.05665e+03, atom= 2656
Step=  838, Dmax= 1.3e-02 nm, Epot= -3.07608e+06 Fmax= 1.51032e+04, atom= 2656
Step=  839, Dmax= 1.6e-02 nm, Epot= -3.07632e+06 Fmax= 5.53879e+03, atom= 2656
Step=  841, Dmax= 9.4e-03 nm, Epot= -3.07638e+06 Fmax= 6.84926e+03, atom= 2656
Step=  842, Dmax= 1.1e-02 nm, Epot= -3.07645e+06 Fmax= 7.98146e+03, atom= 2656
Step=  843, Dmax= 1.4e-02 nm, Epot= -3.07649e+06 Fmax= 9.86582e+03, atom= 2656
Step=  844, Dmax= 1.6e-02 nm, Epot= -3.07653e+06 Fmax= 1.14739e+04, atom= 2656
Step=  845, Dmax= 2.0e-02 nm, Epot= -3.07654e+06 Fmax= 1.42491e+04, atom= 2656
Step=  846, Dmax= 2.4e-02 nm, Epot= -3.07655e+06 Fmax= 1.64468e+04, atom= 2656
Step=  848, Dmax= 1.4e-02 nm, Epot= -3.07685e+06 Fmax= 1.93293e+03, atom= 2656
Step=  850, Dmax= 8.5e-03 nm, Epot= -3.07697e+06 Fmax= 9.26455e+03, atom= 2656
Step=  851, Dmax= 1.0e-02 nm, Epot= -3.07709e+06 Fmax= 4.03845e+03, atom= 2656
Step=  852, Dmax= 1.2e-02 nm, Epot= -3.07711e+06 Fmax= 1.18573e+04, atom= 2656
Step=  853, Dmax= 1.5e-02 nm, Epot= -3.07725e+06 Fmax= 7.29181e+03, atom= 2656
Step=  855, Dmax= 8.8e-03 nm, Epot= -3.07734e+06 Fmax= 4.21840e+03, atom= 2656
Step=  856, Dmax= 1.1e-02 nm, Epot= -3.07738e+06 Fmax= 9.58317e+03, atom= 2656
Step=  857, Dmax= 1.3e-02 nm, Epot= -3.07748e+06 Fmax= 6.96388e+03, atom= 2656
Step=  859, Dmax= 7.6e-03 nm, Epot= -3.07757e+06 Fmax= 2.94619e+03, atom= 2656
Step=  860, Dmax= 9.1e-03 nm, Epot= -3.07764e+06 Fmax= 8.96605e+03, atom= 2656
Step=  861, Dmax= 1.1e-02 nm, Epot= -3.07775e+06 Fmax= 5.32825e+03, atom= 2656
Step=  863, Dmax= 6.5e-03 nm, Epot= -3.07782e+06 Fmax= 3.26184e+03, atom= 2656
Step=  864, Dmax= 7.9e-03 nm, Epot= -3.07789e+06 Fmax= 7.03666e+03, atom= 2656
Step=  865, Dmax= 9.4e-03 nm, Epot= -3.07797e+06 Fmax= 5.31739e+03, atom= 2656
Step=  866, Dmax= 1.1e-02 nm, Epot= -3.07800e+06 Fmax= 9.53644e+03, atom= 2656
Step=  867, Dmax= 1.4e-02 nm, Epot= -3.07809e+06 Fmax= 8.24015e+03, atom= 2656
Step=  869, Dmax= 8.1e-03 nm, Epot= -3.07820e+06 Fmax= 2.40977e+03, atom= 2656
Step=  870, Dmax= 9.8e-03 nm, Epot= -3.07828e+06 Fmax= 1.03963e+04, atom= 2656
Step=  871, Dmax= 1.2e-02 nm, Epot= -3.07841e+06 Fmax= 4.96841e+03, atom= 2656
Step=  873, Dmax= 7.0e-03 nm, Epot= -3.07848e+06 Fmax= 4.25897e+03, atom= 2656
Step=  874, Dmax= 8.4e-03 nm, Epot= -3.07854e+06 Fmax= 6.81643e+03, atom= 2656
Step=  875, Dmax= 1.0e-02 nm, Epot= -3.07861e+06 Fmax= 6.45676e+03, atom= 2656
Step=  876, Dmax= 1.2e-02 nm, Epot= -3.07865e+06 Fmax= 9.50910e+03, atom= 2656
Step=  877, Dmax= 1.5e-02 nm, Epot= -3.07872e+06 Fmax= 9.58912e+03, atom= 2656
Step=  879, Dmax= 8.8e-03 nm, Epot= -3.07885e+06 Fmax= 1.85294e+03, atom= 2656
Step=  880, Dmax= 1.1e-02 nm, Epot= -3.07896e+06 Fmax= 1.19282e+04, atom= 2656
Step=  881, Dmax= 1.3e-02 nm, Epot= -3.07912e+06 Fmax= 4.58768e+03, atom= 2656
Step=  883, Dmax= 7.6e-03 nm, Epot= -3.07919e+06 Fmax= 5.32141e+03, atom= 2656
Step=  884, Dmax= 9.1e-03 nm, Epot= -3.07926e+06 Fmax= 6.58650e+03, atom= 2656
Step=  885, Dmax= 1.1e-02 nm, Epot= -3.07931e+06 Fmax= 7.67281e+03, atom= 2656
Step=  886, Dmax= 1.3e-02 nm, Epot= -3.07936e+06 Fmax= 9.48721e+03, atom= 2656
Step=  887, Dmax= 1.6e-02 nm, Epot= -3.07940e+06 Fmax= 1.10307e+04, atom= 2656
Step=  888, Dmax= 1.9e-02 nm, Epot= -3.07941e+06 Fmax= 1.37007e+04, atom= 2656
Step=  889, Dmax= 2.3e-02 nm, Epot= -3.07942e+06 Fmax= 1.58146e+04, atom= 2656
Step=  891, Dmax= 1.4e-02 nm, Epot= -3.07970e+06 Fmax= 1.86167e+03, atom= 2656
Step=  893, Dmax= 8.1e-03 nm, Epot= -3.07981e+06 Fmax= 8.89644e+03, atom= 2656
Step=  894, Dmax= 9.8e-03 nm, Epot= -3.07992e+06 Fmax= 3.89513e+03, atom= 2656
Step=  895, Dmax= 1.2e-02 nm, Epot= -3.07994e+06 Fmax= 1.13881e+04, atom= 2656
Step=  896, Dmax= 1.4e-02 nm, Epot= -3.08008e+06 Fmax= 7.02430e+03, atom= 2656
Step=  898, Dmax= 8.4e-03 nm, Epot= -3.08017e+06 Fmax= 4.04080e+03, atom= 2656
Step=  899, Dmax= 1.0e-02 nm, Epot= -3.08021e+06 Fmax= 9.23026e+03, atom= 2656
Step=  900, Dmax= 1.2e-02 nm, Epot= -3.08030e+06 Fmax= 6.67833e+03, atom= 2656
Step=  902, Dmax= 7.3e-03 nm, Epot= -3.08039e+06 Fmax= 2.85164e+03, atom= 2656
Step=  903, Dmax= 8.7e-03 nm, Epot= -3.08045e+06 Fmax= 8.59898e+03, atom= 2656
Step=  904, Dmax= 1.0e-02 nm, Epot= -3.08056e+06 Fmax= 5.14574e+03, atom= 2656
Step=  905, Dmax= 1.3e-02 nm, Epot= -3.08056e+06 Fmax= 1.13050e+04, atom= 2656
Step=  906, Dmax= 1.5e-02 nm, Epot= -3.08067e+06 Fmax= 8.50156e+03, atom= 2656
Step=  908, Dmax= 9.1e-03 nm, Epot= -3.08078e+06 Fmax= 3.39924e+03, atom= 2656
Step=  909, Dmax= 1.1e-02 nm, Epot= -3.08081e+06 Fmax= 1.08680e+04, atom= 2656
Step=  910, Dmax= 1.3e-02 nm, Epot= -3.08094e+06 Fmax= 6.24073e+03, atom= 2656
Step=  912, Dmax= 7.8e-03 nm, Epot= -3.08102e+06 Fmax= 4.00988e+03, atom= 2656
Step=  913, Dmax= 9.4e-03 nm, Epot= -3.08107e+06 Fmax= 8.29321e+03, atom= 2656
Step=  914, Dmax= 1.1e-02 nm, Epot= -3.08115e+06 Fmax= 6.48898e+03, atom= 2656
Step=  915, Dmax= 1.4e-02 nm, Epot= -3.08116e+06 Fmax= 1.12005e+04, atom= 2656
Step=  916, Dmax= 1.6e-02 nm, Epot= -3.08124e+06 Fmax= 1.01035e+04, atom= 2656
Step=  918, Dmax= 9.7e-03 nm, Epot= -3.08138e+06 Fmax= 2.69794e+03, atom= 2656
Step=  919, Dmax= 1.2e-02 nm, Epot= -3.08142e+06 Fmax= 1.26305e+04, atom= 2656
Step=  920, Dmax= 1.4e-02 nm, Epot= -3.08159e+06 Fmax= 5.76725e+03, atom= 2656
Step=  922, Dmax= 8.4e-03 nm, Epot= -3.08165e+06 Fmax= 5.26090e+03, atom= 2656
Step=  923, Dmax= 1.0e-02 nm, Epot= -3.08170e+06 Fmax= 7.96247e+03, atom= 2656
Step=  924, Dmax= 1.2e-02 nm, Epot= -3.08176e+06 Fmax= 7.93749e+03, atom= 2656
Step=  925, Dmax= 1.5e-02 nm, Epot= -3.08179e+06 Fmax= 1.10834e+04, atom= 2656
Step=  926, Dmax= 1.7e-02 nm, Epot= -3.08184e+06 Fmax= 1.18325e+04, atom= 2656
Step=  928, Dmax= 1.0e-02 nm, Epot= -3.08201e+06 Fmax= 1.93957e+03, atom= 2656
Step=  929, Dmax= 1.3e-02 nm, Epot= -3.08208e+06 Fmax= 1.45062e+04, atom= 2656
Step=  930, Dmax= 1.5e-02 nm, Epot= -3.08230e+06 Fmax= 5.27445e+03, atom= 2656
Step=  932, Dmax= 9.1e-03 nm, Epot= -3.08236e+06 Fmax= 6.60040e+03, atom= 2656
Step=  933, Dmax= 1.1e-02 nm, Epot= -3.08241e+06 Fmax= 7.61214e+03, atom= 2656
Step=  934, Dmax= 1.3e-02 nm, Epot= -3.08246e+06 Fmax= 9.49336e+03, atom= 2656
Step=  935, Dmax= 1.6e-02 nm, Epot= -3.08249e+06 Fmax= 1.09594e+04, atom= 2656
Step=  936, Dmax= 1.9e-02 nm, Epot= -3.08251e+06 Fmax= 1.36928e+04, atom= 2656
Step=  937, Dmax= 2.3e-02 nm, Epot= -3.08251e+06 Fmax= 1.57286e+04, atom= 2656
Step=  939, Dmax= 1.4e-02 nm, Epot= -3.08278e+06 Fmax= 1.89154e+03, atom= 2656
Step=  941, Dmax= 8.1e-03 nm, Epot= -3.08289e+06 Fmax= 8.82957e+03, atom= 2656
Step=  942, Dmax= 9.7e-03 nm, Epot= -3.08300e+06 Fmax= 3.92063e+03, atom= 2656
Step=  943, Dmax= 1.2e-02 nm, Epot= -3.08301e+06 Fmax= 1.13158e+04, atom= 2656
Step=  944, Dmax= 1.4e-02 nm, Epot= -3.08314e+06 Fmax= 7.03814e+03, atom= 2656
Step=  946, Dmax= 8.4e-03 nm, Epot= -3.08322e+06 Fmax= 3.99144e+03, atom= 2656
Step=  947, Dmax= 1.0e-02 nm, Epot= -3.08326e+06 Fmax= 9.23719e+03, atom= 2656
Step=  948, Dmax= 1.2e-02 nm, Epot= -3.08335e+06 Fmax= 6.62098e+03, atom= 2656
Step=  950, Dmax= 7.3e-03 nm, Epot= -3.08343e+06 Fmax= 2.87882e+03, atom= 2656
Step=  951, Dmax= 8.7e-03 nm, Epot= -3.08349e+06 Fmax= 8.53498e+03, atom= 2656
Step=  952, Dmax= 1.0e-02 nm, Epot= -3.08358e+06 Fmax= 5.16604e+03, atom= 2656
Step=  953, Dmax= 1.3e-02 nm, Epot= -3.08359e+06 Fmax= 1.12323e+04, atom= 2656
Step=  954, Dmax= 1.5e-02 nm, Epot= -3.08370e+06 Fmax= 8.51167e+03, atom= 2656
Step=  956, Dmax= 9.0e-03 nm, Epot= -3.08380e+06 Fmax= 3.35123e+03, atom= 2656
Step=  957, Dmax= 1.1e-02 nm, Epot= -3.08383e+06 Fmax= 1.08707e+04, atom= 2656
Step=  958, Dmax= 1.3e-02 nm, Epot= -3.08395e+06 Fmax= 6.18320e+03, atom= 2656
Step=  960, Dmax= 7.8e-03 nm, Epot= -3.08402e+06 Fmax= 4.03481e+03, atom= 2656
Step=  961, Dmax= 9.4e-03 nm, Epot= -3.08407e+06 Fmax= 8.22844e+03, atom= 2656
Step=  962, Dmax= 1.1e-02 nm, Epot= -3.08415e+06 Fmax= 6.50709e+03, atom= 2656
Step=  963, Dmax= 1.3e-02 nm, Epot= -3.08416e+06 Fmax= 1.11254e+04, atom= 2656
Step=  964, Dmax= 1.6e-02 nm, Epot= -3.08424e+06 Fmax= 1.01114e+04, atom= 2656
Step=  966, Dmax= 9.7e-03 nm, Epot= -3.08437e+06 Fmax= 2.64922e+03, atom= 2656
Step=  967, Dmax= 1.2e-02 nm, Epot= -3.08441e+06 Fmax= 1.26302e+04, atom= 2656
Step=  968, Dmax= 1.4e-02 nm, Epot= -3.08457e+06 Fmax= 5.70851e+03, atom= 2656
Step=  970, Dmax= 8.4e-03 nm, Epot= -3.08463e+06 Fmax= 5.28546e+03, atom= 2656
Step=  971, Dmax= 1.0e-02 nm, Epot= -3.08468e+06 Fmax= 7.89483e+03, atom= 2656
Step=  972, Dmax= 1.2e-02 nm, Epot= -3.08474e+06 Fmax= 7.95507e+03, atom= 2656
Step=  973, Dmax= 1.5e-02 nm, Epot= -3.08476e+06 Fmax= 1.10048e+04, atom= 2656
Step=  974, Dmax= 1.7e-02 nm, Epot= -3.08480e+06 Fmax= 1.18392e+04, atom= 2656
Step=  976, Dmax= 1.0e-02 nm, Epot= -3.08497e+06 Fmax= 1.88821e+03, atom= 2656
Step=  977, Dmax= 1.3e-02 nm, Epot= -3.08505e+06 Fmax= 1.45046e+04, atom= 2656
Step=  978, Dmax= 1.5e-02 nm, Epot= -3.08525e+06 Fmax= 5.21239e+03, atom= 2656
Step=  980, Dmax= 9.0e-03 nm, Epot= -3.08531e+06 Fmax= 6.62647e+03, atom= 2656
Step=  981, Dmax= 1.1e-02 nm, Epot= -3.08536e+06 Fmax= 7.54030e+03, atom= 2656
Step=  982, Dmax= 1.3e-02 nm, Epot= -3.08540e+06 Fmax= 9.51194e+03, atom= 2656
Step=  983, Dmax= 1.6e-02 nm, Epot= -3.08544e+06 Fmax= 1.08750e+04, atom= 2656
Step=  984, Dmax= 1.9e-02 nm, Epot= -3.08545e+06 Fmax= 1.36996e+04, atom= 2656
Step=  985, Dmax= 2.2e-02 nm, Epot= -3.08545e+06 Fmax= 1.56285e+04, atom= 2656
Step=  987, Dmax= 1.3e-02 nm, Epot= -3.08571e+06 Fmax= 1.93666e+03, atom= 2656
Step=  989, Dmax= 8.1e-03 nm, Epot= -3.08581e+06 Fmax= 8.74529e+03, atom= 2656
Step=  990, Dmax= 9.7e-03 nm, Epot= -3.08591e+06 Fmax= 3.96358e+03, atom= 2656
Step=  991, Dmax= 1.2e-02 nm, Epot= -3.08592e+06 Fmax= 1.12256e+04, atom= 2656
Step=  992, Dmax= 1.4e-02 nm, Epot= -3.08604e+06 Fmax= 7.07115e+03, atom= 2656
Step=  994, Dmax= 8.4e-03 nm, Epot= -3.08612e+06 Fmax= 3.92306e+03, atom= 2656
Step=  995, Dmax= 1.0e-02 nm, Epot= -3.08615e+06 Fmax= 9.26402e+03, atom= 2656
Step=  996, Dmax= 1.2e-02 nm, Epot= -3.08624e+06 Fmax= 6.54299e+03, atom= 2656
Step=  998, Dmax= 7.2e-03 nm, Epot= -3.08632e+06 Fmax= 2.92713e+03, atom= 2656
Step=  999, Dmax= 8.7e-03 nm, Epot= -3.08638e+06 Fmax= 8.44854e+03, atom= 2656
Step= 1000, Dmax= 1.0e-02 nm, Epot= -3.08647e+06 Fmax= 5.20964e+03, atom= 2656
Step= 1001, Dmax= 1.3e-02 nm, Epot= -3.08647e+06 Fmax= 1.11363e+04, atom= 2656
Step= 1002, Dmax= 1.5e-02 nm, Epot= -3.08657e+06 Fmax= 8.54551e+03, atom= 2656
Step= 1004, Dmax= 9.0e-03 nm, Epot= -3.08667e+06 Fmax= 3.27913e+03, atom= 2656
Step= 1005, Dmax= 1.1e-02 nm, Epot= -3.08670e+06 Fmax= 1.08982e+04, atom= 2656
Step= 1006, Dmax= 1.3e-02 nm, Epot= -3.08682e+06 Fmax= 6.10117e+03, atom= 2656
Step= 1008, Dmax= 7.8e-03 nm, Epot= -3.08689e+06 Fmax= 4.08547e+03, atom= 2656
Step= 1009, Dmax= 9.3e-03 nm, Epot= -3.08693e+06 Fmax= 8.13766e+03, atom= 2656
Step= 1010, Dmax= 1.1e-02 nm, Epot= -3.08701e+06 Fmax= 6.55183e+03, atom= 2656
Step= 1011, Dmax= 1.3e-02 nm, Epot= -3.08701e+06 Fmax= 1.10245e+04, atom= 2656
Step= 1012, Dmax= 1.6e-02 nm, Epot= -3.08709e+06 Fmax= 1.01457e+04, atom= 2656
Step= 1014, Dmax= 9.7e-03 nm, Epot= -3.08721e+06 Fmax= 2.57413e+03, atom= 2656
Step= 1015, Dmax= 1.2e-02 nm, Epot= -3.08725e+06 Fmax= 1.26570e+04, atom= 2656
Step= 1016, Dmax= 1.4e-02 nm, Epot= -3.08741e+06 Fmax= 5.62322e+03, atom= 2656
Step= 1018, Dmax= 8.4e-03 nm, Epot= -3.08747e+06 Fmax= 5.33712e+03, atom= 2656
Step= 1019, Dmax= 1.0e-02 nm, Epot= -3.08751e+06 Fmax= 7.80049e+03, atom= 2656
Step= 1020, Dmax= 1.2e-02 nm, Epot= -3.08757e+06 Fmax= 8.00036e+03, atom= 2656
Step= 1021, Dmax= 1.4e-02 nm, Epot= -3.08758e+06 Fmax= 1.08992e+04, atom= 2656
Step= 1022, Dmax= 1.7e-02 nm, Epot= -3.08763e+06 Fmax= 1.18736e+04, atom= 2656
Step= 1024, Dmax= 1.0e-02 nm, Epot= -3.08778e+06 Fmax= 1.81015e+03, atom= 2656
Step= 1025, Dmax= 1.2e-02 nm, Epot= -3.08787e+06 Fmax= 1.45288e+04, atom= 2656
Step= 1026, Dmax= 1.5e-02 nm, Epot= -3.08807e+06 Fmax= 5.12463e+03, atom= 2656
Step= 1028, Dmax= 9.0e-03 nm, Epot= -3.08812e+06 Fmax= 6.67933e+03, atom= 2656
Step= 1029, Dmax= 1.1e-02 nm, Epot= -3.08817e+06 Fmax= 7.44161e+03, atom= 2656
Step= 1030, Dmax= 1.3e-02 nm, Epot= -3.08821e+06 Fmax= 9.55812e+03, atom= 2656
Step= 1031, Dmax= 1.6e-02 nm, Epot= -3.08824e+06 Fmax= 1.07644e+04, atom= 2656
Step= 1032, Dmax= 1.9e-02 nm, Epot= -3.08825e+06 Fmax= 1.37336e+04, atom= 2656
Step= 1033, Dmax= 2.2e-02 nm, Epot= -3.08826e+06 Fmax= 1.55016e+04, atom= 2656
Step= 1035, Dmax= 1.3e-02 nm, Epot= -3.08850e+06 Fmax= 2.00919e+03, atom= 2656
Step= 1037, Dmax= 8.1e-03 nm, Epot= -3.08859e+06 Fmax= 8.63197e+03, atom= 2656
Step= 1038, Dmax= 9.7e-03 nm, Epot= -3.08868e+06 Fmax= 4.03566e+03, atom= 2656
Step= 1039, Dmax= 1.2e-02 nm, Epot= -3.08870e+06 Fmax= 1.11077e+04, atom= 2656
Step= 1040, Dmax= 1.4e-02 nm, Epot= -3.08881e+06 Fmax= 7.13167e+03, atom= 2656
Step= 1042, Dmax= 8.4e-03 nm, Epot= -3.08889e+06 Fmax= 3.82748e+03, atom= 2656
Step= 1043, Dmax= 1.0e-02 nm, Epot= -3.08892e+06 Fmax= 9.31834e+03, atom= 2656
Step= 1044, Dmax= 1.2e-02 nm, Epot= -3.08901e+06 Fmax= 6.43842e+03, atom= 2656
Step= 1046, Dmax= 7.2e-03 nm, Epot= -3.08908e+06 Fmax= 3.00238e+03, atom= 2656
Step= 1047, Dmax= 8.7e-03 nm, Epot= -3.08913e+06 Fmax= 8.33559e+03, atom= 2656
Step= 1048, Dmax= 1.0e-02 nm, Epot= -3.08921e+06 Fmax= 5.27995e+03, atom= 2656
Step= 1049, Dmax= 1.2e-02 nm, Epot= -3.08922e+06 Fmax= 1.10134e+04, atom= 2656
Step= 1050, Dmax= 1.5e-02 nm, Epot= -3.08931e+06 Fmax= 8.60701e+03, atom= 2656
Step= 1052, Dmax= 9.0e-03 nm, Epot= -3.08941e+06 Fmax= 3.17987e+03, atom= 2656
Step= 1053, Dmax= 1.1e-02 nm, Epot= -3.08944e+06 Fmax= 1.09531e+04, atom= 2656
Step= 1054, Dmax= 1.3e-02 nm, Epot= -3.08956e+06 Fmax= 5.99208e+03, atom= 2656
Step= 1056, Dmax= 7.8e-03 nm, Epot= -3.08962e+06 Fmax= 4.16332e+03, atom= 2656
Step= 1057, Dmax= 9.3e-03 nm, Epot= -3.08966e+06 Fmax= 8.01966e+03, atom= 2656
Step= 1058, Dmax= 1.1e-02 nm, Epot= -3.08973e+06 Fmax= 6.62385e+03, atom= 2656
Step= 1059, Dmax= 1.3e-02 nm, Epot= -3.08974e+06 Fmax= 1.08966e+04, atom= 2656
Step= 1060, Dmax= 1.6e-02 nm, Epot= -3.08981e+06 Fmax= 1.02079e+04, atom= 2656
Step= 1062, Dmax= 9.7e-03 nm, Epot= -3.08993e+06 Fmax= 2.47140e+03, atom= 2656
Step= 1063, Dmax= 1.2e-02 nm, Epot= -3.08997e+06 Fmax= 1.27109e+04, atom= 2656
Step= 1064, Dmax= 1.4e-02 nm, Epot= -3.09012e+06 Fmax= 5.51048e+03, atom= 2656
Step= 1066, Dmax= 8.3e-03 nm, Epot= -3.09018e+06 Fmax= 5.41676e+03, atom= 2656
Step= 1067, Dmax= 1.0e-02 nm, Epot= -3.09022e+06 Fmax= 7.67826e+03, atom= 2656
Step= 1068, Dmax= 1.2e-02 nm, Epot= -3.09027e+06 Fmax= 8.07362e+03, atom= 2656
Step= 1069, Dmax= 1.4e-02 nm, Epot= -3.09029e+06 Fmax= 1.07657e+04, atom= 2656
Step= 1070, Dmax= 1.7e-02 nm, Epot= -3.09033e+06 Fmax= 1.19361e+04, atom= 2656
Step= 1072, Dmax= 1.0e-02 nm, Epot= -3.09048e+06 Fmax= 1.70422e+03, atom= 2656
Step= 1073, Dmax= 1.2e-02 nm, Epot= -3.09057e+06 Fmax= 1.45790e+04, atom= 2656
Step= 1074, Dmax= 1.5e-02 nm, Epot= -3.09076e+06 Fmax= 5.01042e+03, atom= 2656
Step= 1076, Dmax= 9.0e-03 nm, Epot= -3.09082e+06 Fmax= 6.76051e+03, atom= 2656
Step= 1077, Dmax= 1.1e-02 nm, Epot= -3.09086e+06 Fmax= 7.31496e+03, atom= 2656
Step= 1078, Dmax= 1.3e-02 nm, Epot= -3.09089e+06 Fmax= 9.63254e+03, atom= 2656
Step= 1079, Dmax= 1.5e-02 nm, Epot= -3.09093e+06 Fmax= 1.06254e+04, atom= 2656
Step= 1080, Dmax= 1.9e-02 nm, Epot= -3.09093e+06 Fmax= 1.37967e+04, atom= 2656
Step= 1081, Dmax= 2.2e-02 nm, Epot= -3.09095e+06 Fmax= 1.53465e+04, atom= 2656
Step= 1083, Dmax= 1.3e-02 nm, Epot= -3.09118e+06 Fmax= 2.11000e+03, atom= 2656
Step= 1085, Dmax= 8.0e-03 nm, Epot= -3.09126e+06 Fmax= 8.48939e+03, atom= 2656
Step= 1086, Dmax= 9.6e-03 nm, Epot= -3.09134e+06 Fmax= 4.13727e+03, atom= 2656
Step= 1087, Dmax= 1.2e-02 nm, Epot= -3.09136e+06 Fmax= 1.09605e+04, atom= 2656
Step= 1088, Dmax= 1.4e-02 nm, Epot= -3.09146e+06 Fmax= 7.22274e+03, atom= 2656
Step= 1090, Dmax= 8.3e-03 nm, Epot= -3.09153e+06 Fmax= 3.70136e+03, atom= 2656
Step= 1091, Dmax= 1.0e-02 nm, Epot= -3.09156e+06 Fmax= 9.40349e+03, atom= 2656
Step= 1092, Dmax= 1.2e-02 nm, Epot= -3.09166e+06 Fmax= 6.30352e+03, atom= 2656
Step= 1094, Dmax= 7.2e-03 nm, Epot= -3.09172e+06 Fmax= 3.10850e+03, atom= 2656
Step= 1095, Dmax= 8.6e-03 nm, Epot= -3.09177e+06 Fmax= 8.19161e+03, atom= 2656
Step= 1096, Dmax= 1.0e-02 nm, Epot= -3.09185e+06 Fmax= 5.38166e+03, atom= 2656
Step= 1097, Dmax= 1.2e-02 nm, Epot= -3.09186e+06 Fmax= 1.08603e+04, atom= 2656
Step= 1098, Dmax= 1.5e-02 nm, Epot= -3.09194e+06 Fmax= 8.69931e+03, atom= 2656
Step= 1100, Dmax= 8.9e-03 nm, Epot= -3.09203e+06 Fmax= 3.05024e+03, atom= 2656
Step= 1101, Dmax= 1.1e-02 nm, Epot= -3.09207e+06 Fmax= 1.10379e+04, atom= 2656
Step= 1102, Dmax= 1.3e-02 nm, Epot= -3.09218e+06 Fmax= 5.85317e+03, atom= 2656
Step= 1104, Dmax= 7.7e-03 nm, Epot= -3.09224e+06 Fmax= 4.27158e+03, atom= 2656
Step= 1105, Dmax= 9.3e-03 nm, Epot= -3.09228e+06 Fmax= 7.87159e+03, atom= 2656
Step= 1106, Dmax= 1.1e-02 nm, Epot= -3.09234e+06 Fmax= 6.72693e+03, atom= 2656
Step= 1107, Dmax= 1.3e-02 nm, Epot= -3.09235e+06 Fmax= 1.07380e+04, atom= 2656
Step= 1108, Dmax= 1.6e-02 nm, Epot= -3.09241e+06 Fmax= 1.03011e+04, atom= 2656
Step= 1110, Dmax= 9.6e-03 nm, Epot= -3.09252e+06 Fmax= 2.33826e+03, atom= 2656
Step= 1111, Dmax= 1.2e-02 nm, Epot= -3.09257e+06 Fmax= 1.27944e+04, atom= 2656
Step= 1112, Dmax= 1.4e-02 nm, Epot= -3.09272e+06 Fmax= 5.36893e+03, atom= 2656
Step= 1114, Dmax= 8.3e-03 nm, Epot= -3.09278e+06 Fmax= 5.52621e+03, atom= 2656
Step= 1115, Dmax= 1.0e-02 nm, Epot= -3.09282e+06 Fmax= 7.52619e+03, atom= 2656
Step= 1116, Dmax= 1.2e-02 nm, Epot= -3.09287e+06 Fmax= 8.17726e+03, atom= 2656
Step= 1117, Dmax= 1.4e-02 nm, Epot= -3.09289e+06 Fmax= 1.06028e+04, atom= 2656
Step= 1118, Dmax= 1.7e-02 nm, Epot= -3.09292e+06 Fmax= 1.20287e+04, atom= 2656
Step= 1120, Dmax= 1.0e-02 nm, Epot= -3.09306e+06 Fmax= 1.56837e+03, atom= 2656
Step= 1121, Dmax= 1.2e-02 nm, Epot= -3.09317e+06 Fmax= 1.46565e+04, atom= 2656
Step= 1122, Dmax= 1.5e-02 nm, Epot= -3.09336e+06 Fmax= 4.86884e+03, atom= 2656
Step= 1124, Dmax= 8.9e-03 nm, Epot= -3.09341e+06 Fmax= 6.87100e+03, atom= 2656
Step= 1125, Dmax= 1.1e-02 nm, Epot= -3.09346e+06 Fmax= 7.15847e+03, atom= 2656
Step= 1126, Dmax= 1.3e-02 nm, Epot= -3.09348e+06 Fmax= 9.73782e+03, atom= 2656
Step= 1127, Dmax= 1.5e-02 nm, Epot= -3.09352e+06 Fmax= 1.04561e+04, atom= 2656
Step= 1129, Dmax= 9.3e-03 nm, Epot= -3.09364e+06 Fmax= 1.64702e+03, atom= 2656
Step= 1130, Dmax= 1.1e-02 nm, Epot= -3.09374e+06 Fmax= 1.29311e+04, atom= 2656
Step= 1131, Dmax= 1.3e-02 nm, Epot= -3.09389e+06 Fmax= 4.54508e+03, atom= 2656
Step= 1133, Dmax= 8.0e-03 nm, Epot= -3.09394e+06 Fmax= 5.92700e+03, atom= 2656
Step= 1134, Dmax= 9.6e-03 nm, Epot= -3.09398e+06 Fmax= 6.67509e+03, atom= 2656
Step= 1135, Dmax= 1.2e-02 nm, Epot= -3.09403e+06 Fmax= 8.40167e+03, atom= 2656
Step= 1136, Dmax= 1.4e-02 nm, Epot= -3.09406e+06 Fmax= 9.75498e+03, atom= 2656
Step= 1137, Dmax= 1.7e-02 nm, Epot= -3.09408e+06 Fmax= 1.19405e+04, atom= 2656
Step= 1138, Dmax= 2.0e-02 nm, Epot= -3.09409e+06 Fmax= 1.42263e+04, atom= 2656
Step= 1140, Dmax= 1.2e-02 nm, Epot= -3.09428e+06 Fmax= 1.49699e+03, atom= 2656
Step= 1141, Dmax= 1.4e-02 nm, Epot= -3.09438e+06 Fmax= 1.72148e+04, atom= 2656
Step= 1142, Dmax= 1.7e-02 nm, Epot= -3.09462e+06 Fmax= 5.34619e+03, atom= 2656
Step= 1144, Dmax= 1.0e-02 nm, Epot= -3.09465e+06 Fmax= 8.24534e+03, atom= 2656
Step= 1145, Dmax= 1.2e-02 nm, Epot= -3.09471e+06 Fmax= 7.96244e+03, atom= 2656
Step= 1146, Dmax= 1.5e-02 nm, Epot= -3.09471e+06 Fmax= 1.15754e+04, atom= 2656
Step= 1147, Dmax= 1.8e-02 nm, Epot= -3.09476e+06 Fmax= 1.17560e+04, atom= 2656
Step= 1149, Dmax= 1.1e-02 nm, Epot= -3.09490e+06 Fmax= 2.22610e+03, atom= 2656
Step= 1150, Dmax= 1.3e-02 nm, Epot= -3.09492e+06 Fmax= 1.46053e+04, atom= 2656
Step= 1151, Dmax= 1.5e-02 nm, Epot= -3.09510e+06 Fmax= 5.58597e+03, atom= 2656
Step= 1153, Dmax= 9.2e-03 nm, Epot= -3.09515e+06 Fmax= 6.52145e+03, atom= 2656
Step= 1154, Dmax= 1.1e-02 nm, Epot= -3.09519e+06 Fmax= 8.04222e+03, atom= 2656
Step= 1155, Dmax= 1.3e-02 nm, Epot= -3.09523e+06 Fmax= 9.37998e+03, atom= 2656
Step= 1156, Dmax= 1.6e-02 nm, Epot= -3.09525e+06 Fmax= 1.16082e+04, atom= 2656
Step= 1157, Dmax= 1.9e-02 nm, Epot= -3.09527e+06 Fmax= 1.34576e+04, atom= 2656
Step= 1159, Dmax= 1.2e-02 nm, Epot= -3.09543e+06 Fmax= 1.56026e+03, atom= 2656
Step= 1160, Dmax= 1.4e-02 nm, Epot= -3.09551e+06 Fmax= 1.65998e+04, atom= 2656
Step= 1161, Dmax= 1.7e-02 nm, Epot= -3.09574e+06 Fmax= 5.11590e+03, atom= 2656
Step= 1163, Dmax= 9.9e-03 nm, Epot= -3.09578e+06 Fmax= 7.86493e+03, atom= 2656
Step= 1164, Dmax= 1.2e-02 nm, Epot= -3.09583e+06 Fmax= 7.79294e+03, atom= 2656
Step= 1165, Dmax= 1.4e-02 nm, Epot= -3.09584e+06 Fmax= 1.09183e+04, atom= 2656
Step= 1166, Dmax= 1.7e-02 nm, Epot= -3.09588e+06 Fmax= 1.16384e+04, atom= 2656
Step= 1168, Dmax= 1.0e-02 nm, Epot= -3.09602e+06 Fmax= 1.91169e+03, atom= 2656
Step= 1169, Dmax= 1.2e-02 nm, Epot= -3.09607e+06 Fmax= 1.42881e+04, atom= 2656
Step= 1170, Dmax= 1.5e-02 nm, Epot= -3.09624e+06 Fmax= 5.17635e+03, atom= 2656
Step= 1172, Dmax= 8.9e-03 nm, Epot= -3.09629e+06 Fmax= 6.51242e+03, atom= 2656
Step= 1173, Dmax= 1.1e-02 nm, Epot= -3.09633e+06 Fmax= 7.47211e+03, atom= 2656
Step= 1174, Dmax= 1.3e-02 nm, Epot= -3.09636e+06 Fmax= 9.36475e+03, atom= 2656
Step= 1175, Dmax= 1.5e-02 nm, Epot= -3.09639e+06 Fmax= 1.07608e+04, atom= 2656
Step= 1176, Dmax= 1.8e-02 nm, Epot= -3.09640e+06 Fmax= 1.35027e+04, atom= 2656
Step= 1177, Dmax= 2.2e-02 nm, Epot= -3.09641e+06 Fmax= 1.54503e+04, atom= 2656
Step= 1179, Dmax= 1.3e-02 nm, Epot= -3.09662e+06 Fmax= 1.89334e+03, atom= 2656
Step= 1181, Dmax= 8.0e-03 nm, Epot= -3.09670e+06 Fmax= 8.64726e+03, atom= 2656
Step= 1182, Dmax= 9.6e-03 nm, Epot= -3.09678e+06 Fmax= 3.90177e+03, atom= 2656
Step= 1183, Dmax= 1.1e-02 nm, Epot= -3.09679e+06 Fmax= 1.10897e+04, atom= 2656
Step= 1184, Dmax= 1.4e-02 nm, Epot= -3.09689e+06 Fmax= 6.97622e+03, atom= 2656
Step= 1186, Dmax= 8.3e-03 nm, Epot= -3.09696e+06 Fmax= 3.87626e+03, atom= 2656
Step= 1187, Dmax= 9.9e-03 nm, Epot= -3.09698e+06 Fmax= 9.14652e+03, atom= 2656
Step= 1188, Dmax= 1.2e-02 nm, Epot= -3.09706e+06 Fmax= 6.45797e+03, atom= 2656
Step= 1190, Dmax= 7.1e-03 nm, Epot= -3.09712e+06 Fmax= 2.89330e+03, atom= 2656
Step= 1191, Dmax= 8.6e-03 nm, Epot= -3.09716e+06 Fmax= 8.33368e+03, atom= 2656
Step= 1192, Dmax= 1.0e-02 nm, Epot= -3.09724e+06 Fmax= 5.15278e+03, atom= 2656
Step= 1193, Dmax= 1.2e-02 nm, Epot= -3.09724e+06 Fmax= 1.09824e+04, atom= 2656
Step= 1194, Dmax= 1.5e-02 nm, Epot= -3.09732e+06 Fmax= 8.45142e+03, atom= 2656
Step= 1196, Dmax= 8.9e-03 nm, Epot= -3.09741e+06 Fmax= 3.22078e+03, atom= 2656
Step= 1197, Dmax= 1.1e-02 nm, Epot= -3.09743e+06 Fmax= 1.07810e+04, atom= 2656
Step= 1198, Dmax= 1.3e-02 nm, Epot= -3.09753e+06 Fmax= 6.00005e+03, atom= 2656
Step= 1200, Dmax= 7.7e-03 nm, Epot= -3.09759e+06 Fmax= 4.05927e+03, atom= 2656
Step= 1201, Dmax= 9.2e-03 nm, Epot= -3.09762e+06 Fmax= 8.00531e+03, atom= 2656
Step= 1202, Dmax= 1.1e-02 nm, Epot= -3.09768e+06 Fmax= 6.49971e+03, atom= 2656
Step= 1203, Dmax= 1.3e-02 nm, Epot= -3.09769e+06 Fmax= 1.08508e+04, atom= 2656
Step= 1204, Dmax= 1.6e-02 nm, Epot= -3.09775e+06 Fmax= 1.00525e+04, atom= 2656
Step= 1206, Dmax= 9.6e-03 nm, Epot= -3.09785e+06 Fmax= 2.50395e+03, atom= 2656
Step= 1207, Dmax= 1.1e-02 nm, Epot= -3.09788e+06 Fmax= 1.25394e+04, atom= 2656
Step= 1208, Dmax= 1.4e-02 nm, Epot= -3.09801e+06 Fmax= 5.50648e+03, atom= 2656
Step= 1210, Dmax= 8.3e-03 nm, Epot= -3.09806e+06 Fmax= 5.31734e+03, atom= 2656
Step= 1211, Dmax= 9.9e-03 nm, Epot= -3.09810e+06 Fmax= 7.65083e+03, atom= 2656
Step= 1212, Dmax= 1.2e-02 nm, Epot= -3.09814e+06 Fmax= 7.95164e+03, atom= 2656
Step= 1213, Dmax= 1.4e-02 nm, Epot= -3.09816e+06 Fmax= 1.07059e+04, atom= 2656
Step= 1214, Dmax= 1.7e-02 nm, Epot= -3.09819e+06 Fmax= 1.17793e+04, atom= 2656
Step= 1216, Dmax= 1.0e-02 nm, Epot= -3.09832e+06 Fmax= 1.72875e+03, atom= 2656
Step= 1217, Dmax= 1.2e-02 nm, Epot= -3.09839e+06 Fmax= 1.44092e+04, atom= 2656
Step= 1218, Dmax= 1.5e-02 nm, Epot= -3.09856e+06 Fmax= 4.99199e+03, atom= 2656
Step= 1220, Dmax= 8.9e-03 nm, Epot= -3.09860e+06 Fmax= 6.66651e+03, atom= 2656
Step= 1221, Dmax= 1.1e-02 nm, Epot= -3.09864e+06 Fmax= 7.27272e+03, atom= 2656
Step= 1222, Dmax= 1.3e-02 nm, Epot= -3.09867e+06 Fmax= 9.51412e+03, atom= 2656
Step= 1223, Dmax= 1.5e-02 nm, Epot= -3.09870e+06 Fmax= 1.05485e+04, atom= 2656
Step= 1224, Dmax= 1.8e-02 nm, Epot= -3.09871e+06 Fmax= 1.36411e+04, atom= 2656
Step= 1225, Dmax= 2.2e-02 nm, Epot= -3.09872e+06 Fmax= 1.52224e+04, atom= 2656
Step= 1227, Dmax= 1.3e-02 nm, Epot= -3.09892e+06 Fmax= 2.06867e+03, atom= 2656
Step= 1229, Dmax= 8.0e-03 nm, Epot= -3.09898e+06 Fmax= 8.42636e+03, atom= 2656
Step= 1230, Dmax= 9.5e-03 nm, Epot= -3.09906e+06 Fmax= 4.08104e+03, atom= 2656
Step= 1231, Dmax= 1.1e-02 nm, Epot= -3.09907e+06 Fmax= 1.08693e+04, atom= 2656
Step= 1232, Dmax= 1.4e-02 nm, Epot= -3.09916e+06 Fmax= 7.14094e+03, atom= 2656
Step= 1234, Dmax= 8.2e-03 nm, Epot= -3.09922e+06 Fmax= 3.67732e+03, atom= 2656
Step= 1235, Dmax= 9.9e-03 nm, Epot= -3.09925e+06 Fmax= 9.30475e+03, atom= 2656
Step= 1236, Dmax= 1.2e-02 nm, Epot= -3.09933e+06 Fmax= 6.25084e+03, atom= 2656
Step= 1238, Dmax= 7.1e-03 nm, Epot= -3.09939e+06 Fmax= 3.07245e+03, atom= 2656
Step= 1239, Dmax= 8.5e-03 nm, Epot= -3.09943e+06 Fmax= 8.11719e+03, atom= 2656
Step= 1240, Dmax= 1.0e-02 nm, Epot= -3.09949e+06 Fmax= 5.32753e+03, atom= 2656
Step= 1241, Dmax= 1.2e-02 nm, Epot= -3.09950e+06 Fmax= 1.07572e+04, atom= 2656
Step= 1242, Dmax= 1.5e-02 nm, Epot= -3.09957e+06 Fmax= 8.61668e+03, atom= 2656
Step= 1244, Dmax= 8.9e-03 nm, Epot= -3.09965e+06 Fmax= 3.01966e+03, atom= 2656
Step= 1245, Dmax= 1.1e-02 nm, Epot= -3.09968e+06 Fmax= 1.09370e+04, atom= 2656
Step= 1246, Dmax= 1.3e-02 nm, Epot= -3.09978e+06 Fmax= 5.79131e+03, atom= 2656
Step= 1248, Dmax= 7.7e-03 nm, Epot= -3.09983e+06 Fmax= 4.23773e+03, atom= 2656
Step= 1249, Dmax= 9.2e-03 nm, Epot= -3.09986e+06 Fmax= 7.78780e+03, atom= 2656
Step= 1250, Dmax= 1.1e-02 nm, Epot= -3.09991e+06 Fmax= 6.67253e+03, atom= 2656
Step= 1251, Dmax= 1.3e-02 nm, Epot= -3.09992e+06 Fmax= 1.06240e+04, atom= 2656
Step= 1252, Dmax= 1.6e-02 nm, Epot= -3.09997e+06 Fmax= 1.02153e+04, atom= 2656
Step= 1254, Dmax= 9.5e-03 nm, Epot= -3.10008e+06 Fmax= 2.30227e+03, atom= 2656
Step= 1255, Dmax= 1.1e-02 nm, Epot= -3.10011e+06 Fmax= 1.26906e+04, atom= 2656
Step= 1256, Dmax= 1.4e-02 nm, Epot= -3.10024e+06 Fmax= 5.29799e+03, atom= 2656
Step= 1258, Dmax= 8.2e-03 nm, Epot= -3.10029e+06 Fmax= 5.49475e+03, atom= 2656
Step= 1259, Dmax= 9.9e-03 nm, Epot= -3.10033e+06 Fmax= 7.43137e+03, atom= 2656
Step= 1260, Dmax= 1.2e-02 nm, Epot= -3.10036e+06 Fmax= 8.12377e+03, atom= 2656
Step= 1261, Dmax= 1.4e-02 nm, Epot= -3.10038e+06 Fmax= 1.04755e+04, atom= 2656
Step= 1262, Dmax= 1.7e-02 nm, Epot= -3.10041e+06 Fmax= 1.19411e+04, atom= 2656
Step= 1264, Dmax= 1.0e-02 nm, Epot= -3.10054e+06 Fmax= 1.52527e+03, atom= 2656
Step= 1265, Dmax= 1.2e-02 nm, Epot= -3.10063e+06 Fmax= 1.45501e+04, atom= 2656
Step= 1266, Dmax= 1.5e-02 nm, Epot= -3.10080e+06 Fmax= 4.78726e+03, atom= 2656
Step= 1268, Dmax= 8.8e-03 nm, Epot= -3.10083e+06 Fmax= 6.84325e+03, atom= 2656
Step= 1269, Dmax= 1.1e-02 nm, Epot= -3.10087e+06 Fmax= 7.05095e+03, atom= 2656
Step= 1270, Dmax= 1.3e-02 nm, Epot= -3.10090e+06 Fmax= 9.68618e+03, atom= 2656
Step= 1271, Dmax= 1.5e-02 nm, Epot= -3.10093e+06 Fmax= 1.03139e+04, atom= 2656
Step= 1273, Dmax= 9.2e-03 nm, Epot= -3.10104e+06 Fmax= 1.67517e+03, atom= 2656
Step= 1274, Dmax= 1.1e-02 nm, Epot= -3.10112e+06 Fmax= 1.27557e+04, atom= 2656
Step= 1275, Dmax= 1.3e-02 nm, Epot= -3.10125e+06 Fmax= 4.55418e+03, atom= 2656
Step= 1277, Dmax= 7.9e-03 nm, Epot= -3.10129e+06 Fmax= 5.81766e+03, atom= 2656
Step= 1278, Dmax= 9.5e-03 nm, Epot= -3.10133e+06 Fmax= 6.66517e+03, atom= 2656
Step= 1279, Dmax= 1.1e-02 nm, Epot= -3.10136e+06 Fmax= 8.26667e+03, atom= 2656
Step= 1280, Dmax= 1.4e-02 nm, Epot= -3.10139e+06 Fmax= 9.71820e+03, atom= 2656
Step= 1281, Dmax= 1.6e-02 nm, Epot= -3.10141e+06 Fmax= 1.17695e+04, atom= 2656
Step= 1282, Dmax= 2.0e-02 nm, Epot= -3.10141e+06 Fmax= 1.41489e+04, atom= 2656
Step= 1284, Dmax= 1.2e-02 nm, Epot= -3.10158e+06 Fmax= 1.42331e+03, atom= 2656
Step= 1285, Dmax= 1.4e-02 nm, Epot= -3.10167e+06 Fmax= 1.71098e+04, atom= 2656
Step= 1286, Dmax= 1.7e-02 nm, Epot= -3.10188e+06 Fmax= 5.23298e+03, atom= 2656
Step= 1288, Dmax= 1.0e-02 nm, Epot= -3.10191e+06 Fmax= 8.23531e+03, atom= 2656
Step= 1289, Dmax= 1.2e-02 nm, Epot= -3.10196e+06 Fmax= 7.81622e+03, atom= 2656
Step= 1290, Dmax= 1.5e-02 nm, Epot= -3.10197e+06 Fmax= 1.15381e+04, atom= 2656
Step= 1291, Dmax= 1.8e-02 nm, Epot= -3.10201e+06 Fmax= 1.15704e+04, atom= 2656
Step= 1293, Dmax= 1.1e-02 nm, Epot= -3.10213e+06 Fmax= 2.28002e+03, atom= 2656
Step= 1294, Dmax= 1.3e-02 nm, Epot= -3.10214e+06 Fmax= 1.43823e+04, atom= 2656
Step= 1295, Dmax= 1.5e-02 nm, Epot= -3.10230e+06 Fmax= 5.61720e+03, atom= 2656
Step= 1297, Dmax= 9.2e-03 nm, Epot= -3.10234e+06 Fmax= 6.37471e+03, atom= 2656
Step= 1298, Dmax= 1.1e-02 nm, Epot= -3.10237e+06 Fmax= 8.05103e+03, atom= 2656
Step= 1299, Dmax= 1.3e-02 nm, Epot= -3.10240e+06 Fmax= 9.20451e+03, atom= 2656
Step= 1300, Dmax= 1.6e-02 nm, Epot= -3.10242e+06 Fmax= 1.15852e+04, atom= 2656
Step= 1301, Dmax= 1.9e-02 nm, Epot= -3.10244e+06 Fmax= 1.32416e+04, atom= 2656
Step= 1303, Dmax= 1.1e-02 nm, Epot= -3.10259e+06 Fmax= 1.63499e+03, atom= 2656
Step= 1304, Dmax= 1.4e-02 nm, Epot= -3.10263e+06 Fmax= 1.63340e+04, atom= 2656
Step= 1305, Dmax= 1.6e-02 nm, Epot= -3.10283e+06 Fmax= 5.17328e+03, atom= 2656
Step= 1307, Dmax= 9.8e-03 nm, Epot= -3.10286e+06 Fmax= 7.68756e+03, atom= 2656
Step= 1308, Dmax= 1.2e-02 nm, Epot= -3.10291e+06 Fmax= 7.82139e+03, atom= 2656
Step= 1309, Dmax= 1.4e-02 nm, Epot= -3.10292e+06 Fmax= 1.07119e+04, atom= 2656
Step= 1310, Dmax= 1.7e-02 nm, Epot= -3.10295e+06 Fmax= 1.16313e+04, atom= 2656
Step= 1312, Dmax= 1.0e-02 nm, Epot= -3.10307e+06 Fmax= 1.78896e+03, atom= 2656
Step= 1313, Dmax= 1.2e-02 nm, Epot= -3.10312e+06 Fmax= 1.42559e+04, atom= 2656
Step= 1314, Dmax= 1.5e-02 nm, Epot= -3.10328e+06 Fmax= 5.02153e+03, atom= 2656
Step= 1316, Dmax= 8.8e-03 nm, Epot= -3.10332e+06 Fmax= 6.56017e+03, atom= 2656
Step= 1317, Dmax= 1.1e-02 nm, Epot= -3.10336e+06 Fmax= 7.28977e+03, atom= 2656
Step= 1318, Dmax= 1.3e-02 nm, Epot= -3.10338e+06 Fmax= 9.38904e+03, atom= 2656
Step= 1319, Dmax= 1.5e-02 nm, Epot= -3.10341e+06 Fmax= 1.05444e+04, atom= 2656
Step= 1321, Dmax= 9.1e-03 nm, Epot= -3.10351e+06 Fmax= 1.40428e+03, atom= 2656
Step= 1322, Dmax= 1.1e-02 nm, Epot= -3.10361e+06 Fmax= 1.29959e+04, atom= 2656
Step= 1323, Dmax= 1.3e-02 nm, Epot= -3.10374e+06 Fmax= 4.26188e+03, atom= 2656
Step= 1325, Dmax= 7.9e-03 nm, Epot= -3.10379e+06 Fmax= 6.06767e+03, atom= 2656
Step= 1326, Dmax= 9.5e-03 nm, Epot= -3.10383e+06 Fmax= 6.37591e+03, atom= 2656
Step= 1327, Dmax= 1.1e-02 nm, Epot= -3.10385e+06 Fmax= 8.50393e+03, atom= 2656
Step= 1328, Dmax= 1.4e-02 nm, Epot= -3.10388e+06 Fmax= 9.42182e+03, atom= 2656
Step= 1329, Dmax= 1.6e-02 nm, Epot= -3.10389e+06 Fmax= 1.19931e+04, atom= 2656
Step= 1330, Dmax= 2.0e-02 nm, Epot= -3.10391e+06 Fmax= 1.38392e+04, atom= 2656
Step= 1332, Dmax= 1.2e-02 nm, Epot= -3.10407e+06 Fmax= 1.67987e+03, atom= 2656
Step= 1333, Dmax= 1.4e-02 nm, Epot= -3.10410e+06 Fmax= 1.68290e+04, atom= 2656
Step= 1334, Dmax= 1.7e-02 nm, Epot= -3.10431e+06 Fmax= 5.44678e+03, atom= 2656
Step= 1336, Dmax= 1.0e-02 nm, Epot= -3.10433e+06 Fmax= 7.95997e+03, atom= 2656
Step= 1337, Dmax= 1.2e-02 nm, Epot= -3.10437e+06 Fmax= 8.04086e+03, atom= 2656
Step= 1338, Dmax= 1.5e-02 nm, Epot= -3.10438e+06 Fmax= 1.12453e+04, atom= 2656
Step= 1339, Dmax= 1.8e-02 nm, Epot= -3.10441e+06 Fmax= 1.17859e+04, atom= 2656
Step= 1341, Dmax= 1.1e-02 nm, Epot= -3.10453e+06 Fmax= 2.01790e+03, atom= 2656
Step= 1342, Dmax= 1.3e-02 nm, Epot= -3.10456e+06 Fmax= 1.46022e+04, atom= 2656
Step= 1343, Dmax= 1.5e-02 nm, Epot= -3.10472e+06 Fmax= 5.33455e+03, atom= 2656
Step= 1345, Dmax= 9.1e-03 nm, Epot= -3.10476e+06 Fmax= 6.61242e+03, atom= 2656
Step= 1346, Dmax= 1.1e-02 nm, Epot= -3.10479e+06 Fmax= 7.76772e+03, atom= 2656
Step= 1347, Dmax= 1.3e-02 nm, Epot= -3.10481e+06 Fmax= 9.42871e+03, atom= 2656
Step= 1348, Dmax= 1.6e-02 nm, Epot= -3.10483e+06 Fmax= 1.12922e+04, atom= 2656
Step= 1349, Dmax= 1.9e-02 nm, Epot= -3.10484e+06 Fmax= 1.34509e+04, atom= 2656
Step= 1351, Dmax= 1.1e-02 nm, Epot= -3.10498e+06 Fmax= 1.37649e+03, atom= 2656
Step= 1352, Dmax= 1.4e-02 nm, Epot= -3.10506e+06 Fmax= 1.65618e+04, atom= 2656
Step= 1353, Dmax= 1.6e-02 nm, Epot= -3.10527e+06 Fmax= 4.88531e+03, atom= 2656
Step= 1355, Dmax= 9.8e-03 nm, Epot= -3.10530e+06 Fmax= 7.91708e+03, atom= 2656
Step= 1356, Dmax= 1.2e-02 nm, Epot= -3.10534e+06 Fmax= 7.54386e+03, atom= 2656
Step= 1357, Dmax= 1.4e-02 nm, Epot= -3.10535e+06 Fmax= 1.09247e+04, atom= 2656
Step= 1358, Dmax= 1.7e-02 nm, Epot= -3.10539e+06 Fmax= 1.13456e+04, atom= 2656
Step= 1360, Dmax= 1.0e-02 nm, Epot= -3.10549e+06 Fmax= 2.02891e+03, atom= 2656
Step= 1361, Dmax= 1.2e-02 nm, Epot= -3.10552e+06 Fmax= 1.39802e+04, atom= 2656
Step= 1362, Dmax= 1.5e-02 nm, Epot= -3.10567e+06 Fmax= 5.23524e+03, atom= 2656
Step= 1364, Dmax= 8.8e-03 nm, Epot= -3.10570e+06 Fmax= 6.30292e+03, atom= 2656
Step= 1365, Dmax= 1.1e-02 nm, Epot= -3.10574e+06 Fmax= 7.50220e+03, atom= 2656
Step= 1366, Dmax= 1.3e-02 nm, Epot= -3.10576e+06 Fmax= 9.12048e+03, atom= 2656
Step= 1367, Dmax= 1.5e-02 nm, Epot= -3.10579e+06 Fmax= 1.07466e+04, atom= 2656
Step= 1368, Dmax= 1.8e-02 nm, Epot= -3.10579e+06 Fmax= 1.32079e+04, atom= 2656
Step= 1369, Dmax= 2.2e-02 nm, Epot= -3.10579e+06 Fmax= 1.53742e+04, atom= 2656
Step= 1371, Dmax= 1.3e-02 nm, Epot= -3.10598e+06 Fmax= 1.75004e+03, atom= 2656
Step= 1373, Dmax= 7.9e-03 nm, Epot= -3.10605e+06 Fmax= 8.65795e+03, atom= 2656
Step= 1374, Dmax= 9.5e-03 nm, Epot= -3.10612e+06 Fmax= 3.73485e+03, atom= 2656
Step= 1375, Dmax= 1.1e-02 nm, Epot= -3.10612e+06 Fmax= 1.10570e+04, atom= 2656
Step= 1376, Dmax= 1.4e-02 nm, Epot= -3.10621e+06 Fmax= 6.77921e+03, atom= 2656
Step= 1378, Dmax= 8.2e-03 nm, Epot= -3.10627e+06 Fmax= 3.93314e+03, atom= 2656
Step= 1379, Dmax= 9.8e-03 nm, Epot= -3.10628e+06 Fmax= 8.92729e+03, atom= 2656
Step= 1380, Dmax= 1.2e-02 nm, Epot= -3.10635e+06 Fmax= 6.47631e+03, atom= 2656
Step= 1382, Dmax= 7.1e-03 nm, Epot= -3.10640e+06 Fmax= 2.75746e+03, atom= 2656
Step= 1383, Dmax= 8.5e-03 nm, Epot= -3.10644e+06 Fmax= 8.32355e+03, atom= 2656
Step= 1384, Dmax= 1.0e-02 nm, Epot= -3.10650e+06 Fmax= 4.99236e+03, atom= 2656
Step= 1386, Dmax= 6.1e-03 nm, Epot= -3.10654e+06 Fmax= 3.00117e+03, atom= 2656
Step= 1387, Dmax= 7.3e-03 nm, Epot= -3.10658e+06 Fmax= 6.59760e+03, atom= 2656
Step= 1388, Dmax= 8.8e-03 nm, Epot= -3.10663e+06 Fmax= 4.90119e+03, atom= 2656
Step= 1389, Dmax= 1.1e-02 nm, Epot= -3.10664e+06 Fmax= 8.93706e+03, atom= 2656
Step= 1390, Dmax= 1.3e-02 nm, Epot= -3.10670e+06 Fmax= 7.61188e+03, atom= 2656
Step= 1392, Dmax= 7.6e-03 nm, Epot= -3.10676e+06 Fmax= 2.31094e+03, atom= 2656
Step= 1393, Dmax= 9.1e-03 nm, Epot= -3.10680e+06 Fmax= 9.59833e+03, atom= 2656
Step= 1394, Dmax= 1.1e-02 nm, Epot= -3.10688e+06 Fmax= 4.71376e+03, atom= 2656
Step= 1396, Dmax= 6.6e-03 nm, Epot= -3.10692e+06 Fmax= 3.87374e+03, atom= 2656
Step= 1397, Dmax= 7.9e-03 nm, Epot= -3.10696e+06 Fmax= 6.44631e+03, atom= 2656
Step= 1398, Dmax= 9.4e-03 nm, Epot= -3.10700e+06 Fmax= 5.90844e+03, atom= 2656
Step= 1399, Dmax= 1.1e-02 nm, Epot= -3.10702e+06 Fmax= 8.96493e+03, atom= 2656
Step= 1400, Dmax= 1.4e-02 nm, Epot= -3.10706e+06 Fmax= 8.81578e+03, atom= 2656
Step= 1402, Dmax= 8.2e-03 nm, Epot= -3.10713e+06 Fmax= 1.84520e+03, atom= 2656
Step= 1403, Dmax= 9.8e-03 nm, Epot= -3.10719e+06 Fmax= 1.09627e+04, atom= 2656
Step= 1404, Dmax= 1.2e-02 nm, Epot= -3.10729e+06 Fmax= 4.42142e+03, atom= 2656
Step= 1406, Dmax= 7.0e-03 nm, Epot= -3.10733e+06 Fmax= 4.80179e+03, atom= 2656
Step= 1407, Dmax= 8.5e-03 nm, Epot= -3.10736e+06 Fmax= 6.29295e+03, atom= 2656
Step= 1408, Dmax= 1.0e-02 nm, Epot= -3.10740e+06 Fmax= 6.98137e+03, atom= 2656
Step= 1409, Dmax= 1.2e-02 nm, Epot= -3.10742e+06 Fmax= 9.00409e+03, atom= 2656
Step= 1410, Dmax= 1.5e-02 nm, Epot= -3.10745e+06 Fmax= 1.00995e+04, atom= 2656
Step= 1411, Dmax= 1.8e-02 nm, Epot= -3.10745e+06 Fmax= 1.29350e+04, atom= 2656
Step= 1412, Dmax= 2.1e-02 nm, Epot= -3.10746e+06 Fmax= 1.45506e+04, atom= 2656
Step= 1414, Dmax= 1.3e-02 nm, Epot= -3.10763e+06 Fmax= 1.91984e+03, atom= 2656
Step= 1416, Dmax= 7.6e-03 nm, Epot= -3.10768e+06 Fmax= 8.06670e+03, atom= 2656
Step= 1417, Dmax= 9.1e-03 nm, Epot= -3.10775e+06 Fmax= 3.84612e+03, atom= 2656
Step= 1418, Dmax= 1.1e-02 nm, Epot= -3.10775e+06 Fmax= 1.03866e+04, atom= 2656
Step= 1419, Dmax= 1.3e-02 nm, Epot= -3.10783e+06 Fmax= 6.76630e+03, atom= 2656
Step= 1421, Dmax= 7.8e-03 nm, Epot= -3.10788e+06 Fmax= 3.53248e+03, atom= 2656
Step= 1422, Dmax= 9.4e-03 nm, Epot= -3.10790e+06 Fmax= 8.83374e+03, atom= 2656
Step= 1423, Dmax= 1.1e-02 nm, Epot= -3.10796e+06 Fmax= 5.97658e+03, atom= 2656
Step= 1425, Dmax= 6.8e-03 nm, Epot= -3.10801e+06 Fmax= 2.90388e+03, atom= 2656
Step= 1426, Dmax= 8.1e-03 nm, Epot= -3.10805e+06 Fmax= 7.74722e+03, atom= 2656
Step= 1427, Dmax= 9.8e-03 nm, Epot= -3.10810e+06 Fmax= 5.05762e+03, atom= 2656
Step= 1428, Dmax= 1.2e-02 nm, Epot= -3.10811e+06 Fmax= 1.02573e+04, atom= 2656
Step= 1429, Dmax= 1.4e-02 nm, Epot= -3.10817e+06 Fmax= 8.19292e+03, atom= 2656
Step= 1431, Dmax= 8.4e-03 nm, Epot= -3.10824e+06 Fmax= 2.88502e+03, atom= 2656
Step= 1432, Dmax= 1.0e-02 nm, Epot= -3.10826e+06 Fmax= 1.04103e+04, atom= 2656
Step= 1433, Dmax= 1.2e-02 nm, Epot= -3.10834e+06 Fmax= 5.51735e+03, atom= 2656
Step= 1435, Dmax= 7.3e-03 nm, Epot= -3.10838e+06 Fmax= 4.03523e+03, atom= 2656
Step= 1436, Dmax= 8.7e-03 nm, Epot= -3.10841e+06 Fmax= 7.41336e+03, atom= 2656
Step= 1437, Dmax= 1.0e-02 nm, Epot= -3.10846e+06 Fmax= 6.35866e+03, atom= 2656
Step= 1438, Dmax= 1.3e-02 nm, Epot= -3.10846e+06 Fmax= 1.01110e+04, atom= 2656
Step= 1439, Dmax= 1.5e-02 nm, Epot= -3.10851e+06 Fmax= 9.73470e+03, atom= 2656
Step= 1441, Dmax= 9.1e-03 nm, Epot= -3.10859e+06 Fmax= 2.18214e+03, atom= 2656
Step= 1442, Dmax= 1.1e-02 nm, Epot= -3.10862e+06 Fmax= 1.21020e+04, atom= 2656
Step= 1443, Dmax= 1.3e-02 nm, Epot= -3.10873e+06 Fmax= 5.02544e+03, atom= 2656
Step= 1445, Dmax= 7.8e-03 nm, Epot= -3.10877e+06 Fmax= 5.25472e+03, atom= 2656
Step= 1446, Dmax= 9.4e-03 nm, Epot= -3.10880e+06 Fmax= 7.05265e+03, atom= 2656
Step= 1447, Dmax= 1.1e-02 nm, Epot= -3.10883e+06 Fmax= 7.76155e+03, atom= 2656
Step= 1448, Dmax= 1.4e-02 nm, Epot= -3.10885e+06 Fmax= 9.94936e+03, atom= 2656
Step= 1449, Dmax= 1.6e-02 nm, Epot= -3.10887e+06 Fmax= 1.13982e+04, atom= 2656
Step= 1451, Dmax= 9.8e-03 nm, Epot= -3.10898e+06 Fmax= 1.42193e+03, atom= 2656
Step= 1452, Dmax= 1.2e-02 nm, Epot= -3.10905e+06 Fmax= 1.38977e+04, atom= 2656
Step= 1453, Dmax= 1.4e-02 nm, Epot= -3.10920e+06 Fmax= 4.51368e+03, atom= 2656
Step= 1455, Dmax= 8.4e-03 nm, Epot= -3.10923e+06 Fmax= 6.56429e+03, atom= 2656
Step= 1456, Dmax= 1.0e-02 nm, Epot= -3.10926e+06 Fmax= 6.66510e+03, atom= 2656
Step= 1457, Dmax= 1.2e-02 nm, Epot= -3.10928e+06 Fmax= 9.27447e+03, atom= 2656
Step= 1458, Dmax= 1.5e-02 nm, Epot= -3.10931e+06 Fmax= 9.77021e+03, atom= 2656
Step= 1460, Dmax= 8.7e-03 nm, Epot= -3.10940e+06 Fmax= 1.64970e+03, atom= 2656
Step= 1461, Dmax= 1.0e-02 nm, Epot= -3.10946e+06 Fmax= 1.20798e+04, atom= 2656
Step= 1462, Dmax= 1.3e-02 nm, Epot= -3.10956e+06 Fmax= 4.40524e+03, atom= 2656
Step= 1464, Dmax= 7.5e-03 nm, Epot= -3.10960e+06 Fmax= 5.47036e+03, atom= 2656
Step= 1465, Dmax= 9.1e-03 nm, Epot= -3.10964e+06 Fmax= 6.41865e+03, atom= 2656
Step= 1466, Dmax= 1.1e-02 nm, Epot= -3.10967e+06 Fmax= 7.79962e+03, atom= 2656
Step= 1467, Dmax= 1.3e-02 nm, Epot= -3.10969e+06 Fmax= 9.32830e+03, atom= 2656
Step= 1468, Dmax= 1.6e-02 nm, Epot= -3.10970e+06 Fmax= 1.11343e+04, atom= 2656
Step= 1469, Dmax= 1.9e-02 nm, Epot= -3.10971e+06 Fmax= 1.35472e+04, atom= 2656
Step= 1471, Dmax= 1.1e-02 nm, Epot= -3.10985e+06 Fmax= 1.27801e+03, atom= 2656
Step= 1472, Dmax= 1.4e-02 nm, Epot= -3.10993e+06 Fmax= 1.63788e+04, atom= 2656
Step= 1473, Dmax= 1.6e-02 nm, Epot= -3.11012e+06 Fmax= 4.89297e+03, atom= 2656
Step= 1475, Dmax= 9.7e-03 nm, Epot= -3.11014e+06 Fmax= 7.93881e+03, atom= 2656
Step= 1476, Dmax= 1.2e-02 nm, Epot= -3.11018e+06 Fmax= 7.34529e+03, atom= 2656
Step= 1477, Dmax= 1.4e-02 nm, Epot= -3.11018e+06 Fmax= 1.10874e+04, atom= 2656
Step= 1478, Dmax= 1.7e-02 nm, Epot= -3.11022e+06 Fmax= 1.09185e+04, atom= 2656
Step= 1480, Dmax= 1.0e-02 nm, Epot= -3.11032e+06 Fmax= 2.27535e+03, atom= 2656
Step= 1481, Dmax= 1.2e-02 nm, Epot= -3.11033e+06 Fmax= 1.35797e+04, atom= 2656
Step= 1482, Dmax= 1.5e-02 nm, Epot= -3.11046e+06 Fmax= 5.46698e+03, atom= 2656
Step= 1484, Dmax= 8.7e-03 nm, Epot= -3.11049e+06 Fmax= 5.95264e+03, atom= 2656
Step= 1485, Dmax= 1.0e-02 nm, Epot= -3.11052e+06 Fmax= 7.78662e+03, atom= 2656
Step= 1486, Dmax= 1.3e-02 nm, Epot= -3.11055e+06 Fmax= 8.64537e+03, atom= 2656
Step= 1487, Dmax= 1.5e-02 nm, Epot= -3.11056e+06 Fmax= 1.11537e+04, atom= 2656
Step= 1488, Dmax= 1.8e-02 nm, Epot= -3.11058e+06 Fmax= 1.24897e+04, atom= 2656
Step= 1490, Dmax= 1.1e-02 nm, Epot= -3.11070e+06 Fmax= 1.68168e+03, atom= 2656
Step= 1491, Dmax= 1.3e-02 nm, Epot= -3.11073e+06 Fmax= 1.54040e+04, atom= 2656
Step= 1492, Dmax= 1.6e-02 nm, Epot= -3.11089e+06 Fmax= 5.07535e+03, atom= 2656
Step= 1494, Dmax= 9.4e-03 nm, Epot= -3.11092e+06 Fmax= 7.17633e+03, atom= 2656
Step= 1495, Dmax= 1.1e-02 nm, Epot= -3.11095e+06 Fmax= 7.59330e+03, atom= 2656
Step= 1496, Dmax= 1.3e-02 nm, Epot= -3.11096e+06 Fmax= 1.00570e+04, atom= 2656
Step= 1497, Dmax= 1.6e-02 nm, Epot= -3.11099e+06 Fmax= 1.12208e+04, atom= 2656
Step= 1499, Dmax= 9.7e-03 nm, Epot= -3.11109e+06 Fmax= 1.55691e+03, atom= 2656
Step= 1500, Dmax= 1.2e-02 nm, Epot= -3.11115e+06 Fmax= 1.37244e+04, atom= 2656
Step= 1501, Dmax= 1.4e-02 nm, Epot= -3.11128e+06 Fmax= 4.62889e+03, atom= 2656
Step= 1503, Dmax= 8.4e-03 nm, Epot= -3.11131e+06 Fmax= 6.40733e+03, atom= 2656
Step= 1504, Dmax= 1.0e-02 nm, Epot= -3.11135e+06 Fmax= 6.77967e+03, atom= 2656
Step= 1505, Dmax= 1.2e-02 nm, Epot= -3.11136e+06 Fmax= 9.10663e+03, atom= 2656
Step= 1506, Dmax= 1.5e-02 nm, Epot= -3.11139e+06 Fmax= 9.87597e+03, atom= 2656
Step= 1508, Dmax= 8.7e-03 nm, Epot= -3.11148e+06 Fmax= 1.50653e+03, atom= 2656
Step= 1509, Dmax= 1.0e-02 nm, Epot= -3.11154e+06 Fmax= 1.21840e+04, atom= 2656
Step= 1510, Dmax= 1.3e-02 nm, Epot= -3.11166e+06 Fmax= 4.24948e+03, atom= 2656
Step= 1512, Dmax= 7.5e-03 nm, Epot= -3.11169e+06 Fmax= 5.59082e+03, atom= 2656
Step= 1513, Dmax= 9.0e-03 nm, Epot= -3.11172e+06 Fmax= 6.26033e+03, atom= 2656
Step= 1514, Dmax= 1.1e-02 nm, Epot= -3.11175e+06 Fmax= 7.91025e+03, atom= 2656
Step= 1515, Dmax= 1.3e-02 nm, Epot= -3.11177e+06 Fmax= 9.16200e+03, atom= 2656
Step= 1516, Dmax= 1.6e-02 nm, Epot= -3.11179e+06 Fmax= 1.12327e+04, atom= 2656
Step= 1517, Dmax= 1.9e-02 nm, Epot= -3.11179e+06 Fmax= 1.33680e+04, atom= 2656
Step= 1519, Dmax= 1.1e-02 nm, Epot= -3.11193e+06 Fmax= 1.40785e+03, atom= 2656
Step= 1520, Dmax= 1.3e-02 nm, Epot= -3.11198e+06 Fmax= 1.62131e+04, atom= 2656
Step= 1521, Dmax= 1.6e-02 nm, Epot= -3.11216e+06 Fmax= 4.99380e+03, atom= 2656
Step= 1523, Dmax= 9.7e-03 nm, Epot= -3.11217e+06 Fmax= 7.78646e+03, atom= 2656
Step= 1524, Dmax= 1.2e-02 nm, Epot= -3.11221e+06 Fmax= 7.44871e+03, atom= 2656
Step= 1525, Dmax= 1.4e-02 nm, Epot= -3.11222e+06 Fmax= 1.09218e+04, atom= 2656
Step= 1526, Dmax= 1.7e-02 nm, Epot= -3.11225e+06 Fmax= 1.10118e+04, atom= 2656
Step= 1528, Dmax= 1.0e-02 nm, Epot= -3.11235e+06 Fmax= 2.13881e+03, atom= 2656
Step= 1529, Dmax= 1.2e-02 nm, Epot= -3.11236e+06 Fmax= 1.36687e+04, atom= 2656
Step= 1530, Dmax= 1.4e-02 nm, Epot= -3.11249e+06 Fmax= 5.31738e+03, atom= 2656
Step= 1532, Dmax= 8.7e-03 nm, Epot= -3.11252e+06 Fmax= 6.06259e+03, atom= 2656
Step= 1533, Dmax= 1.0e-02 nm, Epot= -3.11255e+06 Fmax= 7.63302e+03, atom= 2656
Step= 1534, Dmax= 1.3e-02 nm, Epot= -3.11257e+06 Fmax= 8.74418e+03, atom= 2656
Step= 1535, Dmax= 1.5e-02 nm, Epot= -3.11258e+06 Fmax= 1.09905e+04, atom= 2656
Step= 1536, Dmax= 1.8e-02 nm, Epot= -3.11260e+06 Fmax= 1.25752e+04, atom= 2656
Step= 1538, Dmax= 1.1e-02 nm, Epot= -3.11272e+06 Fmax= 1.54996e+03, atom= 2656
Step= 1539, Dmax= 1.3e-02 nm, Epot= -3.11275e+06 Fmax= 1.54881e+04, atom= 2656
Step= 1540, Dmax= 1.6e-02 nm, Epot= -3.11292e+06 Fmax= 4.92866e+03, atom= 2656
Step= 1542, Dmax= 9.3e-03 nm, Epot= -3.11294e+06 Fmax= 7.27710e+03, atom= 2656
Step= 1543, Dmax= 1.1e-02 nm, Epot= -3.11298e+06 Fmax= 7.44627e+03, atom= 2656
Step= 1544, Dmax= 1.3e-02 nm, Epot= -3.11298e+06 Fmax= 1.01450e+04, atom= 2656
Step= 1545, Dmax= 1.6e-02 nm, Epot= -3.11301e+06 Fmax= 1.10641e+04, atom= 2656
Step= 1547, Dmax= 9.7e-03 nm, Epot= -3.11311e+06 Fmax= 1.67072e+03, atom= 2656
Step= 1548, Dmax= 1.2e-02 nm, Epot= -3.11315e+06 Fmax= 1.35711e+04, atom= 2656
Step= 1549, Dmax= 1.4e-02 nm, Epot= -3.11328e+06 Fmax= 4.72413e+03, atom= 2656
Step= 1551, Dmax= 8.4e-03 nm, Epot= -3.11331e+06 Fmax= 6.27286e+03, atom= 2656
Step= 1552, Dmax= 1.0e-02 nm, Epot= -3.11334e+06 Fmax= 6.87157e+03, atom= 2656
Step= 1553, Dmax= 1.2e-02 nm, Epot= -3.11336e+06 Fmax= 8.96248e+03, atom= 2656
Step= 1554, Dmax= 1.4e-02 nm, Epot= -3.11338e+06 Fmax= 9.95778e+03, atom= 2656
Step= 1556, Dmax= 8.7e-03 nm, Epot= -3.11347e+06 Fmax= 1.38788e+03, atom= 2656
Step= 1557, Dmax= 1.0e-02 nm, Epot= -3.11354e+06 Fmax= 1.22618e+04, atom= 2656
Step= 1558, Dmax= 1.2e-02 nm, Epot= -3.11365e+06 Fmax= 4.12037e+03, atom= 2656
Step= 1560, Dmax= 7.5e-03 nm, Epot= -3.11368e+06 Fmax= 5.68416e+03, atom= 2656
Step= 1561, Dmax= 9.0e-03 nm, Epot= -3.11371e+06 Fmax= 6.12954e+03, atom= 2656
Step= 1562, Dmax= 1.1e-02 nm, Epot= -3.11374e+06 Fmax= 7.99362e+03, atom= 2656
Step= 1563, Dmax= 1.3e-02 nm, Epot= -3.11376e+06 Fmax= 9.02358e+03, atom= 2656
Step= 1564, Dmax= 1.6e-02 nm, Epot= -3.11377e+06 Fmax= 1.13042e+04, atom= 2656
Step= 1565, Dmax= 1.9e-02 nm, Epot= -3.11378e+06 Fmax= 1.32170e+04, atom= 2656
Step= 1567, Dmax= 1.1e-02 nm, Epot= -3.11391e+06 Fmax= 1.50989e+03, atom= 2656
Step= 1568, Dmax= 1.3e-02 nm, Epot= -3.11394e+06 Fmax= 1.60701e+04, atom= 2656
Step= 1569, Dmax= 1.6e-02 nm, Epot= -3.11412e+06 Fmax= 5.07012e+03, atom= 2656
Step= 1571, Dmax= 9.7e-03 nm, Epot= -3.11414e+06 Fmax= 7.66232e+03, atom= 2656
Step= 1572, Dmax= 1.2e-02 nm, Epot= -3.11417e+06 Fmax= 7.52407e+03, atom= 2656
Step= 1573, Dmax= 1.4e-02 nm, Epot= -3.11417e+06 Fmax= 1.07861e+04, atom= 2656
Step= 1574, Dmax= 1.7e-02 nm, Epot= -3.11420e+06 Fmax= 1.10759e+04, atom= 2656
Step= 1576, Dmax= 1.0e-02 nm, Epot= -3.11430e+06 Fmax= 2.03168e+03, atom= 2656
Step= 1577, Dmax= 1.2e-02 nm, Epot= -3.11431e+06 Fmax= 1.37273e+04, atom= 2656
Step= 1578, Dmax= 1.4e-02 nm, Epot= -3.11444e+06 Fmax= 5.19848e+03, atom= 2656
Step= 1580, Dmax= 8.7e-03 nm, Epot= -3.11447e+06 Fmax= 6.14228e+03, atom= 2656
Step= 1581, Dmax= 1.0e-02 nm, Epot= -3.11450e+06 Fmax= 7.50991e+03, atom= 2656
Step= 1582, Dmax= 1.2e-02 nm, Epot= -3.11452e+06 Fmax= 8.81317e+03, atom= 2656
Step= 1583, Dmax= 1.5e-02 nm, Epot= -3.11453e+06 Fmax= 1.08578e+04, atom= 2656
Step= 1584, Dmax= 1.8e-02 nm, Epot= -3.11453e+06 Fmax= 1.26302e+04, atom= 2656
Step= 1586, Dmax= 1.1e-02 nm, Epot= -3.11466e+06 Fmax= 1.44934e+03, atom= 2656
Step= 1587, Dmax= 1.3e-02 nm, Epot= -3.11470e+06 Fmax= 1.55394e+04, atom= 2656
Step= 1588, Dmax= 1.6e-02 nm, Epot= -3.11487e+06 Fmax= 4.81457e+03, atom= 2656
Step= 1590, Dmax= 9.3e-03 nm, Epot= -3.11489e+06 Fmax= 7.34640e+03, atom= 2656
Step= 1591, Dmax= 1.1e-02 nm, Epot= -3.11493e+06 Fmax= 7.33039e+03, atom= 2656
Step= 1592, Dmax= 1.3e-02 nm, Epot= -3.11493e+06 Fmax= 1.02021e+04, atom= 2656
Step= 1593, Dmax= 1.6e-02 nm, Epot= -3.11495e+06 Fmax= 1.09391e+04, atom= 2656
Step= 1595, Dmax= 9.7e-03 nm, Epot= -3.11505e+06 Fmax= 1.75363e+03, atom= 2656
Step= 1596, Dmax= 1.2e-02 nm, Epot= -3.11508e+06 Fmax= 1.34469e+04, atom= 2656
Step= 1597, Dmax= 1.4e-02 nm, Epot= -3.11520e+06 Fmax= 4.78962e+03, atom= 2656
Step= 1599, Dmax= 8.3e-03 nm, Epot= -3.11523e+06 Fmax= 6.17000e+03, atom= 2656
Step= 1600, Dmax= 1.0e-02 nm, Epot= -3.11526e+06 Fmax= 6.93182e+03, atom= 2656
Step= 1601, Dmax= 1.2e-02 nm, Epot= -3.11528e+06 Fmax= 8.85072e+03, atom= 2656
Step= 1602, Dmax= 1.4e-02 nm, Epot= -3.11530e+06 Fmax= 1.00078e+04, atom= 2656
Step= 1604, Dmax= 8.6e-03 nm, Epot= -3.11538e+06 Fmax= 1.30101e+03, atom= 2656
Step= 1605, Dmax= 1.0e-02 nm, Epot= -3.11546e+06 Fmax= 1.23068e+04, atom= 2656
Step= 1606, Dmax= 1.2e-02 nm, Epot= -3.11557e+06 Fmax= 4.02476e+03, atom= 2656
Step= 1608, Dmax= 7.5e-03 nm, Epot= -3.11560e+06 Fmax= 5.74447e+03, atom= 2656
Step= 1609, Dmax= 9.0e-03 nm, Epot= -3.11563e+06 Fmax= 6.03229e+03, atom= 2656
Step= 1610, Dmax= 1.1e-02 nm, Epot= -3.11565e+06 Fmax= 8.04390e+03, atom= 2656
Step= 1611, Dmax= 1.3e-02 nm, Epot= -3.11568e+06 Fmax= 8.91919e+03, atom= 2656
Step= 1612, Dmax= 1.5e-02 nm, Epot= -3.11568e+06 Fmax= 1.13418e+04, atom= 2656
Step= 1613, Dmax= 1.9e-02 nm, Epot= -3.11569e+06 Fmax= 1.31004e+04, atom= 2656
Step= 1615, Dmax= 1.1e-02 nm, Epot= -3.11582e+06 Fmax= 1.57839e+03, atom= 2656
Step= 1616, Dmax= 1.3e-02 nm, Epot= -3.11583e+06 Fmax= 1.59547e+04, atom= 2656
Step= 1617, Dmax= 1.6e-02 nm, Epot= -3.11600e+06 Fmax= 5.11859e+03, atom= 2656
Step= 1619, Dmax= 9.6e-03 nm, Epot= -3.11602e+06 Fmax= 7.56879e+03, atom= 2656
Step= 1620, Dmax= 1.2e-02 nm, Epot= -3.11605e+06 Fmax= 7.56818e+03, atom= 2656
Step= 1622, Dmax= 6.9e-03 nm, Epot= -3.11611e+06 Fmax= 1.51755e+03, atom= 2656
Step= 1623, Dmax= 8.3e-03 nm, Epot= -3.11617e+06 Fmax= 9.37598e+03, atom= 2656
Step= 1624, Dmax= 1.0e-02 nm, Epot= -3.11624e+06 Fmax= 3.72704e+03, atom= 2656
Step= 1626, Dmax= 6.0e-03 nm, Epot= -3.11628e+06 Fmax= 4.12614e+03, atom= 2656
Step= 1627, Dmax= 7.2e-03 nm, Epot= -3.11631e+06 Fmax= 5.32359e+03, atom= 2656
Step= 1628, Dmax= 8.6e-03 nm, Epot= -3.11634e+06 Fmax= 5.97985e+03, atom= 2656
Step= 1629, Dmax= 1.0e-02 nm, Epot= -3.11636e+06 Fmax= 7.63345e+03, atom= 2656
Step= 1630, Dmax= 1.2e-02 nm, Epot= -3.11638e+06 Fmax= 8.63713e+03, atom= 2656
Step= 1631, Dmax= 1.5e-02 nm, Epot= -3.11639e+06 Fmax= 1.09755e+04, atom= 2656
Step= 1632, Dmax= 1.8e-02 nm, Epot= -3.11640e+06 Fmax= 1.24389e+04, atom= 2656
Step= 1634, Dmax= 1.1e-02 nm, Epot= -3.11652e+06 Fmax= 1.59877e+03, atom= 2656
Step= 1635, Dmax= 1.3e-02 nm, Epot= -3.11654e+06 Fmax= 1.53141e+04, atom= 2656
Step= 1636, Dmax= 1.5e-02 nm, Epot= -3.11670e+06 Fmax= 4.97257e+03, atom= 2656
Step= 1638, Dmax= 9.3e-03 nm, Epot= -3.11672e+06 Fmax= 7.15713e+03, atom= 2656
Step= 1639, Dmax= 1.1e-02 nm, Epot= -3.11674e+06 Fmax= 7.47376e+03, atom= 2656
Step= 1640, Dmax= 1.3e-02 nm, Epot= -3.11676e+06 Fmax= 1.00044e+04, atom= 2656
Step= 1641, Dmax= 1.6e-02 nm, Epot= -3.11678e+06 Fmax= 1.10716e+04, atom= 2656
Step= 1643, Dmax= 9.6e-03 nm, Epot= -3.11687e+06 Fmax= 1.58160e+03, atom= 2656
Step= 1644, Dmax= 1.2e-02 nm, Epot= -3.11691e+06 Fmax= 1.35666e+04, atom= 2656
Step= 1645, Dmax= 1.4e-02 nm, Epot= -3.11704e+06 Fmax= 4.61052e+03, atom= 2656
Step= 1647, Dmax= 8.3e-03 nm, Epot= -3.11707e+06 Fmax= 6.32073e+03, atom= 2656
Step= 1648, Dmax= 1.0e-02 nm, Epot= -3.11709e+06 Fmax= 6.73848e+03, atom= 2656
Step= 1649, Dmax= 1.2e-02 nm, Epot= -3.11711e+06 Fmax= 8.99737e+03, atom= 2656
Step= 1650, Dmax= 1.4e-02 nm, Epot= -3.11713e+06 Fmax= 9.80165e+03, atom= 2656
Step= 1652, Dmax= 8.6e-03 nm, Epot= -3.11720e+06 Fmax= 1.47346e+03, atom= 2656
Step= 1653, Dmax= 1.0e-02 nm, Epot= -3.11726e+06 Fmax= 1.20780e+04, atom= 2656
Step= 1654, Dmax= 1.2e-02 nm, Epot= -3.11736e+06 Fmax= 4.19933e+03, atom= 2656
Step= 1656, Dmax= 7.4e-03 nm, Epot= -3.11739e+06 Fmax= 5.54442e+03, atom= 2656
Step= 1657, Dmax= 8.9e-03 nm, Epot= -3.11742e+06 Fmax= 6.19492e+03, atom= 2656
Step= 1658, Dmax= 1.1e-02 nm, Epot= -3.11744e+06 Fmax= 7.83810e+03, atom= 2656
Step= 1659, Dmax= 1.3e-02 nm, Epot= -3.11746e+06 Fmax= 9.07219e+03, atom= 2656
Step= 1660, Dmax= 1.5e-02 nm, Epot= -3.11747e+06 Fmax= 1.11261e+04, atom= 2656
Step= 1662, Dmax= 9.3e-03 nm, Epot= -3.11757e+06 Fmax= 9.86983e+02, atom= 2656

writing lowest energy coordinates.

Steepest Descents converged to Fmax < 1000 in 1663 steps
Potential Energy  = -3.1175688e+06
Maximum force     =  9.8698315e+02 on atom 2656
Norm of force     =  1.1028193e+01

GROMACS reminds you: "The easiest way to scale well is to have bad single-core performance" (Blind Freddie)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx grompp -f step4.1_equilibration.mdp -c em.gro -r em.gro -p topol.top -n index.ndx -o nvt.tpr
                :-) GROMACS - gmx grompp, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx grompp -f step4.1_equilibration.mdp -c em.gro -r em.gro -p topol.top -n index.ndx -o nvt.tpr

Replacing old mdp entry 'nstxtcout' by 'nstxout-compressed'

NOTE 1 [file step4.1_equilibration.mdp]:
  leapfrog does not yet support Nose-Hoover chains, nhchainlength reset to
  1

Setting the LD random seed to -4507649

Generated 700 of the 703 non-bonded parameter combinations
Generating 1-4 interactions: fudge = 1

Generated 378 of the 703 1-4 parameter combinations

Excluding 3 bonded neighbours molecule type 'PROA'

turning H bonds into constraints...

Excluding 3 bonded neighbours molecule type 'PROB'

turning H bonds into constraints...

Excluding 1 bonded neighbours molecule type 'POT'

turning H bonds into constraints...

Excluding 1 bonded neighbours molecule type 'CLA'

turning H bonds into constraints...

Excluding 2 bonded neighbours molecule type 'TIP3'

turning H bonds into constraints...

Setting gen_seed to -572645673

Velocities were taken from a Maxwell distribution at 303.15 K
Number of degrees of freedom in T-Coupling group SOLU is 7043.00
Number of degrees of freedom in T-Coupling group SOLV is 362841.00

The largest distance between excluded atoms is 0.400 nm between atom 1472 and 1480

Determining Verlet buffer for a tolerance of 0.005 kJ/mol/ps at 303.15 K

Calculated rlist for 1x1 atom pair-list as 1.238 nm, buffer size 0.038 nm

Set rlist, assuming 4x4 atom pair-list, to 1.200 nm, buffer size 0.000 nm

Note that mdrun will redetermine rlist based on the actual pair-list setup

NOTE 2 [file step4.1_equilibration.mdp]:
  Removing center of mass motion in the presence of position restraints
  might cause artifacts. When you are using position restraints to
  equilibrate a macro-molecule, the artifacts are usually negligible.

Calculating fourier grid dimensions for X Y Z
Using a fourier grid of 108x108x108, spacing 0.116 0.116 0.116

Estimate for the relative computational load of the PME mesh part: 0.25

This run will generate roughly 147 Mb of data

There were 2 NOTEs

GROMACS reminds you: "I don't believe in astrology; I'm a Sagittarian and we're skeptical." (Arthur C. Clarke)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx mdrun -v -deffnm nvt -nb gpu
                 :-) GROMACS - gmx mdrun, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx mdrun -v -deffnm nvt -nb gpu

Reading file nvt.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Changing nstlist from 20 to 100, rlist from 1.2 to 1.298

1 GPU selected for this run.
Mapping of GPU IDs to the 2 GPU tasks in the 1 rank on this node:
  PP:0,PME:0
PP tasks will do (non-perturbed) short-ranged interactions on the GPU
PP task will update and constrain coordinates on the CPU
PME tasks will do all aspects on the GPU
Using 1 MPI thread
Using 56 OpenMP threads 

starting mdrun 'Title'
125000 steps,    125.0 ps.
step 2900: timed with pme grid 108 108 108, coulomb cutoff 1.200: 351.3 M-cycles
step 3100: timed with pme grid 100 100 100, coulomb cutoff 1.250: 384.3 M-cycles
step 3300: timed with pme grid 84 84 84, coulomb cutoff 1.488: 499.1 M-cycles
step 3500: timed with pme grid 96 96 96, coulomb cutoff 1.302: 399.1 M-cycles
step 3700: timed with pme grid 100 100 100, coulomb cutoff 1.250: 374.5 M-cycles
step 3900: timed with pme grid 104 104 104, coulomb cutoff 1.202: 357.6 M-cycles
step 4100: timed with pme grid 108 108 108, coulomb cutoff 1.200: 351.6 M-cycles
step 4300: timed with pme grid 100 100 100, coulomb cutoff 1.250: 375.1 M-cycles
step 4500: timed with pme grid 104 104 104, coulomb cutoff 1.202: 357.9 M-cycles
step 4700: timed with pme grid 108 108 108, coulomb cutoff 1.200: 353.1 M-cycles
              optimal pme grid 108 108 108, coulomb cutoff 1.200
step 124900, remaining wall clock time:     0 s          
Writing final coordinates.
step 125000, remaining wall clock time:     0 s          
               Core t (s)   Wall t (s)        (%)
       Time:    13535.437      241.752     5598.9
                 (ns/day)    (hour/ns)
Performance:       44.674        0.537

GROMACS reminds you: "When a distinguished but elderly scientist states that something is possible, he is almost certainly right. When he states that something is impossible, he is very probably wrong." (Arthur C. Clarke)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx grompp -f step5_production.mdp -c nvt.gro -t nvt.cpt -p topol.top -n index.ndx -o md.tpr
                :-) GROMACS - gmx grompp, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx grompp -f step5_production.mdp -c nvt.gro -t nvt.cpt -p topol.top -n index.ndx -o md.tpr

Replacing old mdp entry 'nstxtcout' by 'nstxout-compressed'

NOTE 1 [file step5_production.mdp]:
  leapfrog does not yet support Nose-Hoover chains, nhchainlength reset to
  1

Setting the LD random seed to -21785

Generated 700 of the 703 non-bonded parameter combinations
Generating 1-4 interactions: fudge = 1

Generated 378 of the 703 1-4 parameter combinations

Excluding 3 bonded neighbours molecule type 'PROA'

turning H bonds into constraints...

Excluding 3 bonded neighbours molecule type 'PROB'

turning H bonds into constraints...

Excluding 1 bonded neighbours molecule type 'POT'

turning H bonds into constraints...

Excluding 1 bonded neighbours molecule type 'CLA'

turning H bonds into constraints...

Excluding 2 bonded neighbours molecule type 'TIP3'

turning H bonds into constraints...
Number of degrees of freedom in T-Coupling group SOLU is 7043.00
Number of degrees of freedom in T-Coupling group SOLV is 362841.00

The largest distance between excluded atoms is 0.411 nm between atom 508 and 519

Determining Verlet buffer for a tolerance of 0.005 kJ/mol/ps at 303.15 K

Calculated rlist for 1x1 atom pair-list as 1.296 nm, buffer size 0.096 nm

Set rlist, assuming 4x4 atom pair-list, to 1.223 nm, buffer size 0.023 nm

Note that mdrun will redetermine rlist based on the actual pair-list setup

Reading Coordinates, Velocities and Box size from old trajectory

Will read whole trajectory
Last frame         -1 time  125.000   

Using frame at t = 125 ps

Starting time for run is 0 ps
Calculating fourier grid dimensions for X Y Z
Using a fourier grid of 108x108x108, spacing 0.116 0.116 0.116

Estimate for the relative computational load of the PME mesh part: 0.24

NOTE 2 [file step5_production.mdp]:
  This run will generate roughly 5307 Mb of data


There were 2 NOTEs

GROMACS reminds you: "Some People Say Not to Worry About the Air" (The Talking Heads)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx mdrun -v -deffnm md -nb gpu
                 :-) GROMACS - gmx mdrun, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx mdrun -v -deffnm md -nb gpu

Reading file md.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Changing nstlist from 20 to 100, rlist from 1.223 to 1.343

1 GPU selected for this run.
Mapping of GPU IDs to the 2 GPU tasks in the 1 rank on this node:
  PP:0,PME:0
PP tasks will do (non-perturbed) short-ranged interactions on the GPU
PP task will update and constrain coordinates on the CPU
PME tasks will do all aspects on the GPU
Using 1 MPI thread
Using 56 OpenMP threads 


WARNING: This run will generate roughly 5211 Mb of data

starting mdrun 'Title'
50000000 steps, 100000.0 ps.
step 2600: timed with pme grid 108 108 108, coulomb cutoff 1.200: 375.0 M-cycles
step 2800: timed with pme grid 100 100 100, coulomb cutoff 1.250: 399.5 M-cycles
step 3000: timed with pme grid 84 84 84, coulomb cutoff 1.488: 540.1 M-cycles
step 3200: timed with pme grid 96 96 96, coulomb cutoff 1.302: 432.2 M-cycles
step 3400: timed with pme grid 100 100 100, coulomb cutoff 1.250: 410.3 M-cycles
step 3600: timed with pme grid 104 104 104, coulomb cutoff 1.202: 396.7 M-cycles
step 3800: timed with pme grid 108 108 108, coulomb cutoff 1.200: 393.5 M-cycles
              optimal pme grid 108 108 108, coulomb cutoff 1.200
step 49999900, remaining wall clock time:     0 s          
Writing final coordinates.
step 50000000, remaining wall clock time:     0 s          
               Core t (s)   Wall t (s)        (%)
       Time:  5718750.747   102120.582     5600.0
                         1d04h22:00
                 (ns/day)    (hour/ns)
Performance:       84.606        0.284

GROMACS reminds you: "Oh, There Goes Gravity" (Eminem)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx energy -f md.edr -o potential.xvg
                :-) GROMACS - gmx energy, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx energy -f md.edr -o potential.xvg

Opened md.edr as single precision energy file

Select the terms you want from the following list by
selecting either (part of) the name or the number or a combination.
End your selection with an empty line or a zero.
-------------------------------------------------------------------
  1  Bond             2  U-B              3  Proper-Dih.      4  Improper-Dih. 
  5  CMAP-Dih.        6  LJ-14            7  Coulomb-14       8  LJ-(SR)       
  9  Coulomb-(SR)    10  Coul.-recip.    11  Potential       12  Kinetic-En.   
 13  Total-Energy    14  Conserved-En.   15  Temperature     16  Pressure      
 17  Constr.-rmsd    18  Box-X           19  Box-Y           20  Box-Z         
 21  Volume          22  Density         23  pV              24  Enthalpy      
 25  Vir-XX          26  Vir-XY          27  Vir-XZ          28  Vir-YX        
 29  Vir-YY          30  Vir-YZ          31  Vir-ZX          32  Vir-ZY        
 33  Vir-ZZ          34  Pres-XX         35  Pres-XY         36  Pres-XZ       
 37  Pres-YX         38  Pres-YY         39  Pres-YZ         40  Pres-ZX       
 41  Pres-ZY         42  Pres-ZZ         43  #Surf*SurfTen   44  Box-Vel-XX    
 45  Box-Vel-YY      46  Box-Vel-ZZ      47  T-SOLU          48  T-SOLV        

11 0
Last energy frame read 50000 time 100000.000         

Statistics over 50000001 steps [ 0.0000 through 100000.0000 ps ], 1 data sets
All statistics are over 500001 points

Energy                      Average   Err.Est.       RMSD  Tot-Drift
-------------------------------------------------------------------------------
Potential                -2.61849e+06         17    2582.53   -89.5361  (kJ/mol)

GROMACS reminds you: "Remember, being healthy is basically dying as slowly as possible." (Ricky Gervais)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx energy -f nvt.edr -o temperature.xvg
                :-) GROMACS - gmx energy, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx energy -f nvt.edr -o temperature.xvg

Opened nvt.edr as single precision energy file

Select the terms you want from the following list by
selecting either (part of) the name or the number or a combination.
End your selection with an empty line or a zero.
-------------------------------------------------------------------
  1  Bond             2  U-B              3  Proper-Dih.      4  Improper-Dih. 
  5  CMAP-Dih.        6  LJ-14            7  Coulomb-14       8  LJ-(SR)       
  9  Coulomb-(SR)    10  Coul.-recip.    11  Position-Rest.  12  Potential     
 13  Kinetic-En.     14  Total-Energy    15  Conserved-En.   16  Temperature   
 17  Pressure        18  Constr.-rmsd    19  Vir-XX          20  Vir-XY        
 21  Vir-XZ          22  Vir-YX          23  Vir-YY          24  Vir-YZ        
 25  Vir-ZX          26  Vir-ZY          27  Vir-ZZ          28  Pres-XX       
 29  Pres-XY         30  Pres-XZ         31  Pres-YX         32  Pres-YY       
 33  Pres-YZ         34  Pres-ZX         35  Pres-ZY         36  Pres-ZZ       
 37  #Surf*SurfTen   38  T-SOLU          39  T-SOLV        

16 0
Last energy frame read 125 time  125.000          

Statistics over 125001 steps [ 0.0000 through 125.0000 ps ], 1 data sets
All statistics are over 1251 points

Energy                      Average   Err.Est.       RMSD  Tot-Drift
-------------------------------------------------------------------------------
Temperature                 303.183      0.022    12.6559  -0.195303  (K)

GROMACS reminds you: "I like to wait, then I feel like I do something" (Carl Caleman)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx energy -f md.edr -o mdtemperature.xvg
                :-) GROMACS - gmx energy, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx energy -f md.edr -o mdtemperature.xvg

Opened md.edr as single precision energy file

Select the terms you want from the following list by
selecting either (part of) the name or the number or a combination.
End your selection with an empty line or a zero.
-------------------------------------------------------------------
  1  Bond             2  U-B              3  Proper-Dih.      4  Improper-Dih. 
  5  CMAP-Dih.        6  LJ-14            7  Coulomb-14       8  LJ-(SR)       
  9  Coulomb-(SR)    10  Coul.-recip.    11  Potential       12  Kinetic-En.   
 13  Total-Energy    14  Conserved-En.   15  Temperature     16  Pressure      
 17  Constr.-rmsd    18  Box-X           19  Box-Y           20  Box-Z         
 21  Volume          22  Density         23  pV              24  Enthalpy      
 25  Vir-XX          26  Vir-XY          27  Vir-XZ          28  Vir-YX        
 29  Vir-YY          30  Vir-YZ          31  Vir-ZX          32  Vir-ZY        
 33  Vir-ZZ          34  Pres-XX         35  Pres-XY         36  Pres-XZ       
 37  Pres-YX         38  Pres-YY         39  Pres-YZ         40  Pres-ZX       
 41  Pres-ZY         42  Pres-ZZ         43  #Surf*SurfTen   44  Box-Vel-XX    
 45  Box-Vel-YY      46  Box-Vel-ZZ      47  T-SOLU          48  T-SOLV        

15 0
Last energy frame read 50000 time 100000.000         

Statistics over 50000001 steps [ 0.0000 through 100000.0000 ps ], 1 data sets
All statistics are over 500001 points

Energy                      Average   Err.Est.       RMSD  Tot-Drift
-------------------------------------------------------------------------------
Temperature                 303.151    0.00059    0.87304 -0.0023368  (K)

GROMACS reminds you: "Good judgement is the result of experience; experience is the result of bad judgement." (Mark Twain)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx energy -f npt.edr -o density.xvg
                :-) GROMACS - gmx energy, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx energy -f npt.edr -o density.xvg


-------------------------------------------------------
Program:     gmx energy, version 2023-plumed_2.9.0
Source file: src/gromacs/commandline/cmdlineparser.cpp (line 271)
Function:    void gmx::CommandLineParser::parse(int*, char**)

Error in user input:
Invalid command-line options
  In command-line option -f
    File 'npt.edr' does not exist or is not accessible.
    The file could not be opened.
      Reason: No such file or directory
      (call to fopen() returned error code 2)

For more information and tips for troubleshooting, please check the GROMACS
website at http://www.gromacs.org/Documentation/Errors
-------------------------------------------------------
user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx energy -f nvt.edr -o density.xvg
                :-) GROMACS - gmx energy, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx energy -f nvt.edr -o density.xvg

Opened nvt.edr as single precision energy file

Select the terms you want from the following list by
selecting either (part of) the name or the number or a combination.
End your selection with an empty line or a zero.
-------------------------------------------------------------------
  1  Bond             2  U-B              3  Proper-Dih.      4  Improper-Dih. 
  5  CMAP-Dih.        6  LJ-14            7  Coulomb-14       8  LJ-(SR)       
  9  Coulomb-(SR)    10  Coul.-recip.    11  Position-Rest.  12  Potential     
 13  Kinetic-En.     14  Total-Energy    15  Conserved-En.   16  Temperature   
 17  Pressure        18  Constr.-rmsd    19  Vir-XX          20  Vir-XY        
 21  Vir-XZ          22  Vir-YX          23  Vir-YY          24  Vir-YZ        
 25  Vir-ZX          26  Vir-ZY          27  Vir-ZZ          28  Pres-XX       
 29  Pres-XY         30  Pres-XZ         31  Pres-YX         32  Pres-YY       
 33  Pres-YZ         34  Pres-ZX         35  Pres-ZY         36  Pres-ZZ       
 37  #Surf*SurfTen   38  T-SOLU          39  T-SOLV        

^C
user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx energy -f nvt.edr -o pressure.xvg
                :-) GROMACS - gmx energy, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx energy -f nvt.edr -o pressure.xvg

Opened nvt.edr as single precision energy file

Select the terms you want from the following list by
selecting either (part of) the name or the number or a combination.
End your selection with an empty line or a zero.
-------------------------------------------------------------------
  1  Bond             2  U-B              3  Proper-Dih.      4  Improper-Dih. 
  5  CMAP-Dih.        6  LJ-14            7  Coulomb-14       8  LJ-(SR)       
  9  Coulomb-(SR)    10  Coul.-recip.    11  Position-Rest.  12  Potential     
 13  Kinetic-En.     14  Total-Energy    15  Conserved-En.   16  Temperature   
 17  Pressure        18  Constr.-rmsd    19  Vir-XX          20  Vir-XY        
 21  Vir-XZ          22  Vir-YX          23  Vir-YY          24  Vir-YZ        
 25  Vir-ZX          26  Vir-ZY          27  Vir-ZZ          28  Pres-XX       
 29  Pres-XY         30  Pres-XZ         31  Pres-YX         32  Pres-YY       
 33  Pres-YZ         34  Pres-ZX         35  Pres-ZY         36  Pres-ZZ       
 37  #Surf*SurfTen   38  T-SOLU          39  T-SOLV        

17 0
Last energy frame read 125 time  125.000          

Statistics over 125001 steps [ 0.0000 through 125.0000 ps ], 1 data sets
All statistics are over 1251 points

Energy                      Average   Err.Est.       RMSD  Tot-Drift
-------------------------------------------------------------------------------
Pressure                    -981.14        2.6    249.109   -15.3853  (bar)

GROMACS reminds you: "He's using code that only you and I know" (Kate Bush)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx energy -f md.edr -o mdpressure.xvg
                :-) GROMACS - gmx energy, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx energy -f md.edr -o mdpressure.xvg

Opened md.edr as single precision energy file

Select the terms you want from the following list by
selecting either (part of) the name or the number or a combination.
End your selection with an empty line or a zero.
-------------------------------------------------------------------
  1  Bond             2  U-B              3  Proper-Dih.      4  Improper-Dih. 
  5  CMAP-Dih.        6  LJ-14            7  Coulomb-14       8  LJ-(SR)       
  9  Coulomb-(SR)    10  Coul.-recip.    11  Potential       12  Kinetic-En.   
 13  Total-Energy    14  Conserved-En.   15  Temperature     16  Pressure      
 17  Constr.-rmsd    18  Box-X           19  Box-Y           20  Box-Z         
 21  Volume          22  Density         23  pV              24  Enthalpy      
 25  Vir-XX          26  Vir-XY          27  Vir-XZ          28  Vir-YX        
 29  Vir-YY          30  Vir-YZ          31  Vir-ZX          32  Vir-ZY        
 33  Vir-ZZ          34  Pres-XX         35  Pres-XY         36  Pres-XZ       
 37  Pres-YX         38  Pres-YY         39  Pres-YZ         40  Pres-ZX       
 41  Pres-ZY         42  Pres-ZZ         43  #Surf*SurfTen   44  Box-Vel-XX    
 45  Box-Vel-YY      46  Box-Vel-ZZ      47  T-SOLU          48  T-SOLV        

16 0
Last energy frame read 50000 time 100000.000         

Statistics over 50000001 steps [ 0.0000 through 100000.0000 ps ], 1 data sets
All statistics are over 500001 points

Energy                      Average   Err.Est.       RMSD  Tot-Drift
-------------------------------------------------------------------------------
Pressure                     1.0677     0.0017    82.6995 -0.0114636  (bar)

GROMACS reminds you: "Get Down In 3D" (George Clinton)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx trjconv -s md.tpr -f md.xtc -o md_noPBC.xtc -pbc mol -center
                :-) GROMACS - gmx trjconv, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx trjconv -s md.tpr -f md.xtc -o md_noPBC.xtc -pbc mol -center

Note that major changes are planned in future for trjconv, to improve usability and utility.
Will write xtc: Compressed trajectory (portable xdr format): xtc
Reading file md.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Reading file md.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Select group for centering
Group     0 (         System) has 184069 elements
Group     1 (        Protein) has  2824 elements
Group     2 (      Protein-H) has  1398 elements
Group     3 (        C-alpha) has   165 elements
Group     4 (       Backbone) has   495 elements
Group     5 (      MainChain) has   658 elements
Group     6 (   MainChain+Cb) has   822 elements
Group     7 (    MainChain+H) has   818 elements
Group     8 (      SideChain) has  2006 elements
Group     9 (    SideChain-H) has   740 elements
Group    10 (    Prot-Masses) has  2824 elements
Group    11 (    non-Protein) has 181245 elements
Group    12 (          Other) has 181245 elements
Group    13 (            POT) has   172 elements
Group    14 (            CLA) has   182 elements
Group    15 (           TIP3) has 180891 elements
Select a group: 1
Selected 1: 'Protein'
Select group for output
Group     0 (         System) has 184069 elements
Group     1 (        Protein) has  2824 elements
Group     2 (      Protein-H) has  1398 elements
Group     3 (        C-alpha) has   165 elements
Group     4 (       Backbone) has   495 elements
Group     5 (      MainChain) has   658 elements
Group     6 (   MainChain+Cb) has   822 elements
Group     7 (    MainChain+H) has   818 elements
Group     8 (      SideChain) has  2006 elements
Group     9 (    SideChain-H) has   740 elements
Group    10 (    Prot-Masses) has  2824 elements
Group    11 (    non-Protein) has 181245 elements
Group    12 (          Other) has 181245 elements
Group    13 (            POT) has   172 elements
Group    14 (            CLA) has   182 elements
Group    15 (           TIP3) has 180891 elements
Select a group: 0
Selected 0: 'System'
Reading frame       0 time    0.000   
Precision of md.xtc is 0.001 (nm)
Using output precision of 0.001 (nm)
Last frame       1000 time 100000.000    ->  frame    999 time 99900.000      
 ->  frame   1000 time 100000.000      
Last written: frame   1000 time 100000.000


GROMACS reminds you: "In the processing of models we must be especially cautious of the human weakness to think that models can be verified or validated. Especially one's own." (Roald Hoffmann)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx rms -s md_0_1.tpr -f md_0_1_noPBC.xtc -o rmsd.xvg -tu ns
                  :-) GROMACS - gmx rms, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx rms -s md_0_1.tpr -f md_0_1_noPBC.xtc -o rmsd.xvg -tu ns


-------------------------------------------------------
Program:     gmx rms, version 2023-plumed_2.9.0
Source file: src/gromacs/commandline/cmdlineparser.cpp (line 271)
Function:    void gmx::CommandLineParser::parse(int*, char**)

Error in user input:
Invalid command-line options
  In command-line option -s
    File 'md_0_1.tpr' does not exist or is not accessible.
    The file could not be opened.
      Reason: No such file or directory
      (call to fopen() returned error code 2)
  In command-line option -f
    File 'md_0_1_noPBC.xtc' does not exist or is not accessible.
    The file could not be opened.
      Reason: No such file or directory
      (call to fopen() returned error code 2)

For more information and tips for troubleshooting, please check the GROMACS
website at http://www.gromacs.org/Documentation/Errors
-------------------------------------------------------
user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ 
user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx rms -s md.tpr -f md_noPBC.xtc -o rmsd.xvg -tu ns
                  :-) GROMACS - gmx rms, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx rms -s md.tpr -f md_noPBC.xtc -o rmsd.xvg -tu ns

Reading file md.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Reading file md.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Select group for least squares fit
Group     0 (         System) has 184069 elements
Group     1 (        Protein) has  2824 elements
Group     2 (      Protein-H) has  1398 elements
Group     3 (        C-alpha) has   165 elements
Group     4 (       Backbone) has   495 elements
Group     5 (      MainChain) has   658 elements
Group     6 (   MainChain+Cb) has   822 elements
Group     7 (    MainChain+H) has   818 elements
Group     8 (      SideChain) has  2006 elements
Group     9 (    SideChain-H) has   740 elements
Group    10 (    Prot-Masses) has  2824 elements
Group    11 (    non-Protein) has 181245 elements
Group    12 (          Other) has 181245 elements
Group    13 (            POT) has   172 elements
Group    14 (            CLA) has   182 elements
Group    15 (           TIP3) has 180891 elements
Select a group: 4
Selected 4: 'Backbone'
Select group for RMSD calculation
Group     0 (         System) has 184069 elements
Group     1 (        Protein) has  2824 elements
Group     2 (      Protein-H) has  1398 elements
Group     3 (        C-alpha) has   165 elements
Group     4 (       Backbone) has   495 elements
Group     5 (      MainChain) has   658 elements
Group     6 (   MainChain+Cb) has   822 elements
Group     7 (    MainChain+H) has   818 elements
Group     8 (      SideChain) has  2006 elements
Group     9 (    SideChain-H) has   740 elements
Group    10 (    Prot-Masses) has  2824 elements
Group    11 (    non-Protein) has 181245 elements
Group    12 (          Other) has 181245 elements
Group    13 (            POT) has   172 elements
Group    14 (            CLA) has   182 elements
Group    15 (           TIP3) has 180891 elements
Select a group: 0
Selected 0: 'System'
Last frame       1000 time  100.000   

GROMACS reminds you: "I'm not interrupting you, I'm putting our conversation in full-duplex mode." (Antone Roundy)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx rms -s em.tpr -f md_noPBC.xtc -o rmsd_xtal.xvg -tu ns
                  :-) GROMACS - gmx rms, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx rms -s em.tpr -f md_noPBC.xtc -o rmsd_xtal.xvg -tu ns

Reading file em.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Reading file em.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Select group for least squares fit
Group     0 (         System) has 184069 elements
Group     1 (        Protein) has  2824 elements
Group     2 (      Protein-H) has  1398 elements
Group     3 (        C-alpha) has   165 elements
Group     4 (       Backbone) has   495 elements
Group     5 (      MainChain) has   658 elements
Group     6 (   MainChain+Cb) has   822 elements
Group     7 (    MainChain+H) has   818 elements
Group     8 (      SideChain) has  2006 elements
Group     9 (    SideChain-H) has   740 elements
Group    10 (    Prot-Masses) has  2824 elements
Group    11 (    non-Protein) has 181245 elements
Group    12 (          Other) has 181245 elements
Group    13 (            POT) has   172 elements
Group    14 (            CLA) has   182 elements
Group    15 (           TIP3) has 180891 elements
Select a group: 4
Selected 4: 'Backbone'
Select group for RMSD calculation
Group     0 (         System) has 184069 elements
Group     1 (        Protein) has  2824 elements
Group     2 (      Protein-H) has  1398 elements
Group     3 (        C-alpha) has   165 elements
Group     4 (       Backbone) has   495 elements
Group     5 (      MainChain) has   658 elements
Group     6 (   MainChain+Cb) has   822 elements
Group     7 (    MainChain+H) has   818 elements
Group     8 (      SideChain) has  2006 elements
Group     9 (    SideChain-H) has   740 elements
Group    10 (    Prot-Masses) has  2824 elements
Group    11 (    non-Protein) has 181245 elements
Group    12 (          Other) has 181245 elements
Group    13 (            POT) has   172 elements
Group    14 (            CLA) has   182 elements
Group    15 (           TIP3) has 180891 elements
Select a group: 0
Selected 0: 'System'
Last frame       1000 time  100.000   

GROMACS reminds you: "Lets get back to beer" (Yuxuan Zhuang, in a discussion about science communication)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ gmx gyrate -s md.tpr -f md_noPBC.xtc -o gyrate.xvg
                :-) GROMACS - gmx gyrate, 2023-plumed_2.9.0 (-:

Executable:   /apps/codes/gromacs-2023/bin/gmx
Data prefix:  /apps/codes/gromacs-2023
Working dir:  /home/user/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs
Command line:
  gmx gyrate -s md.tpr -f md_noPBC.xtc -o gyrate.xvg

Reading file md.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Reading file md.tpr, VERSION 2023-plumed_2.9.0 (single precision)
Group     0 (         System) has 184069 elements
Group     1 (        Protein) has  2824 elements
Group     2 (      Protein-H) has  1398 elements
Group     3 (        C-alpha) has   165 elements
Group     4 (       Backbone) has   495 elements
Group     5 (      MainChain) has   658 elements
Group     6 (   MainChain+Cb) has   822 elements
Group     7 (    MainChain+H) has   818 elements
Group     8 (      SideChain) has  2006 elements
Group     9 (    SideChain-H) has   740 elements
Group    10 (    Prot-Masses) has  2824 elements
Group    11 (    non-Protein) has 181245 elements
Group    12 (          Other) has 181245 elements
Group    13 (            POT) has   172 elements
Group    14 (            CLA) has   182 elements
Group    15 (           TIP3) has 180891 elements
Select a group: 1
Selected 1: 'Protein'
Last frame       1000 time 100000.000   

GROMACS reminds you: "Look at these, my work-strong arms" (P.J. Harvey)

user@user:~/Downloads/AB 23.5.24/charmm-gui/charmm-gui-1637690923/gromacs$ 


