# HW2: hangman #

## Due ##
Monday, September 25th at 11:59pm

## Overview ##
In this project, you will be making an iOS application for the Hangman game. Users should be able to start a game, make guesses for a phrase (list of phrases provided), see their progresses toward the phrase, see a list of previously guessed, incorrect letters, see how many guesses they have left (indicated by a hangman image - basic images provided), be alerted of a win or loss, and start a new game.

Though we do not have many requirements for this project, you are encouraged to customize your app. Here's a screenshot from a past project submission for some inspiration:

![alt text](/README-images/hangman.png)

## Getting started ##
Begin by cloning the project repository onto your local computer:

	git clone https://github.com/iosdecal/ios-decal-proj1.git
	

We have provided you code to interact with the list of locations in Berkeley (see **HangmanPhrases.swift**), but you will implement the rest of the features on your own. Add the following code to your code to generate a random  word (where you decide to add these lines is up to you!). 

     let hangmanPhrases = HangmanPhrases()
     
     // Generate a random phrase for the user to guess
     let phrase: String = hangmanPhrases.getRandomPhrase()
     print(phrase)

## Requirements ##
You **must** include all features listed under the "Hangman Game View" and "Finished Game States / Start New Game" sections. 

### Hangman game view ###
* a UILabel that displays the "_"s corresponding to each word in the provided puzzle string
* a UILabel that displays the incorrect guesses thus far
* a TextField (where the user enters a letter as a guess) **If you decide to create a custom keyboard, this is not required**
* The user should only be able to guess a single letter
* A "Guess" button which determines whether the letter entered in the textfield is correct or not, and updates the game accordingly
* If that letter appears in the puzzle string, the corresponding "_" should be replaced by the correctly guessed letter
* If that letter does not appear in the puzzle string, that letter should be added to a UILabel keeping track of "Incorrect Guesses: ", and the Hangman image should update to represent the number of incorrect guesses
* A square-dimensioned UIImageView that represents the "state" of the Hangman, with appropriate images for each "state"

### Finished game states, start new game ###
- A win state, indicated by an alert (Pop up box). This should prevent additional guesses. Here's a helpful article on creating Alerts: [How to Use UIAlertController in Swift](https://medium.com/ios-os-x-development/how-to-use-uialertcontroller-in-swift-70143d7fbede)
- A fail state, indicated by an alert (Pop up box). This should prevent additional guesses. 
- A "Start Over" button, which starts a new game

### Optional additions / features ###
* A smart way for the user to guess letters (since a TextField for letter entry isn't ideal UX).
* Customized design, including, but not limited to, custom images for the Hangman states
* Anything else that you think will impress us or you think would be fun to implement!


## Tips for getting started ## 
not sure where to begin? Here's one way you could break up the tasks

### Creating the Model
Though you can get away with putting all of your code in a view controller file for this assignment (it's not large in scale), we recommend you create a Model to contain your data structures / game logic / etc. To do this, create a new Swift file **HangmanGame.swift** (you can name it whatever you want). Some suggestions of what to add in here include:
- a list holding the characters guessed by the user
- the phrase the user is trying to guess
- a function to determine whether or not the user is in a win state, in progress state, or lose state
- a `guess` function that takes in a character and updates your data structures

Note: none of these are required... this list is just to help you brainstorm!

### Creating the UI / configuring view controller
- drag out a view controller from the object library in **Main.storyboard**, and create a corresponding view controller class (New > Cocoa Touch Class > subclass UIViewController) **HangmanViewController.swift**. Link these by setting the "Custom Class" of your View Controller in **Main.storyboard** to "HangmanViewController"
- set up your UI in **Main.storyboard** (a `UIImageView` for the hangman image, `UILabel`s, `UIButton`s, etc.)
- use AutoLayout to position your views. If creating a custom keyboard, you may find it helpful to nest your letter buttons in stack views (great exercise!) 
- create outlets + actions from Storyboard to **HangmanViewController.swift**

### Linking your Model to your UI via your View Controller
In your view controller swift file, create an instance of your Model:

    let hangmanGame = HangmanGame()

You can then use the public methods defined in your model to determine what should be displayed in your UI at each state of the game.

## Grading and submission ##

If you complete all of the required features you will get full credit. We will deduct points for missing features, bugs, and UI layout issues. If you impress us with additional features (see the Optional Features section), you may be awarded an additional extra credit point.

**note - though encouraged, you do not have to layout your app for horizontal phone orientations. However, TA's will be testing your apps using an arbitrarily picked simulator, so make sure your app layout is supported on all iOS Devices in the vertical orientation.** 

To submit, add your folder to a private repository (if you don't have free private repositories, get them here with the [github student developer pack](https://education.github.com/pack)). If you're new to GitHub, you can find detailed instructions on how to add your assignment to a repo [here](http://iosdecal.com/other_files/submission_instructions.pdf).

Using your private repository, submit your assignment to [Gradescope](https://gradescope.com/courses/9817/assignments/35309/). Please test that you uploaded correctly by downloading your submission, and testing that downloaded version in Xcode.
