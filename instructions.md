[[Home](index.md)] [[Installation](instructions.md)] [[RStudio Server](https://spintechit.com/bugsnet-demo-request/)] [[Vignettes](vignettes)]

# Installation instructions

## 1\. Install JAGS version 4.3.0

Go to the [Sourceforge](https://sourceforge.net/projects/mcmc-jags/) page.

Click on Files \> JAGS \> 4.x

Select your operating system and download JAGS-4.3.0, then install.

Note for MAC users: you may get a message saying that the app cannot be installed due to an unidentified developper. In that case, you have to go in your Security and Privacy settings to allow the installation.

## 2\. Install R version 3.6.1 (if R is already installed on your machine please make sure you update to 3.6.1)

Download and install base R from [CRAN](https://cran.r-project.org/).

Note: returning R users on Windows can quickly update R using
``` r
install.packages("installr")
installr::updateR(TRUE)
```

## 3\. Install Rstudio

Download and install the most recent version of RStudio Desktop (free version) from [RStudio](https://www.rstudio.com/products/rstudio/download).

## 4\. Install BUGSnet

Open RStudio and run

``` r
install.packages(c("remotes", "knitr"))
remotes::install_github("audrey-b/BUGSnet@v1.0.3", upgrade = TRUE, build_vignettes = TRUE)
```

If you are asked to install additional packages say yes to all.

## 5\. Check that BUGSnet works

If everything installed properly, the following [test script](testscript.txt) should run without error. Simply copy and paste to your RStudio console, then run.
