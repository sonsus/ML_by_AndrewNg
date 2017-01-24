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
  
  
###feature rescaling (or normalization)
#####Uneven range of feature value tortures developers who want to find an optimal learning rate.  
>Too large range: too many iterations   
>Too small range: overshoot(divergence)   
>One cost function can have both above (e.g. think skewed contour plot)   
>	--finding optimal learning rate might vary according to its initial state

#####two ways for normalization
>x'=x-u/range  
>x'=x-u/stdev
