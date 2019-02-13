Lesson one notes:

* Contains 7 lessons and we tend to expect about 10 hours of homework
* So totally expect about in 70 hours of work in total 
* From my analysis its going to take about 5 hour per lecture plus 10 hour for the homework, so in total 
roughly 15 hrs pro week
*  IF you follow this 15 hour model and at the end you ll build up the Image clasification at the world class 
level/classify the text/supermarket prices/Netflix predictions etc and worldclass problems
* Leave about the Naysayers, its doesnt need lot of learning and so on

ADVICES:
--------
--------

* You ll able to build the things much more faster than understanding in  the thoery and 
Remember, you will learn "How it works before you learn why it works"
* Get experience to get our hands on and know how to work with the code and
how to work with the data 
	* The best way to create models is to do lot of models and do lots of 
	CODING and STUDY them CAREFULLY

CODING:
--------
--------
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
* The size says what size the images you want to work with beacuse there is a shortcoming of
the current DL: which a GPU has to apply the same amount of instruction inorder to be fast
a varying shapes and sizes cannot do that.
* So we have to make sure the images are of same size and shape
* In part1 of the course, we ll be making the images just square
* In Part2 we ll make you rectangles as well
* Nearly everyone does the square, which is 224 * 224 extremely common size,
this is most important bit which I will teach in the course what works and what not.
* In Fast.ai everything returns is known as the data bunch object, of course we ll 
learn about them, whats in them and so on.
* As the data_bunch will contain the training data, validation data and/or test data.
* Then we need to do the all of the data of same size specifically same mean, same
standard deviation etc.., so using normalized function we would get the standard stuff out of the
data.

till[30 min]
