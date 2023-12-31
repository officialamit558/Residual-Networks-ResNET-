# Residual-Networks(ResNET)

Q) Why used ResNet?

#### -> Addressing vanishing gradient problem (By Introducing the skip connection  that allow the gradient to bypass certain layers, mitigating the vanishing gradient problem and facilitating the training of very deep networks.
#### -> Ease of optimization 
-> Deeper networks(ResNet architectures can be significantly deeper than traditional networks without suffering from degradation issues, where accuracy saturates and then degrades rapidly as the network becomes deeper.)
->State-of-the-art performance
-> Transfer learning

# Step of making this model

step 1) Import the all relevent library from tensorflow .keras
step 2) Building a Residual Network ( The Identity Block + The Convolutional Block)
step 3) In identity block used the conv2D layer + BatchNormalization + ReLU activation function
step 4) In convolutional block used the Conv2D layer in the sortcut path way + conv2D layer + BatchNormalization + ReLU activation function
step 5) Building Your First ResNet Model (50 layers) 
        # . stage 1) conv2D + BatchN + ReLU + MAXPUL
        # . stage 2) Convolutional block + 2 * identity block
        # . stage 3) Conolutional block + 3* identity block
        # . stage 4) Conolutional block + 5*identity block
        # . stage 5) Convolutional block + 2*identity block
step 6) Get the summary of the model , In which we get the parameters = 23,600,006 and Trainable params:=  23,546,886
Non-trainable params:=  53,120
step 7) Compile our model and used the adam optimizer and 0.0000015 learning rate .
step 8) This is time of ready our model to train by different type of datasets.
step 9) Fit our model with 10 epoch and 32 batch size and evaluate our modell on the training datasets
step 10) Now time of Test on Your Own Image and accuracy is 94%
