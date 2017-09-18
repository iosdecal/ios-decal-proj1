# hw2: hangman #

## due ##
Monday, September 25th at 11:59pm

## overview ##
In this project, you will be making an iOS application for the Hangman game. Users should be able to start a game, make guesses for a phrase (list of phrases provided), see their progresses toward the phrase, see a list of previously guessed, incorrect letters, see how many guesses they have left (indicated by a hangman image - basic images provided), be alerted of a win or loss, and start a new game.

Though we do not have many requirements for this project, you are encouraged to customize your app. Here's a screenshot from a past project submission for some inspiration:

![alt text](/README-images/hangman.png)

## getting started ##
We have provided you code to interact with the list of locations in Berkeley, but you will implement the rest of the features on your own. 

Begin by cloning the project repository onto your local computer:

	git clone https://github.com/iosdecal/ios-decal-proj1.git


## Requirements ##
You **must** include all features listed under the "Hangman Game View" and "Finished Game States / Start New Game" sections. 

###  Hangman Game View ###
* A UILabel that displays the "_"s corresponding to each word in the provided puzzle string
* A UILabel that displays the incorrect guesses thus far
* A TextField (where the user enters a letter as a guess)
* The user should only be able to guess a single letter
* A "Guess" button which determines whether the letter entered in the textfield is correct or not, and updates the game accordingly
* If that letter appears in the puzzle string, the corresponding "_" should be replaced by the correctly guessed letter
* If that letter does not appear in the puzzle string, that letter should be added to a UILabel keeping track of "Incorrect Guesses: ", and the Hangman image should update to represent the number of incorrect guesses
* A square-dimensioned UIImageView that represents the "state" of the Hangman, with appropriate images for each "state"

### Finished Game States, Start New Game ###
- A win state, indicated by an Alert (Pop up box). This should prevent additional guesses
- A fail state, indicated by an Alert (Pop up box). This should prevent additional guesses
- A "Start Over" button, which starts a new game

### Optional Additions / Features ###
* A smart way for the user to guess letters (since a TextField for letter entry isn't ideal UX).
* Customized design, including, but not limited to, custom images for the Hangman states
* Anything else that you think will impress us or you think would be fun to implement!

## Grading and Submission ##

If you complete all of the required features you will get full credit. We will deduct points for missing features, bugs, and UI layout issues. If you impress us with additional features (see the Optional Features section), you may be awarded an additional extra credit point.

**Note - though encouraged, you do not have to layout your app for horizontal phone orientations. However, TA's will be testing your apps using an arbitrarily picked simulator, so make sure your app layout is supported on all iOS Devices in the vertical orientation.** 

To submit, add your playground folder to a private repository (if you don't have free private repositories, get them here with the [github student developer pack](https://education.github.com/pack)). If you're new to GitHub, you can find detailed instructions on how to add your assignment to a repo [here](http://iosdecal.com/other_files/submission_instructions.pdf).

Using your private repository, submit your assignment to [Gradescope](https://gradescope.com/courses/9817/assignments/35309/). Please test that you uploaded correctly by downloading your submission, and testing that downloaded version in Xcode.
