# GrapeTree

This is forked version of GrapeTree which will only contain the content responsible for drawing trees on the front-end. With this version, there won't be a need for hosting a server with a specific version of GrapeTree, and the software can be tailored towards your specific application.



**For detailed help please see: [http://enterobase.readthedocs.io/en/latest/grapetree/grapetree-about.html](http://enterobase.readthedocs.io/en/latest/grapetree/grapetree-about.html)**

**For a formal description, please see the accepted manuscript in Genome Research: [https://doi.org/10.1101/gr.232397.117
](https://doi.org/10.1101/gr.232397.117
)**





### Documentation

Developers may wish to look at the [JavaScript documentation](https://achtman-lab.github.io/GrapeTree/documentation/developer/index.html) (JSDoc).

There you can find the functionalities of the scripts which produce the trees.



## Inputs
#### profile
The profile file is a tab-delimited text file.

Follow an example here: https://github.com/achtman-lab/GrapeTree/blob/master/examples/simulated_data.profile
```
#Strain	Gene_1	Gene_2	Gene_3	Gene_4	Gene_5	Gene_6	Gene_7	...
0	1	1	1	1	1	1	1	...
1	1	1	1	1	1	1	1	...
2	1	2	2	2	2	2	2	...
...
```
The first row is required and represents column labels. It has to start with a '#'. Collumn labels that start with a '#' are treated as comments and will not be used in downstream analysis. The first column needs to be unique identifiers for strains.
Each of the remaining rows presents a different strain.

Use '-' or '0' to represent missing alleles. 

#### Aligned FASTA
An aligned FASTA file contains multiple sequences of the same length in FASTA format. Many sequence alignment tools, e.g., MAFFT and MUSCLE, use FASTA as a default format for their outputs. 

Find an example here: http://wwwabi.snv.jussieu.fr/public/Clustal2Dna/fastali.html

Note that GrapeTree supports only p-distance for the moment.  

#### metadata
The metadata file is either a tab-delimited or a comma-delimited text file. This is only used for tree presentation in the standardalone version.

Follow an example here: https://github.com/achtman-lab/GrapeTree/blob/master/examples/simulated_data.metadata.txt
```
ID	Country	Year
0	China	1983
1	China	1984
...
```
The first row is required and describes the labels of the columns. If a column labeled with "ID" presents, it will be used to correlate metadata with profiles, otherwise the first column will be used.

## outputs
#### tree
The tree is described in NEWICK format. https://en.wikipedia.org/wiki/Newick_format

#### distance matrix
Use the option '--method distance' to generate a distance matrix without calculating the tree.
The matrix is presented in PHYLIP format. http://evolution.genetics.washington.edu/phylip/doc/distance.html


## License
Copyright Warwick University This program is free software: you can
redistribute it and/or modify it under the terms of the GNU General Public
License as published by the Free Software Foundation, either version 3 of the
License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but without
any warranty; without even the implied warranty of merchantability or fitness
for a particular purpose. See the GNU General Public License for more
details.

You should have received a copy of the GNU General Public License along with
this program. If not, see <http://www.gnu.org/licenses/>.

## External programs
Detailed information for the standard NJ implemented in FastME V2: http://www.atgc-montpellier.fr/fastme/

## Citation
EnteroMSTree - GrapeTree has been formally accepted by Genome Research. Please use the citation:

Z Zhou, NF Alikhan, MJ Sergeant, N Luhmann, C Vaz, AP Francisco, JA Carrico,
M Achtman (2018) "GrapeTree: Visualization of core genomic relationships among 
100,000 bacterial pathogens", Genome Res; doi:
[https://doi.org/10.1101/gr.232397.117](https://doi.org/10.1101/gr.232397.117)

