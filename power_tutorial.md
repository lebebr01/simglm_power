Power Analysis by Simulation using R, simglm, and Shiny

# description
Power analyses are commonly needed for grant applications to be successful and are also useful for research studies to ensure that the sample sizes have sufficient ability to detect the effect of interest. Some statistical models have closed form solutions for estimating power, however these closed form solutions make many assumptions, such as homogeneity of variance, balanced data, normal residuals, etc, that may not hold with real-world data. The impact of the model misspecification is likely an overestimate of power. Power by simulation is a way to obtain more relatistic power estimates and once the general framework is understood, similar principles can be used to conduct a power analysis by simulation for a wide variety of experimental designs and statistical models. The tutorial will briefly introduce what power is and start doing an analysis for two groups and compare the power by simulation results with that to the power.t.test() function within R. Furthermore, the power analysis by simulation will be extended to generate data from non-normal distributions, unbalanced data, and heterogeneity of variance to explore their impact on statistical power. A second example, conducting power for a repeated measures analysis, will also be done to show the power analysis for a more complicated design. Impacts on power related to missing data, non-normal error distributions, and model misspecification will be highlighted in the second example. These tutorials will be supported by a Shiny app distributed within the simglm R package on CRAN (https://cran.r-project.org/package=simglm) where users can install the package and run the Shiny app with two lines of code in R. The code for the package will also be hosted on GitHub (https://github.com/lebebr01/simglm) for transparency and also for issue tracking. Finally, the Shiny app will also provide valid R code to run the power analysis outside of the Shiny app. This means that users could run a small power simulation within the Shiny app, copy and paste the R code generated from the Shiny app, then run this in an R console. The writing of the R code may be beneficial for some users and this would also allow them to benefit from running the simulation outside of the Shiny application, particularly for more complicated designs. 


# prerequisites
- Basic understanding of statistical principles, including type I error, power, and regression analysis.

# Who would use
- Graduate students, applied researchers conducting power analysis for grant applications, journal articles, or other research. This may also benefit early career researchers across disciplines, particularly as the tutorial and Shiny application will be able to be extendable and valid R code will be produces within the app to be used later.

# Other Comments
The current form of the Shiny app can be run with the commands below to get an idea of feel and structure of the app. The Shiny app will be updated to include more options and also implement the newer tidy simulation syntax that has been developed for the simglm R package (https://cran.r-project.org/web/packages/simglm/vignettes/tidy_simulation.html): 

install.packages(c("simglm", "shinydashboard", "highcharter"))
simglm::run_shiny()
