Lab 04b: Let's build a character creator!
===

## Standard Setup Process

1. Create a repo called `lab-04c-character-creator` on Github (I recommend starting with the template repo)
    - make sure to click add a `README.md`
1. Copy the URL of the new repo
1. From the command line (terminal) clone your repo:
    1. Check with `pwd` that you are in correct directory for labs
    1. `git clone <url>`
    1. **`cd` into your repo from the command line**
    1. Launch vscode with `code .`

## Goal

You will make a form that accepts user input for the attributes of a character (for example, strength, empathy, happiness, driving skill, whatever). These should be number inputs, between 1 and 10. When the user submits the form, you will render to the page images that go along with the attributes of the character. For example, if the user selects happiness of 8 and a strength of 10, you might show an image of a beaming smile next to an image of the incredible Hulk.

## Some guidance 

_(note that this is mostly copied from the calculator lab: there is nothing new under the sun!):_

1) In the HTML, Your inputs and buttons will need ids.
    - **Validation step**: look at the ids in the Elements tab in the browser
1) You will need to add event listeners to your buttons.
    - **Validation step**: log out 'Hello world! I am the add button' to validate that your event handler worked.
1) On click, you will need to be able to get the current number the user has typed into the inputs.
    - Get the inputs with `document.getElementById`
    - Get the value by using `.value` on the element
    - **Validation step**: Log out the values of all of your inputs
1) On click, you need to figure out an appropriate image to go along with each of the user's selected status numbers. I want you to write a function for each status that takes in a number and returns an appropriate image. For example `getHappinessImage(8)` might return the url for a smiling face. These image paths can be paths in your own project, or images hosted somewhere out on the web.
    - **Validation step**: log out the correct value
1) In the HTML, you will need a div to put image urls into. You'll probably want some starter images as placeholders, so you can change the `src` of these.

## Suggested order of building:
1) Make HTML with inputs, a button, and a few starter images. 
1) Write functions for `getHappinessImage`, `getStrengthImage`, etc. 
    - You may want to write tests first to practice good TDD.
1) Grab all the input and images from the DOM using `getElementById`
1) Add an event listener to the button. 
1) In the "cool zone", 
    1) Get all the values of the inputs.
    1) Use these values along with your `getHappinessImage`, `getStrengthImage`, etc functions to get urls for images.
    1) Change the `src` of your img tags (grabbed in step three above) to the appropriate image urls that are returned from your `getHappinessImage`, `getStrengthImage`, etc functions.

## Points Break Down

Looking For | Points (10)
:--|--:
Deployed on GitHub pages, with link in the About section of the Github repo | 1
At least three functions that take in numbers and return appropriate image urls (i.e., `getHappinessImage(4)`) | 1 point per function
Tests for your `getWhateverImage` functions | 1 point per test
Use the functions to render images to the page based on user input | 3
STRETCH: combine all your `getWhateverImage` functions into a single tests function that takes in a string and the number and returns an appropriate image. For example, `getImage('happiness', 4)` would return the correct image for a happiness level of 4. This function should _use the previous functions inside of it_. | +1
