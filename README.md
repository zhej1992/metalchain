Instructions for using metalchain
The algorithm for searching metal chains from 3D APT map

1. Download and install the following programs:
  R (Download at https://cran.r-project.org/mirrors.html – choose any mirror link)
  RStudio (Download at https://www.rstudio.com/products/rstudio/download/)
  
2. Download and install the dplyr package in RStudio.

3. Go to https://github.com/. On right, click "Clone or Download" and then "Download Zip". This will download a local copy of the repository (folder) to your computer.

4. Modify the R script
  In metalchain.R, modify the working directory to the location of of the crystal+gaussian noise.csv file (line 6).
  Define the value of k for k-means algorithm (knum, line 7). The default is 400.
  Define the number of runs of the algorithm (run_times, line 5). The default is 5.
  
5. Run the metalchain.R file
  The dataset fed into the algorithm is a virtual data simulated by adding a Gaussian noise to the crystal structure of MOF-74.
  The input data contains the coordinate of each metal, the # of rod they belonging to and their positions on the rod.
  
6. Results will be saved in:
  the folder of each run, containing
    atom info.csv, the chain assignment for each metal, only metals belonging to the chains that passed the selection are listed;
    atom info_all.csv, the chain assignment for each metal,  metels assigned to all the chains are listed;
    error.csv, for each selected chain, the number of metals that are correctly assigned and the total number of metals;
    error_all.csv, for all the chains, the number of metals that are correctly assigned and the total number of metals;
  the working directory, containing
    error_stat, for each run, within the selected chains, the accuracy of metal assignment;
    error_all_stat, for each run, among all the chains, the accuracy of metal assignment.
    
  
