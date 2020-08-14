Session 4 Assignment - Team Submission
Team Members
1. S.A.Ezhirko
2. Naga Pavan Kumar Kalepu
3. Varsha Raveendran

-------------------------------------------------------------------------------------------------------------------------------------
Version Number |             Architecture             |               Description             |               Results               |
-------------------------------------------------------------------------------------------------------------------------------------
Version 1      |                                      | Added Batch norm after each layer,    | Test accuracy is 99.44% but number  |
               |                                      | number of channels updated in each    | of parameters around 21000          |  
               |                                      | layer from 8 till 32 geometrically    |                                     |      
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
-------------------------------------------------------------------------------------------------------------------------------------
Version 2      |                                      | Reduced number of paramters below     |Test Accuracy is 99.37 %             |
               |                                      | 20000 but didn't reach target test    |                                     |  
               |                                      | accuracy 99.4 %                       |                                     |      
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
-------------------------------------------------------------------------------------------------------------------------------------
Version 3      |                                      | Observed model was overfitting in the |Test Accuracy is 99.43 %             |
               |                                      | version 2, so added dropout layers    |                                     |  
               |                                      | after conv4 and conv5 as we should not|                                     |      
               |                                      | add near final output layer and got   |                                     |
               |                                      | target accuracy and removed batchnorm |                                     |
               |                                      | before the last layer                 |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
-------------------------------------------------------------------------------------------------------------------------------------
Version 4      |                                      | Added batch norm before the last layer| v4.1 - test accuracy - 99.53% at    |
               |                                      | and hit the highest test accuracy of  | epoch 15 at learning rate = 0.02    |  
               |                                      | all the versions which is 99.5 % at   | v4.2 - test accuracy - 99.5% at     |      
               |                                      | epoch 12 & 17                         | epoch 15 at learning rate = 0.01    |
               |                                      | Number of parameters are 18,058       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
               |                                      |                                       |                                     |
-------------------------------------------------------------------------------------------------------------------------------------
Version 5      |                                      | Added only 6 Convolution layers.Added | v5.1 - test accuracy - 99.55% at    |
               |                                      | Batchnorm at each layer except last   | epoch 16 at learning rate =0.02 with| 
               |                                      | layer. Added Dropout layer at 3rd and | BatchNormalization at end of each   |      
               |                                      | 5th convolution layer. Tried with 0.12| layer and drop out of 0.15          |
               |                                      | , 0.10, 0.15 Dropout values. Tried    | v5.2 - test accuracy - 99.5% at     |
               |                                      | 0.02 and 0.01 as learning rates.      | epoch 13 at learning rate =0.01 with|
               |                                      | Number of parameters are 18,802       | BatchNormalization at end of each   |
               |                                      |                                       | layer and drop out of 0.15          |
               |                                      |                                       | V5.3 - test accuracy - 99.39% at    |
               |                                      |                                       | epoch 8 with drop out = 0.10        |
               |                                      |                                       | V5.4 - test accuracy - 99.41% at    |
               |                                      |                                       | epoch 9 with drop out = 0.12        |
   
