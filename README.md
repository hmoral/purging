# Simulations for the manuscript
**Dussex, Morales, Grossen, Dalen & van Oosterhout Purging and accumulation of genetic load in conservation**

## Methods
The model simulated an exome of 10,000 genes of 500 bp each with a recombination rate r=1e-4 (no recombination within genes), and a per base mutation rate m=5e-8. Deleterious selection coefficients (s) were taken from a gamma distribution (mean=-0.05 and shape=0.5) with a tail of 5% of lethal mutation and negative relationship between selection and dominance coefficients (h), following Kardos et al. (2022). We simulated an ancestral population at equilibrium (Ne=10,000) undergoing a severe decline (Ne=10 for 20 generations), followed by a recovery (Ne=2,000 for 20 generations). We calculated the total genetic load and its components, realized and masked load, following the formulas from Bertorelle et al. (2022).

## Code dependencies:
- SLiM3 (https://messerlab.org/slim/)
- Parallel for bash

### test run
A single replicate for a small run with an ancestral population size Ne=1000

```slim -d "K=1000" -d "outPath='./'" -d "outName='out_test'" -d "del_mut=10000" purging_WFnonWF_uncondLoad_exome.slim```
