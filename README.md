# seacarbx - seacarb extension for deep-time carbonate system calculations

*seacarbx* is a **seacarb** e**x**tension written in R, which enables to use *seacarb* (Gattuso et al., 2019) for deep-time carbonate system calculations. For this, the functions carb, K0, K1, K2, Ks, Kw, Kb, Kspa, and Kspc were modfied to account for the effect of seawater [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] on the dissociation constants of carbonic and boric acid. Their names are based on the original names, and suffixed with a ‘x’. In addition to the modified functions, seacarbx contains *MyAMI* that are tabulated parameters defining the temperature and salinity dependencies of the conditional equilibrium constants for [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] in the range 0–60 mM (from Hain et al., 2015). Please read the manual for more details.

If you use *seacarbx* for your published research, please cite it as:

Raitzsch, M., Gattuso, J.-P. and Hain, M. (2020): seacarbx - seacarb extension for deep-time carbonate system calculations, Zenodo, http://doi.org/10.5281/zenodo.4139858.

**but please also acknowledge the original works of the following:**

Gattuso J.-P., Epitalon J.-M., Lavigne H. and Orr J. (2019): seacarb: seawater carbonate chemistry. R package version 3.2.12. http://CRAN.R-project.org/package=seacarb.

Hain, M. P., Sigman, D. M., Higgins, J. A. and Haug, G. H. (2015): The effects of secular calcium and magnesium concentration changes on the thermodynamics of seawater acid/base chemistry: Implications for Eocene and Cretaceous ocean carbon chemistry and buffering, Glob. Biogeochem. Cyc., 29(5), 517–533, http://doi.org/10.1002/2014GB004986.
