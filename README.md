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
4000 total images, 1000 per category

Classes:

  -Angry
  
  -Sad
  
  -Relaxed
  
  -Happy
  
And tested with some of our own

We divided the data for training into: 
2800 images for training and 1200 for testing

### Overall, we saw good success with each model: 

-Our first model is a simple CNN that we made and trained from scratch, which ended up with a 90% testing accuracy. 

-Our second mode, which utilized transfer learning with the VGG16 model, improved significantly, jumping up to 98% testing accuracy.

-Our final model, which used a VGG16 model again but with some finetuning in its layers, resulted in 99.98% testing accuracy, incorrectly predicting one image.

The dataset can be found here: https://www.kaggle.com/datasets/danielshanbalico/dog-emotion

To run and use the program, download and store the .ipynb file and all the personal images in the same directory, then put the dataset stored in "dog/Dog Emotion/" files in that same directory. 
