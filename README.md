# Class

## Download the file covariance Matrix.txt.

Either by cloning the repo
```
$ git clone git@github.com:jquetzalcoatl/Class.git
```
or by doing
```
$ wget https://raw.githubusercontent.com/jquetzalcoatl/Class/main/covarianceMatrix.txt
```
or simply select the data from `https://raw.githubusercontent.com/jquetzalcoatl/Class/main/covarianceMatrix.txt` and save it in a txt file.


## Obtain the components

Open R and run:
```
m <- as.matrix(read.delim("/PATH/TO/covarianceMatrix.txt", header = FALSE))  #Change path accordingly
d <- eigen(m)
eigenvalues <- d$values
eigenvectors <- d$vector

plot(eigenvalues)
plot(eigenvectors[1:200,3], pch=21, bg="red", col="blue", cex = 1,lwd = 3)
```
