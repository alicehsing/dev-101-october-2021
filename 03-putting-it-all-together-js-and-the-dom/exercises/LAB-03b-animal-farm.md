# Lab03b - Animal Farm

## Goal

For this lab, you will be experimenting with click event listeners as well as audio tags. Your final web page will have at least three images of animals that play an animal sound when clicked.

## Standard Setup

1. Create a new repository using the [template](https://github.com/alchemycodelab/alchemy-dev-101-template)
1. Copy the url and clone this repo
1. `cd` into the folder after you clone and use `code .` to open in VS Code

## Research

Find at least three three animal images that you want to include in your animal farm. There are some sample sound files in the [animal-sounds](./animal-sounds) directory however feel free to find different ones.

## Code

_Repeat this for each image_

1. Add your image and sound file to the `assets` folder
1. In `index.html` add an `<img>` tag and an `<audio>` tag that point to your image / sound file. Make sure these html elements have an ID.
1. In `app.js` make two variables that will point to your image tag and your sound tag. This might look something like this:
    ```javascript
    const dogSound = document.getElementById('dog');
    const dogImage = document.getElementById('dog-image');
    ```
1. Add an event listener to the image that plays the sound on click. You will use the `.play()` method on the sound variable to accomplish this.
    ```javascript
    dogImage.addEventListener('click', () => {
        dogSound.play();
    });
    ```
1. ACP and then repeat process for other images

## Points Break Down

| Looking For                                                                          | Points (10) |
| :----------------------------------------------------------------------------------- | ----------: |
| Deployed on GitHub pages, with link in the About section of the Github repo          |           1 |
| At least 3 nicely styled animal images                                               |           3 |
| Images play an associated animal sound when you click on them                        |           6 |
| (Stretch) Pick a key to associate with each animal and add a keydown event listener |          +1 |
| (Stretch) Add CSS animation to the image while the sound is playing                  |         + 1 |
