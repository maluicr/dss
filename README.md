
# dss.c.64.exe to run with blockdss R package

dss.c.64.exe is a geostatistics and geosciences modeling stand-alone software developed at CERENA (https://cerena.pt/) research center. blockdss package (https://github.com/maluicr/blockdss) is a R-wrapper running block simulation algorithm from dss.c.64.exe.

# Download instructions

To run blockdss R package you first need to download the dss.c.64.exe. Follow these general steps:

1. create a folder called "input" in the working directory, 
2. copy the zipped dss.c.64.exe inside,
3. unzip the file into the same folder. 

You may execute these steps manually or from your R console directly, running the following code:

```r
# create folder input
inp <- "./input/"
if(!file.exists(inp)) dir.create(inp, recursive = TRUE)

# download dss.c.64.exe.zip from github
gitURL <- "https://github.com/maluicr/dss/raw/main/DSS.C.64.exe.zip"
utils::download.file(url = gitURL, destfile = file.path(inp, "DSS.C.64.exe.zip"))

# unzip file
unzip(file.path(inp, "DSS.C.64.exe.zip"), exdir = inp)
```

Please check your final folder structure, it should be as follows:

```
+---your R project (working directory)
|   \---input
|       \---dss.c.64.exe
```
