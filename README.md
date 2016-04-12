# IsoErrorAnalysis readme

###Date: 12/4/2016

###Author: Dr. Cheng Chang

###Version v1.0

## Goal
The tool IsoErrorAnalysis is developed and used to calculate the peptide isotopic abundance error in MS data.

##Description
It was used in the unpblished paper "A quantitative and in-depth survey of the isotopic abundance distribution errors in shotgun proteomics"

### Run IsoErrorAnalysis
1. It was developed on the platform of Microsoft Visual C++ 2010 and could be directly run on any Windows system (Microsoft Windows 10/8/7/2003/XP/2000, 64 bit or 32 bit version).
2. Open a CMD command window and run "IsoErrorAnalysis.exe -help" for detail information.

### Input files
1. MS data: the original Thermo raw files
2. peptide identification results (after QC): Three software tools are supported now.

- evidence.txt from MaxQuant
- pepXML file of PeptideProphet in Trans-Proteomic Pipeline (TPP)
- PepList file of PepDistiller developed in our lab.

### Output files
*.error.single file is the output file which contains 24 columns:

- peptide: peptide sequence
- protein: protein ID
- XIC index
- XIC total number
- MS1 scan number
- IsoNumber
- IsoID
- RankID
- MS1 RT
- Iso m/z
- Iso mass
- Iso mass error
- IsoExp: experimental isotopic intensity
- IsoTheoretical: theoretical isotopic intensity
- Iso BaseInt: isotopic baseline intensity
- S/N
- Error-Add: isotopic error using the additive model
- Error-Multi: isotopic error using the multiple model
- Error-Norm: isotopic error using the normalized model
- Goodness: goodness of fit between theoretical and experimental isotopic intensity profiles
- RIA deviation(%)
- RIA error(%)
- ModIntensity: Corrected isotopic intensity
- ModError: Corrected isotopic error

