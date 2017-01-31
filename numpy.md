#Numpy: Playing with matrix
#####original text from numpy.org (https://docs.scipy.org/doc/numpy-dev/user/quickstart.html)

ndarray generation

matmul(a,b) 
indexing, slicing
a[1]==a[1,:]
a[...,1]==a[:,:,1] (if a.dim==3) 

reshape(2,-1) do not change the original, just return reshaped matrix
  (putting -1 let the program calculate the # of columns automatically)   
   
resize(2,5) change the original to be in (2,5) size

a.T==transpose of a
