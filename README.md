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
##Week1	
###Cost function:   
calculates squared error of prediction (=h(x)- y) values to estimate how optimal the choice is. This is criterion for finding a good hypothesis. This could be described well by contour plot.

###Gradient descent:   
θj:=θj−α(∂/∂θj)J(θ0,θ1) where j = 0,1    
J: cost function  
Gradient descent makes small step(α) toward the direction where J value decreases. j=0,1 is feature indices which required to be updated simultaneously to make this model physical. α is called learning rate which might be a critical factor for convergence of learning process.

