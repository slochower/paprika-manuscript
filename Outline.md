# Manuscript outline

- Introduction
    - What are the benefits of absolute binding free energy calculations?
    - Favorable performance in past competitions suggets further development is a worthwhile endeavor
    - We can provide a full thermodynamic profile of binding with competitive rates of convergence to alchemical techniques

- How `paprika` works
    - Basic setup
        - Alignment
        - Solvation
        - Definition and application of restraints
        - Integrated simulation execution, written input files, or OpenMM `System` objects
        - Analysis with TI or MBAR; blocking or autocorrelation statistical inefficiency
    - Highlight reproducibility
    - Extensibility
        - Can save and load restraints and results
        - Can run with AMBER / OpenMM
        - Working towards a stable API, where we can take in new `ForceField` objects or sets of parameters and return $\Delta G$ estimates

- Examples
    - A simple example with one restraint
        - K^{+}-Cl^{-}
        - Plot $\partial U / \partial \lambda$ 
        - Plot PMF
    - An example with a few restraints
        - Something akin to CB6-butane in implicit solvent
    - An example that's challening to converge 
        - Maybe CB8-G3

- Conclusion
    - Robust method of computing binding free energies
    - Allows a lot of user customization
    - Has sane defaults (we will pick some of these for the OpenFF integration)
    - Provides reliable uncertainty methods
    - Produces estimates that agree well with experiment (at least compared to competing packages)
    - Is well-tested

- Related projects
    - CHARMM-GUI: https://pubs.acs.org/doi/full/10.1021/acs.jctc.5b00935
    - GridMAT-MD: https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.21172
    - BLUES: https://pubs.acs.org/doi/full/10.1021/acs.jpcb.7b11820
    - PlayMolecule: https://pubs.acs.org/doi/abs/10.1021/acs.jcim.7b00190
    - `pmemd.ti`: https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.25187
    - https://joss.theoj.org/about