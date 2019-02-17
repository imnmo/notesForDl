# Image classification:
-----------------------

* Contains 7 lessons and we tend to expect about 10 hours of homework
* So totally expect about in 70 hours of work in total 
* From my analysis its going to take about 5 hour per lecture plus 10 hour for the homework, so in total 
roughly 15 hrs pro week
*  IF you follow this 15 hour model and at the end you ll build up the Image classification at the world class 
level/classify the text/supermarket prices/Netflix predictions etc and world-class problems
* Leave about the Naysayers, its doesn't need lot of learning and so on

ADVICES:
--------

* You ll able to build the things much more faster than understanding in  the thoery and 
Remember, you will learn "How it works before you learn why it works"
* Get experience to get our hands on and know how to work with the code and
how to work with the data 
	* The best way to create models is to do lot of models and do lots of 
	CODING and STUDY them CAREFULLY

CODING:
--------
### Data Preparation:
* Do the shift + Enter for the coding part
* three lines are special directives to the JP notebooks so called code magics 
* load the library for the fast ai and fast ai sits on top of the Pytorch and one of the ways is that 
pytorch is modern than the tensorflow and things can be done lot more quickly
* Fast ai + Pytorch
* Fast ai 
	* vision
	* NLP
	* tabular data
	* Collaborating filtering
* Never do the import * because of the production issues(but the Data scientist way is bit different)
* DataSets 
	* the main thing we are going to look at them is the academic academic datasets,
because academics spend lot of time curating the stuffs and also in the designing.
	* Another important thing to know is that using the Kaggle dataset that is to have the proper
	  to have a proper baseline at place.
	* With Kaggle competition you can see how well you did at the competition and can see how well you did with the dataset
	* SO academic has lot of stuff so as the kaggle competition

* Pet datasets classifying the different classes. this kind of problem in classifying the problem of course 
a harder problem is **Fine Grained classification** 
* First step is to download the data,using the method called *untar_data*
help(untar_data) helps in showing what it is actually and it also provides you the type you need to pass
* in DataType Union is **either** string path or nothing and similarly 
* Within the Fast.ai library the the Path is codded in the constants eg see
*URLS.PETS* 
* IN JP just put the semicolon or just put the variable so it just prints out.
* Whenever you run them next time it will just cache them so it is just automatic and its pretty easy.
* IN python there is something called as **Path** variable where you just append the things 
to the variable
* If you are starting with a dataset trying to do deep learning on it what you do ??
	* 	Just try to see what's in there.
	* **Understanding the data is the key to problem we like to solve**
* using the *get_image_files* just gives the files
* For image dataset is pretty common way is to have one folder with all images in it.
* jargon: *In machine learning **Label** is the thing we are trying to predict
* And also label is part of the filename like lable_no_extension -> we need to extract the
labels from the data  
* For DL models:
		* You need pictures file containing the data
		* You need some labels
* In Fast.ai there something called as *ImageDataBunch* which helps to get the 
			* training set
			* validation set
			* labels 
* lets say from the data. lets extract the labels using the  *from_name_re*	
* So the *ImageDataBunch* takes the following files and path and pattern to extract and get tranforms
finally the size.
* The size says what size the images you want to work with because there is a shortcoming of
the current DL: which a GPU has to apply the same amount of instruction in order to be fast
a varying shapes and sizes cannot do that.
* So we have to make sure the images are of same size and shape
* In part1 of the course, we ll be making the images just square
* In Part2 we ll make you rectangles as well
* Nearly everyone does the square, which is 224 * 224 extremely common size,
this is most important bit which I will teach in the course what works and what not.
* In Fast.ai everything returns is known as the data bunch object, of course we ll 
learn about them, whats in them and so on.
* As the data_bunch will contain the training data, validation data and/or test data.
* Then we need to do normalize the all of the data of same size specifically same mean, same
standard deviation etc.., so using normalized function we would get the standard stuff out of the
data.
* Let us take a look at the few picture to make sure what we understood, 
*data.show_batch* as you can see they are zoomed and cropped in a very decent way.
* So what we are doing is also called as center cropping, that we grab the middle bit and resizing. 
We'll talk about the cropping and resizing which is very important bit. 
* **Data Augmentation** where it discusses about the how much and where to crop and we also resize the pictures 
and sometimes we do padding
* Why do we normalize the images? Because pixel values start out from 1- 255 and some pixel values/(channle RGB) tend
to be really bright or dull or uneven. We try to normalize these RGB channels or pixel values to the 
mean of 0 and Standard deviation of 1 , we'll learn bit about that later
* So **if model isn't accurate , then one thing to check is the it contains if its Normalized**
* Question: As GPU man is power of 2 does 256  sounds more practical than 224 on GPU utlization. The brief
answer is model are designed for final layer be it 7 * 7 , so 2 pow if 7 ~ 224.
* **To be a good practitioner will be able to looks at the data**  some might have rotated or conatin the text on them
and so on.
* Then not looking at the pictures is important but also the labels, so all of the labels are present 
in as the classes.
* SO these classes are the label which we extracted probably the 37 labels/classes
* *data.c* is the length of the labels or classes. For regression and multi label classification**
will do for now. 

### Training the model:
* A model will be trained at the fast.ai using something called as the *Learner* just like
*dataBunch* general concept for data and there are sub classes to particular applications like 
image 
* A *learner* that can learn fit the model, and particular *convLearner* it means the convolution
learner (which we'll learn more about that in later in next three lectures)
* For the convLearner you need to say what's your data like  *dataBunch* what your path
* Then you need to say whats your model , that particular kind of model called as resnet
which works extremely well with what size you want or how big is it. 
* One is the Reset-34 and other is Resnet-50 , when we started with smaller one because
it will be faster.
* That's all the bit you need to know about the architecture now, to really pick & the third parameter is
called as the metrics which really gets printed out as it gets trained.
* First time running the command, its downloading the resnet-34 pretrained weights:
Whats is this particularly means this particular model/resnet-34  has already been trained for particular task
The task it looked about 1.5 million pictures using a dataset called as imageNet. So we can 
downlaod the pretrained weights. 
* So we don't start  from fresh or from scratch but we just reuse the the resnet-34 pretarined weights.
 & I don't think this our dataset of 37 classes has been seen by resnet-34
* This particular resnet has already seen some of the images and knowns about picture
and how to recognize the very few things
* **Transfer Learning** its kind of using/reusing the pre-trained weights and applying the knowledge
to our data sets -> we'll learn lot about them later.
* We take a per-trained model and fit it so instead of taking from scratch. By doing
this way of *transfer learning* 1/100th or less of the time of regular training and 
1/100th less data for training potentially 1000 times.
* Remember the Nikhails lesson on cricket , as you know there is no examples of cricket or baseball
in the ImageNet but with just 30 examples (bare less), its just figured out. Nearly perfect classifier
### Validation:
* Ok hold on for a moment, how can you say that it ables to recognize cricket or baseball
**May be its cheating** its called **Over fitting** 
* To make sure we don't over fit the data, we use something called as the **validation set**.
A validation set is the set of images, that our model doesn't or will not able to look at.
* So this metrics /error_rate gets printed out based on the validation set. 
* When we created the data bunch it automatically created the validation set for us. 
* We actually make it nearly impossible to not to use the validation set, because without that
you never know if you are over-fitting as print out metrics and make sure learner doest see them and
* Here at fast.ai we bake in the best practices and we built on the data bunch object
* Now there is something called as the fit it, but i practice use the fit_one_cycle 
the one_cycle fitting is dramatically better, we'll learn about them
* Shift + tab will say what you need to parse it. Cycle length 
* Now the epochs or how many times we go through the data set , how many we show the 
dataset to the model and so it learn from it. 
* If the same picture if sees too many times then it would over fit.
* We'll also learn about fine tunning this number, but 4 is a good number. After 4 epochs 
the error rate is 6% and about ~2 min 
* It means 94% of time we picked exact dog/cat , now we ll look at the paper. Nice thing 
in using the academic paper or kaggle datasets we can compare our solution with other
kind of benchmark.
* In academic papers there is section calls as the **Experiments** where we see the benchmark,
at 2012 it was nearly 60% accuracy now its about 94% in our machine. 
* **Motivation** You see DL is improving at the rate of 5-10% a year which no other fields has made it.
 which in turn means DL can be applied to real world problem, its no longer myth or Hype.
We can really solve bunch of good problems.
* We don't know why it works , but eventually we'll get to there 
* **Most important is seeing what goes in and seeing what comes out**
* We already start looking at **what goes in** that's the sample of 
*data.show_batch* INput: images/data and the next important thing is
what goes out 
* There is actually only other software which actually does try to do things
like fast.ai is *keras*
* Faster and training is faster; the lines of code is much larger (31)
for keras on comparison to fast.ai
* Question: Why are you using Resnet as supposed to use the inception
-> the answer is architecture go t dawnbench and see the results 
resnet will be good enough
-> Models differ, edge computing for eg on mobile phone , run it on 
the server and try to query on them
* Now we got the trained model *see learn.fit_one_cycle()* what happened is
creating a set of weight, if you have done liner regression or logistic regression 
you might be familiar with the weights, we have found some co-efficients
and parameters and it took 1.56 minutes
* If you want to play around the model little bit more after and just want to
save in the current then use *save method*
* The save will be saved in the model sub-directory where it came from
* We have seen effectively **what goes in** using the *data_show* method
* Now we will see **what comes out** using the class called **classificationInterpreteratin**
* Using the Factory method *from learner* by passing learner, remember
learner object knows two things **data** and **what the model**
* So thats what needed to interpret the model with data and the trained model
* Most important things to do is the plot them:
	* Will learn about the loss function shortly 
	* loss function will say how good is your predictions*
	* top loss method just what are the top loss which we were really confident
	* Apart from the *top_losses method another useful tool is called as the 
	*confusion matrix* 
	* Especially when having lot of classes don't use confusion matrix but use
	**most_confused**
* Lets make the model better, so how can we make them better?
* using **Fine tuning**  since we use the per-trained model and try to run the lern_fit_
on_cyle will just run on the last layers and be fast in fitting the model
* But to really get it, do **unfreeze** says please train the whole model 
* Then we call the *fit_one_cycle* again error is much worse 17%
* Visualization of the convolutional neural networks layers and layers of
computation its convultion as it goes over layers
* Different layers of the neueral networsk represents different levels of
semantic complexity and actually we dont want to change the layers but just
build top of that.
* Then bring back the where we was using *load* method so that we just load
back the saved co-effcients or pre-weights
* Then *learning rate finder* the  fastest rate at which the training model
gets trained without getting ripped apart by using **lr_find** method
* Then using the *learn.recorder.plot()* plot the results of the found results of 
learning rate. The learning rate actually says **How quickly am I updating the parameters
of the model* 
* the **lr_find** defaults to 0.003 but thats too high and we would like to 
bring that lower based on the current scenario lets try to select the value
in between or in range of the better values  
* Again unfreeze and pass the slice and pass it the slice and make the
second part of the slice about where it gets getting worse 
* I would say with this two stage its pretty much enough to get the 
world class models of course you cannot win a Kaggle competition
* Devops **If you run out of memory** try to make them smaller and 
run them again i.e batch size 



## Homework
--------
* try to run the code and try to get your own data set
* Franciso is putting a guide how to download the data(ggogle images)
* get your GPU running and try to run your notebooks
* repeat the process on your own dataset and get on the forum and 
say what success you had.
* say your constraints and everything you hit on the model.

## Some more on datasets: 
------------
* How to create labels for your dataset, because for your data set it wont be 
a Regex base approach and can be of different formats
* using MNIST models sometimes  
* You could actually try to download the whole documentation and try to run the
all the examples from them just like that
* **Whats goes in and what goes out**

## Homework:  parts completed ✅
- crestle.ai
- Started with aws but is expensive and moved to cheaper RI based crestle
  later will move to GCP as it cheaper. 	
- read & run lesson1-pets.ipynb notebook
- read [Tips for Building Image dataset](https://forums.fast.ai/t/tips-for-building-large-image-datasets/26688)
- read [Lesson 1 notes](https://forums.fast.ai/t/deep-learning-lesson-1-notes/27748)
- read fastai documentation
- run lesson1-pets.ipynb
- get your own image dataset
  - Repeat process on your own dataset
  - Share on Forums X
- did the oxford dataset and achieved 50% accuracy which is pretty low,
may be the data sets was not cleaned up like garbage in and garbage out as probably
I missed good split for train/validation/test split?
- Challenge was to get the right dataset or DataBunch object as it was the 
difficult task for me and what dataset to start with spent too much on datasets.

## TOtal Time Spent 🕜:clock130:
5 hours for lecture + 5 hr on homework + 2 hr on googling and learning
= 12 hours.

