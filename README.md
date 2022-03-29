
# dss.c.64.exe to run with blockdss R package

dss.c.64.exe is a geostatistics and geosciences modeling stand-alone software. It has several functions to manipulate 2d-3d data as well as provide univariate and multivariate analysis. The software has been developed in CERENA (https://cerena.pt/) research center. blockdss package (https://github.com/maluicr/blockdss) is a R-wrapper for running block simulation algorithm from dss.c.64.exe. 

# Download instructions

To run blockdss package you first need to download the dss.c.64.exe. First create a folder called "input" in the working directory, copy the zipped dss.c.64.exe inside and unzip the downloaded file into the same folder. The final folder structure should be as follows:

```
+---your R project
|   \---input
|       \---dss.c.64.exe
```

You can copy the zipped file into the input folder from your R console directly, using the following code (please remember to unzip the file after running the code below):

```
# create folder input
inp <- "./input/"
if(!file.exists(inp)) dir.create(inp, recursive = TRUE)

# download dss.c.64.exe.zip from github
gitURL <- "https://github.com/maluicr/dss/raw/main/DSS.C.64.exe.zip"
utils::download.file(url = gitURL, destfile = paste0(inp, "DSS.C.64.exe.zip"))
```
