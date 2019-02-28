# Manuscript outline

- Introduction
    - What are the benefits of absolute binding free energy calculations?
        - Direct comparison with experiment
        - Good for force field development
        - ?
    - Brief background on what has been done with US for binding free energy (here or in discussion?)
        - B Roux: https://www.pnas.org/content/102/19/6825
        - M Zacharias: https://pubs.acs.org/doi/abs/10.1021/acs.jctc.8b01022 
        - NonEq: 
            - https://www.pnas.org/content/98/7/3658.short
            - https://onlinelibrary.wiley.com/doi/abs/10.1002/jcc.23398
            - Lots of Steered MD, too many ... maybe we just mention that NonEq exists, but don't get into it
        - APR Tutorial?
        - FETool
        - I thought there was another tool in amber to do this ... maybe thinking of FEW.pl, but that seems alchemical. 
    - Favorable performance in past competitions suggets further development is worthwhile, and easy/tested tool not available
    - We can provide a full thermodynamic profile of binding with competitive rates of convergence to alchemical techniques
    (NMH: Is the "full thermodynamic profile" meant to be distinguishing aspect of APR? because Yank could do that do.  It's more of a relative vs absolute thing I think)

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
    - Future work: 
        - replica exchange (depending on the timelines, maybe it will already be a feature)
        - Command line tool (not sure if worthwhile, but non-python people might like it)
        - other stuff I can't remember

- Related projects  (NMH: what is the criteria for these? They seem very random.  Add Yank?)
    - CHARMM-GUI: https://pubs.acs.org/doi/full/10.1021/acs.jctc.5b00935
    - GridMAT-MD: https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.21172
    - BLUES: https://pubs.acs.org/doi/full/10.1021/acs.jpcb.7b11820
    - PlayMolecule: https://pubs.acs.org/doi/abs/10.1021/acs.jcim.7b00190
    - `pmemd.ti`: https://onlinelibrary.wiley.com/doi/full/10.1002/jcc.25187
    - https://joss.theoj.org/about
