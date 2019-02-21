# Data cleaning and production:
-----------------------
* Share your ideas because by sharing you are able to really get good the mistakes you
are doing. 
* A guy about the WhatsApp clean up between meme/photos and images
* Spectrum sound classificiation, where we are able to get about 80% of the
results using classificiation -> turning sound into pictures
* State of the art accuracy for DCHD Suvash Thapliya 99.02% 
* Alena Harley 
* Simon Wilison and natalie downe
* james Delinger bird classificiation
* Daniel Armstrong who has no idea tried to open a PR 
* zuchinni vs cucumber classifier
* Discovering the country by looking at the aerial view. 
* So don't worry if you haven't had or got a project, some of them
had already got a head start and they do it well while others don'the
* We dig into Dig deeper on CV application. 



ADVICES:
--------
* code first -> you just able to run the code and get something hapeening
and experiment
* Watch the videos atleast three times 
* Dont stop at lesson 1 and keep continuning and be in the game
* This learning is based on the David perkins
* Learning about the soccer analogy -> type soccer
*   


CODING:
--------
### Data Preparation:
 * How to create a own classifier an your own image data set 
 * pyImageSearch 
 * classify the teddy bear -> diffrent types of them 
 * click on  the particular cell and then directly jump into the mkdir cell
 and do this iteratively.
 * Jeremy is experimentalist, I play aorund and get this into the work
 * Human creativity is best inspired by trying things out and getting into the
results 
* You just know if download from kaggle or academic data set you have train,vaid and test(Which I suppose
I miss them)
* We just need a validate set otherwise we don't know how our models might 
work
* Whats is this np.random.seed(42)-> what is it fixed? You try to have a
same validation set again and again. because hyperparamter change has improved
by model ? 
* Now we got the data bunch and just do steps like we did in the last 
class until the learning rate finder
* We'll learn about the learning rate finder today !
* Within the learning rate finder you are looking for strongest downward slope
 thats is kind of sticking around for quite sometime 
* So we have come long way in the classification problem, may be we could
do better if our dataset is less noisy 
* **Combining human expert with compuetr learner** is very useful skillset
* Based on the losses we are going to look about and see which are noisy
* now lets clean up the mislabelled images, you can get the unused or wrongly mis classified
and hit delete to remove them
* If you just realize that within the Jupyter notebooks we could actually 
clean up and develop a widget sort of thing which is possible.
* Creating the widgets in the Jupyter is lets you create tools for your follow 
practioners.

   
### Model in Production:
* After doing the clean up and getting an improvement of 1% is normal and
thats quite acceptable
* After traning the inference or just prediction can be done in the
GPU because we dont want to run in the Google scale and the order which we are speaking
is 0.02 to 0.01
* Again inference is you got the trained model/pre-trained weights and how you are 
going to use them-> or just infer them
* All the classifiers which you are creating can be turned into the Web apps
* Most of them in share your work thread usually have everything going as good as possible 
and 1 /20 have problems
* Lets talk about the ones which has problems -> thats me :)
* Most problems converge:
	* no of epochs
	* learning rate is high or low
* remember validation loss had become more and its always underneath 1 < 1
* if your learning rate is too low then the training loss will be really higher
than your validation loss. this really means if haven't fitted enough. The number of 
epochs is too low as well
* when train_loss > valid_loss only two possibilities
		* too few epochs and too few lr.
* Have a right balance between  the epochs and the lrs.
* Too many epochs (overfitting)
	* I turned off data augmentation, dropouts and weight decay
	* Only way to say that you are overfiiting is error is improving for while
and then its starts to degrade
* **if train_loss < valid_loss then you are overfitting is absolutely not true!!**
* **any model trained correctly will always have train loss < valid_loss and the errors are improving
* **FOUR IMPORTANT THINGS** 
		*  epchs an lr (being high or low)	
* Lets learn about the lr,loss etc..,
* When ever we see a picture(black and white) is actually a numbers/ or just matrix 
if we see a colored pictured it would be the tensor or just contains the 3rd dimensions
* try to question the accuracy and errorate ?? and try to read the src code
* 3e-3 and slice is upto 10 times less 3e-4 and 3e-3 just works(rule of thumb)
* Adam geitgey.
* Reproduce the temp vs ice cream dots with equation 
* Question: when genertaing new dataset how much should be get??
 [till 1.08]




## Homework
--------


## Some more on datasets: 
------------


## Homework:  parts completed 

## TOtal Time Spent 🕜:clock130:


