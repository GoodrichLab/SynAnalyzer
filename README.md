# README
![SynAnalyzer logo showing an inner hair cell on a coordinate axes with a magnifying glass highlighting type I spiral\
ganglion neuron terminals at the basoleratl surface of the inner hair cell.](/Assets/SynAnalyzerLogo_Small.png)

## Project Description
This repository contains the source code for the Franco et al manuscript, currently under revision at Nature Communications.
The initial version of the manuscript is viewable on Biorxiv at https://www.biorxiv.org/content/10.1101/2025.08.27.672747v1.
This code was used to generate the synapse and terminal arrays described in this manuscript. These arrays are composed of
thumbnail maximum projection images (1.5 um x 1.5 um), centered at specified locations. The code walks the user through
scoring each of these thumbnail images to manually determine if there is a synapse at this position and whether it appears
to colocalize with tdTomato (tdT) fluorescence signal.\

Potential users of this code are strongly urged to read this manuscript first before attempting to run this code to ensure
they understand the full image analysis pipeline.

## System Requirements
This source code is relatively basic and is expected to run on most standard computers. The only expected limitation depends
on the size of the micrographs being analyzed and the number of thumbnails that will need to be generated. However, this
source code was only tested on a MacBook Pro and future users may need to optimize the code for their one usage.\
The details of operating system, software, and environment in which this source code was developed is provided below:\
* Hardware
  * MacBook Pro, 2 TB Hard drive space
  * 2.4 GHz 8-Core Intel Core i9
  * 64 GB 2667 MHz DDR4
  * Graphics: AMD Radeo Pro 5500 M 8 GB, Intel UHD Graphics 630 1536 MB
* Operative System: macOS Monterey Version 12.4
* Python Environment    

## Installation Instructions
Since this source code is a set of Python notebooks and ImageJ macros, there is no installation required.
Python notebooks can be opened in a cloud-based platform such as Google Colab, which do not require that the user setup
a dedicated environment. The ImageJ macros do not need to be installed as plugins and can simple be opened in ImageJ
and run from within the program. 
