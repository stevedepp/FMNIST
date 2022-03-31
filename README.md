## FMNIST classification with deconvolutional layers

Below is a 4 min 44 sec video demonstrating Colab [notebook's](https://github.com/stevedepp/FMNIST/blob/master/FMNIST_Depp.ipynb) speed and ease of use in building the basics of computer vision classification: 
- [x] retrieving dependencies.  
- [x] retrieving data from Google Drive and loading into Colab environment.  
- [x] exploring data and transforming where necessary.   
- [x] segmenting the data into representative train, validation and test sets. 
- [x] reshaping the sets per model needs.  
- [x] model hyperparameters. 
- [x] running and evaluating DNN and CNN models.  
- [x] employing deconvolutions to review layer activations for tunning model dimensions. 

The colab notebook from this demo video is included in this repo's code library [here](https://github.com/stevedepp/FMNIST/blob/master/FMNIST_Depp.ipynb).

Some general thoughts on cloud-based solutions, Colab and computer vision are found [here](https://github.com/stevedepp/reflections/blob/main/cloud_colab_cv.md)

You can read the transcript & slides below or click this 4 min 44 sec demo [video](https://github.com/stevedepp/FMNIST/blob/DEPP_462_55_DV_1.mp4) to hear it with sound.

![demo](https://github.com/stevedepp/FMNIST_classification/blob/DEPP_462_55_DV_1.mp4)











#

> hello.  thank you for taking a minute to listen to my demo video.  i was looking forward to this week’s video because it gives us an opportunity to …

**Steve Depp**   
**462-55**   

**Goals**  
- [x] Colab  
- [x] GPU  
- [ ] Publish Jupyterbook on GitHub (tomorrow)  

#

> '… use Colab and …'

**Colab**  
Dislikes  
- A bit laggy   
Likes
- Autocomplete
- Hierarchical section headings
- Github / Drive
- GPU access
   
#

> … to get experience with the speed of GPUs.  

GPU 

|                 | CPU         | GPU        |
| :---            | :---        | :---       | 
| Fully connected | 17 seconds  | 14 seconds |
| Convolutional   | 377 seconds | 23 seconds |
    
#

> this presentation will briefly touch upon getting hooked up to cloud computing to download data, to build models and to examine the performance of those models.

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

#

> here on top i am getting hooked up to my google drive and in the middle i’m getting hooked up to kaggle and down at the bottom i’m using kaggle to download the data.   

**Steps**    

Hooked up & Loaded up:  
- [x] Kaggle
- [x] Google docs

<img width="732" alt="Access Google drive Kaggle" src="https://user-images.githubusercontent.com/38410965/112354314-f18be580-8ca2-11eb-9385-e6b6f6420514.png">

<img width="766" alt="Load dataset" src="https://user-images.githubusercontent.com/38410965/112354284-e9cc4100-8ca2-11eb-818e-6c42deffba1b.png">

#

> a quick look at the data.  here in the middle i calculated the mean pixel values for the 10 labels. it shows that not all images are the same: sneaker images are lighter than the images of coats.  shirts and t-shirts are quite similar in their pixel values.  you can see that shirts have a mean pixel value of 85.01 and t-shirts have a mean pixel value of 82.77.   so, that’ll make sneakers and coats easier to distinguish and shirts and t-shirts more difficult to distinguish.  at the bottom i calculate the correlation between the image pixels.  some target images are less related than others. so for example the images of dresses are unrelated to the images of t-shirts, sandals, boots and sneakers.  so, this might make these images easier to classify for a fully connected model.  also the correlations between the train and the test sets are the same which leads me to expect good generalization between the train and the test sets.    


**Steps**

Looked at the data

- [x] nulls & nans … none

<img width="489" alt="(9, 'Ankle-boot') (4, 'Coat) (9, 'Ankle-boot') (4, 'Coat')" src="https://user-images.githubusercontent.com/38410965/112354225-d9b46180-8ca2-11eb-904a-5faf0273b7e4.png">

- [x] greys
  - light sneakers = 42.79 
  - dark coats = 98.04

<img width="292" alt="Figure Mean pixel values by item" src="https://user-images.githubusercontent.com/38410965/112354179-ce613600-8ca2-11eb-95f7-54e87b7202f5.png">

- [x] correlations
  - boots vs dresses (27%) and t-shirts (25%)
  - dresses vs sandals (17%) and sneakers (20%)
  - train = test

<img width="820" alt="Table Mean correlations amongst images of items in train set" src="https://user-images.githubusercontent.com/38410965/112354148-c73a2800-8ca2-11eb-94d2-3eb0163f983e.png">

<img width="803" alt="Table Mean correlations diff fro" src="https://user-images.githubusercontent.com/38410965/112354104-bee1ed00-8ca2-11eb-98d4-09a902c33ea4.png">

#

> so as for performance … here are the two models: this is a fully connected and a convolutional model.  the fully connected has one hidden layer and the convolutional has three.  they have roughly the same number of parameters.  both do generalize quite well: the fully connected tops out at around 89% and the convolutional is still rising after 10 epochs at 92%.    it was evident that both models were getting confused between shirts and t-shirts and i’ve kind of itemized that here.  


**Performance**

- [x] Structure 
- [x] Accuracy 

<img width="920" alt="Fully connected" src="https://user-images.githubusercontent.com/38410965/112354048-b25d9480-8ca2-11eb-8e8b-e783b219d705.png">

<img width="945" alt="Confused" src="https://user-images.githubusercontent.com/38410965/112353975-a4a80f00-8ca2-11eb-9a60-303c07ff6628.png">

#

> in order to sort of look at that in a little more detail i looked at the activations and the gradients for shirts and t-shirts.  
 
**Steps**
 
Under the hood
- [x] activations
- [x] filters
- [x] class activation heatmaps

# 

> so here is a shirt with label number 6 and one of its activations which is kinda murky.  here are the convolutional layer 1 and 2 for this image.   
 
Shirt = 6

![Pasted Graphic 18](https://user-images.githubusercontent.com/38410965/112353921-98bc4d00-8ca2-11eb-8b75-b670e84de64b.png)

Convolutional 2 activation

![Pasted Graphic 25](https://user-images.githubusercontent.com/38410965/112353877-8e01b800-8ca2-11eb-8f8c-1eb77599e2a3.png)

Convolutional 1

<img width="934" alt="Pasted Graphic 19" src="https://user-images.githubusercontent.com/38410965/112353756-70cce980-8ca2-11eb-9794-9c9967afc70c.png">

Convolutional 2

<img width="926" alt="Pasted Graphic 20" src="https://user-images.githubusercontent.com/38410965/112353687-5eeb4680-8ca2-11eb-9292-b65e9367a531.png">

#

> here’s the t-shirt and here’s its activation which is a lot more distinct. and then if you look here again, the convolution layer 1 and 2 are more distinct as well.  so its probably going to classify t-shirt better.  


T-shirt = 0

![10](https://user-images.githubusercontent.com/38410965/112353668-572ba200-8ca2-11eb-94a2-1c637460d680.png)

Convolutional 2 activation

![Pasted Graphic 24](https://user-images.githubusercontent.com/38410965/112353626-4b3fe000-8ca2-11eb-90a0-428dab740b62.png)

Convolutional 1

![Pasted Graphic 22](https://user-images.githubusercontent.com/38410965/112353509-2c414e00-8ca2-11eb-9152-3cfc6156cfce.png)

Convolutional 2

![Pasted Graphic 23](https://user-images.githubusercontent.com/38410965/112353459-2186b900-8ca2-11eb-9d72-3661a274b0fc.png)

#

> here i take the gradient.  it’s the mean gradient to weight the activations.  and it shows the edges being formed in the activations here and here.  this edge is actually more distinct and related to this t-shirt, this feature of this t-shirt whereas this is not really a shirt feature.  so you can see why the t-shirt might be easier to identify.   

<img width="762" alt="T-shirt = 0" src="https://user-images.githubusercontent.com/38410965/112353378-12077000-8ca2-11eb-92cb-cafa7265d76e.png">

#

> finally at the bottom here i look at the layer filters, and it’s interesting.  it’s pretty.  but one of the big things i gather from this, aside from the fact that the first layer has you know horizontal and vertical lines and this has a little bit more complex features in the second convolutional layer, the thing i take away from this is that there’s a lot of noisy filters here.  this isn’t all the filters.  this is just a percentage of the filters, but this percentage of filters is quite noisy which means that we can probably get rid of some of these filters and still have the same level of performance.   

<img width="934" alt="d Convolutional layer filters" src="https://user-images.githubusercontent.com/38410965/112353296-fdc37300-8ca1-11eb-8db7-f2b42d417c82.png">

#

> so in conclusion, i do think i will continue to use Colab.  it gives us access to the speed of GPUs but probably more important for classes and going forward is it gives us access to each other.  so thank you very much for listening.  

**Conclusion**  

Colab is a worth using
- [x] Access to teams
- [x] Access to GPUs

CNN > FC  
- Both generalized
- CNN still climbing at 92%
- Worth it even on a CPU

Under the hood  
- Not much confusion except shirts (6)
- Can remove some filters
