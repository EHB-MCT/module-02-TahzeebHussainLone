# Module 02 - Exercises

## Exercise 01: Interactive Sketch

Let's refresh some p5.js skills and draw a bouncing ball.
Than we will learn to make them interactive with controls, using HTML input elements (sliders, color pickers, etc.).

### Instructions

Open `main.js` and follow the steps in the comments:

1.  **Define variables:**
    -   Create variables for `size`, `speed`, and `colorVal` to control your sketch and give them initial values
    -   Create variables for the position of the ball `x` and `y` and give them initial values -
    -   add `speedX`and `directionX` (set directionX to 1 or -1). We create a separate variable for direction now, so we don't have to take care about it when changing the speed with the slider later.
    -   Start by movement on 1 axis, come back and add `speedY`and `directionY` later.

2.  **Draw oop:**
    -   Use these variables inside the `draw()` function.
    -   Update the position `x` by adding `speed`.
    -   Add the bouncing logic.

3.  **Select inputs:**
    -   Use `document.querySelector` to select the HTML inputs (`#size-input`, `#speed-input`, `#color-input`).

4.  **Add Event listeners:**
    -   Add an `"input"` event listener to each input element.
    -   Inside the listener function, update the corresponding variable with `input.value`.
    -   **Important:** `input.value` is always a string! Use `Number(input.value)` if you need a number (for size/speed).

5.  **Expand by using arrays to create multiple balls:**
    -   Create an array for the positions, speeds, directions, size and color of the balls.
    -   Implement the logic to draw and update the balls using the arrays.
    -   Add an amount input field to control the number of balls.



## Exercise 02: Reviews

Practice working with Objects and Arrays to create a dynamic review system.

### Instructions

Open `main.js` and follow the steps in the comments:

1.  **Setup Data:**
    -   An array of objects (`reviews`) is already provided. Each object has a `name`, `rating`, and `text`.

2.  **Select Elements:**
    -   Select the container where reviews will be displayed (`#reviews-container`).
    -   Select the form (`#review-form`) and its input fields (`#name`, `#rating`, `#review`).

3.  **Render Function:**
    -   Create a function `renderReviews()` that:
        -   Clears the container (`innerHTML = ""`).
        -   Loops through the `reviews` array.
        -   For each review, creates a new `div` with class `review-item`.
        -   Sets the `innerHTML` of this div using the template provided in `index.html`.
        -   Appends the new div to the container.

4.  **Initial Render:**
    -   Call `renderReviews()` once when the page loads to see the initial data.

5.  **Handle Form Submission:**
    -   Add a `"submit"` event listener to the form.
    -   **Prevent Default:** Use `e.preventDefault()` to stop the page from reloading.
    -   **Create Object:** Make a new review object using values from the input fields. *Remember to convert the rating to a number!*
    -   **Update Data:** `push` the new object into the `reviews` array.
    -   **Update View:** Call `renderReviews()` again to display the new list.
