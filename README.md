# whos-that-pokemon
Creating a Convolutional neural network to classify pictures of pokemon 
data comes from the following sources
  https://www.kaggle.com/datasets/brkurzawa/original-150-pokemon-image-search-results/code?resource=download
  https://www.kaggle.com/datasets/thedagger/pokemon-generation-one
  and additional sources manually collected to make sure there was no overlap

convert images to PNG: 
  Python notebook that converts all of the images into PNG's from jpegs or gifs 
  pulls the value count of each folder to ensure we have at least 100 images of pokemon 
    need to add images if there arent enough pictures
  it then creates a train/validation split of 80/20% 
  using these new folders it cleans the images of all corrupt images and then converts all RGB's to RGBA
  data can then move on to next step
  
Pokemon EDA:
  python notebook that plots the number of images on each class so we can see how many files there are and how many each class has

model set up:
  contains the datagen for training and validation files
  sets up the hyper parameter search for the initial model
    saves the hyper parameters to a file directory
  runs the model and saves the history to a csv
    plots the history of the runs
  includes a small prediction section to test the model
  
 model set up advanced CNN96:'
  python notebook
  contains the datagen for training and validation files
  sets up the hyper parameters for the final 96x96 CNN
    saves the hyper parameters to a file directory
  runs the model and saves the history to a csv
    plots the history of the runs
    saves the best model according to validation data
  includes a small prediction section to test the mode
 
csv reader:
  This python notebook is used to pull the csv's created from the previous model runs
    this is because the training takes a long time and I wanted to break it into chunks and I wanted to preserve the history of the runs so I can run however many epochs in batches or shutdown my kernel if there is an issue
    
