
# 'seacarbx' Manual

## Description
*seacarbx* is a **seacarb** e**x**tension written in R, which enables to use *seacarb* ([Gattuso et al., 2019](http://CRAN.R-project.org/package=seacarb)) for deep-time carbonate system calculations or for culturing studies carried out in seawater with modified [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>]. For this, the functions **carb**, **K0**, **K1**, **K2**, **Ks**, **Kw**, **Kb**, **Kspa**, and **Kspc** were modfied to account for the effect of seawater [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] on the dissociation constants of carbonic and boric acid. Their names are based on the original names, and suffixed with a ‘x’. In addition to the modified functions, *seacarbx* contains **MyAMI** that are tabulated parameters defining the temperature and salinity dependencies of the conditional equilibrium constants for [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] in the range 1–60 mM (from [Hain et al., 2015](http://dx.doi.org/10.1002/2014GB004986), and revised by [Hain et al., 2018](https://doi.org/10.1002/2018GB005931)), as well as a function for bilinear interpolation.


## Prerequisites
*seacarbx* requires a base R installation (recommended with an installation of RStudio) and an installation of the package *seacarb*. You may install it with:

```{undefined}
install.packages("seacarb")
```

Then load the required library:
```{undefined}
library(seacarb)
```

## Usage
First, load the rda file, which contains the functions and the tabulated *MYAMI* data:
```{undefined}
load("~/path-to-your-directory/seacarbx.rda")
```
The syntax is basically the same as for the original functions, except the additional input parameters [Mg<sup>2+</sup>] and [Ca<sup>2+</sup>] (in mol/L), which are, as an example, called like this:
```{undefined}
carbx(flag=1, var1=8.1, var2=12e-6, S=35, T=25, ca=10.2821e-03, mg=52.8171e-03,...)
```
Every time that the input variables [Ca<sup>2+</sup>] and/or [Mg<sup>2+</sup>] are changed in the seacarbx functions, the bilinear interpolation function *lookup_fn* is called automatically, which computes accurate parameters from the MyAMI lookup table.

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

<br><br>
