# walkr
Consider the intersection of two spaces: the complete solution space
to Ax = b and the N-Simplex. The intersection of these two spaces is 
a convex polytope. **walkr** samples from this 
intersection using two Monte-Carlo Markov Chain (MCMC) methods: 
hit-and-run and Dikin walk. **walkr** also provide tools to examine sample 
quality.

# Getting Started

* Install from CRAN(released version):

  `install.packages("walkr")`
  
* Install from GitHub (development version):  

  `devtools::install_github("andyyao95/walkr")`  

# Sampling Points  
```
  library(walkr)  
  A <- matrix(1, ncol = 3)  
  b <- 1    
  sampled_points <- walkr(A = A, b = b, points = 1000, 
                          method = "dikin", ret.format = "list")   
```
# Visualizing the Sampled Points  

  `explore_walkr(sampled_points)`
