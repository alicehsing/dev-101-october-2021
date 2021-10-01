Lab 03a (aka Lab 02a Part 2): Interactive Name Tag
===

1) Update the project so that the user is able to change the name on the nametag with an input and a button.

1) STRETCH GOAL: Also update your nametag repo to add three buttons that change the background color of the tag to `pink`, `lightgreen`, or `lightblue` (or whatever colors you like) depending on the button you click.

## Things to Do

1. Add an `app.js` file and link to it in your `index.html` using a `<script>` tag right before the closing `</body>` tag:
    ```html
    <script src="app.js" type="module"></script>
    ```
1. In `index.html` you will need to add 
    1. Add additional form control elements (an `<input>` and a `<button>`)
    1. Add `id` attributes and values to each element you are going to need to bring into JavaScript land:
    ```html
    <button id="update-button">Update</button>
    ```
1. In `app.js`, you will need use `document.getElementById('id')` to reference each needed element, and store in variable. 
    ```js
    const updateButton = document.getElementById('update-button');
    ```
1. You will need add event listeners to capture user events:
    ```js
    updateButton.addEventListener('click', () => {
        
        // code in here will run with the button is clicked

    });
    ```
1. You will need to use the `.value` property to read values out of the form controls:
    ```js
    const name = nameInput.value;
    ```
1. You will need to assign the `.textContent` property to set new text values on elements:
    ```js
    nameElement.textContent = name;
    ```



## Points Break Down

Looking For | Points (10)
:--|--:
Deployed on GitHub pages, with link in the About section of the Github repo | 2
Nicely styled text input and styled buttons | 2
Clicking the text input button changes the name of the nametag to the value of the input | 6
Clicking the color buttons changes the background color of then nametag | +1
Add pronouns to the nametag | +1
Give the user the option to change the font | +1
Tell the user how many times they've changed the name (hint: use `let` to track this changing state) | +1
