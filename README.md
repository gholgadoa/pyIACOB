# Introduction to pyIACOB (v1.00):

This package has been created mainly to manipulate data from the IACOB spectroscopic
database (see Simón-Díaz et al. 2011), which currently gathers high-resolution spectra
(R~25000-85000) of Galactic OBA stars taken with the FIES@NOT2.5m and HERMES@MERCATOR1.2m
facilities at the Roque de los Muchachos Observatory, and FEROS@ESO2.2m at La Silla
Observatory.

The main scientific goal pursued by the IACOB project is to use these data to perform
single snap-shot and multi-epoch quantitative spectroscopic analyses providing a complete
empirical overview of the physical properties of these stars.

To achieve this goal, several programs (written in IDL) have been developed by the team
of collaborators (mainly at the Instituto de Astrofísica de Canarias). This package has
modules that facilitate the use these programs either by preparing their input data or by
creating summary tables with their results. The current list of supported programs are:

- IACOB-Broad (S. Simón-Díaz & A. Herrero 2013)
- MAUI (M.A. Urbaneja 2017)

Created by: Abel de Burgos

# Python Requirements:

- Python 3.8.2 or above
- numpy 1.20.2
- scipy 1.6.2
- random 1.2.2
- astropy 4.2.1
- astroquery 0.4.3
- matplotlib 3.3.4
- progressbar 2.5

# Other Requirements:

Access to the spectroscopic data stored locally. Available spectra from the IACOB
database can be downloaded from http://research.iac.es/proyecto/iacob/iacobcat/

# Installation:

1. Modify the paths in *paths.txt* to match with your working directories:
  - *main* path must point to the location of your working directory.
  - *data* path must point to the directory where the spectra are located.
  - *maui*, *ib* paths to the respective directories of each of these programs.
  - *mist* path must point to where the MIST isochrones/tracks are located.

2. Create the main working sub-folders that are needed in your working directory:
  - lists/lines/
  - plots/
  - tables/
  - tmp/

3. Put the included file *ALL_OBs_n4+.txt* inside the tables folder.

NOTE: For mist.py to work, drop me an email and I will send you the needed files (~600mb)

# Overview of the modules:

- db.py contains functions to search spectra or create master tables within the IACOB
  database, to search tables and lists and make queries in Simbad.

- spec.py contains functions that manipulate an input spectrum and plot it.

- RV.py contains functions to calculate the radial velocity offset via cross-correlation
  or via input list of lines. It also allows to create RV curves.

- RVEWFW.py contains functions to interactively or automatically obtain Equivalent Widths,
  Full Widths, and Radial Velocities for a given input of stars.

- IACOBBroad.py contains functions which helps the user to generate output and input
  tables for IACOB-Broad.

- maui.py contains functions which helps the user to generate output and input tables for
  MAUI, with some additional features regarding the analysis of the results.

- mist.py contains functions to retrieve either an evolutionary track or an isochrone.

- tools.py contains utility functions which could also be interested.

# Sending corrections / comments:

- Preferably via pull requests / issues within the GitHub framework
- Directly by email at abel.burgos@iac.es

# Acknowledgments:

Sergio Simón-Díaz
