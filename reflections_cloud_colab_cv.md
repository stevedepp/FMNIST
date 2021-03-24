**What problem does the cloud solve when considering real-world computer vision problems?**

CV and other AI subsets are well served in the cloud in similar ways:

Variable compute which addresses    
- continuous scalability: speed and dimension when you need it.  
- near limitless storage if you are creative   
- variable configure: your solution running on different hardware (hardware you don't have access to but your customer does).   
- serverless tech / stateless application servers which enable instant access to different languages and configurations that afford e.g. concurrency, parallelization, scale.   

All these might solve problems which are otherwise insolvable on a local platform and allowÂ tinkering with hardware configurations, much as one might tinker with lines of code.  We gain access to APIs for computer vision:   
- https://aws.amazon.com/rekognition/.   
- https://www.ibm.com/cloud/watson-visual-recognition   
- https://cloud.google.com/vision/   
- https://azure.microsoft.com/en-us/services/cognitive-services/computer-vision/   
- https://azure.microsoft.com/en-us/services/cognitive-services/face/   
- https://azure.microsoft.com/en-us/services/media-services/video-indexer/   

Access is less plan driven than event driven. Analogies:
- cloud vs centralized server vs a desktop GPU   
- uber vs. a bus vs. a taxi   
- bitcoin vs. automated settlements vs. traditional payments   
- Amazon Marketplace vs. eBay vs. Walmart   

**How could colab notebooks and/or Jupyter Books be used to exchange ideas or build research portfolios?**

My principal view on this is that exchanging ideas is easier when everyone is in the same environment.  

- The cloud environment of Colab serves as a control device for independent members of a team.  
- Sharing notebooks and publish to Github is an advantage for team work and version control.   
- Any team member more comfortable with Jupyter on their local computer can save it down and use it there.

So there is a big radius of comfort.

There is also no computer envy.

A bigger point is that the team can have a hardware discussion.  We all can tinker with the same config and decide what works best together.  It's not just a software solution then. 

I took a few notes on Colab this week.  I have never used it before and wanted to try a lot of different things as I did so.  I am definitely impressed with features in Colab relative to Jupyter.   Until MSDS 453 last quarter, Jupyter was my go to environment. 

- I found it extremely easy to get Kaggle and Drive wired into Colab and found those linkages useful.  So, I would expect that the CV APIs listed above will be equally useful.  
- Autocomplete.  Tab gives method autocomplete in Juypter.  Colab pops up the docstring and method parameters.  I think this will flatten the learning curve as it brings Spyder like features to Jupyter-like environment. (I don't like Spyder.)  
- Colab is a little laggy.  
- I like how you can find older versions time stamps and see comparisons between those versions. This already saved me an hour.  
- I am not entirely comfortable with saving everything in Google Drive, but this is my first time really doing that.  
- I love collapsible section headings.  I had favored RawNBConvert over Markdown in Jypyter, but in Colab I am the opposite of that.    
- I was able to use a GPU which sped up the CNN but slowed down my RForest.  That all of use can use the same underlying power enables better collaboration. I could not get TPU running, but that may just be me.    
- I am somewhat worried about having dependency on internet connection for my compute.  I was planning to build my own GPU equipped computer, but after using e.g. Colab I am not so sure I will do that now.  


**What are some key differences between biological and machine vision?**   

After reading a bit on computer and biological vision I might take a different perspective on this question.

First, I read through an article that highlights how the fields of biological and computer vision separated shortly after Marr (1982) attempted to unify them around similar computational problems.  Experimental tools limited the study of biological vision and computing power limited the study of machine vision. Medathati et al. (2016) suggest that time is ripe for common ground: limits are no longer in place and so advancements and inspiration are possible on both playing fields.   

The diversion I want to address is at minute 39:40 in BladeRunner2049 when Jared Leto as a blind Niander Wallace says "Now let's have a look at you."  This is after he's physically inspected the new, but still infertile, female replicant.  His subsequent actions make it clear that the several drone-like eyes that enter the room are not visual tools alone.  They enable him to sense other dimensions, notably some form of visual density measure, akin to X-ray or Ultrasound.  This is how he determines the replicants infertility.  

It would be comforting to grant a blind human the ability to see, much like the rest of us.  This would offer common experiences, but why stop there?    

- Humans have more than 5 senses: pain, temperature, balance, the passing of time.  
- Our senses work together to provide a mosaic of abstract cognition.  
- We sense vision with our brain as much as with our eyes (hallucinations).  
- Animals can sense:  
  - UV and polarized light (Mantis Shrimp and Octopus)  
  - magnetic fields (pigeons, sea turtles and other migrating aquatics such as Salmon)  
  - electricity of other animals' muscle contraction (sharks and platypus)  
  - air and water pressure (Weatherfish)  
  - 3 dimensional sight via echolocation (dolphin, porpoise, bat)  
  - infrared and radiation detection (pit vipers)    

If these senses work together, I don't think we should paint a target on biological sight when this clearly isn't what we are after when we represent how we perceive our surroundings.   

Marr, D. (1982). Vision: A computational investigation into the human representation and processing of visual information, henry holt and co. Inc., New York, NY, 2(4.2).

Medathati, N. K., Neumann, H., Masson, G. S., & Kornprobst, P. (2016). Bio-inspired computer vision: Towards a synergistic approach of artificial and biological vision. Computer Vision and Image Understanding, 150, 1-30.
