# Native multiqubit Toffoli gates on ion trap quantum computers

## Abstract
We examine the detailed scenario for implementing n-control-qubit Toffoli gates and select gates on ion-trap quantum computers, especially those that shuttle ions into interaction zones. We determine expected performance of these gates with realistic parameters for an ion-trap quantum computer and taking into account the time variation of the exchange integrals. This allows us to estimate the errors due to spin-phonon entanglement as well. While there are challenges with implementing these gates, because their performance always has some degree of error, they should be feasible on current hardware, but they may be too slow to be used efficiently in quantum codes on noisy intermediate scale quantum computers.

## Overview

* `IdentitySequenceGeneration.ipynb`: Generates sequences of U2/U3 gates of a given length, such that the action of the sequence is equivalent to an identity gate.
* `finding_gaps.ipynb`: Finds Matrix visualisation of circuit gaps for any given quantum circuit on any required backend.
* `padding.ipynb`: Pads the circuit gaps in a given quantum circuit with identity sequences.
* `error_padding.ipynb`: Evaluates the error in a given gapped circuit and its padded version.

### Timed Padding

* `backend_times.ipynb`: Can be used to obtain gate execution times for any backend.
* `finding_timed_gapsOurense.ipynb`: Finds circuit gaps according to gate execution times, designed specifically for Ourense.
* `finding_small_timed_gapsOurense.ipynb`: Reduces matrix visualization of timed circuit gaps produced by `finding_timed_gapsOurense.ipynb` to more compact form, designed specifically for Ourense.
* `timed_padding.ipynb`: Pads the circuit gaps according to gate execution times, designed specifically for Ourense.

### Gate Error Statistics

* `U3vsU2_multipleruns.ipynb`: Compares error statistics for execution of U3 and U2 gates on a given backend. 
* `VigoErrorStats_Lambda.ipynb`: Finds the error statistics of U3 gate as function of parameter Lambda and Phi for Vigo.
* `VigoErrorStats_Theta.ipynb`: Finds the error statistics of U3 gate as function of parameter Theta and Phi for Vigo.
* `3DplotsErrorStats.ipynb`: Uses data from error statistics to get surface plots of noise to obtain optimization points.

### Reduced Padding

* `ThresholdPadding.ipynb`: Uses parameters threshold and force_threshold to reduce the amount of padding in a given circuit gap.
* `ReducedSpreadPadding_FixDepth_Vigo.ipynb`: Implements reduced padding with gates spread over the gap. The data is collected by varying the type of gap but keeping the gap length as fixed and equal to 20. Implemented on Vigo. 
* `ReducedSpreadPad_VarDepth_Half_Vigo.ipynb`: Implements reduced padding with gates spread over the gap. The data is collected by varying the length of gap (depth) but keeping the type of circuit as fixed. The maximum padding length is only half of the gap length. Implemented on Vigo.
* `ReducedSpreadPad_VarDepth_Full_Vigo.ipynb`: Implements reduced padding with gates spread over the gap. The data is collected by varying the length of gap (depth) but keeping the type of circuit as fixed. The maximum padding length is equal to the gap length. Implemented on Vigo.
* `VarDepth_DataAnalysis.ipynb`: Uses data from Variable Depth codes to obtain error reduction plots.


