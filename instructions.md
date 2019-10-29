[[Home](index.md)] [[Installation](instructions.md)] [[RStudio Server](https://spintechit.com/bugsnet-demo-request/)] [[Vignettes](vignettes)]

# Installation instructions

## 1\. Install JAGS

Go to the [Sourceforge](https://sourceforge.net/projects/mcmc-jags/) page.

Click on Files \> JAGS \> 4.x

Select your operating system and download JAGS-4.3.0, then install.

## 2\. Install R

Download and install the most recent version of base R from [CRAN](https://cran.r-project.org/).

## 3\. Install Rstudio

Download and install the most recent version of RStudio Desktop (free version) from [RStudio](https://www.rstudio.com/products/rstudio/download).

## 4\. Install BUGSnet

Open RStudio and run

``` r
install.packages(c("installr", "remotes", "knitr"))
installr::updateR(TRUE)
installr::install.Rtools(choose_version = FALSE, check = TRUE)
remotes::install_github("audrey-b/BUGSnet@v1.0.3", dependencies = TRUE, upgrade = TRUE, build_vignettes = TRUE)
```

## 5\. Check that BUGSnet works

If everything installed properly, the following [test script](testscript.txt) should run without error. Simply copy and paste to your RStudio console, then run.
