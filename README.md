# MLP
Error Minimization using Multilayer Perceptrons:

In order to do this task, the following steps were performed-
1. A Guassian class conditional pdf (probability density function) for 3 Dimensional real valued random vectors was stated as P(X) = P(L=0) P(X|L=0) + P(L=1) P(X|L=1) + P(L=2) P(X|L=2) + P(L=3) P(X|L=3) 
2. Assuming the class priors to be uniform, P(L=0) = P(L=1) = P(L=2) = P(L=3) = 0.25
3. The following mean (m0,m1,m2,m3) and covariance (c0,c1,c2,c3) matrices were taken for this task:   

    For class label 0: P(L=0) = 0.25
    P(X|L=0) = g(X|m0,c0) ; where m0 = [2.2, 0, 0] and c0 = [[1, -0.5, 0.3], [-0.5, 1, -0.5], [0.3, -0.5, 1]]
    
    For class label 1: P(L=0) = 0.25
    P(X|L=1) = g(X|m1,c1) ; where m1 = [2.2, 2.2, 0] and c1 = [[1, 0.5, 0], [0.5, 1, 0.5], [0, -0.5, 1]]
    
    For class label 2: P(L=0) = 0.25
    P(X|L=2) = g(X|m2,c2) ; where m2 = [2.2, 0, 2.2] and c2 = [[1, 0.3, -0.2], [0.3, 1, 0.3], [-0.2, 0.3, 1]]
    
    For class label 3: P(L=0) = 0.25
    P(X|L=3) = g(X|m3,c3) ; where m3 = [0, 2.2, 0] and c3 = [[1, 0.3, 0.6], [0.3, 1, 0.3], [0.6, 0.3, 1]]
      
While choosing the parameters (mean and covariance), the Maximum A Posterior Classifier uses the true data obtained from the pdf and reports an error of within 15% for all the input samples used (100, 200, 500, 1000, 2000, 5000, 100000). The 100000 input sample dataset is used for testing the model. 
 
4. Input samples of sizes 100, 200, 500, 1000, 2000, 5000, 100000 are generated.
5. A two layer Multilayer Perceptron is used (consisting of P number of perceptrons in the first hidden layer). The optimal number of perceptrons needed are then determined by the help of K Fold cross validation. (K = 10)
6. The model is trained with different insput sample sizes after determining the optimal number of perceptrons . Maximum Likelihood Parameter Estimation is being used to train the MLP. 
7. The trained MLP model is then used for Performance Assessment on the test set comprising of 100000 input samples.
8. The results (graph between Probability of Error and Number of Data Points in training data using semilog axis) were plotted using Matplotlib.
    


The Project was executed on Google Colab. Visit the URL to view:
https://colab.research.google.com/drive/1dPcA6j4fSqs8yoXjQ84Gtr0Yfuh5GRb6?usp=sharing
