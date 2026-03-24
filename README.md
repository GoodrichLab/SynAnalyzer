# README
![SynAnalyzer logo showing an inner hair cell on a coordinate axes with a magnifying glass highlighting type I spiral\
ganglion neuron terminals at the basoleratl surface of the inner hair cell.](/Assets/Logos/0_SynAnalyzerLogo_Small.png)

## Authors and Acknowledgement
This repository and its content were created and will be maintained by Joy Franco. However, all authors of the accompanying
manuscript contributed their ideas for how the code should function and what features would be necessary. For that reason,
please cite our manuscript when referring to this repository. Currently this manuscript can be cited via the Biorxiv preprint (link below).
Additional citation information will be provided at the time of publication.

Thumbnail arrays of synapses and synapse scoring process was inspired by Liberman, Wang, and Liberman 2011 (DOI:10.1523/JNEUROSCI.3389-10.2011).

## Project Description
This repository contains the source code for the Franco,...,Goodrich 2025 preprint, currently under revision at Nature Communications.
The initial version of the manuscript is viewable on Biorxiv at https://www.biorxiv.org/content/10.1101/2025.08.27.672747v1.
This code was used to generate the synapse and terminal arrays described in this manuscript. These arrays are composed of
thumbnail sum intensity projection images (2 um x 2 um), centered at specified xyz coordinates. The code walks the user through
scoring each of these thumbnail images to manually determine if there is a synapse at this position and whether it appears
to colocalize with tdTomato (tdT) fluorescence signal.

Potential users of this code are strongly urged to read this manuscript first before attempting to run this code to ensure
they understand the full image analysis pipeline.

## System Requirements
This source code is relatively basic and is expected to run on most standard computers. The only expected limitation depends
on the size of the micrographs being analyzed and the number of thumbnails that will need to be generated. However, this
source code was only tested on a MacBook Pro and future users may need to optimize the code for their own usage.
The details of operating system, software, and environment in which this source code was developed is provided below:
* Hardware
   * MacBook Pro, 2 TB Hard drive space
   * 2.4 GHz 8-Core Intel Core i9
   * 64 GB 2667 MHz DDR4
   * Graphics: AMD Radeo Pro 5500 M 8 GB, Intel UHD Graphics 630 1536 MB
* Operative System: macOS Monterey Version 12.4
* Python Environment:
   * Python 3.8.17
   * Key packages (beyond standard Python environments):
      * os, numpy, pandas, glob, xlrd, openpyxl, datetime, matplotlib, seaborn, math, scipy
* ImageJ version:
   * ImageJ2
   * Version: 2.14.0/1.54f
   * Build: c89e8500e4     

## Installation Instructions
Since this source code is a set of Python notebooks and ImageJ macros, there is no installation required.
Python notebooks can be opened in a cloud-based platform such as Google Colab, which do not require that the user setup
a dedicated environment. The ImageJ macros do not need to be installed as plugins and can simple be opened in ImageJ
and run from within the program. For users just getting started with ImageJ it may be best to download ImageJ as FIJI,
which includes several useful plugins. Setting up the tools necessary to run the Demo should take less than one hour.

## Demo
Users are strongly encouraged to run the demo code with the provided test images prior to any attempts to use this
code for their own data sets. It is largely expected that users will need to modify this code in order for it to
work with their own data. To run this demo, proceed with the steps below using the User Guide as a reference:
1. Clone this repository (refer to GitHub documentation for additional details)
2. Setup their local Python environment (refer to Python community resources for additional details)
3. Setup their local ImageJ software (refer to ImageJ documentation for additional details)
4. Save the demo files to your local hard drive. While it may be possible to run this analysis with the files stored on a server, this approach was not tested.
5. Update the filepath names in the code to ensure that all inputs are drawn from the appropriate location and that all
outputs are saved in a known location.
6. Follow the steps provided in the User Guide

## Expected Runtime
The exact runtime for this code will depend largely on the size of the images being analyzed and the number of xyz coordinates for which thumbnails need to be generated. For reference, the Demo image set includes an image that is 640 MB and has a total of 513 xyz coodinates. On the system described above it took approximately 30 minutes to generate all thumbnails and arrays for this image. It is expected that an additional 20 minutes is needed to analyze/score these thumbnails. The duration required scales relatively linearly with the number of xyz coordinates on this operating system such that an image of the same size with half the xyz coordinates can be run in 15 minutes with an additional 10 minutes needed for analysis.

## Instructions for use
Please refer to the steps above under the "Demo" heading before attempting to use this code for a custom dataset.
Users are also strongly encouraged to review the User Guide, which includes a psuedocode description of the codes functionality.
