
## Session 6 Assignment - Team Submission
Team Members
1. S.A.Ezhirko
2. Naga Pavan Kumar Kalepu
3. Varsha Raveendran
**********************************************************************************************************************

### Code Explanation

Base Code: The base CNN model is taken from the previous Version 6 of Session 5 assignment. The Base CNN archicture consist of 6 Convolution layers, 1 maxpool at GRF = 5 and a Global Average pooling layer at the end. The total number of parameters in the CNN Model are 7,612 and the best training accuracy achieved in 15 epochs is 99.41 and best validation accuracy achieved in 15 epochs is 99.49

Following regularization experiments are performed on the base CNN model.
1.	with L1 + BN
2.	with L2 + BN
3.	with L1 and L2 with BN
4.	with GBN
5.	with L1 and L2 with GBN

Technique To choose Lambda Values

  To find the best hyperparameter value (Lambda value) for L1 and L2 for above stated combinations, Grid Search technique is used. The Grid Search algorithm sequentially trains the CNN model with a range of hyperparameter values for l1 with BN, l2 with BN, l1&l2 with BN & l1&l2 with GBN. The Grid Search algorithm takes in a range of values from 4 buckets [0,0.0001], [0,0.001], [0,0.01],[0,0.1]. First range from the bucket is taken and 20 uniform distributed random values are picked with in those range. In order to give equal priority to all the values in the range, uniform distribution is chosen over normal distribution. The picked random value is assigned to L1, L2 and L1 + L2 regularization and the model is trained for 15 epochs. The best validation accuracy is then taken and saved to compare with next set of random values. On completion of 20 trials on a given range, the random value that gave the best validation accuracy is taken and saved to compare against with another range of values. This experiment is repeated for chosen 4 ranges and the random value that gave the best validation accuracy among the 4 ranges are chosen to be the lambda value for the regularization.

With above approach Coarse and Finer search 4 * 4 * 20 * 15 = 4800 epochs overall to get best parameters for 4 models (l1, l2, l1&l2) with BN & l1&l2 with GBN.
- 4 - number of models
- 4 - number of ranges
- 20 - number of random values per range
- 15 - number of epochs
  
Total 4800 epochs to get best parameters.