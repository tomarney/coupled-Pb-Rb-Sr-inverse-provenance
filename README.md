# Inverse provenance via Rb–Sr ages and clustering of coupled Pb isotopes

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.14903540.svg)](https://doi.org/10.5281/zenodo.14903540)&nbsp;&nbsp;[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tomarney/coupled-Pb-Rb-Sr-inverse-provenance/HEAD)

Supplementary code to the paper 
> &nbsp;\
> **West Antarctic subglacial geology distinguished by coupled Pb isotopes and Rb–Sr ages in ice-rafted feldspars**
> 
> Arney, Thomas [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0003-4380-4079),
> Hillenbrand, Claus-Dieter [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0003-0240-7317),
> Belgrano, Thomas [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0003-2160-1895),
> Milton, J. Andy [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0003-4245-5532),
> Siddoway, Christine Smith [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0003-0478-6138),
> Foster, Gavin [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0003-3688-9668),
> Wilson, Paul [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0001-6425-8906),
> Wellner, Julia [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0002-6807-8635),
> Bohaty, Steve [![ORCID iD icon](https://orcid.org/sites/default/files/images/orcid_16x16.png)](https://orcid.org/0000-0002-1193-7398)\
> &nbsp;

This is an archive of the data processing code used in the above article, not the data. **Full results are depositied with UK Polar Data Centre**. Only enough data to reproduce the processing is given here, to avoid duplication. Please refer to (and/or cite) the Polar Data Centre record for the final data. Please cite the peer-reviewed article for the approach and methods, rather than the Zenodo record.

Contents:

- [`RbSr_isotopes_DRS.py`](RbSr_isotopes_DRS.py) is the Data Reduction Scheme used in iolite for the Rb–Sr analysis.

- [`data/`](data) contains input CSV files needed for the processing, including measurement data output by iolite and previously published data.

- [`1 Pb clustering.ipynb`](<1 Pb clustering.ipynb>) is the code used to preprocess the Pb isotope data, generate the training dataset, and cluster it.

  - This saves the resultant models `Pb_RobustScaler.obj` and `Pb_GMM.obj` to enable re-use for classification in the `2 Pb classification.ipynb` notebook without running the `1 Pb clustering.ipynb` notebook again.

- [`2 Pb classification.ipynb`](<2 Pb classification.ipynb>) uses the fitted model to classify the full Pb isotope dataset.

- [`3 Rb-Sr process.ipynb`](<3 Rb-Sr process.ipynb>) carries out matrix-matched calibration of the Rb–Sr data, age calculations, uncertainty propagation, and validation.

## Running the code

The easiest way to replicate the processing is by running the notebooks in the online [Binder](https://mybinder.org/v2/gh/tomarney/coupled-Pb-Rb-Sr-inverse-provenance/HEAD).