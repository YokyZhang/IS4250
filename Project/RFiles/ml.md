Assume the estimated parameters from different samples are 123, 234,
345, 456, and 567.

To use Maximum Likelihood (ML) method to estimate the parameters of the
model.

    library(stats4)
    f <- function(alpha){
      logL = n*log(alpha) - alpha*sum(x)
      return (logL)
    }
    x= c(123,234,345,456,567)
    n = length(x)
    a = optimize(f,c(0,1),maximum = TRUE)
    1/a$maximum

    ## [1] 346.4544
