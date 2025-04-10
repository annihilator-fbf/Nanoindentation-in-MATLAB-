# Nanoindentation data processing with MATLAB
In this repository you can find live scripts and apps - designed with App Designer - to analyze and postprocess nanoindentation data of the iMicro, from KLA Instruments, and the FT-NMT04, from FemtoTools, nanoindenters. Contour plots and hardness/elastic modulus dependence with indentation depth are plotted.

## Table of contents
- [Scripts](#Scripts)
- [Apps](#Apps)
- [Data Requirements](#DataRequirements)
- [Author](#Author)
- [Acknowledgments](#acknowledgments)
- [License](#license)


## Scripts
- **contourplots_femtotools**: obtain hardness and modulus histograms and contour plots from tests performed with the FT-NMT04 nanoindenter. Additional pixel images of the maps is plotted to test accuracy with Machine Learning methods.
- **contourplots_imicro**: obtain hardness and modulus histograms and contour plots from tests - both 3D or 4D - performed with the iMicro nanoindenter. When working with 4D data, the desired depth to plot can be selected. Additional pixel images of the maps is plotted to test accuracy with Machine Learning methods.
- **reduced_modulus_converter**: enable the automatic conversion from reduced modulus to the elastic modulus, for only one value. This feature is useful when working with FT-NMT04, as it measures the reduced modulus
- **analyst_script**: it filters the data of single indents, calculate the mean and standard deviation of hardness/elastic modulus and plot the results as hardness/elastic modulus in function of penetration depth. Only valid for data from iMicro nanoindenter. Interpolation and "number of values" methods are included, which changes the plotting methodology.

## Apps
- **Contour plot app**: adapts the contourplots_femtotools and the contourplots_imicro scripts into one single app. iMicro and FT-NMT04 test data can be processed, and both histograms and contour plots can be obtained. Additional features include saving the filtered data, analyze histograms and contour plots in detail - which shows the images in a separate window -, and save them in low, medium or high quality, in a specific location on your computer.
- **Analyst app**: adapts the analyst_script in a user-friendly app. Hardness and elastic modulus dependence with indentation depth is plotted, with or without including the standard deviation for each indent. Also, the load-displacement curves of all the indents can be plotted. Filtered data can be saved in a specific location on your computer. Valid for iMicro and NanoXP test data.

## Data requirements
Errors may raise from unexpected test data format. Please, pay attention to the requirements stated below before using the scripts or apps:
- **iMicro**: 3D and 4D mapping lead to different columns in the excel file. In 3D mapping, HARDNESS, MODULUS, X POSITION and Y POSITION columns must be included. In 4D mapping, INDENT and DEPTH columns, in addition to the previously mentioned, must be included. When using the analyst script or app, LOAD, DEPTH, HARDNESS and MODULUS columns must be included.
- **FT-NMT04**: data must be in .txt format, including Hardness [MPa], Reduced Mod. [MPa], Pos Y [um] and Pos Z [um] columns.

## Author
[Francesc Barbera Flichi](https://www.linkedin.com/in/francescbarberaflichi/)
[CIEFMA - Center for Research in Structural Integrity, Reliability and Micromechanics of Materials](https://ciefma.upc.edu/es)

## Acknowledgements
Special thanks to [Laia Ortiz Membrado](https://github.com/laiaorme/High-speed-Nanoindentation-Data-Analysis-through-GMM-Clustering-and-Skew-Normal-Mixture.git) for actively contributing to the development of this work.

## License
This project is licensed under the [Creative Commons Attribution 4.0 International](LICENSE).  
You are free to use, modify and redistribute this project, provided the original author is properly credited.
