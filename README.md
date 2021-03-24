# [FMNIST Colab notebook](https://github.com/stevedepp/FMNIST/blob/master/FMNIST_Depp.ipynb)

A demo of a Colab [notebook's](https://github.com/stevedepp/FMNIST/blob/master/FMNIST_Depp.ipynb) speed and ease of use in building the basics of computer vision classification: 
- [x] retrieving dependencies.  
- [x] retrieving data from Google Drive and loading into Colab environment.  
- [x] exploring data and transforming where necessary.   
- [x] segmenting the data into representative train, validation and test sets. 
- [x] reshaping the sets per model needs.  
- [x] model hyperparameters. 
- [x] running and evaluating DNN and CNN models.  
- [x] employing deconvolutions to review layer activations for tunning model dimensions. 

The colab notebook from this demo video is included in this repo's code library [here](https://github.com/stevedepp/FMNIST/blob/master/FMNIST_Depp.ipynb).

Transcript & slides are below. Please click this demo video to hear it with sound.

![demo](https://user-images.githubusercontent.com/38410965/111723158-7c9b5480-8839-11eb-834a-4c7a0849980c.mp4)











**Steve Depp**   
**462-55**   

**Goals**  
- [x] Colab  
- [x] GPU  
- [ ] Publish Jupyterbook on GitHub (tomorrow)  


**Colab**  
Dislikes  
- A bit laggy   
Likes
- Autocomplete
- Hierarchical section headings
- Github / Drive
- GPU access
   


GPU 

|                 | CPU         | GPU        |
| :---            | :---        | :---       | 
| Fully connected | 17 seconds  | 14 seconds |
| Convolutional   | 377 seconds | 23 seconds |
    

**Steps**  
  
Colab hooks up:  
- [x] Kaggle
- [x] Google drive

Easy to load / explore data:  
- [x] nulls & nans
- [x] greys
- [x] correlations

Performance  
- [x] structure
- [x] accuracy

Under the hood
- [x] activations
- [x] filters
- [x] class activation heatmaps



**Steps**    

Hooked up & Loaded up:  
- [x] Kaggle
- [x] Google docs


**Steps**

Looked at the data

- [x] nulls & nans … none

- [x] greys
  - light sneakers = 42.79 
  - dark coats = 98.04

- [x] correlations
  - boots vs dresses (27%) and t-shirts (25%)
  - dresses vs sandals (17%) and sneakers (20%)
  - train = test


Performance

- [x] Structure 
- [x] Accuracy 


**Steps**
 
Under the hood
	✓	activations
	✓	filters
	✓	class activation heatmaps

Shirt = 6

Convolutional 2 activation

Convolutional 1

Convolutional 2


T-shirt = 0

Convolutional 2 activation

Convolutional 1

Convolutional 2










Conclusion
  
Colab is a worth using
	◦	Access to teams
	◦	Access to GPUs 
CNN > FC
	◦	Both generalized
	◦	CNN still climbing at 92%
	◦	Worth it even on a CPU

Under the hood
	◦	Not much confusion except shirts (6)
	◦	Can remove some filters
