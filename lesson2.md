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
  * You got a good learning rate no higher or no lower
  * you are training for longer time and your accuracy is not good enough.
  * Usuallay get more data.then you get higher accauracy lower error rate without 
  any overfitting.
  * Start with small amount of data and get started and then go about further
	* which organizations most of the times do it wrong is gathering a bunch of data most time which 
	   they dont need.
* Question: What if its unbalanced data ? nothing just try it, it will work
* ResNET 34 is just a function, it doesn't take any room or any special space.
* Remember RESNET 34 it just says its a  line or quadratic or anything like that
	-> again its just a architecture rather than the anything you might think of, we'll learn
		more about that in the upcoming lecture.
* only on the step **load('stage-1')** where we actually store the values,
or the pre-trained weights like Y = aX + b, where a,b are the pre-trained weights.
* But resnet34 you just don't store just two numbers but you ll store a bunch of
million or so.
* Derive the equation from simple Y= aX + b to Y = a1X1 + a2X2
			```math 
			Lets say,
			Y = aX + b
			with matrices and vectors we get,
			Y = a1X1 + a2X2 where i.X2 = 1,
			we know from dot product rule, Y = Xa 
			the a & b are going to fit the line somehow
			```
* This somehow technique is called as the SGD!
* SGD is two variants: Student gradient descent, where I did something and just learnt some stuff by trying and
type is called as **Stochastic gradient descent**
* Lets generate a synthetic data and we ll learn about the Pytorch
* **tensor** means **Array** and in the world of deep learning, it just means
array. jagged array is not a tensor
* Tesnor is an array a rectangular, cube where row or every column of same 
length like *4 X 3* is a tensor
* An Image is an 3d tensor 
* No dimensions with tesnors but either **Rank** or just **Axes** 
rank means how many axes are there. An Image generally is Rank 3 tensor
* in maths its called rank1 tensor as vectors and rank2 tensor as matrices and
rank3 tensor as something. If you got 64images then its called as rank4 tensors
beacuse its 3-d of image and 1-d or rank of the 64
* Follow the math create a tensor of n,2 where n is the rows and 2 is the 
coloumn
* and then take the zeroth coloumn and distribute between -1 to 1
* Important bits in Pytorch: How to create an array and how to mutate an array or change the array
and finally how to do matrix multiplication 
*  [Till 1.25]
			




## Homework
--------


## Some more on datasets: 
------------


## Homework:  parts completed 

## TOtal Time Spent 🕜:clock130:


