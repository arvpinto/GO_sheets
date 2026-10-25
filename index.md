---
layout: default
---

<p><b>Atomistic models of graphene oxide sheets with different degrees of oxidation, built for molecular dynamics simulations of the adsorption of biological molecules.</b></p>

<p>Each model is a periodic sheet of about 15 &times; 15 nm with the same carbon backbone (8540 carbon atoms), decorated with hydroxyl and epoxy groups to reach a C/O ratio between 1.8 and 3.0. The atomic charges and non-bonded parameters (GAFF2-AIM) were derived from linear-scaling DFT calculations in CP2K, with DDEC6 charges and atomic volumes from Chargemol. The topologies are ready to use in GROMACS.</p>

---

<h2>I - Models</h2>

<p>The number in each folder name is the C/O ratio of the sheet (GO_18 has C/O = 1.8). The counts come from the files in each folder.</p>

| Model | C/O ratio | Atoms | Hydroxyl groups | Epoxy groups | Files | DFT and parameter files |
| :--- | ---: | ---: | ---: | ---: | :--- | :--- |
| GO_18 | 1.8 | 15&nbsp;597 | 2312 | 2433 | <a href="https://github.com/arvpinto/GO_sheets/tree/main/GO_18" target="_blank">GO_18</a> | <a href="https://zenodo.org/record/7323314" target="_blank">Zenodo</a> |
| GO_20 | 2.0 | 14&nbsp;964 | 2154 | 2116 | <a href="https://github.com/arvpinto/GO_sheets/tree/main/GO_20" target="_blank">GO_20</a> | <a href="https://zenodo.org/record/7323388" target="_blank">Zenodo</a> |
| GO_22 | 2.2 | 14&nbsp;352 | 1930 | 1952 | <a href="https://github.com/arvpinto/GO_sheets/tree/main/GO_22" target="_blank">GO_22</a> | <a href="https://zenodo.org/record/7323436" target="_blank">Zenodo</a> |
| GO_24 | 2.4 | 13&nbsp;827 | 1726 | 1833 | <a href="https://github.com/arvpinto/GO_sheets/tree/main/GO_24" target="_blank">GO_24</a> | <a href="https://zenodo.org/record/7323444" target="_blank">Zenodo</a> |
| GO_26 | 2.6 | 13&nbsp;439 | 1614 | 1671 | <a href="https://github.com/arvpinto/GO_sheets/tree/main/GO_26" target="_blank">GO_26</a> | <a href="https://zenodo.org/record/7323454" target="_blank">Zenodo</a> |
| GO_28 | 2.8 | 13&nbsp;122 | 1532 | 1518 | <a href="https://github.com/arvpinto/GO_sheets/tree/main/GO_28" target="_blank">GO_28</a> | <a href="https://zenodo.org/record/7323465" target="_blank">Zenodo</a> |
| GO_30 | 3.0 | 12&nbsp;819 | 1432 | 1415 | <a href="https://github.com/arvpinto/GO_sheets/tree/main/GO_30" target="_blank">GO_30</a> | <a href="https://zenodo.org/record/7323484" target="_blank">Zenodo</a> |

<p>The Zenodo records hold the files from the linear-scaling DFT and non-bonded parameter calculations of each model.</p>

<h2>II - Files</h2>

<p>Each model folder contains:</p>

- <p><b>GO_sheet_#_#.gro</b>: the initial coordinates (built with the MakeGraphitics library) in GROMACS format.</p>
- <p><b>GO_sheet_#_#.top</b>: the GAFF2-AIM topology in GROMACS format.</p>
- <p><b>CP2K_OPT_GEO.xyz</b>: the coordinates optimized with CP2K, in XYZ format.</p>
- <p><b>DDEC6_even_tempered_net_atomic_charges.xyz</b> and <b>DDEC_atomic_Rcubed_moments.xyz</b>: the Chargemol output files with the atomic charges and volumes.</p>

<p>The <a href="https://github.com/arvpinto/GO_sheets/tree/main/amber99sb-ildn.ff-modified" target="_blank">amber99sb-ildn.ff-modified</a> folder holds the amber99sb-ildn force field in GROMACS format, modified with the graphene oxide sheet parameters (taken from <a href="https://www.bio2byte.be/acpype/" target="_blank">ACPYPE</a>).</p>

<h2>III - Using the models in GROMACS</h2>

<p>The sheets are periodic in the XY plane, so the bonds across the box edges are part of the topology. Use them with the following option in the *.mdp file:</p>

<pre>
periodic-molecules = yes
</pre>

<p>The coordinate files define a box of 14.937 &times; 14.870 &times; 8.000 nm with the sheet in the XY plane.</p>

<h2>IV - Citation</h2>

<p>If you use these models, please cite:</p>

<p align="center">Pinto, A. V.; Ferreira, P.; Fernandes, P. A.; Magalh&atilde;es, A. L.; Ramos, M. J. Development of Nanoscale Graphene Oxide Models for the Adsorption of Biological Molecules. <i>J. Phys. Chem. B</i> <b>2023</b>, 127 (2), 557-566. <a href="https://doi.org/10.1021/acs.jpcb.2c06037" target="_blank">https://doi.org/10.1021/acs.jpcb.2c06037</a></p>

<pre>
@article{Pinto2023GO,
  author  = {Pinto, Alexandre V. and Ferreira, Pedro and Fernandes, Pedro A. and Magalh{\~a}es, Alexandre L. and Ramos, Maria J.},
  title   = {Development of Nanoscale Graphene Oxide Models for the Adsorption of Biological Molecules},
  journal = {The Journal of Physical Chemistry B},
  year    = {2023},
  volume  = {127},
  number  = {2},
  pages   = {557--566},
  doi     = {10.1021/acs.jpcb.2c06037}
}
</pre>
