pvemri
======

A matlab implementation of the partial volume estimation for brain MRI (Tohka, Zijedenbos, Evans, NeuroImage 2004). 
The function also implement "the incremental k-means" based preliminary segmentation (Manjon et al MRM 2008).

Installation: You'll need to compile two c files into mex. Saying (in Matlab)

mex c_icm_trans.c

mex c_tissue_fractions.c

works most of the time. Mex files for 64-bit Windows are provided. In case mex-compilation won't work, 
check the pure Matlab implementation in pure_matlab subdir. However, this is not recommended as it is very slow 
compared to optimized c-code in mex-files.

Usage : The function pvemrimex2.m is the main function including all the pure Matlab components of the algorithm. pvemrimex2 is 
extremely fast and should run in under 10 seconds for a normal MRI volume (e.g. 181 x 217 x 181). 

References:

The method itself:

J. Tohka, A. Zijdenbos, and A.C. Evans. Fast and robust parameter estimation for statistical partial 
volume models in brain MRI. NeuroImage, 23(1):84 - 97, 2004.

Incremental k-means:

J.V. Manjón, J. Tohka , G. García-Martí, J. Carbonell-Caballero, J.J. Lull, L. Martí-Bonmatí and M. Robles. Robust 
MRI Brain Tissue Parameter Estimation by Multistage Outlier Rejection. Magnetic Resonance in Medicine, 59:866 - 873, 2008.

The fast implementation:

J. Tohka . FAST-PVE: Extremely Fast Markov Random Field Based Brain MRI Tissue Classification. SCIA 2013, 
Scandinavian Conference on Image Analysis, Helsinki, Finland, 2013, Lecture Notes in Computer Science vol. 
7944 pp. 266 - 276, 2013.
