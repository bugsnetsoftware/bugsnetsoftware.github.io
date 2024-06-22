[[Home](index.md)] [[Installation](instructions.md)] [[Vignettes](vignettes)]

# Installation instructions

## 1\. Install JAGS

Go to the [Sourceforge](https://sourceforge.net/projects/mcmc-jags/) page.

Click on Files \> JAGS \> 4.x

After selecting your operating system, download and install the latest version of JAGS.

Note for MAC users: you may get a message saying that the app cannot be installed due to an unidentified developper. In that case, you have to go in your Security and Privacy settings to allow the installation.

## 2\. Install the latest version of R (if R is already installed on your machine please make sure you update to 4.4.0 or higher)

Download and install base R from [CRAN](https://cran.r-project.org/).

Note: returning R users on Windows can quickly update R using
``` r
install.packages("installr")
installr::updateR(TRUE)
```

## 3\. Install Rstudio

Download and install the most recent version of RStudio Desktop (free version) from [RStudio](https://www.rstudio.com/products/rstudio/download).

## 4\. Install Rtools

Open RStudio, copy and paste the code below in the console and hit Enter.

``` r
install.packages("pkgbuild")
pkgbuild::has_build_tools()
```

If asked to install the tools say Yes and proceed with the installation.

## 5\. Install BUGSnet

In RStudio, copy and paste the code below in the console and hit Enter.

``` r
install.packages(c("remotes", "knitr"))
remotes::install_github("audrey-b/BUGSnet@v1.1.2", upgrade = TRUE, build_vignettes = TRUE, dependencies = TRUE)
```

If you are asked to install additional packages say Yes to all.

## 6\. Check that BUGSnet works

If everything installed properly, the following [test script](testscript.txt) should run without error. Simply copy and paste to your RStudio console, then hit Enter.

# Troubleshooting

If you experience a message of the sort : 

ERROR: failed to lock directory ‘C:\Users\useruser\Documents\R\win-library\3.6’ for modifying
Try removing ‘C:\Users\useruser\Documents\R\win-library\3.6/00LOCK’

close RStudio and delete the 00LOCK file manually. Reopen RStudio and retry.
