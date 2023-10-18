# hydroclimatic-hazards-hotspots
This repository contains code used to test a framework to map hotspots of floods, heat waves and droughts in Sweden.
The order of usage is heat waves, droughts and floods. For each hazard, the observed data is downloaded from SMHI's API.
Then environmental data is interpolated in a grid (temperature and monthly precipitation) to obtain the indices HWI, SPI, SPEI, DFI.
The generated netCDF files were not included due to their size, please contact me if you would like to download them.
After the indices are computed, maps of hotspots and trends are generated using percentiles of accumulated intensities in a year or decade.
The results are validated against a list of documented hazards using binary classification metrics such as true positive rate, false positive rate, accuracy and F-Score.
Then the compound effects are assessed calculating return periods and the likelihood multiplication factor for pairs of hazards.
