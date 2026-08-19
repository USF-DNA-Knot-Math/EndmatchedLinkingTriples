# Endmatched Linking Triples
This repository contains Mathematica code to compute the End-matched Linking triple measure for a given set of directed embedded piecewise-linear curves with endpoints.

ExampleComputation.nb contains a description of all the functions and a computation for a pair of curves in the tensegrity triangle model 3T12(PDB ID: 8SJM). All the functions can be found in functions.m, and coordinates.zip contains some sample coordinates from Tensegrity triangle data deposited in the PDB database.

To compute for any desired list of piecewise linear curves: define the list of coordinates for the curves, say curve1, curve2, curve3 ... curven, and use the following function: 

Computelinkingtriplesendmatched[{curve1, curve2, ..., curven}]  

This will return the end-matched linking triples for all four end-matchings and for all the curves taken pairwise.

To view the intermediate steps: swap the curve1 and curve2 with your coordinates in ExampleComputation.nb, and choose the desired end-matched projection by changing the values of p1 and p2 in {ini1,ini2,term1,term2}. Running this will generate the projections, crossing information, and finally the linking triples for the pair {curve1, curve2}
