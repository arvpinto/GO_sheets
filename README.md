<h1 align="center">
Graphene Oxide sheet models (GAFF2-AIM) in GROMACS format
</h1><br>



- CP2K_OPT_GEO.xyz is the optimized coordinates from CP2K in XYZ format

- DDEC6_even_tempered_net_atomic_charges.xyz and DDEC_atomic_Rcubed_moments.xyz are the Chargemol output files with atomic charges and volumes

- GO_sheet_#_#.gro is the initial coordinates (produced with the MakeGraphitics library) in GROMACS format

- GO_sheet_#_#.top is the GAFF2-AIM topology in GROMACS format

- amber99sb-ildn.ff-modified/ is the amber99sb-ildn force field in GROMACS format, modified with GO sheet parameters (taken from https://www.bio2byte.be/acpype/)<br>

Note: Since these structures are periodic in the XY plane, they are meant to be used with the "periodic-molecules = yes" option in the *.mdp file of GROMACS.

<h1 align="center">
Don't forget to cite ;)
</h1><br>
Pinto, A.V. et al. (2022) “Development of Nanoscale Graphene Oxide Models for the Adsorption of Biological Molecules” The Journal of Physical Chemistry B. Soon available at: https://doi.org/10.1021/acs.jpcb.2c06037. 
