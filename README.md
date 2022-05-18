# GrapeTree

This is forked version of GrapeTree which will only contain the scripts responsible for drawing trees on the client-side. With this version, there won't be a need for hosting a server to run GrapeTree, and the software can be tailored towards your specific application.


To use GrapeTree visualization tools include the scripts found in the js folder to your project and then follow the [documentation](https://achtman-lab.github.io/GrapeTree/documentation/developer/index.html).

## Minimum running example of current version

Include the js files in an appropiate folder where you keep your js scripts.
Then to initialize, include the following snippet in your html:
```html
<script src="js/jquery-1.9.1.min.js"></script>
<script src="js/d3.min.js"></script>
<script src="js/base_tree.js"></script>
<script src="js/d3_m_tree.js"></script>
<div id="tree-holder" style="width:400px;height:400px;"></div>
<script>
var tree = new D3MSTree("tree-holder", data);
</script>
```





### Documentation

Developers may wish to look at the [JavaScript documentation](https://achtman-lab.github.io/GrapeTree/documentation/developer/index.html) (JSDoc). Here you can find the functionalities of the scripts which produce the trees.


For detailed help please see: [http://enterobase.readthedocs.io/en/latest/grapetree/grapetree-about.html](http://enterobase.readthedocs.io/en/latest/grapetree/grapetree-about.html)



For a formal description, please see the accepted manuscript in Genome Research: [https://doi.org/10.1101/gr.232397.117
](https://doi.org/10.1101/gr.232397.117
)

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

