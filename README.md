# Native multiqubit Toffoli gates on ion trap quantum computers

## Abstract
We examine the detailed scenario for implementing n-control-qubit Toffoli gates and select gates on ion-trap quantum computers, especially those that shuttle ions into interaction zones. We determine expected performance of these gates with realistic parameters for an ion-trap quantum computer and taking into account the time variation of the exchange integrals. This allows us to estimate the errors due to spin-phonon entanglement as well. While there are challenges with implementing these gates, because their performance always has some degree of error, they should be feasible on current hardware, but they may be too slow to be used efficiently in quantum codes on noisy intermediate scale quantum computers.

## Overview

In Numerical Results section, we have simulated the model for various cases and have generated plots and tables to describe our observations. The data for these results have been stored in .mat files in this repository with descriptions of data files listed below. 
Unless specified, each of the data files have probability data points (named "Prob") and corresponding discrete times (named "t"). The probability data set, "Prob", is in matrix form with rows representing different combinations of ion states. For n=2 Bit Toffoli Gates, we have total of 3 ions and thus, there are 8 possible states. In such cases, the probability data set has 8 rows with each row representing the probability of ions to be in states 
|-,-,->, |-,+,->, |-,-,+>, |-,+,+>, |+,-,->, |+,+,->, |+,-,+> and |+,+,+> respectively, at a given time. 

### Static vs. Time-Dependent Exchange Couplings (J)

Each file has "Prob" matrix of size 8x601 and "t" matrix of size 1x601, where 601 represents the number of time steps.

* `StaticCoupling.mat`: Includes time-evolution of 2-Bit i-Toffoli Gate when Exchange Coupling is Static. B<sub>y</sub>/&hbar;=2&pi; x75.98Hz and &mu;=1.0095&omega;<sub>CM</sub>. Used in Figure 1. 
* `TimeDepCoupling.mat`: Includes time-evolution of 2-Bit i-Toffoli Gate when Exchange Coupling is Time-Dependent. B<sub>y</sub>/&hbar;=2&pi; x75.98Hz and &mu;=1.0095&omega;<sub>CM</sub>. Used in Figure 2. 

All the simulations and data after this has Time-Dependent Exchange Couplings only to keep the model closer to real case.

### B<sub>y</sub> and &mu; Dependence

Each file has "Prob" matrix of size 8x301 and "t" matrix of size 1x301, where 301 represents the number of time steps.

* `760By.mat`: Includes time-evolution of 2-Bit i-Toffoli Gate when B<sub>y</sub>/&hbar;=2&pi; x759.8Hz & &mu;=1.0095&omega;<sub>CM</sub>. Used in Figure 3a and Table 1.
* `7600By.mat`: Includes time-evolution of 2-Bit i-Toffoli Gate when B<sub>y</sub>/&hbar;=2&pi; x7598Hz & &mu;=1.0095&omega<sub>CM</sub>. Used in Figure 3b and Table 1. 
* `mu10380.mat`: Includes time-evolution of 2-Bit i-Toffoli Gate when &mu;=1.0380&omega;<sub>CM</sub> and B<sub>y</sub>/&hbar;=2&pi; x75.98Hz. Used in Figure 4a.
* `mu10665.mat`: Includes time-evolution of 2-Bit i-Toffoli Gate when &mu;=1.0665&omega;<sub>CM</sub> and B<sub>y</sub>/&hbar;=2&pi; x75.98Hz. Used in Figure 4b.
* `mu10950.mat`: Includes time-evolution of 2-Bit i-Toffoli Gate when &mu;=1.0950&omega;<sub>CM</sub> and B<sub>y</sub>/&hbar;=2&pi; x75.98Hz. Used in Figure 4c.

### Select Gate

Each file has "Prob" matrix of size 8x301 and "t" matrix of size 1x301, where 301 represents the number of time steps.
The following data has been used in Table 5.

* `Select4J.mat`: Includes time-evolution of 2-Bit i-Select Gate when B<sub>y</sub>/&hbar=4J. B<sub>y</sub>/&hbar;=2&pi; x75.98Hz and &mu;=0.9905&omega;<sub>ZZ</sub>.
* `Select12J.mat`: Includes time-evolution of 2-Bit i-Select Gate when B<sub>y</sub>/&hbar=12J. B<sub>y</sub>/&hbar;=2&pi; x75.98Hz and &mu;=0.9905&omega;<sub>ZZ</sub>. Used in Figure 6.
* `Select-12J.mat`: Includes time-evolution of 2-Bit i-Select Gate when B<sub>y</sub>/&hbar=-12J. B<sub>y</sub>/&hbar;=2&pi; x75.98Hz and &mu;=0.9905&omega;<sub>ZZ</sub>.
* `Select-4J.mat`: Includes time-evolution of 2-Bit i-Select Gate when B<sub>y</sub>/&hbar=-4J. B<sub>y</sub>/&hbar;=2&pi; x75.98Hz and &mu;=0.9905&omega;<sub>ZZ</sub>.

### n-Bit i-Toffoli Gate

#### Time Evolution

Each file has "Prob" matrix of size 4x301 and "t" matrix of size 1x301, where 301 represents the number of time steps. The 4 rows correspond to (all control states, target state) = (down, down); (down, up); (up, down) and (up, up) respectively.

* `3BitToff.mat`: Includes time-evolution of 3-Bit i-Toffoli Gate for when all control qubits are in either up state or down state; When B<sub>y</sub>/&hbar;=2&pi; x75.98Hz & &mu;=1.00713&omega;<sub>CM</sub>. Used in Figure 5a; 
* `4BitToff.mat`: Includes time-evolution of 4-Bit i-Toffoli Gate for when all control qubits are in either up state or down state; When B<sub>y</sub>/&hbar;=2&pi; x75.98Hz & &mu;=1.00571&omega;<sub>CM</sub>. Used in Figure 5b.
* `5BitToff.mat`: Includes time-evolution of 5-Bit i-Toffoli Gate for when all control qubits are in either up state or down state; When B<sub>y</sub>/&hbar;=2&pi; x75.98Hz & &mu;=1.00476&omega;<sub>CM</sub>. Used in Figure 5c.

#### Probabilities to Flip

Each file has "Prob" matrix of size (rows)x101 and "t" matrix of size 1x101, where 101 represents the number of time steps.

* `n3Table.mat`: Includes time-evolution of 3-Bit i-Toffoli Gate for all control combinations when B<sub>y</sub>/&hbar;=2&pi; x75.98Hz & &mu;=1.00713&omega;<sub>CM</sub>. Used in Table 2. The "Prob" has 8 rows corresponding to probability to flip the target qubit state for each control combination starting from control state |-,-,->.
* `n4Table.mat`: Includes time-evolution of 4-Bit i-Toffoli Gate for all control combinations when B<sub>y</sub>/&hbar;=2&pi; x75.98Hz & &mu;=1.00571&omega;<sub>CM</sub>. Used in Table 3. The "Prob" has 16 rows corresponding to probability to flip the target qubit state for each control combination starting from control state |-,-,-,->.
* `n5Table.mat`: Includes time-evolution of 5-Bit i-Toffoli Gate for all control combinations when B<sub>y</sub>/&hbar;=2&pi; x75.98Hz & &mu;=1.00476&omega;<sub>CM</sub>. Used in Table 4. The "Prob" has 32 rows corresponding to probability to flip the target qubit state for each control combination starting from control state |-,-,-,-,->.

