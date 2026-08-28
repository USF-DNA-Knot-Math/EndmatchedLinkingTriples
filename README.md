# End-matched Linking Triples
This repository contains Mathematica procedures to compute the End-matched Linking triple measure for a given set of directed embedded piecewise-linear curves with endpoints.

## Introduction
The **EndmatchedLinkingTriples** takes as **input** an **ordered set** of sets of coordinates that describe **piecewise-linear, directed** curves with **endpoints** embedded in **3-space**. The **output** is a **table of end-matched linking triples** for all the curves taken pairwise. The End-matched linking triple is defined as below:

For an ordered pair of curves $(a,b)$, we consider all possible projections obtained by mapping endpoints of these curves onto each other. For each such projection diagram $D$, we record three values **$(C_1, C_2, \epsilon)$**:

- $C_1$ : The sum of signed crossings in $D$ such that arc in **$a$ is the under-arc**, and the arc in **$b$ is over-arc**.
- $C_2$ : The sum of signed crossings in $D$ such that arc in **$a$ is the over-arc**, and the arc in **$b$ is under-arc**.
- $\epsilon$ : The sign of the crossing obtained at the end-matching after a **small perturbation** of the **projection direction**.

The 3-tuple **$(C_1, C_2, \epsilon)$** is the **End-matched Linking Triple**.

For two endpoints on each curve, there are eight such projections. Half of these projections are redundant since a projection projecting $\iota_a \in a$ onto $\iota_b \in b$ will give the same sign of crossings as the projection projecting $\iota_b$ onto $\iota_a$. So, we consider the convention that the endpoint of the second curve is projected onto the endpoint of the first curve. Therefore, for each pair of curves we have four End-matched projections, and hence four End-matched Linking Triples.

## Tutorial
**ExampleComputation.nb** contains a description of all the procedures and a sample computation for a pair of curves in the **tensegrity triangle model 3T12(PDB ID: 8SJM)**.

- All the procedures can be found in **procedures.m**.
- **SampleCoords\Coord.nb** contains some **sample coordinates** extracted from Tensegrity triangle data deposited in the PDB database.

To view the **intermediate steps** in the sample computation:
1. **Swap curve1 and curve2** in **ExampleComputation.nb** with your desired coordinates. 
2. **Choose the desired end-matched projection** by changing the values of **p1 and p2** among {ini1,ini2,term1,term2}.
3.  Running all cells will **generate the end-matched projection**, the **crossing information**, and finally the **End-matched Linking Triples** for the pair {curve1, curve2}

To compute for **any desired list** of piecewise linear curves: 
1. Define the **list of coordinates** for the curves, say curve1, curve2, curve3 ... curven
2. Then, use the following procedure:

    **Computelinkingtriplesendmatched[{curve_1, curve_2, ..., curve_n}]**

    This will return the **end-matched linking triples for all four end-matchings** and for all the **curves taken pairwise**.

## Acknowledgements
This work was supported by NSF grants DMS-2054321, CCF-2505771, and CCF-2107267.
