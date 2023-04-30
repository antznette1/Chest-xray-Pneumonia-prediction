# Traffic-sign-prediction-using-cnn

For this task, we trained the chest Xray dataset using CNN. Proceeded to re-split the data as the validation set in the existing dataset is too small.  

Model 1 with SoftMax activation and 2 Maxpooling layers

The train, validation, and test sets all show very low accuracy levels. We attribute this to the adoption of a dense layer of 1 and the softmax activation function. Softmax is an option for binary predictions, albeit it is less common; however, the dense layer must be 2. This is due to the fact that argmax makes predictions after converting the two values that softmax produces—one for each class's score and another—into probabilities.
 

Model 2 with sigmoid activation

I applied the sigmoid activation function to improve the model. Given that the dense layer in this instance is 1, this is perfect. When a single number is the desired output, sigmoid can be utilised. The score is converted by Sigmoid into a ones and zeros. In order to decrease the pixels and force the model to select only the most crucial features, I additionally added two additional pooling layers. As a result, fewer labels were incorrectly predicted due to the model's higher accuracy. Only 45 photos were incorrectly predicted by the model overall. Below is a table that summarises the model 2 accuracy and confusion matrix.
