# Looking-while-listening Task
The aim of this project is to create a variant of the looking-while-listening task, usually used on preverbal infants to assess their lexical capacities and their understanding of certain common words. In this version of the task, instead of analysing the participants' gazes, the participants will only have to click on the right picture with their mouse. 
The task will work like this : On each trial, participants will see two pictures displayed on the right and left sides of their screen and will hear, after 4 seconds, a target-word prompting them to click at one of the objects presented on the screen. Once the participant has clicked on one of the two pictures, the next trial starts. If the participant has not clicked on any pictures, the pictures will remain on the screen for 4 sec after the target-word onset and then the next trial will start. Participants will see four times each of the four picture-pairs accompanied either by the name of one of the object or the other (2 times each). Each picture-pair, therefore, will be seen by the participant four times. Because this task was originally developped for infants it is a very easy task. In my variant, I will ask the participant to be as fast as possible in responding at each trial. I will collect participants' data in a seperate text file which will contain : participant id number, the trial (what was the target word), the words-pair, the accuracy (has the participants clicked on the right picture) and the response time. In addition to this datafile, two histograms will be printed at the end of the experiment : one for participants' accuracy and one for participants' reaction time for each target words. 

# The code

The code can be divided in two parts : the first part is for data analysis and the second one is the experimental task. Four different modules are used : Expyriment, os.path, matplotlib and random. I will describe how they are used in the following section. 

## Data analysis part : 


