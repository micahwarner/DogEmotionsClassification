# Dog Emotions Classification

This code is a convolutional neural network that takes in the Dog Emotion data from Kaggle and classifies what emotion each dog is portraying. 

The code also implements transfer learning twice with the VGG16 model by freezing all of the convolutional layers and only freezing the first 10 layers and having the non-frozen VGG16 layers at a learning rate of .01 and our added layers at a learning rate of .0001. 

### Motivation: 
Our project title was inspired by the “Big Dawgs” in the Artificial Neural Networks Class, and we partly chose this since we were able to look at pictures of Dogs for hours.

Dogs live in approximately 66% of American households and are a huge part of our society with most people treating their pet like their child. 

As AI progresses and integrates into our society, models like the one we have created will not only benefit the user, but their pets as well. 

AI that is able to determine the emotions of a dog would be able to learn patterns to better understand when to feed, introduce toys, or issue out treats to enhance the dog's living experience. 

### Solution: 
 We decided to create a convolutional neural network to classify basic emotions that dogs are portraying. 

### The Dataset:
Our data comes from a data set we found on Kaggle. The data set contains images that were collected from various online sources and manually annotated by the author of the data set Daniel Shan Balico. The data set contains 4,000 images of dogs in total. There are 1,000 images for each emotion of the dogs. The emotions are labeled into either happy, sad, angry, relaxed. For our model we decided to split the data into 2800 images for the training data and 1200 images for the testing data. The photos from the data set all come in the size of 192 x 192 x 3. After we trained and ran our model we later on tested photos we used of our own dogs and Snapchat’s Dog filter to see if the model is accurate and these photos had to be shrunk down to a size of 192 x 192 x 3. 


### Overall, we saw good success with each model: 

-Our first model is a simple CNN that we made and trained from scratch, which ended up with a 90% testing accuracy. 

-Our second mode, which utilized transfer learning with the VGG16 model, improved significantly, jumping up to 98% testing accuracy.

-Our final model, which used a VGG16 model again but with some finetuning in its layers, resulted in 99.98% testing accuracy, incorrectly predicting one image.

##### More Details:
We created our own convolutional neural network with 5 layers and originally only had a 68% training accuracy and 90% testing accuracy. To improve our accuracy even more, we used transfer learning. For transfer learning, we decided to use the VGG16 model. VGG16 helped our model significantly. This is because VGG16 is a pretrained model that is used to classify images in large data sets. It has 16 layers in the Neural Network but our group removed 3 of them and then added 2. Therefore, the new model has 15 layers in the Neural Network. We then froze the convolutional layers, stopping the picture processing from changing its algorithm, but fine tuned our output layers to train them to identify the dogs. After using VGG16, the accuracy improved to 86% on the training data and 98% on the testing data. We did not stop here. Lastly, we created another model that is similar to the second model. In this network, instead of freezing all of the picture processing layers, we only froze 10 of the 12 layers, but created two different learning rates for the picture processing side of the network and our own added layers. This allowed the less generalized aspects of the VGG16 model to train towards the dog model as well as the newer layers. This was by far the best model since only one picture in the testing set was labeled incorrectly. 

The dataset can be found here: https://www.kaggle.com/datasets/danielshanbalico/dog-emotion

To run and use the program, download and store the .ipynb file and all the personal images in the same directory, then put the dataset stored in "dog/Dog Emotion/" files in that same directory. 
