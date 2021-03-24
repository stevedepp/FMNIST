What problem does the cloud solve when considering real-world computer vision problems?

CV and other AI subsets are well served in the cloud in similar ways:

**Variable compute which addresses**
	•	continuous scalability: speed and dimension when you need it.
	•	near limitless storage if you are creative
	•	variable configure: your solution running on different hardwareÂ  (hardware you don't have access to but your customer does).
	•	serverless tech / stateless application servers which enable instant access to different languages and configurations that afford e.g. concurrency, parallelization, scale.
All these might solve problems which are otherwise insolvable on a local platform and allowÂ tinkering with hardware configurations, much as one might tinker with lines of code.
We gain access to APIs for computer vision:Â 
	•	https://aws.amazon.com/rekognition/
	•	https://www.ibm.com/cloud/watson-visual-recognition
	•	https://cloud.google.com/vision/
	•	https://azure.microsoft.com/en-us/services/cognitive-services/computer-vision/
	•	https://azure.microsoft.com/en-us/services/cognitive-services/face/
	•	https://azure.microsoft.com/en-us/services/media-services/video-indexer/
Access is less plan driven than event driven. Â Analogies:
	•	cloud vs centralized server vs a desktop GPU
	•	uber vs. a bus vs. a taxi
	•	bitcoin vs. automated settlements vs. traditional payments
	•	Amazon Marketplace vs. eBay vs. Walmart
How could colab notebooks and/or Jupyter Books be used to exchange ideas or build research portfolios?
I took a few notes on Colab this week. Â I have never used it before and wanted to try a lot of different things as I did so. Â I am definitely impressed with features in Colab relative to Jupyter. Â  Until MSDS 453 last quarter, Jupyter was my go to environment. Â 
	•	I found it extremely easy to get Kaggle and Drive wired into ColabÂ and found those linkages useful. Â So, I would expect that the CV APIs listed above will be equally useful.
	•	Autocomplete. Â Tab gives method autocomplete in Juypter. Â Colab popups the docstrings and parameters which I am guessing will be very helpful in flattening the learning curve. This sort of brings Spyder like features to Jupyter-like environment.
	•	Colab isÂ a little laggy.
	•	I like how you can find older versions time stamps and see comparisons between those versions. This alreadyÂ saved me an hour.
	•	I am not entire comfortable with saving everything in Google Drive,Â but this is my first time really doing that.
	•	I love collapsible section headings. Â I had beenÂ a user of rawNBConvert in Jypyter.)
I was able to use a GPU which sped up the CNN but slowed down for RF
I could not get TPU running, but that may just be me.Â 
Â 
As for how this assists with collaboration:
clearly being able to share books and publish to Github is an advantage
and anyone comfortable with Jupyter can save it down and use it there.Â 
so there is a big radius to comfort
plus we all can operate on teh same machinery
not only is there no envy but thereâ€™s more hardware discussion that can occur.Â Â we all can tinker with the same config
Â 
I am somewhat worried about having dependency on internet connection for my compute.Â Â I was planning to build my own GPU equipped computer, but after using e.g. Colab I am not so sure I will do that now.Â Â 
Â 
So far however I am impressed with what I can access for free with Colab for example.Â Â 
Â 
Â 
Â 
Â 
What are some key differences between biological and machine vision?Â 
Â 
Â 
Â 
After reading a bit on computer and biological vision I might take a different perspective on this.Â Â First though I had a look at an article that highlights how the field of biological and computer vision separated shortly after Marr (1982) principally because his attempts to unify the fields around the similar problems they solve (Medathati et al., 2016).Â Â I cannot afford Marrâ€™s book at this time, but it is one I want to read; his 1979 article is only 82 pages and free here.
Â 
The diversion I want to address is at minute 39:40 in BladeRunner2049 when Jared Leto as a blind Niander Wallace says â€œNow letâ€™s have a look at you.â€Â Â This is after heâ€™s physically inspected the new, but still infertile female replicant.Â Â His subsequent actions make it clear that the several drone like â€œeyesâ€ that enter the room are not visual tools alone.Â Â They enable him to sense other dimensions, notably some form of visual density measure, akin to X-ray or Ultrasound. While it would be comforting to grant a human the ability to see, much like the other 7 billion humans.Â Â This would offer common experiences, but why stop there?Â Â Humans sense with more than the 5 we commonly discuss: pain, temperature, balance, the passing of time.Â Â And our senses work together.Â Â We sense vision with our brain as much as with our eyes (hallucinations).Â Â Animals can sense UV and polarized light (Mantis Shrimp, Octopus), magnetic fields (pigeons, sea turtles and other migrating aquatics such as Salmon), electricity of other animalsâ€™ muscle contraction (sharks and platypus), air and water pressure (Weatherfish), 3 dimensional sight via echolocation (dolphin, porpoise, bat), infrared and radiation detection (pit vipers).Â Â If these senses work together, I donâ€™t think we should make such a big deal of human biological sight when this clearly isntÂ 
Â 
Marr, D. (1982). Vision: A computational investigation into the human representation and processing of visual information, henry holt and co.Â Inc., New York, NY,Â 2(4.2).
Â 
Medathati, N. K., Neumann, H., Masson, G. S., & Kornprobst, P. (2016). Bio-inspired computer vision: Towards a synergistic approach of artificial and biological vision.Â Computer Vision and Image Understanding,Â 150, 1-30.
