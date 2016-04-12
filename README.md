# IsoErrorAnalysis readme

###Date: 12/4/2016

###Author: Dr. Cheng Chang

###Version v1.1

## Goal
The tool IsoErrorAnalysis is developed and used to calculate the peptide isotopic abundance error in MS data.

## Description
1. It was used in the unpblished paper "A quantitative and in-depth survey of the isotopic abundance distribution errors in shotgun proteomics".
2. It was developed on the platform of Microsoft Visual C++ 2010 and could be directly run on any Windows system (Microsoft Windows 10/8/7/2003/XP/2000, 64 bit or 32 bit version).


## Usage

1. Open a CMD command window and run "IsoErrorAnalysis.exe -help" for detail information.
2. Usage: IsoErrorAnalysis.exe parameter1 parameter2 parameter3
	
	**example: IsoErrorAnalysis.exe c:\test\UPS2_A1.PepList c:\test\UPS2_A1.raw c:\test\UPS2_A1.output.txt**
	- parameter1: input peptide file, including (1) PepXML of PeptideProphet (2) evidence.txt of MaxQuant (v1.5.0.25 or higher) (3) PepList of PepDistiller
	- parameter2: input raw file: Thermo raw files are fully supported.
	- parameter3: output file full path


## Input file format
1. MS data: the original Thermo raw files
2. peptide identification results (after QC): Three software tools are supported now.

- evidence.txt from MaxQuant
- pepXML file of PeptideProphet in Trans-Proteomic Pipeline (TPP)
- PepList file of [PepDistiller](http://www.ncbi.nlm.nih.gov/pubmed/22623377) developed in our lab.

## Output file format
output file is the output file which contains 24 columns:

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

