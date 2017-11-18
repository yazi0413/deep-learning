2017Stanford
image classification
    "semantic gap" problem 
    KNN,k-nearest neighbor(never used)
        terrible performance at test time
        distance metrics on level of whole images can be very unintuitive
    linear classification
        f(x,W)=Wxi+b
            loss function:  quantifying what it means to have a good "W"
                hinge loss & square hinge loss
                weight regularization
                    L1 & L2 in common use
                L=1/N*sum(max(0,f(Xi,W)j-f(Xi,W)yi+)|j/=yi + lamda R(W)
                softmax classifier (Multinomial Logistic Regression), more popular than SVM
                    Li=-log(exp(yi)/sum(exp(ej)))
                SVM: Li=sum(max(0,sj-syi+1))
                    the main difference between SVM and softmax is, (% SVM cares about the sample接近于分类边界; % softmax is kinda based on all data, cases about all samples.)
                    
            optimization:   start with random W and find a W that minimizes the loss!
                gradient,dW. always use analytic gradient, but check implementation with numerical gradient. this is called Gradient Check
                    numerical gradient: approximate, slow, easy to write
                    analytic gradient: exact, fast, error-prone
                mini-batch gradient descent
                learning rate
                
            convNets:       tweak the functional form of f
        CNN, convolutional neural network
ImageNet