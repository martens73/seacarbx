
# 'seacarbx' Manual
### Markus Raitzsch, Jean-Pierre Gattuso, and Mathis Hain
#### October 2020

## Description
*seacarbx* is a **seacarb** e**x**tension written in R, which enables to use *seacarb* ([Gattuso et al., 2019](http://CRAN.R-project.org/package=seacarb)) for deep-time carbonate system calculations. For this, the functions **carb**, **K0**, **K1**, **K2**, **Ks**, **Kw**, **Kb**, **Kspa**, and **Kspc** were modfied to account for the effect of seawater [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] on the dissociation constants of carbonic and boric acid. Their names are based on the original names, and suffixed with a ‘x’. In addition to the modified functions, *seacarbx* contains **MyAMI** that are tabulated parameters defining the temperature and salinity dependencies of the conditional equilibrium constants for [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] in the range 0–60 mM (from [Hain et al., 2015](http://dx.doi.org/10.1002/2014GB004986)).


## Prerequisites
*seacarbx* requires a base R installation (recommended with an installation of RStudio) and installed packages of *seacarb* and *dplyr*. You may install them at once with:

```{undefined}
install.packages(c("seacarb","dplyr"))
```

or separately with:

```{undefined}
install.packages("name of the package")
```

Then load the required libraries:
```{undefined}
library(seacarb)
library(dplyr)
```

## Usage
First, load the rda file, which contains the functions and the tabulated *MYAMI* data:
```{undefined}
load("seacarbx.rda")
```
The syntax is principally used the same way as for the original functions, except for the additional input parameters [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] (in mM), which are, as an example, called like this:
```{undefined}
carbx(flag=1, var1=8.1, var2=12e-6, S=35, T=25, ca=10, mg=53,...)
```

## Functions
- carbx() is the equivalent to the function carb(), and returns parameters of the seawater carbonate system, based on a given pair of known carbonate system variables.

- K0x() is the equivalent to the function K0(), and returns Henry’s constant mol/(kg/atm).

- K1x() is the equivalent to the function K1(), and returns the first dissociation constant of carbonic acid (mol/kg).

- K2x() is the equivalent to the function K2(), and returns the second dissociation constant of carbonic acid (mol/kg).

- Ksx() is the equivalent to the function Ks(), and returns the stability constant of hydrogen sulfate (mol/kg).

- Kwx() is the equivalent to the function Kw(), and returns the ion product of water (mol<sup>2</sup>/kg<sup>2</sup>)

- Kbx() is the equivalent to the function Kb(), and returns the dissociation constant of boric acid (mol/kg)

- Kspax() is the equivalent to the function Kspa(), and returns the solubility product of aragonite (mol/kg)

- Kspcx() is the equivalent to the function Kspc(), and returns the solubility product of calcite (mol/kg)

For more details, we refer here to the [**manual** of the original *seacarb* package](https://cran.r-project.org/web/packages/seacarb/seacarb.pdf).

## Citation
If you use seacarbx, please cite it with... will follow soon (with doi)...

but please also acknowledge the original works of the following:

Gattuso J.-P., Epitalon J.-M., Lavigne H. and Orr J. (2019): seacarb: seawater carbonate chemistry. R package version 3.2.12. http://CRAN.R-project.org/package=seacarb.

Hain, M. P., Sigman, D. M., Higgins, J. A. and Haug, G. H. (2015): The effects of secular calcium and magnesium concentration changes on the thermodynamics of seawater acid/base chemistry: Implications for Eocene and Cretaceous ocean carbon chemistry and buffering, Glob. Biogeochem. Cyc., 29(5), 517–533, http://doi.org/10.1002/2014GB004986.

<br><br>
