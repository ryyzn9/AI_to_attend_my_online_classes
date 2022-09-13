# AI_to_attend_my_online_classesSo, I made an AI to attend my online classes for me.
We all now how boring it gets after a while to attend online classes. So, I made an AI to attend them for me.

So, lets get started on what the AI needs to do:


These are the things I roughed up the AI needs to do
Let's see how will the AI get the data from the class?


So from the above image I hope you get the basic gist of how the data collection will work.

Lets Start with the data collection and processing:

Firstly lets start with the installs we need:


Now lets get started with the setup like set up the things we need for the whole code:


you will know why we need gender or teacher later in this article
Now lets get started with the screenshot part:



suppose this is my screen so upon running the code

This is the screenshot
Now lets take this image and use OpenCV to preprocess it for tesseract OCR:


So, basically what the above code does is take the screenshoted image and make it negative so that the black turns white and the white turns black and then detect the the text and draw rectangles around it on the original image.


Negative image

original image with rectangles
Now the image is ready for OCR!!

The OCR code is:


So, what the above code basically does is use OCR on the preprocessed image and paste the output in a text file hence making a document of whats being said in the class. Here is the recognised file from my AIML class in college:

AIML Class 20 Apr 2022.pdf
Edit description
drive.google.com

as you can see the OCR is so fast that it scans the sentences more than once even before they finish (I am in the process of fixing this).

now lets make each word a element of a list so that iteration through it is easyer:


Now that we have a list lets scan through the words and find if the professor has said my name and respond with yes sir/yes man depending on the gender of the teacher:


So, now in the above program the thing thats happening is its going through the list containing all words and searching for my name ‘Eeman’ but as it is captions there might be variation on how the teacher says it so its checking for all the possible spellings that spells Eeman. Now once my name is found it will play a pre-recorded yes sir or yes mam sound according to the gender of the teacher.

Now lets get to the notes part:

One of the things it wanted this to do is summarise everything that has happened in class at the end of the class.

First lets make one using GPT-3:


So, in the above code its getting the recognised.txt file from my google drive and turning it into a list and changing it into packets of 4001 tokens and passing it though GPT-3. Then the AI is taking the text and summarising it.

Now lets try the GPT-Neo method:

So, GPT-3 is paid and me poor and free trial ended so lets make an alternative version in GPT-Neo as it is free 🙂

Here is the code its almost same:


And with that my notes is part done.

How will the AI mute unmute:

So, the AI knows when to say Yes sir/Yes mam but it doesn't know how to mute unmute.

So the exact co-ordinates of the mute/unmute button in my screen is this:


1223 X 22
The code is pretty simple here it is:


Using MacOs so code is so long
now my AI can mute/unmute when needed.

Now we need my voice because my AI needs to talk in my voice:

For that I am going to use Descript. Its an amazing tool used to make a copy of your voice basically and make it say what you want.(Scary but Awesome).


Descript

creating my voice over dub
This process takes time (a lot of time) so you have to wait 🙂 let wait…


Still waiting 🙂
This took more time than I expected.


Its done!!!

Text can be said in my voice using the app in our case we use the API
Once its done I have my voice and use it to make my AI say anything I want!

Lets get started with the question detection and answering part:

lets start with getting recognised.txt file from my drive:


lets download the required libraries:


Lets make a function named line-maker to divide the lines as elements of a list:


now lets use this function:


Now lets google the sentences and find answers:


for creative questions lets use GPT-Neo for them:


Now our AI can answer questions letsss goooooo.

And thats the end of this code. I am going to make a sequel of this which I wanna do stuff with 3d and more believable AI. So, Stay tuned.

Here is a recording of my AI attending my class it works well gave me attendance 😁:

I forgot to record a real class. So, here is a sample class made by my friends.


The Video
I will make a better video and post it soon.

Well it works!!!!
