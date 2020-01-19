# Looking-while-listening Task
The aim of this project is to create a variant of the looking-while-listening task, usually used on preverbal infants to assess their lexical capacities and their understanding of certain common words. In this version of the task, instead of analysing the participants' gazes, the participants will only have to click on the right picture with their mouse. 
The task will work like this : On each trial, participants will see two pictures displayed on the right and left sides of their screen and will hear, after 4 seconds, a target-word prompting them to click at one of the objects presented on the screen. Once the participant has clicked on one of the two pictures, the next trial starts. If the participant has not clicked on any pictures, the pictures will remain on the screen for 4 sec after the target-word onset and then the next trial will start. Participants will see four times each of the four picture-pairs accompanied either by the name of one of the object or the other (2 times each). Each picture-pair, therefore, will be seen by the participant four times. Because this task was originally developped for infants it is a very easy task. In my variant, I will ask the participant to be as fast as possible in responding at each trial. I will collect participants' data in a seperate text file which will contain : participant id number, the trial (what was the target word), the words-pair, the accuracy (has the participants clicked on the right picture) and the response time. In addition to this datafile, two histograms will be printed at the end of the experiment : one for participants' accuracy and one for participants' reaction time for each target words. 

# The code

The code can be divided in two parts : the first part is for data analysis and the second one is the experimental task. Four different modules are used : Expyriment, os.path, matplotlib and random. I will describe how they are used in the following section. 

## Data analysis part : 
I use matplotlib for plots and histograms. 

function Trueinstances :
function that takes as an argument a list of lists and verifies if the second argument in each list is "True". This will allow compute the participant's matching accuracy by knowing how many time has he clicked on the target words (how many "true instances"). 

function AccuracyPlot : 
Takes as an argument a table. Will create a histogram showing how many matches between a target word and a picture were accurate and how many were innacurate (i.e. True or False).

function moyenne : 
function that takes two arguments, a tab and a string. It computes the mean reaction time of participants for the two instances of the same target-word. ----> develop a clear and short explanation

function RTplot : 
Takes a table as an argument and creates a histogram with the mean participant's reaction time for each target-word in the experimental task. 

## Experimental task

- Main matrix : "tableau" : 
This matrix group the stimuli paths that will be used during the task. This matrix is composed of 16 rows and 4 columns, each row representing one of the sixteen trials in the task. Each row of the matrix contains four elements : the audio-stimuli path (which will prompt the target-word in each trial), the first visual-stimuli path (picture 1), the second stimuli path (picture 2) and finally an integer (1 or 2) indicating if the target word is picure 1 or picture 2. Here the os.path.join module allows the code to be portable and to work on every operating systems. 

- Using expyriment to create the experimental task:

I create a new Experiment object by calling the Experiment class in the submodule design and name it “Looking-while-listening task”. Immediately after I initialize this experiment to be the active one. This does the following:
Starts an experimental clock, creates the screen and creates an event file. Others expyriment modules allow to set different experimental parameters, for example the mouse-cursor, the fixation cross, the data variable names... Then, starting the experiment does the following two things: presents a screen asking for the subject number and creates a data file in which the data will be stored. Similarly, different expyriment modules will be used to create the button-boxes in the task, to present the stimuli in each trial, to set the duration of a trial,to end the experiment...

- The experimental loop :
The loop does the following : it randomizes the order of the 16 trials of the task. In each trial, it presents the stimuli and registers participant's response (accuracy) and reaction time. Adds every data variable to the datafile and to the empty matrix 'tabData' that will be used to create histograms. Starts again until the 16 trials (i.e : i = 16) have been presented to the participant. 



