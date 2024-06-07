## Cavatica Tips and Tricks

Tips and tricks to be aware of for tech support:

### Make sure project has network access and advise switching over if it doesn't.
We almost always need network access for installing other packages, but it seems no-network is the default when creating a new project, leading to some issues that I encountered and might be especially confusing for other people.

![image](https://github.com/nf-osi/tutorials/assets/32753274/71348891-69b8-4e9e-b0f3-f9e4b753edb0)

### Be aware that installed packages are not persistent between sessions without some additional steps.
That is, you'll often start a session and install a package that you need, do some work, and then stop the session.
Stopping the session leads to a "saving" job that only saves the analysis files and _not_ the packages you installed.
The next session will require reinstalling that package because it won't be able to be loaded with `library(somepackage)` (which is what you might have expected).
This will be especially annoying if it was required to install a lot of additional packages that needed compilation.

Since Data Studio requisitions/utilizes a new cloud computing resource with every initialization, it deletes all the data written into system folders. 
This does mean that all installed R or Python packages will normally be deleted if they are installed in the default manner.

In order to avoid this, it is possible to install packages into the "workspace" folder instead (and then load them from that location when needed).
 
For example, the installation script for R packages from within an R session would look like the following:

```
# library path
libpath <- "/sbgenomics/workspace/rpkgs"
if (!dir.exists(libpath)) dir.create(libpath)
# set library path
.libPaths(libpath)
install.packages("ggsci")
```

This will create a folder named "rpkgs" under the workspace folder and install the packages at that location.
 
Bioconductor packages installed via BiocManager and GitHub packages installed via devtools can be installed with exactly the same command as before without modification (the library path would be a "global" setting for this R session).
 
You can load the installed packages from this folder when you re-initialize the R Data Studio session via the following:
``` 
libpath <- "/sbgenomics/workspace/rpkgs/"
.libPaths(libpath)
library("ggsci")
```
