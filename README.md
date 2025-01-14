# FrozenChicken

### Goal 
Promote, simplify, and ease the meta-analysis of chicken microarray data.

### Contents
This R package, named *affyChickGenomeArrayfrmavecs*, was automatically created by package frmaTools version 1.34.0.  
It contains the frozen vectors for commercially available (in situ oligonucleotide) Chicken microarray chips.   
**About the platform used** | Affymetrix Chicken Genome Array | GEO platform id: [GPL3213](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL3213).

### Citation
This package contents are explained, together with usage case examples, in the following publication:   

Isabel Duarte^, Marta Liber^, Ramiro Magno & Raquel P. Andrade. *FrozenChicken: Promoting the meta-analysis of chicken microarray data*. 2021. BioRxiv. https://doi.org/10.1101/2021.02.25.432894. (^Equal contribution)

The code is also available in zenodo: https://doi.org/10.5281/zenodo.3765944


### Installation

If you do not have the package `remotes` install it first:

```R
install.packages("remotes")
```

Then install the R package `FrozenChicken` directly from GitHub:

```R
# Install the package from GitHub
remotes::install_github("iduarte/FrozenChicken")
```

Then you can load the library named `affyChickGenomeArrayfrmavecs` and use these frozen vectors to normalize chicken microarray data from different experiments:

```R
library(affyChickGenomeArrayfrmavecs)
```

### Details 
**Motivation** | Public repositories like Gene Expression Omnibus (GEO) and ArrayExpress currently contain
11.661 datasets from *Gallus gallus* representing a wealth of data that can be explored to
answer fundamental questions and generate new hypothesis. However, since these data come
from different experiments, their meta-analysis requires proper normalization to deal with the
technical biases and batch effects before making the data comparable for statistical analysis.  
An effective method for such normalization is the single-array pre-processing provided by the
**Frozen Robust Multiarray Analysis - fRMA** (McCall MN, et al. Biostatistics. 2010). This method uses frozenRMA vectors pre-computed
from great amounts of available data for the same microarray chip, accounting for the
aforementioned biases. However, such frozen vectors are only available for some organisms
(most notably, human, mouse, zebrafish, and fluit-fly among many others), but not for *Gallus gallus*,
hence delaying the proper meta-analysis of chicken transcriptomics datasets.   

Here, we present our R package - *affyChickGenomeArrayfrmavecs* - containing the chicken frozen
vectors that can be directly plugged-in to any fRMA chicken microarray analysis, without having to first generate the required frozen parameters.  

**Methods** | We used 118 Geo DataSets from Affymetrix Chicken Genome Array platform and
randomly selected 4 arrays per batch (**Batch number = 118 and Batch size = 4**). This gives us a powerful set of **472** chips from which to compute the frozen parameters.  
These results have been automatically put into an R package using the frmaTools (version 1.34.0) and made freely available here for the benefit of the chicken research community.

### Authors and Funding
This scientific work was developed by Marta Liber, Isabel Duarte, Ramiro Magno, and Raquel P. Andrade.   
The work was funded by FCT, Portugal (grant PTDC/BEX-BID/5410/2014) and Research Center Grant UID/BIM/04773/2013 CBMR 1334.

