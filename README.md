# ML_by_AndrewNg

##intro (before week1)
intro ML

Supervised - regression, classification
Unsupervised - clustering 

regression vs classification
clustering 

##intro(2)
0103
model representation
training set -> learning algorithm =>> hypothesis
            input ---> hypothesis ---> prediction (y)

univariate linear regression == linear regression with one variable

when y value (predicted value) is limited to be discrete --> classification
							   is continuous --> regression
##Week1: Linear-regression with one var
###Cost function:   
calculates squared error of prediction (=h(x)- y) values to estimate how optimal the choice is. This is criterion for finding a good hypothesis. This could be described well by contour plot.

###Gradient descent:   
θj:=θj−α(∂/∂θj)J(θ0,θ1) where j = 0,1    
J: cost function  
Gradient descent makes small step(α) toward the direction where J value decreases. j=0,1 is feature indices which required to be updated simultaneously to make this model physical. α is called learning rate which might be a critical factor for convergence of learning process.

##Week2: Multivariable regression
### vector representation of a cost function J(\theta)
Instead of using a form of sum, use vector multiplication for convenience (and this is better choice for computing efficacy)
each feature of a training example x<sub>j</sub><sup>(i)</sup> becomes an element of a vector x<sup>(i)</sup> with x<sub>0</sub> =1

>J(theta)=sum<sub>i=0 to m</sub>(transpose(theta)x<sup>(i)</sup> - y<sup>(i)</sup>)<sup>2</sup>     
>Where h(theta)=transpose(Theta)x<sup>(i)</sup>= theta0+theta1*x1+theta2*x2...(to n th sum)   

#####If we put all training examples (column vectors) into a matrix by row-wise
#####(and let theta be a column vector then...
> h<sub>theta</sub>(X) (m x 1 column vector) = X (m x n+1) * theta (n+1 x 1)    
	   
	   
###feature rescaling (or normalization)
#####Uneven range of feature value tortures developers who want to find an optimal learning rate.  
>Too large range: too many iterations   
>Too small range: overshoot(divergence)   
>One cost function can have both above (e.g. think skewed contour plot)   
>	--finding optimal learning rate might vary according to its initial state

#####two ways for normalization
>x'=x-u/range  
>x'=x-u/stdev

### Determining Learning Rate
##### slow convergence: 
when alpha is too miniscule or sometimes when alpha value is close to the threshold value to divergence
##### divergence:
overshoot when learning rate is too huge

If J(theta) decreases lesser than, with rule of thumb, 10<sup>-3</sup> then it is considered converged.
Determining threshold value (which was 10<sup>-3</sup>) is difficult part of ML.

###Combining Parameters
if given features could be combined into lesser number of brilliant way, it could be a good simplification
  
  
###Polynomial Regression
To make a better fit, one can make linear regression function into polynomial.
>h=a<sub>0</sub>+a<sub>1</sub>x+a<sub>2</sub>x<sup>2</sup>+...  
and this could be considered multivar linear regression  
>h=a<sub>0</sub>+a<sub>1</sub>x+a<sub>2</sub>y+...

##### square, cube, quadruple and higher order variable has different range so normalization is required
