# SlopeWeightedEccentricity

[![View SlopeWeightedEccentricity.m on File Exchange](https://www.mathworks.com/matlabcentral/images/matlab-file-exchange.svg)](https://uk.mathworks.com/matlabcentral/fileexchange/96509-slopeweightedeccentricity-m)

(c) Gabriella Alodia &#8212; 2021

<tt>SlopeWeightedEccentricity.m</tt> is a Matlab-based geomorphometric algorithm to obtain the numerical description of both magmatic and tectonic crust in a slow-spreading ridge through a series of calculation based on the distribution of the azimuth and plunge observed in the seafloor morphology.

<b>Input</b>
1. A gridded shipborne multibeam bathymetry (depths in metres) in *.xyz format (here: <tt>'Input_Bathymetry_15s.xyz'</tt>)
2. A Laplacian-of-Gaussian (LoG) mask created from the bathymetry using a third party software/tool in *.xyz format (here: <tt>'Input_LoG_mask.xyz'</tt>)

![Input](https://github.com/alodiaga/SlopeWeightedEccentricity/blob/main/Images/Input_images.png)

If the LoG mask is not going to be used, we suggest creating a grid with the size and region of the gridded shipborne multibeam bathymetry and assigning the number '1' to all the cells (a 'no mask' example named <tt>'Input_no_mask.xyz'</tt> is provided) OR by exempting all the lines with the associated 'mask' from this script.

<b>Output</b>
1. Terrain eccentricity (here: <tt>'Output_eccentricity.xyz'</tt>)
2. Weight matrix: 1-sin(slope) (here: <tt>'Output_weight.xyz'</tt>)
3. SWE: Slope-weighted eccentricity (here: <tt>'Output_SWE.xyz'</tt>)
4. Masked SWE (here: <tt>'Output_SWE_masked.xyz'</tt>)

![Output](https://github.com/alodiaga/SlopeWeightedEccentricity/blob/main/Images/Output_images.png)

Each output is exported in *.xyz format. The resulting *.xyz data can be converted into *.grd using the <tt>xyz2grd</tt> function in GMT (http://gmt.soest.hawaii.edu/doc/5.3.2/xyz2grd.html)

The shipborne multibeam bathymetry data sample is downloaded from the GMRT MapTool (https://www.gmrt.org/GMRTMapTool/) with the extent <tt>xmin/xmax/ymin/ymax</tt> of <tt>-46/-44/12.5/13.15</tt>

Preprint Citation:

Alodia, G., Green, C., McCaig, A., & Paton, D. (2020). Slope-Weighted Eccentricity: Automatic Terrain Classification of Atlantic Ocean Crust. ESSOAr: Earth and Space Science Open Archive. [https://doi.org/10.1002/essoar.10502634.1]

Full paper currently in preparation.
