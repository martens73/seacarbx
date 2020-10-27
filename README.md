# seacarbx
seacarbx - seacarb extension for deep-time carbonate system calculations

seacarbx is a seacarb extension, which enables to use seacarb (Gattuso et al., 2019) for deep-time carbonate system calculations. For this, the functions carb, K0, K1, K2, Ks, Kw, Kb, Kspa, and Kspc were modfied to account for the effect of seawater [Mg2+] and [Ca2+] on the dissociation constants of carbonic and boric acid. Their names are based on the original names, and suffixed with a ‘x’. In addition to the modified functions, seacarbx contains MyAMI that are tabulated parameters defining the temperature and salinity dependencies of the conditional equilibrium constants for [Mg2+] and [Ca2+] in the range 0–60 mM (from Hain et al., 2015). Please read the manual for more details.
